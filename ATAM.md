ATAM Procedure

Architectural Decisions:<br>
AD1: Active Redundancy<br>
AD2: Cache-Aside Caching<br>
AD3: Weighted Round-Robin Load Balancing<br>
AD4: Monitering & Logging<br>
AD5: Maintenance Strategy<br>

Sensitivity:<br>
S1: Cache hit ratio<br>
S2: Load balancing weights<br>
S3: Fallover Speed<br>
S4: Network Latency<br>
S5: Database bottlenecks<br>

Tradeoff:<br>
T1: Cache-aside vs. write-through cache <br>
T2: Weighted round-robin vs. least connections<br>
T3: Active redunduncy vs. cost/complexity <br>
T4: Performance vs. consistency <br>

Risk:<br>
R1: Cache warm-up lag<br>
R2: Stale/invalid cache enteries<br>
R3: Fallover misconfig<br>
R4: Uneven load distribution<br>
R5: Operational overhead<br>
R6: Network partitioning<br>

Nonrisk:<br>
NR1: Security exposure<br>
NR2: Data durability<br>
NR3: User session continuity <br>
NR4: Scheduled maintenance <br>
<br>

Scanario: QA2<br>
Scenario Description: The system should remain operational and accessible 99.5% of the time or higher. Scheduled maintenance should cause minimal disruption, and automatic failover mechanisms should recover from crashes or downtime instantly to maintain continuous service availability.<br>
Stimulus: fault or maintenance event<br>
Enviroment: system running as required; redundant servers, monitering tools, and maintenance in order. <br>
Response: fault/maintenance detcted, users experience minimal disruption (<0.5% availibility), instant failover <br>

<table>
  <thead>
    <tr>
      <th>Architectural Decision</th><th>Sensitivities</th><th>Tradeoffs</th><th>Risks</th><th>Non‑Risks</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>AD1</td>
      <td>
        S3<br>
        S4
      </td>
      <td>
        T3
      </td>
      <td>
        R3<br>
        R5<br>
        R6
      </td>
      <td>
        NR1<br>
        NR2<br>
        NR4
      </td>
    </tr>
    <tr>
      <td>AD2</td>
      <td>
        S1<br>
        S5
      </td>
      <td>
        T1<br>
        T4
      </td>
      <td>
        R1<br>
        R2
      </td>
      <td>
        NR1<br>
        NR2<br>
        NR4
      </td>
    </tr>
    <tr>
      <td>AD3</td>
      <td>
        S2<br>
        S4
      </td>
      <td>
        T2
      </td>
      <td>
        R4<br>
        R5
      </td>
      <td>
        NR1<br>
        NR2<br>
        NR3
      </td>
    </tr>
    <tr>
      <td>AD4</td>
      <td>
        S1<br>
        S2<br>
        S3
      </td>
      <td>
        T3 (indirect)<br>
        T4
      </td>
      <td>
        R5<br>
        R3
      </td>
      <td>
        NR1<br>
        NR2<br>
        NR4
      </td>
    </tr>
    <tr>
      <td>AD5</td>
      <td>
        S3<br>
        S4
      </td>
      <td>
        T3
      </td>
      <td>
        R3<br>
        R6
      </td>
      <td>
        NR1<br>
        NR2<br>
        NR4
      </td>
    </tr>
  </tbody>
</table>



