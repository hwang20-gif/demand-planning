### 🎯 Purpose
To address the inconsistencies in how regional planners manage events and to enhance visibility, we are establishing a standardized process. Previously, some planners integrated event demand directly into forecasts or adjustments, making it difficult for Demand Planning, Supply Planning, and S&OP teams to distinguish between organic growth and specific promotions. 

By unifying event management globally, the Global Team aims to enable easier demand comparisons across markets and help Supply Planning more accurately align capacity and supply strategies.

---

### 📘 Definition
* **Events:** Refers not only to marketing and promotional activities (such as Prime Day and Black Friday) but also encompasses all critical milestones affecting demand planning, including Demand Review, Forecast Review, and Regional S&OP meetings. 
* **Global Event Calendar:** A synchronized schedule for all teams to maintain defined event timelines throughout the demand planning cycle.
* **Event Management Workbook:** An independent system within **Maestro Consensus** where events requiring separate management must be established, defined by specific details such as customer information, DCS quantities, weeks, and offsets.

---

### 💡 Importance
* **High Visibility:** Enables teams to seamlessly track and analyze specific event performance.
* **Eliminate Double Counting:** Independent and standardized management prevents event demand from being conflated with baseline demand.
* **Prevent Overstocking:** Establishes a strict **1:1 correlation** between DCS and Sell-in for promotions. This clarifies for planners that additional safety stock or buffers are *not* required for confirmed event demand.

---

### ⚙️ Event Logic & Guardrails
* **Always Incremental:** Event demand is treated as additive (`Final Forecast = Baseline + Event Qty`). If the Baseline already includes the event, planners must manually deduct it to avoid double counting.  
* **Link & Offset:** CSC or KAM provides the lead time offset from Event DCS to Sell-in. The system then automatically projects the Sell-in Forecast based on this offset.  
* **1:1 Ratio:** Maintain a strict 1:1 link between Event DCS and Sell-in; no additional safety stock should be layered on top of events.  
* **Quantity Split:** For large-scale events, demand must be split across multiple weeks after consulting CSC, KAM, and Supply teams to ensure factory capacity support.  
* **ASP Check:** Significant deviations in Average Selling Price (ASP) must be specifically defined and highlighted (e.g., requested via Asana).

---

### 📋 Standard Operating Procedure (SOP)

#### Step 1: Review Global Event Calendar
At the start of each planning cycle, Demand Planners must review the Global Event Calendar to ensure all upcoming events are clearly defined and maintain high visibility during S&OP and Demand Review meetings.  

#### Step 2: Event Consensus
The CCM team conducts an initial review to establish event volume and strategy consensus.  

#### Step 3: Validate Supply Availability
If an event is scheduled to occur within the lead time window, the S&OE team must validate supply availability with GPP before proceeding through the event cycle.  

#### Step 4: Independent System Entry
Based on the CCM consensus, DP loads the event into the Maestro Consensus system via the **Event Management Workbook**, creating an independent record categorized under a specific Customer ID or Customer Subgroup.  

#### Step 5: Validate Baseline Forecast
DP must evaluate whether the current baseline forecast already includes the anticipated promotional event volume.  

#### Step 6: Override DCS Baseline (Anti-Double Counting)
If the forecast already includes the promotion (i.e., the event is not fully incremental), DP must manually adjust down (override) the DCS baseline to exclude the event volume. Planners are also required to collect learnings and examples of these judgmental calls for future reference.  

#### Step 7: Confirm Incremental Logic & 1:1 Link
Event demand is fundamentally treated as "Always Incremental." DP must link DCS to Sell-in (SI) at a 1:1 ratio. **No additional Safety Stock (SS) or Weeks on Hand (WOH) should be added** to the event.  

#### Step 8: Event Quantity Split
If the event quantity is too large to be fulfilled in a single week, DP must sync up with CSC/KAM to define a reasonable split of the event quantity across multiple weeks to smooth out factory loading.  

#### Step 9: Set Lead Time Offset
The event DCS to SI lead time offset must be aligned with and given by CSC/KAM. DP enters this offset into the system to automate the Sell-in forecast projection.  

#### Step 10: ASP Check
DP must flag the event Average Selling Price (ASP) if it differs significantly from the usual ASP.  

#### Step 11: Define the Carry-Over Window (Regional Guidelines)
Post-execution, if there is unsold event volume, DP must execute carry-over rules strictly based on the following regional guidelines:
* **Europe (EU) / AP:** Strictly cut off by the DCS event week; no automatic carry-over.
* **AP (Exception):** CSC will proactively inform if the remaining event quantity is still valid and should be retained.
* **North America (NAM):** Managed case by case. Carry over more per CSC request, with the system load defined by DP.
* **Emerging Markets (EM):** Managed case by case and formally checked with CSC.
* **Latin America (LAT):** Managed case by case. A specific rule will be defined, pushing accountability back to the event owner.  

#### Step 12: Final System Output
The process concludes in the **Maestro Consensus (Event Management Workbook)**. The ultimate deliverable is a **Standalone Event Record** encapsulating the Event Name, Customer ID, DCS Quantity, DCS Week, Offset, and Link parameters. 

This systematic approach ensures that event demand is entirely decoupled from standard forecasts, empowering global supply and demand teams to track event performance accurately and execute consistent capacity planning.
