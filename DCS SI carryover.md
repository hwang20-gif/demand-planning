### 🎯 Purpose
**To ensure the Weekly Supply Plan aligns with the Quarterly Commercial Commitment by preventing unintentional loss of unfulfilled demand.** 

---

### 📘 Definition
* **DCS Carryover:** The process of reassigning **unconsumed forecasts** to future periods. It prevents **forecast drop** when shipments do not occur as planned in a specific week, ensuring that the total quarterly commitment remains intact. 

---

### 💡 Importance
* **System Disaggregation:** Although we input forecasts on a quarterly or monthly basis, the system automatically disaggregates these numbers into weekly plans for supply planning.   
* **Preventing Forecast Erosion:** If actual shipments fall short of the weekly forecast and the system simply discards the unfulfilled portion, the total demand plan will continuously shrink. 

> 💰 **Example Scenario:**
> * **Quarterly Commitment:** $10M
> * **Situation:** Shipments in the early weeks are lower than the weekly forecast.
> * **Risk without Carryover:** The total Demand Plan might drop to $7M, even though the Sales/Commercial teams are still committed to the original $10M target.

---

### ⚙️ Carryover Strategic Logic
**DCS Carryover is not an automatic process. It requires a strategic assessment based on the following two criteria:** 

#### 1. Nature of the Demand: Delay vs. Decline
We must determine if the unconsumed forecast is a **timing issue** or a **demand loss**:
* **Case for Carryover (Delay):** If the shortfall is caused by a temporary shift—such as a customer ordering late, supply constraints, or a delayed promotional event—the volume should be **carried over**.  
* **Case for Reduction (Decline):** If the market demand is weakening or the product has lost its competitive edge, the forecast should be **revised downward** instead of being carried over.

#### 2. Market Segmentation & Regional Rules

* **Mature Markets (NAM, Europe, ANZ, Japan)**
  * **Default Rule: No Carryover by Default.** 
  * *Logic:* These markets are primarily **market-driven**, meaning consumption patterns closely reflect actual end-user demand. If a weekly forecast is 100 but actual shipment is only 50, it is highly probable that the true market demand was only 50. Carrying over the remaining volume risks creating **artificial demand** and inventory buildup. 
  * **Exceptions (Valid Criteria for Carryover):** Only permitted with clear evidence that demand is delayed, not lost:
    1. *Large-scale Events:* Significant spikes such as Prime Day or Black Friday.
    2. *Order Timing:* Explicit customer delays in placing purchase orders (POs).
    3. *Supply Constraints:* Production or allocation issues that prevented fulfillment.
    4. *Logistics/Shipment Delays:* Goods are ready but delayed in transit.
    5. *Commercial Validation:* Formal confirmation from Sales Teams that demand will resurface within the quarter.

* **Emerging Markets (APM, Greater China, Latin America)**
  * **Default Rule: Carryover is Frequently Required.** 
  * *Logic:* These regions are often **commitment-driven** and operate under a push-based model. The quarterly target (e.g., $10M) is a firm commercial promise. Demand is often **backloaded** (clustering at the end of the month/quarter). A shortfall early on indicates a delay in execution, not a drop in demand. To keep Quarterly Sizing intact, unconsumed forecasts are carried over to future weeks.
  * **Common Scenarios for Carryover:**
    1. *Month-End / Quarter-End Push:* Concentrated shipment efforts to meet financial targets.  
    2. *Major Promotional Events:* Large-scale campaigns such as the **618 Shopping Festival**.  
    3. *Phased Fulfillment:* Slow starts compensated by accelerated shipments in later weeks.  
    4. *Commercial Assurance:* Formal confirmation that the Quarterly Commitment remains achievable.

---

### 📋 Standard Operating Procedure (SOP)

#### Step 1: Performance Tracking
* **Action:** Compare **Weekly Forecast** against **Actual Shipments**.  
* **Objective:** Monitor the fulfillment rate and identify any weekly variances.

#### Step 2: Gap Identification
* **Action:** Calculate the **Unconsumed Forecast**.  
* **Formula:** `Gap = Weekly Forecast - Actual Shipment`

#### Step 3: Root Cause Analysis
* **Action:** Diagnose the underlying reason for the gap.  
* **Assessment:** Determine if the variance is due to a **Timing Issue** (e.g., supply constraints, logistics delays) or a **market fluctuation**.

#### Step 4: Commercial Validation
* **Action:** Review the findings with **CCM / Commercial Teams** (e.g., during Catch-up Demand Review meetings).  
* **Verification:** Confirm whether the specific demand is still valid for the remainder of the quarter.

#### Step 5: Regional Logic Assessment
* **NAM, EU, JP, ANZ:** Apply a "No Carryover" policy by default unless a specific execution barrier is identified.  
* **AP GC, APM, LAT:** Apply a "Carryover" policy if the quarterly commitment remains firm, recognizing the backloaded nature of these markets.

#### Step 6: Execution Decision
* **Scenario A (Delay):** If the demand is merely shifted, perform a **Carryover** by reallocating the gap to subsequent weeks.  
* **Scenario B (Loss):** If the demand has evaporated, perform a **Forecast Downside** (Cut) instead of carrying it over.

#### Step 7: System Update
* **Action:** Update the **DCS Forecast** in the system.  
* **Tooling:** Use the **Ivy Script** to generate the upload format based on the adjusted values.

#### Step 8: Final Alignment Audit
* **Action:** Cross-check the updated **Quarterly Demand Plan** against the **Sales Commitment**.  
* **Goal:** Prevent data distortion and ensure a clean, accurate supply signal for the factory.
