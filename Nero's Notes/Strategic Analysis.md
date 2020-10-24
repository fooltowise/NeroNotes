The starting point for a strategic analysis is to do a market-by-market  assessment of the existence and sources of competitive advantage (see [[Strategic Decisions Vs Tactical Decisions]]), and then to assess the size of the respective players. 

This leads to the following decision tree:

```mermaid
graph TD
  A[All Markets] --> B(Competitive Advantage: Yes)
  A --> C(Competitive Advantage:No)
  B --> D{Single Dominant Firm?}
  C -->|Operational Effectiveness|E(Efficiency, Efficiency, Efficiency)
  D-->|Yes| F{Is it You?}
  D -->|No| G(Hard Strategic Decisions)
  G --> H(Game Structure, simulation)
  G --> I(Prisoner's Dilemna, Entry Preemption)
 G --> J(Cooperation, Bargaining)
  F --> |Yes|K(Manage Competitive Advantage)
  F --> |No|L(You are an ant: Exit Gracefully)
```


See Also [[Prisoners Dilemna]]