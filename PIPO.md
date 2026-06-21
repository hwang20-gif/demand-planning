**PIPO** 

**Purpose** 

**Portfolio Optimization & Rigorous Supply Control:** Define clear phase-in/out strategies per product line/SKU and lock LTB quantities in the system to prevent any production overrun beyond the authorized cap.

**Shipment & Terminal Demand Monitoring:** With total supply capped, conduct monthly reviews to stringently track LTB inventory against undershipment or overshipment risks, ensuring a balanced demand-supply execution.

**Definition**

**PIPO (Phase-In Phase-Out):** This is the process of defining and driving which product lines or SKUs should be phased out of the portfolio and which should be phased in, as well as determining the execution approach (either a mandatory "Hard" PIPO or a gradual "Soft" PIPO). This global strategy is defined and spearheaded by the BG/GCO unit.

**PLR (Product Line Rationalization):** This is a strategic decision initiated by the BG/GCO to determine the retention or elimination of specific product lines. It serves as the prerequisite trigger for DP (Demand Planning) to execute subsequent PIPO actions.

**LTB (Last Time Buy):** The final production or purchase order issued by the global planning department to the manufacturing side. Once confirmed, the total product supply is capped and locked, while normal sales activities within each region will continue.

**Importance**

Inventory Risk Mitigation: Apply a strict brake at the source to avoid excess and obsolete inventory during the product's decline phase.

Global Strategy Implementation: Ensure full alignment between regional execution and global headquarters' decisions, preventing any unauthorized procurement or sales.

Demand-Supply Equilibrium: Maintain a stable balance between production and sales through rigorous change management and regular monthly reviews to ensure final order fulfillment.

**Logic**

**Strategic Definition & Alignment:** The starting point of PIPO is the highest-level "Portfolio Management." Once the headquarters (BG/GCO) determines the entry and exit strategies and execution methods (Hard/Soft) for specific SKUs, DP (Demand Planning) must act as the gatekeeper to verify that the LTB demands submitted by the regions are fully aligned with this global portfolio strategy.

**Fixed Supply & Exception Management:** Once the phase-out strategy is activated and the LTB quantity is confirmed, the system logic must "turn off forecast consumption." This means the system will no longer automatically generate future supply-demand forecasts; any subsequent requests to change LTB quantities must go through the exception management process, requiring mandatory top-level approval from the BG/GCO.

**SOP**

BG/GCO defined global PIPO strategy (Hard/Soft) and communicated with regions 

Regions come back with LTB qty/last shipment date 

DP evaluate region request if aligned with global PIPO strategy and load it in by override 

Turn off fcst consumption and any further LTB qty change required BG/GCO approval from regions 

Syn up with GPP and fixed the last time build qty to ensure nothing will be built more than defined LTB 

Regular review (once a month) with CCM if any undership or overship of LTB 

BG/GCO communicate PLR decision to regions and confirm the acknowledgement for DP to action 

