# **Channel Correction** 

**Purpose**   
**To maintain a healthy T1 channel inventory (Weeks on Hand, WOH) and ensure the Sell-in Plan accurately reflects both market demand and actual inventory status.**

Demand Planning is not just about forecasting market demand (DCS / Sell-through). It must also balance the following factors:

* **Channel inventory health**  
* **Future demand coverage**  
* **Customer ordering behavior**  
* **Inventory risks** (e.g., aging or excess)  
* **Shipment stability**  
* **Factory loading impact**

Therefore, the Sell-in Plan does more than just support DCS. It must also:

* **Support target inventory levels**  
* **Maintain healthy channel stock levels**  
* **Avoid shortages**  
* **Avoid overstocking**  
* **Smooth out shipment fluctuations**

At its core, **Channel Correction** means dynamically adjusting the Sell-in Plan and inventory levels based on real-time market demand and current channel inventory conditions.

**Definition**

**Channel Correction** is the process of adjusting the Sell-in Plan based on the gap between the current inventory and the target inventory.

* Calibrate Inventory Levels: Correct and adjust current inventory positions.  
* Restore Channel Health: Bring channel inventory back to a healthy and optimal level.

**Close gap** is about pacing control, not just adjusting raw numbers.

* What it means: It defines the speed of the inventory correction.  
* The core focus: Instead of simply changing shipment volumes, it manages how fast the inventory should return to its target level (e.g., executing the correction over 2 weeks versus 4 weeks to avoid market shock).


**Importance**

Without Channel Correction, the following critical issues will arise: 

**Excess Inventory** 

This leads to:

* **Excess inventory buildup**   
* **Aging and obsolescence risks**   
* **Financial and cash flow pressure**   
* **Warehouse capacity strain** 

### **Deficit Inventory** 

This leads to:

* **Severe shortages / Stockouts**   
* **Missed shipments and lost revenue**   
* **Inability to fulfill customer pull-ins**  
* **Order backlog accumulation** 

### **Extreme Shipment Volatility** 

If the correction mechanism is missing or executed too aggressively, it causes:

* **Huge supply spikes**   
* **Severe shipment fluctuations**   
* **Factory loading instability**   
* **Capacity saturation / Production bottlenecks** 

## **Summary: The Balancing Act of Channel Correction**

Ultimately, the essence of **Channel Correction** is a continuous balancing act among four critical vectors:

* **Market Demand** (DCS / Sell-through)  
* **Inventory Health** (Optimal WOH)  
* **Shipment Stability** (Smooth logistics flow)  
* **Factory Loading** (Balanced production lines)

**Logic**

**Sell-in does not equal DCS.** Sell in \= DCS \+ Inventory Adjustment

### **The System Calculation:**Sell in \= DCS \+ Target Inventory \- Current Inventory

### **Example Scenario**

DCS:1000、Target Inventory:800、Current Inventory:500

### **Calculation:**Sell in= 1,000 \+ 800 \- 500 \= 1,300

### Breakdown of the 1,300 Sell-in Units:

* **1,000 units:** Allocated to support market demand (DCS).  
* **300 units:** Allocated to close the inventory gap.

# **Default Close Gap \= 30%**

* This means the inventory gap is being corrected using a **smoothed and gradual approach**.  
* **Typical Timeframe:** It usually takes approximately **8 weeks** for the inventory to return to its target level.

**"Closing the Gap" manages pacing, not total volume.**

A very common misunderstanding is:

*"A 30% gap adjustment means we are cutting or adding 30% of our total inventory."*

**This is incorrect.** **The True Meaning:** It represents the **correction speed (or pacing rate)**.

### **Example: Understanding the "Close Gap" Rates**

* **30% (Gradual Correction)** A smooth, phased adjustment designed to minimize supply chain shock.  
* **50% (Moderate Speed)** A balanced approach that weighs correction urgency against shipment stability.  
* **80% (Aggressive Pacing)** A rapid adjustment typically used to address urgent inventory imbalances.  
* **100% (Immediate Realignment)** The gap is closed instantly, forcing the inventory back to its target level by the very next week.

### **Why Can't We Just Use 100%?**

If the correction happens too fast, the factory will suddenly experience:

* **A huge spike in shipments** (or a massive drop in shipments).

This directly causes:

* **Loading instability**  
* **Severe supply fluctuations**   
* **Factory saturation / Overload**

Therefore, the **Global Default is set to 30%** to act as a smoothing mechanism.

### **The Objective of the 30% Default:**

* **Smooth out shipment volumes**  
* **Stabilize factory loading**   
* **Avoid extreme highs and lows** 

---

**Planner Decision Logic**

**The system merely provides a baseline; the final decision ultimately rests with the planner.**

### **Factors Planners Must Consider** 

* #### **DCS Demand** 

First, verify the **true market demand**.

* #### **Current Inventory**

Confirm exactly **how much stock is currently held** in T1 channels.

* #### **Product Importance** 

For example:

* Strategic SKUs  
* Class A Products  
* Exclusive Customer Products

**Planner Action:** Planners may be **willing to maintain a higher inventory buffer** (e.g., increasing from 8 weeks to 10 weeks).

* #### **Market Trend** 

If Sell-through is weak and the market is softening, planners will likely **not aggressively build inventory**.

* #### **Promotions / Product Launches** 

During promotion months, product launch periods, or phases with high pull-in demand, planners may **front-load shipments** ahead of schedule.

* #### **Customer Ordering Behavior** 

Different regions exhibit distinct ordering patterns:

* **Quarterly Ordering :** Regions like **Taiwan** and **Korea** often place orders for an entire quarter at once.  
* **Monthly Ordering:** Regions like **Japan**, **Hong Kong (HK)**, and **Australia & New Zealand (ANZ)** prefer monthly ordering.  
* **DC Availability-Based Ordering :** For example, in **China**, customers only place orders when the DC has physical stock available.

* #### **Lead Time** 

Lead times directly impact the **correction timing** and **freeze timing**:

* **Asia-Pacific (AP):** Geographically close to the factory, resulting in shorter lead times.  
* **Australia & New Zealand (ANZ):** Subject to longer shipping lead times.

### **Override Logic** 

The system will perform the initial automatic conversion, but the planner will still manually override it based on the following:

* #### **Weekly Phasing Adjustment** 

The system might distribute the Sell-in plan evenly:

* **W1:** 100 | **W2:** 100 | **W3:** 100

However, due to **Month 1 promotions**, **customer pull-ins**, or specific **shipment timing**, the planner may manually phase it as:

* **W1:** 300 | **W2:** 150 | **W3:** 50


* #### **Inventory Strategy Override** 

#### If a planner determines that a product is highly critical, market risks are elevated, or there is a need to boost service levels, they will **voluntarily hold more inventory**.

**SOP**

* **Step 1: Input & Gap Calculation** Import the actual weeks on hand and target weeks on hand. Calculate the gap between actual vs target to identify which channels are above or below the target inventory level.  
* **Step 2: Gap Evaluation** Directly evaluate the data to determine if the inventory is "too much low or high than WOH target" or if there is a "channel imbalance".  
* **Step 3: Close Gap Logic (Global Default)** Apply the default 30% Close Gap parameter (taking roughly 8 weeks to return to target). If the inventory gap is too high or too low, manually adjust the Close gap %.  
* **Step 4: Exception Handling (Channel Imbalance)** If a severe channel imbalance occurs, take corrective actions: 1\) Validate and update the WOH target, or 2\) Perform manual Sell-in (SI) adjustment units.  
* **Step 5: Regional Actions**  
  * **AP (Asia Pacific):** Execute DCS override for Q+ and Q++ after demand review. Apply SI Freeze for KR/CN/ANZ, and use SI Conversion for JP/HK/TW. Execute Channel Reset in week 2 of the quarter for KR/CN/ANZ (with CSC).  
  * **LAT (Latin America):** Perform SI overrides after regional alignment. Gradually shift towards using the Close gap % logic (especially for C items).  
* **Step 6: Final Output** Execute the finalized sell-in adjustments, conversions, or freezes to smoothly bring the channel inventory back to a healthy target weeks on hand

