### 🎯 Purpose
* **Portfolio Optimization & Rigorous Supply Control:** Define clear phase-in/out strategies per product line/SKU and lock LTB quantities in the system to prevent any production overrun beyond the authorized cap.
* **Shipment & Terminal Demand Monitoring:** With total supply capped, conduct monthly reviews to stringently track LTB inventory against undershipment or overshipment risks, ensuring a balanced demand-supply execution.

---

### 📘 Definition
* **PIPO (Phase-In Phase-Out):** The process of defining and driving which product lines or SKUs should be phased out of the portfolio and which should be phased in, as well as determining the execution approach (either a mandatory "Hard" PIPO or a gradual "Soft" PIPO). This global strategy is defined and spearheaded by the BG/GCO unit.
* **PLR (Product Line Rationalization):** A strategic decision initiated by the BG/GCO to determine the retention or elimination of specific product lines. It serves as the prerequisite trigger for DP (Demand Planning) to execute subsequent PIPO actions.
* **LTB (Last Time Buy):** The final production or purchase order issued by the global planning department to the manufacturing side. Once confirmed, the total product supply is capped and locked, while normal sales activities within each region will continue.

---

### 💡 Importance
* **Inventory Risk Mitigation:** Apply a strict brake at the source to avoid excess and obsolete (E&O) inventory during the product's decline phase.
* **Global Strategy Implementation:** Ensure full alignment between regional execution and global headquarters' decisions, preventing any unauthorized procurement or sales.
* **Demand-Supply Equilibrium:** Maintain a stable balance between production and sales through rigorous change management and regular monthly reviews to ensure final order fulfillment.

---

### ⚙️ PIPO Strategic Logic

#### 1. Strategic Definition & Alignment
The starting point of PIPO is the highest-level "Portfolio Management." Once the headquarters (BG/GCO) determines the entry and exit strategies and execution methods (Hard/Soft) for specific SKUs, DP (Demand Planning) must act as the gatekeeper to verify that the LTB demands submitted by the regions are fully aligned with this global portfolio strategy.

#### 2. Fixed Supply & Exception Management
Once the phase-out strategy is activated and the LTB quantity is confirmed, the system logic must **"turn off forecast consumption."** This means the system will no longer automatically generate future supply-demand forecasts; any subsequent requests to change LTB quantities must go through the exception management process, requiring mandatory top-level approval from the BG/GCO.

---

### 📋 Standard Operating Procedure (SOP)

#### Step 1: Global PIPO Strategy Definition
BG/GCO defines the global PIPO strategy (Hard/Soft) and formally communicates the guidelines and deadlines to all regions.

#### Step 2: Product Line Rationalization (PLR) Notification
BG/GCO communicates the final PLR decision to the regions and confirms the official acknowledgement, triggering the green light for DP to take action.

#### Step 3: Regional Demand Collection
Regions review their terminal market potential and submit their requested LTB quantity along with the expected last shipment date back to the central team.

#### Step 4: DP Evaluation & System Loading
DP evaluates the regional requests to ensure they are fully aligned with the global PIPO strategy. Once validated, DP loads the confirmed quantities into the system using a **Manual Override**.

#### Step 5: System Parameter Configuration (Turn Off Consumption)
DP configures the system to **turn off forecast consumption** for the phased-out SKUs. From this point on, any further changes to the LTB quantity requested by the regions will strictly require formal BG/GCO approval.

#### Step 6: Supply Locking & Factory Alignment
DP syncs up with GPP (Global Production Planning) to freeze and fix the final Last Time Build quantity, ensuring the factory **will not build a single unit more** than the defined LTB cap.

#### Step 7: Post-Execution Monthly Monitoring
DP conducts regular monthly reviews in alignment with CCM to stringently track the fulfillment rate, monitoring if there is any undershipment or overshipment against the locked LTB target to secure a clean product exit.
