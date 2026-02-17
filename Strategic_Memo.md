# Memo

**TO:** COO & VP of Product

**FROM:** Lead Product Analyst, Logistics & Fulfillment

**RE:** Dispatch Inefficiency at 4 Stores is Causing the Delivery Crisis


**SITUATION**

Since January 24th, platform-wide delivery times have surged from 9.3 to 12.2 minutes, triggering a 310% spike in cancellations. At current run rates, this is costing an estimated ₹92,000 per day in lost revenue. The crisis is not platform-wide, it is entirely concentrated in 4 stores.

**FINDING**

The root cause is a dispatch coordination failure. At stores 1, 2, 4, and 9, packed orders are sitting on shelves while available riders stand idle at the same location - neither being connected to the other. Riders at these stores are waiting an average of 4.7 minutes before pickup (vs. 1.2 minutes at healthy stores). This wait time alone accounts for the full delivery time increase. The pattern holds at 2am with minimal order volume, confirming this is a process failure, not a capacity problem.

**WHY OTHER EXPLANATIONS ARE WRONG**

The COO's instinct to hire riders is understandable but misdiagnosed - rider counts are identical in the normal and crisis periods. 

The CTO's rain hypothesis doesn't hold because zero rain events occurred after January 24th.

A demand surge can also be ruled out: orders per day changed by less than 1% between periods.

**RECOMMENDATION**

Within 48 hours: Engineering and Ops to conduct a joint audit of the dispatch workflow at stores 1, 2, 4, and 9 to determine whether this is an algorithm issue, a rider app bug, or a process breakdown. No new hiring is needed before this audit is complete.

**EXPECTED IMPACT**

Resolving the dispatch bottleneck should return average delivery times at affected stores from 14.7 to approximately 9.5 minutes, bringing the platform average back below the 10-minute SLA. 
Primary success metric: platform average delivery time. 
Guardrail: avg orders-in-queue at bottleneck stores returning to below 3 (from current 11.7).

---
