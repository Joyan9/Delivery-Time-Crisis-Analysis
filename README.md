# Blinkit Delivery Time Crisis - Root Cause Analysis Project

 Blinkit, is an Indian quick-commerce company. Blinkit's core value proposition is built on speed. The 10-minute delivery guarantee is not just a marketing tag, it is the primary defensive moat against other quick-commerce competitors.

## Analysis Summary
![Summary of the Analysis Generated Using Notebooklm](https://github.com/Joyan9/Delivery-Time-Crisis-Analysis/blob/main/Analysis_Summary.png)

## 📦 Project Overview

This project includes a **root cause analysis** in a simulated high-stakes business scenario. My job was to analyze a delivery time crisis at Blinkit, where the platform-wide average delivery time has surged from 9 minutes to 14+ minutes.

## 🎯 Mission Goals

Leadership is divided on the solution:
- **COO**: "Hire 1,000 more riders immediately"
- **CMO**: "Pause all marketing until fixed"  
- **CTO**: "It's just seasonal rain, it will pass"

**My job**: Find the ground truth using data, not opinions.

---

## 📊 Dataset Files

### 1. `ds_blinkit_orders.csv` (109,698 rows)
Order-level transaction data for 30 days
- `order_id`: Unique order identifier
- `zone_id`: Delivery zone (101-107)
- `store_id`: Dark store fulfilling the order (1-12)
- `order_time`: When the order was placed
- `delivery_time_mins`: Time from payment to doorstep
- `status`: Delivered/Cancelled
- `cancellation_reason`: Reason if cancelled

### 2. `ds_blinkit_store_load.csv` (34,560 rows)
Store operational snapshots (every 15 minutes)
- `store_id`: Dark store ID
- `timestamp`: Snapshot time
- `active_riders`: Number of available riders at the store
- `orders_in_queue`: Packed orders waiting for rider assignment
- `avg_rider_wait_time`: Average wait time for riders at store

### 3. `ds_blinkit_events.csv` (7 rows)
External events that might affect operations
- `event_id`: Unique event identifier
- `zone_id`: Affected zone
- `event_type`: Rain/Traffic_Jam/Server_Downtime
- `start_time`, `end_time`: Event duration

---

## 🔍 The Crisis

**Normal Period** (Jan 1-23): Average delivery time = **9.29 minutes**  
**Crisis Period** (Jan 24-31): Average delivery time = **12.24 minutes**  
**Impact**: +2.95 minutes (+31% degradation)

**Secondary Effects**:
- Cancellation rate jumped
- "Too long" cancellations spiked significantly
- User retention showing early warning signs

---

## 🎓 Learning Objectives

By completing this project, I'll practice:

1. **Root Cause Analysis**
   - Distinguishing correlation from causation
   - Testing multiple competing hypotheses
   - Using data to challenge assumptions

2. **SQL Analysis**
   - JOIN operations across multiple tables
   - Aggregations and window functions
   - Performance benchmarking

3. **Business Thinking**
   - Understanding stakeholder perspectives
   - Identifying actionable insights
   - Communicating technical findings to non-technical leaders
   - Proposing cost-effective solutions

4. **Data Storytelling**
   - Building a narrative from data
   - Supporting claims with evidence
   - Addressing counterarguments

---

## 📝 Deliverables

### 1. SQL Analysis
A set of queries that:
- Isolate the root cause variables
- Disprove alternative hypotheses
- Quantify the impact
- Identify specific problem areas

### 2. Strategic Memo (1-page)
Addressed to COO & VP of Product:

**Structure:**
1. **Executive Summary**: What is the root cause? (2-3 sentences)
2. **Analysis**: How did you reach this conclusion? (data-driven)
3. **Why Others Were Wrong**: Address the COO, CMO, and CTO's hypotheses
4. **Recommendation**: What's the immediate intervention?
5. **Expected Impact**: What metrics will improve and by how much?

---