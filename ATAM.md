ATAM Procedure

Architectural Decisions:/n
AD1: Active Redundancy
AD2: Cache-Aside Caching
AD3: Weighted Round-Robin Load Balancing
AD4: Monitering & Logging 
AD5: Maintenance Strategy

Sensitivity:
S1: Cache hit ratio
S2: Load balancing weights
S3: Fallover Speed
S4: Network Latency
S5: Database bottlenecks

Tradeoff:
T1: Cache-aside vs. write-through cache 
T2: Weighted round-robin vs. least connections
T3: Active redunduncy vs. cost/complexity 
T4: Performance vs. consistency 

Risk:
R1: Cache warm-up lag
R2: Stale/invalid cache enteries
R3: Fallover misconfig
R4: Uneven load distribution
R5: Operational overhead
R6: Network partitioning

Nonrisk:
NR1: Security exposure
NR2: Data durability
NR3: User session continuity 
NR4: Scheduled maintenance 

Scanario: QA2
Scenario Description: The system should remain operational and accessible 99.5% of the time or higher. Scheduled maintenance should cause minimal disruption, and automatic failover mechanisms should recover from crashes or downtime instantly to maintain continuous service availability.
Stimulus: fault or maintenance event
Enviroment:
Response:





