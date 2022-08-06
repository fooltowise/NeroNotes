# Parallel Computing

Parallel computation has become increasingly common. For example, laptops and desktops come with multiple processors which communicate through shared memory. High-end computation is often done using clusters consisting of individual computers communicating through a network.

Parallelism provides a number of benefits:
- High performance - more processors working on a task usually means it is completed faster
- Better use of resources - a program can execute while another waits on the disk or network.
- Fairness - letting different users or programs share a machine rather than have one program run at a time to completion.
- Convenience - it is often conceptually more straightforward to do a task using a set of concurrent programs for the subtasks rather than have a single program manage all the subtasks.
- Fault tolerance - if a machine fails in a cluster that is serving web pages, the others can take over.

Concrete applications of parallel computing include graphical user interface (GUI) (a dedicated thread handles UI actions while other threads are, for example, busy doing network communication and passing results to the UI thread, resulting in increased responsiveness), Java Virtual Machine (a separate thread handles garbage collection which would otherwise lead to blocking, while another thread is busy running the user code), web servers ( a single logical thread handles a single client request), scientific computing (a large matrix multiplication can be split across a cluster), and web search (multiple machines crawl, index, and retrieve web pages).

The two primary models for parallel computation are the shared memory model, in which each processor can access any location in memory, and the distributed memory model, in which a processor must explicitly send a message to another processor to access its memory. The former is more appropriate in the multicore setting while the latter is more accurate for a cluster. 

Writing correct parallel programs is challenging because of the subtle interactions between parallel components. One of the key challenges is races - two concurrent instructions sequences access the same address memory and at least one of them writes to that address. Other challenges to correctness are:
- starvation (a processor needs a resource but never gets it)
- deadlock (Thread A acquires Lock L1 and Thread B acquires Lock L2, following which A tries to acquire L2 and B tries to acquire L1)
- livelock ( a processor keeps retrying an operation that always fails)

Bugs caused by these issues are difficult to find using testing. Debugging them is also difficult because they may not be reproducible since they are usually load dependent. it is also often true that it is not possible to realize the performance implied by parallelism - sometimes a critical task cannot be parallelized, making it impossible to improve performance, regardless of the number of processors added. Similarly, the overhead of communicating intermediate results between processors can exceed the performance benefits.

## Parallel computing boot camp

A semaphore is a very powerful synchronization construct. Conceptually, a semaphore maintains a set of permits. A thread calling *acquire()* on a semaphore waits, if necessary, until a permit is available, and then takes it. A thread calling *release()* on a semaphore adds a permit and notifies threads waiting on that semaphore, potentially releasing a blocking acquirer. The program below shows how to implement a semaphore in Java, using synchronization, wait(), and notify()
 language primitives. The Java concurrency library provides a full-featured implementation of semaphores which should be used in practice.
 
 ```java
 
 public class Semaphore{
 	private final int MAX_AVAILABLE;
	private int taken;
	
	public Semaphore(int maxAvailable){
		this.MAX_AVAILABLE = maxAvailable;
		this.taken = 0;
	}
	
	public synchronized void acquire() throws InterruptedException {
		while(this.taken == MAX_AVAILABLE){
			wait();
		}
		this.taken++;
	}
	
	public synchronized void release() throws InterruptedException {
			this.taken--;
			this.notifyAll();
	} 
 }
 ```
 
 
 ## Top tips for concurrency
 
 - Start with an algorithm that locks aggressively and is easily seen to be correct. Then add back concurrency, while ensuring the critical parts are locked.
 - When analyzing parallel code, assume a worst-case thread scheduler. In particular, it may choose to schedule the same thread repeatedly, it may alternate between two threads, it may starve a thread, etc.
 - Try to work at a higher level of abstraction. In particular, know the concurrency libraries - don't implement your own **semaphores, thread pools, deferred execution**, etc. (You should know how these features are implemented, and implement them if asked to).
- In a [[Microsoft]], Google or Amazon interview, it's not terribly common to be asked to implement an algorithm with threads (unless you are working in a team for which this is a particularly important skill). It is, however, relatively common for interviewers at any company to assess your general understanding of threads, particularly your understanding of deadlocks.

## Threads in Java

Every thread in Java is created and controlled by a unique object of the java.lang.Thread class. When a standalone application is run, a user thread is automatically created to execute the main() method. This thread is called the main thread.

In Java, we can implement threads in one of two ways:
- by implementing the java.lang.Runnable interface
- by extending the java.lang.Thread class

We will cover both of these below.

### Implementing the Runnable interface

The Runnable interface has the following very simple structure:

```java
public interface Runnable{
	void run();
}
```

To create and use a thread using this interface, we do the following:
1. Create a class which implements the Runnable interface. An object of this class is a Runnable object.
2. Create an object of type Thread by passing a Runnable object as argument of the Thread constructor. The Thread object now has a Runnable object that implements the Run() method.
3. The start() method is invoked on the Thread object created in the previous step.

Example:

```java
public class RunnableThreadExample implements Runnable {
	 public int count = 0;
	 public void run(){
	 	System.out.println("Runnable Thread starting.");
		try{
			while(count<5){
				Thread.sleep(500);
				 count++:
			}
		} catch(InterruptedException exc){
			System.out.println("Runnable Thread interrupted.");
		}
		System.out.println("Runnable Thread terminating.");		
	 }
}

public static void main(String[] args){
	RunnableThreadExample instance = new RunnableThreadExample();
	Thread thread = new Thread(instance);
	thread.start();
	/*waits until above thread counts to 5*/
	while(instance.count!=5){
		try{
			Thread.Sleep(250);
		} catch(InterruptedException exc){
			exc.printStackTrace();
		}
	}
}



```
In the above code, observe that all we really needed to do is have our class implement the Run() method. Another method can then pass an instance of the class to new Thread(obj) and call start() on the thread.

### Extending the Thread class

Alternatively, we can create a thread by extending the Thread class. This will almost always mean that we override the run() method, and the subclass may also call the thread constructor explicitly in its constructor.

The below code provides an example for this:

```java
public class ThreadExample extends Thread {
	int count = 0;
	public void run(){
		System.out.println("Thread Starting.");
		try{
			while(count<5){
				Thread.sleep(500);
				count++;
			}
		}catch(InterruptedException exc){
			System.out.println("Thread interrupted.");
		}
		System.out.println("Thread terminating.")
	}
}


public class ExampleB {
	public static void main(String[] args){
			ThreadExample instance = new ThreadExample();
			instance.start();
			while(instance.count!=5){
				try{
					Thread.sleep(250);
				} catch(InterruptedException exc){
					exc.printStackTrace();
				}
			}
	}
}
```

This code is very similar to the first approach. The difference is that since we are extending the Thread class, rather than just implementing an interface, we can call start() on the instance of the class itself.

### Extending the Thread class vs. Implementing the Runnable interface

When creating threads, there are two reasons why implementing the Runnable interface may be preferable to extending the Thread class:
- Java does not support multiple inheritance. Therefore, extending the Thread class means that the subclass cannot extend any other class. A class implementing the Runnable interface will be able to extend another class.
- A class might only be interested in being runnable, and therefore inheriting the full overhead of the Thread class would be excessive.

## Synchronization and locks

Threads within a given process share the same memory space, which is both a positive and a negative. It enables threads to share data, which can be valuable. However, it also creates the opportunity for issues when two threads modify a resource at the same time. Java provides synchronization in order to control access to shared resources.

The keyword synchronized and the lock form the basis for implementing synchronized execution of code.

### Synchronized methods

Most commonly, we restrict access to shared resources through the use of the synchronized keyword. It can be applied to methods and code blocks, and restricts multiple threads from executing the code simultaneously on the same object.


To clarify the last point, consider the following code:

```java
public class MyClass extends Thread{
	private String name;
	private MyObject myObj;
	public MyClass(MyObject obj, String n){
		name = n;
		myObj = obj;
	}
	
	public void run(){
		myObj.foo(name);
	}
}


public class MyObject{
	public synchronized void foo(String name){
		try{
			System.out.println("Thread " + name + ".foo(): starting.");
			Thread.sleep(3000);
			System.out.println("Thread " + name + ".foo(): ending.");
		}catch(InterruptedException exc){
			System.out.println("Thread " + name + ": interrupted.");
		}
	}
}

```


Can two instances of MyClass call foo at the same time? It depends. If they have the same instance of MyObject, then no. But if they hold different references, then the answer is yes.


```java
/*Different references - both threads can call MyObject.foo()*/
MyObject obj1 = new MyObject();
MyObject obj2 = new MyObject();
MyClass thread1 = new MyClass(obj1, "1");
MyClass thread2 = new MyClass(obj2, "2");
thread1.start();
thread2.start();

/* Same reference to obj. Only one will be allowed to call foo, and the other will be forced to wait*/
MyObject obj = new MyObject();
MyClass thread1 = new MyClass(obj, "1");
MyClass thread2 = new MyClass(obj, "2");
thread1.start();
thread2.start();
```


Static methods synchronize on the class lock. The two threads below could not simultaneously execute synchronized methods on the same class, even if one is calling foo and the other is calling bar.

```java
public class MyClass extends Thread{
	private String name;
	private MyObject myObj;
	public MyClass(MyObject obj, String n){
		name = n;
		myObj = obj;
	}
	
	public void run(){
		if(name.equals("1")) MyObject.foo(name);
		else if(name.equals("2")) MyObject.bar(name);
	}
}


public class MyObject{
	public static synchronized void foo(String name){	/*same as before*/	}
	public static synchronized void bar(String name){	/*same as foo*/	}
}

```

If you run this code, you will see the following printed:
Thread 1.foo(): starting
Thread 1.foo(): ending
Thread 2.bar(): starting
Thread 2.bar(): ending

### Synchronized blocks

Similarly, a block of code can be synchronized. This operated very similarly to synchronizing a method.

```java
public class MyClass extends Thread{
		...
		public void run(){
			myObj.foo(name);
		}
}

public class MyObject{
		public void foo(String name){
			synchronized(this){
			   ...
			}
		}
}

```

Like synchronizing a method, only one thread per instance of MyObject can execute the code within the synchronized block. That means that, if thread1 and thread2 have the same instance of MyObject, only one will be allowed to execute the code block at a time.

## Locks

For more granular control, we can utilize a lock. A lock (or monitor) is used to synchronize access to a shared resource by associating the resource with the lock. A thread gets access to a shared resource by first acquiring the lock associated with the resource. At any given time, at most one thread can hold the lock and, therefore, only one thread can access the shared resource.

A common use case for locks is when a resource is accessed from multiple places, but should be only accessed by one thread at a time. This case is demonstrated by the code below.

```java 
public classs LockedATM {
	private Lock lock;
	private int balance = 100;
	
	public LockedATM(){
		lock = new ReentrantLock();
	}
	
	public int withdraw(int value){
		lock.lock();
		int temp = balance;
		try{
			Thread.sleep(100);
			temp = temp-value;
			Thread.sleep(100);
			balance = temp;
		} catch(InterruptedException e){...}
		lock.unlock();
		return temp;
	}
	
	public int deposit(int value){
		lock.lock();
	int temp = balance;
		try{
			Thread.sleep(100);
			temp = temp+value;
			Thread.sleep(300);
			balance = temp;
		} catch(InterruptedException e){...}
		lock.unlock();
		return temp;
	}
}

```

Of course, we've added code to intentionally slow down the execution of withdraw and deposit, as it helps to illustrate the potential problems that can occur. You may not write code exactly like this, but the situation it mirrors is very, very real. Using a lock will help protect a shared resource from being modified in unexpected ways.


## Deadlocks and deadlock prevention

A deadlock is a situation where a thread is waiting for an object lock that another thread holds, and this second thread is waiting for an object lock that the first thread holds (or an equivalent situation with several threads). Since each thread is waiting for the other thread to relinquish a lock, they both remain waiting forever. The threads are said to be deadlocked.

In order for a deadlock to occur, you must have all four of the following conditions met:
1. *Mutual Exclusion:* Only one process can access a resource at a given time. Or, more accurately, there is limited access to a resource. A deadlock could also occur if a resource has limited capacity.
2. *Hold and Wait:* Processes already holding a resource can request additional resources, without relinquishing their current resources.
3. *No Preemption:* One process cannot forcibly remove another process' resource.
4. *Circular Wait:* Two or more processes from a circular chain where each process is waiting on another resource in the chain.

Deadlock prevention entails removing any of the above conditions, but it gets tricky because many of these conditions are difficult to satisfy. For instance, removing #1 is difficult because many resources can only be used by one process at a time (e.g., printers). Most deadlock prevention algorithms focus on avoiding condition #4: circular wait.
