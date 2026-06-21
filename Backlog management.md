# **Backlog management** 

**Purpose**   
**Manage Real Signals:** To manage the relationship between actual demand signals and the original forecast, rather than just managing orders.  
**Reallocate Demand Visibility:** Consumption fundamentally reallocates demand visibility instead of increasing demand.  
**Avoid Double Counting:** Consume forecasts with actual orders to prevent system double counting.  
**Capture Market Intelligence:** View backlog as market intelligence to detect real demand shifts (e.g., strong sell-out, successful promotions, competitor shortages, or channel front-loading).

**Definition**

**Backlog:** Official sell-in orders placed by T1 customers but not yet fully fulfilled by the factory. Already visible to supply planners in the system. Backlog is an "already materialized real demand signal," while a forecast is just a "planning assumption."  
**Forecast Consumption:** A system calculation logic where actual orders replace (consume)—rather than stack onto—the forecast, as they represent demand that has already occurred.

* **System Demand Formula:**  
  Total System Demand \= Actual Orders \+ Remaining Forecast


**Importance**

If Forecast Consumption is skipped, the system treats bulk orders as incremental demand, stacking them onto the original forecast and causing severe issues:

* Supply Overestimated: e.g., Forecast (1k) \+ Order (1k) \= System mistaken demand (2k).  
* Factory Loading Distortion: Triggers factory overproduction and capacity imbalance.  
* Inventory Risk: Leads to excess inventory, channel stuffing, and unhealthy Weeks of Supply if it's just early ordering without real growth.  
* Signal Distortion: Planners misinterpret a shift in ordering timing as a doubling of actual market demand.

**Logic**

The Consumption Window depends on regional customer ordering behavior:

* NPI: Disabled for first 3 months due to volatile initial demand patterns. Premature consumption blinds planners to real market adoption speed and demand surges.   
* TW & KR: Quarterly Consumption. Customers front-load full-quarter orders at quarter-start.  
* Japan, HK, ANZ: Monthly Rolling (-1 \+ 3 weeks). Order pattern is monthly/bi-weekly rolling orders instead of bulk quarterly.  
* China (CN): Generally Disabled. Behavior is inventory replenishment (order-on-availability) rather than market pull. *Rule: Class C only (Class A/B disabled)* due to potential full-quarter bulk ordering.  
* LATAM: Class C only (validating backlog details with CSC).  
* NAM: In progress; target timeline is November.


**SOP**

### Step 1: Input & Validation Phase

* Definition: Customer orders enter the system as Backlog before factory shipment, representing an actual demand signal.  
* Action: CCM/CSC owns the front-end backlog validation .  
* Review Focus: Validate order legitimacy and identify abnormalities. Conduct large order checks to filter out duplicate orders, panic ordering, or abnormal front-loading. Verified data is then released into the planning system.

### Step 2: Exception Report Generation

* Purpose: Treat backlog as market intelligence to detect underlying demand change signals, rather than just flagging errors.  
* Review Focus: Highlight whether bulk orders deviate from historical behavior or exceed the quarter forecast percentage, providing data-driven insights for planners.

### Step 3: Trigger Forecast Consumption Model

* Core Logic: Actual orders represent realized demand and should consume (replace)—rather than stack onto—the forecast.  
* Significance: Without consumption, bulk orders are treated as incremental demand, causing severe supply overestimation, capacity distortion, and high excess inventory risks.  
* System Formula: Triggers a shift from "Forecast \+ Order" to:  
  Total System Demand \= Actual Orders \+ Remaining Forecast

### Step 4: Consumption Decision Tree

Once triggered, the system automatically applies anti-error logic based on product lifecycle and regional customer ordering behavior:

* NPI (Within 3 Months) ➔ No Consumption: Initial demand is highly volatile. Premature consumption blinds planners to real adoption speed and demand surges; manual monitoring is required.  
* Stock-Driven Ordering (CN) ➔ No Consumption: China customers typically order based on inventory availability (inventory replenishment behavior). Impact is limited, so consumption is disabled for Class A/B materials.  
* Class C Exception (CN/LAT) ➔ Quarterly Consumption: Enabled exclusively for Class C items in China and Latin America as an exception rule.  
* Quarter-Start Bulk Orders (TW/KR) ➔ Quarterly Consumption: TW/KR customers front-load full-quarter orders at the quarter beginning. The system consumes the entire quarter’s forecast to prevent single-week capacity spikes.  
* Rolling Order Pattern (JP/ANZ/HK) ➔ Monthly Rolling Consumption (-1 \+ 3 Weeks): Orders are placed on a monthly or bi-weekly rolling basis. The system consumes forecast within a window of W-1 to W+3.  
* Regional Specific Rules: Europe is set to 13-week consumption per regional policy. North America (NAM) remains pending (target timeline: November).

### Step 5: Sanity Check & Business Judgment

* Frequency: Weekly review for Asia-Pacific (AP); manual report review by planners for Europe.  
* Review Focus: Check for over-consumption and analyze any anomalies in the remaining forecast.  
* Business Judgment: Planners combine market insights with business acumen to determine if bulk orders represent temporary front-loading or true market growth.

### Step 6: Demand Plan & Backlog Synchronization

* Possible Actions: Based on system outputs and manual checks, if true growth is confirmed, planners will execute: updating DCS , manual sell-in overrides, aggressive loading, or channel inventory adjustments.  
* Ultimate Benefit: Synchronized updates allow planners to capture true demand signals earlier, proactively secure supply, avoid shortages, and achieve optimal demand-supply balance.