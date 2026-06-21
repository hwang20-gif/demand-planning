### 🎯 Purpose
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

---

### 📘 Definition
* **Channel Correction:** The process of adjusting the Sell-in Plan based on the gap between the current inventory and the target inventory.
  * **Calibrate Inventory Levels:** Correct and adjust current inventory positions.  
  * **Restore Channel Health:** Bring channel inventory back to a healthy and optimal level.
* **Close gap:** This is about pacing control, not just adjusting raw numbers.
  * **What it means:** It defines the speed of the inventory correction.  
  * **The core focus:** Instead of simply changing shipment volumes, it manages how fast the inventory should return to its target level (e.g., executing the correction over 2 weeks versus 4 weeks to avoid market shock).

---

### 💡 Importance
Without Channel Correction, the following critical issues will arise: 

#### 1. Excess Inventory
* Excess inventory buildup
* Aging and obsolescence risks
* Financial and cash flow pressure
* Warehouse capacity strain 

#### 2. Deficit Inventory
* Severe shortages / Stockouts
* Missed shipments and lost revenue
* Inability to fulfill customer pull-ins
* Order backlog accumulation 

#### 3. Extreme Shipment Volatility
If the correction mechanism is missing or executed too aggressively, it causes:
* Huge supply spikes
* Severe shipment fluctuations
* Factory loading instability
* Capacity saturation / Production bottlenecks 

> 📊 **Summary: The Balancing Act of Channel Correction**
> Ultimately, the essence of Channel Correction is a continuous balancing act among four critical vectors:
> **Market Demand** (DCS) ➔ **Inventory Health** (WOH) ➔ **Shipment Stability** ➔ **Factory Loading**

---

### ⚙️ Calculation & Window Logic
**Sell-in does not equal DCS.** 
> 🧮 **The System Calculation:**
> Sell-in = DCS + Target Inventory - Current Inventory

#### Example Scenario
* **Inputs:** DCS = 1,000 | Target Inventory = 800 | Current Inventory = 500
* **Calculation:** Sell-in = 1,000 + 800 - 500 = **1,300 units**
* **Breakdown of the 1,300 Sell-in Units:**
  * **1,000 units:** Allocated to support market demand (DCS).  
  * **300 units:** Allocated to close the inventory gap.

#### ⏱️ Default Close Gap = 30%
* This means the inventory gap is being corrected using a **smoothed and gradual approach**.  
* **Typical Timeframe:** It usually takes approximately **8 weeks** for the inventory to return to its target level.

⚠️ *A very common misunderstanding is: "A 30% gap adjustment means we are cutting or adding 30% of our total inventory."* **This is incorrect.** It represents the **correction speed (or pacing rate)**.

* **30% (Gradual Correction):** A smooth, phased adjustment designed to minimize supply chain shock. (Global Default)
* **50% (Moderate Speed):** A balanced approach that weighs correction urgency against shipment stability.  
* **80% (Aggressive Pacing):** A rapid adjustment typically used to address urgent inventory imbalances.  
* **100% (Immediate Realignment):** The gap is closed instantly, forcing the inventory back to its target level by the very next week (Causes severe factory overload).

---

### 🧠 Planner Decision Logic
**The system merely provides a baseline; the final decision ultimately rests with the planner.**

#### Factors Planners Must Consider:
* **DCS Demand:** First, verify the true market demand.
* **Current Inventory:** Confirm exactly how much stock is currently held in T1 channels.
* **Product Importance:** For Strategic SKUs, Class A, or Exclusive items, planners may be *willing to maintain a higher inventory buffer* (e.g., increasing from 8 to 10 weeks).
* **Market Trend:** If Sell-through is weak, planners will not aggressively build inventory.
* **Promotions / Product Launches:** Planners may front-load shipments ahead of schedule.
* **Customer Ordering Behavior:** 
  * *Quarterly Ordering:* Taiwan and Korea front-load full-quarter orders.  
  * *Monthly Ordering:* Japan, HK, and ANZ prefer monthly/bi-weekly rolling orders.  
  * *DC Availability-Based:* China customers typically order based on inventory availability.
* **Lead Time:** Shorter for AP (geographically close); longer for ANZ (ocean freight shipping).

#### Override Logic:
* **Weekly Phasing Adjustment:** The system might distribute Sell-in evenly (100/100/100). Planners can manually phase it based on promotion timing (300/150/50).
* **Inventory Strategy Override:** If a product is critical or market risks are elevated, planners will voluntarily hold more inventory to boost service levels.

---

### 📋 Standard Operating Procedure (SOP)

#### Step 1: Input & Gap Calculation
Import the actual weeks on hand and target weeks on hand. Calculate the gap between actual vs target to identify which channels are above or below the target inventory level.  

#### Step 2: Gap Evaluation
Directly evaluate the data to determine if the inventory is "too much low or high than WOH target" or if there is a "channel imbalance".  

#### Step 3: Close Gap Logic (Global Default)
Apply the default 30% Close Gap parameter (taking roughly 8 weeks to return to target). If the inventory gap is too high or too low, manually adjust the Close gap %.  

#### Step 4: Exception Handling (Channel Imbalance)
If a severe channel imbalance occurs, take corrective actions:
1) Validate and update the WOH target, or  
2) Perform manual Sell-in (SI) adjustment units.  

#### Step 5: Regional Actions
* **AP (Asia Pacific):** Execute DCS override for Q+ and Q++ after demand review. Apply SI Freeze for KR/CN/ANZ, and use SI Conversion for JP/HK/TW. Execute Channel Reset in week 2 of the quarter for KR/CN/ANZ (with CSC).  
* **LAT (Latin America):** Perform SI overrides after regional alignment. Gradually shift towards using the Close gap % logic (especially for C items).  

#### Step 6: Final Output
Execute the finalized sell-in adjustments, conversions, or freezes to smoothly bring the channel inventory back to a healthy target weeks on hand.
