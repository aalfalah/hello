## Advantages of Dimensional Modeling for Behavioural User Analytics


The primary advantage of a **dimensional model** lies in its simplicity. With fewer tables and straightforward joins, combined with clearly defined facts at the center, it becomes easier to conceptualise how metrics like sales can be analysed and to create the necessary queries.

A more nuanced benefit of dimensional models is their focus on actionable insights. Unlike models that simply denormalise a 3NF ER structure into fewer tables to handle database limitations for complex BI queries, well-designed dimensional models are purpose-driven. 

They emerge from a deliberate process of exploring and uncovering the details of business events worth measuring. These models are structured around key questions—sometimes referred to as the "7Ws"—to capture the complete context of each event:

- **Who** was involved?
- **What** was done, and to what was it applied?
- **When** did it occur?
- **Where** did it happen?
- **HoW** much or how many were recorded, and how can it be quantified?
- **Why** did it happen?
- **HoW** did it unfold—what was the manner or process?

This approach ensures that dimensions and fact tables are not arbitrary but instead reflect the essential characteristics of meaningful business activities.

![[7WsModelling.png]]