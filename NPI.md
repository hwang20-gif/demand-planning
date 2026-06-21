### 🎯 Purpose
This process outlines the overall workflow for New Product Introduction (NPI), specifically defining when the Demand Planning department should engage, which discussions they need to participate in, and the system configurations and forecast upload tasks they must complete.

**The core objective is to enable early engagement of Demand Planning in NPI forecast planning. This ensures the team thoroughly understands launch assumptions and is granted sufficient lead time for operations, thereby mitigating planning risks caused by delayed data entry into the system.**

---

### 📘 Definition
While the overall NPI process involves multiple departments (including product information preparation, SKU/part number creation, costing, and compliance readiness), **the specific workflow relevant to DP is defined as the complete cycle spanning from SKU enablement, pre-release, bottom-up forecast engagement, and forecast upload, all the way through to post-Gate 2 change control.** 

---

### 💡 Importance
* **Resolving Past Pain Points:** Previously, DP had to wait until Commercial, Region, BG, Finance, and Leadership had all granted final approval before initiating the forecast upload. This left DP with an extremely narrow operational window (often expected to integrate it into the planning cycle the next day). 
* **Early Preparation:** The new process integrates DP into discussions as soon as Commercial / CCM begins establishing the forecast, allowing SKU enablement, data preparation, and assumption alignment to be completed ahead of time.  
* **Enhancing Forecast Credibility:** By providing historical data, look-alike product data, and phase-in/phase-out information, DP verifies whether the Initial Loading Quantity (ILQ) is sufficient and recommends a realistic ramp-up plan to prevent overly aggressive or conservative forecasts.

---

### ⚙️ NPI Logic & Guardrails

#### 1. Forecast Loading Level
Forecasts must be loaded at the lowest granular level possible per region:
* **NAM (North America):** By customer (e.g., Walmart, Best Buy).  
* **Europe:** By forecast stream (e.g., Amazon, Central Distribution (CD), Europe Others). *(Note: Ruben needs to update the allocation percentages).*  
* **AP / GCN / LATAM:** Typically by country.  
* **Emerging Markets:** Segmentation logic is currently uncertain and requires further confirmation with Mickey or the process owner.

#### 2. Timeline & Offset Logic (OSD / DCS / Sell-in Offset)
* **OSD (On-Shelf Date):** The actual product launch date in store/online. DCS is typically set around **2 weeks prior** to OSD.  
* The lead time offset for Sell-in and ILQ (Initial Loading Quantity) varies by region and must follow regional lead time logic or the regional NPI Lead Time Matrix (e.g., the matrix used in the AP region).

#### 3. ILQ & Ramp-up Strategy
* Evaluate historical patterns of look-alike products (e.g., historically, the first month only accounts for 10% of the 12-month total forecast) to determine the ramp-up strategy.  
* Decide whether the new product should ramp up progressively month-by-month, or adopt an aggressive front-loaded forecast in the first 3 months due to strong market demand.

#### 4. Cannibalization & Phase-out
* When a new product acts as a replacement, planners must review the legacy product's sell-out, inventory, and remaining demand.  
* This prevents excessive overlap between new and old forecasts, avoiding over-forecasting the new product while the legacy product still has remaining inventory.

#### 5. Statistical Forecast vs. Override Phase-Out
* During the initial NPI phase, **Manual Overrides must be used** due to a lack of historical data. Statistical forecasts (nearest neighbor or 13 weeks actuals) are not reliable at this stage.  
* After approximately 3 to 6 months post-launch, once sufficient actual data is accumulated, evaluate transitioning control to the system by gradually removing the overrides.

#### 6. First 3 Months Freeze Rule
* The historical rigid rule requiring the first 3 months of the forecast to be frozen is no longer enforced. If market conditions shift, adjustments can be made provided they undergo proper alignment and approval.

#### 7. Post-Gate 2 Change Management
* **Future State:** Any pre-launch forecast adjustments—increases or decreases—cannot simply be updated in the system. They must go through formal alignment with GCO and Commercial/CCM, and the Bottom-up template and market assumptions must be updated concurrently. Casual requests via emails or chat messages are strictly unacceptable.

---

### 📋 Standard Operating Procedure (SOP)

#### Phase 1: Pre-Launch Preparation & System Initialization
* **Step 1.1 (Prepare NPI Foundational Data):** The product team generates new product SKUs, part numbers, costing, and preliminary launch information.
* **Step 1.2 (Provide Product Roadmap and SKU List):** GCO / BG must constantly update the product roadmap for DP starting from this phase. Simultaneously, GCO must share the NPI SKU list ahead of time to initiate subsequent system configurations.
* **Step 1.3 (Track Timeline and SKU Enablement):** DP must utilize the Launch Calendar to track the Gate 2 schedule in advance. The system-side execution for SKU enablement follows this sequence: `SKU COSA approval` ➔ `Pre-release` ➔ `Auto SKU-Org enabled` ➔ `Manual enablement in the MDM system`.
* **Step 1.4 (System Synchronization):** Following manual enablement in MDM, a system synchronization period of approximately 24–48 hours is required before data appears in Maestro / NPI Workbook. DP should utilize this waiting window to begin preliminary forecast preparation.

#### Phase 2: Bottom-Up Forecast Build-Up & Alignment
* **Step 2.1 (Initiate Bottom-Up Forecast):** Commercial / CCM establishes the baseline forecast for the next 12 months and defines the new product's incrementality, GTM (Go-To-Market) channel strategy, product categorization, and specific launch objectives.
* **Step 2.2 (Early DP Engagement):** DP engages in discussions during the initial stages of forecast build-up, providing historical data, verifying the rationality of the ILQ, and recommending a realistic ramp-up plan based on historical patterns.
* **Step 2.3 (Finalize Market Assumption Alignment):** DP and CCM align on parameters: monthly quantity breakdown, Average Selling Price (ASP), On-Shelf Date (OSD), seasonality, embargo date, Last Time Buy (LTB), and cannibalization effects. This data must be fully documented in the NPI Masterfile and Assumption File, and confirmed via a checkbox in the Launch Calendar.

#### Phase 3: Approval Gate
* **Step 3.1 (Regional Review):** Regions review and approve their respective forecasts.
* **Step 3.2 (Final Leadership Approval):** GCO / Finance / Leadership make the final decision.  
  ⚠️ **[Mandatory Rule]:** DP must receive an official approval email that includes the GCO LT, Finance representative Mohammed, and Global Head of Retail Frederic Derreumaux before being authorized to upload.
* **Step 3.3 (Secure Operational Lead Time):** Upon receiving the complete approval email, DP must ensure a minimum of **1 week of lead time** for forecast load & validation to prepare for the system upload.

#### Phase 4: System Execution
* **Step 4.1 (Timeline Parameter Calculation):** DP calculates the DCS timing based on the OSD (typically 2 weeks prior). Based on the regional NPI Lead Time Matrix, DP calculates and sets the specific timing for ILQ and Sell-in.
* **Step 4.2 (Execute Lowest-Grain Forecast Load):** DP loads the forecast into the NPI Workbook within Maestro. ILQ is placed in Month 1, DCS is distributed by month, and the remainder is driven by conversion rates. Input must strictly follow regional lowest levels:
  * *NAM:* By customer (e.g., Walmart, Best Buy).
  * *Europe:* By forecast stream (e.g., Amazon, CD). For "Europe Others," Ruben must calculate and update allocation percentages.
  * *AP / GCN / LATAM:* By country.
  * *Emerging Markets:* Classification must be confirmed with Micky or the regional head prior to uploading.
* **Step 4.3 (Post-Upload Review):** DP performs system checks to identify any missing data, wrong levels, timing issues, or system synchronization delays.

#### Phase 5: Post-Launch Control
* **Step 5.1 (Post-Gate 2 Change Management):** If market conditions shift before the product launch, Commercial / CCM initiates a change request.  
  🛑 **[Strict Prohibition]:** Requesting system changes casually via email or chat messages is strictly prohibited. All changes must undergo formal alignment between GCO and Commercial.
* **Step 5.2 (Update Bottom-Up Templates):** Once changes are aligned, CCM is responsible for updating the Bottom-up Forecast Template and market assumptions. The updated template is then handed over to DP to execute the system data adjustments.
* **Step 5.3 (Post-Launch Monitoring & Override Phase-Out):** DP continuously monitors actual demand, DCS, Sell-in, and Sell-out. Because statistical forecasts are unreliable early on, manual overrides are utilized initially. After 3–6 months post-launch, DP evaluates phasing out overrides to transition routine planning back to standard system logic.
