# Dynamic Weighted Byzantine Agreement
Implements a new model for the Weighted Byzantine Agreement Problem, which allows for the concept of an “inconsistently faulty” node. Nodes operating under load and affected by application defects can produce accurate and inaccurate responses under different conditions. By conclusively updating the weight of a faulty node to 0, previous algorithms could effectively nullify a node that could eventually stabilize back to correct responses. Our model allows for the weights of nodes to be updated back to previous levels based on good behavior. In this way, nodes that are currently behaving badly because of load or an undiagnosed defect can be weighted to 0, to simplify consensus agreements, but can then be brought back up to a previous valid weight if they again begin to produce valid responses.

Additionally, we provide further dynamic updates to the WBA solution by providing the ability for the pool of nodes to switch from using the simplified Queen Algorithm, which tolerates ρ < ¼ to the more robust King Algorithm, which tolerates ρ < ⅓. Because our system affords a set of inconsistently faulty nodes, the total weight of those that are failing fluctuates. For this reason, we provide the ability to fallback to the King Algorithm when consensus cannot be reached because of a larger pool of faulty nodes. We also provide for the ability to switch back to the Queen Algorithm if the pool of faulty nodes appears to be lower.

