# Logistics Operations Analytics Dashboard

A Power BI dashboard project built to help logistics stakeholders monitor revenue, load and delivery activity, fleet efficiency, fuel and maintenance costs, and driver performance and safety.

## Project Overview

Logistics businesses manage connected operations: customer demand creates loads, loads require trucks and drivers, and deliveries affect service quality and operating costs. When these activities are reviewed separately, it can be difficult to understand where revenue is being generated, where costs are accumulating, and which operational areas need attention.

This project brings key operational data into one interactive Power BI report. It is designed to help decision-makers explore performance across four business areas and use the findings to guide commercial, fleet, delivery, and driver-related decisions.

## Business Problem

The business needs a clearer, joined-up view of its logistics operations to answer questions such as:

- Which customers and freight categories contribute most to load revenue?
- How does revenue compare with customers' annual revenue potential?
- How are load volume, weight, and pieces transported distributed across destinations and customers?
- Where are detention time and delivery delays potentially affecting operational efficiency?
- How do fuel and maintenance costs vary by truck make and maintenance type?
- Which trucks show different fuel-efficiency, utilization, or downtime patterns?
- How do drivers compare on miles covered, revenue, on-time delivery, idle hours, and safety outcomes?
- Where should managers investigate opportunities to reduce costs, improve service, and use fleet resources more effectively?

The report provides an analytical view of these questions rather than assuming that one metric alone explains performance.

## Tools Used

- **Microsoft Power BI Desktop** — data modelling, DAX-based measures, report design, interactive visuals, slicers, and navigation between report pages.
- **Power Query** — intended data preparation workflow for cleaning and shaping source data before analysis.
- **DAX (Data Analysis Expressions)** — measures and calculations for operational KPIs and aggregated metrics.
- **Figma** — custom dashboard background and visual design assets used to support a consistent report layout.
- **GitHub** — project versioning and portfolio presentation.

> The Power BI report contains custom-designed page backgrounds, KPI cards, charts, slicers, and navigation buttons. Power Query and Figma are listed as workflow tools for this project; the `.pbix` file alone does not independently document every preparation step or design action.

## Dashboard Structure

The report contains four main analytical dashboards, plus an overview/KPI page and an additional summary page.

### 1. Customer & Revenue

**Purpose:** Understand customer contribution, revenue distribution, and potential commercial opportunities.

**Analysis included:**
- Total load revenue and average revenue per customer
- Revenue by customer and the top 10 customers by revenue
- Revenue by freight type, destination, and customer type
- Actual load revenue compared with annual revenue potential
- Filters for customer account status and load type

**Stakeholder questions:**
- Which customers and freight categories are most important to revenue?
- Is revenue concentrated among a small group of customers?
- Which destinations contribute meaningfully to revenue?
- Where is there a gap between current revenue and estimated customer potential?

### 2. Load & Delivery Operations

**Purpose:** Review freight activity, delivery efficiency, and how loads move through the network.

**Analysis included:**
- Total loads, pieces, and transported weight
- Monthly load trends
- Loads by destination city and freight type
- Pieces by customer and the top 10 customers by transported weight
- Average on-time delivery rate
- Detention minutes by facility and average detention time

**Stakeholder questions:**
- How does load activity change over time?
- Which cities and freight types account for the most activity?
- Which facilities show higher detention time and may require further investigation?
- How well is the operation meeting on-time delivery expectations?

### 3. Fleet, Fuel & Maintenance

**Purpose:** Examine fleet utilization, fuel spending, and maintenance patterns to support cost and asset-management decisions.

**Analysis included:**
- Total fuel cost and fuel cost by truck make
- Average miles per gallon (MPG)
- Average truck downtime by make
- Maintenance cost by maintenance type and truck make
- Monthly maintenance count
- Total trucks and average utilization rate
- A trailer-type filter

**Stakeholder questions:**
- Which truck makes account for higher fuel or maintenance costs?
- How does fuel efficiency differ across the fleet?
- Which truck groups experience more downtime?
- What maintenance types contribute most to maintenance spending?
- Are there patterns in maintenance frequency over time?
- Where could fleet utilization or preventive-maintenance practices be reviewed?

### 4. Driver Performance & Safety

**Purpose:** Compare driver productivity, service performance, idle time, and safety-related outcomes.

**Analysis included:**
- Total drivers, total driver miles, and total driver revenue
- Miles and revenue by driver
- Average idle hours by driver
- Average on-time delivery rate by driver
- Incident count by city
- Cargo-damage cost by driver
- Filters for at-fault and injury indicators

**Stakeholder questions:**
- Which drivers contribute most to miles covered and revenue?
- How does on-time delivery performance vary between drivers?
- Where does idle time warrant operational review?
- Which locations show more recorded safety incidents?
- Which drivers or circumstances are associated with higher cargo-damage costs?
- Where might coaching, route review, or safety interventions be useful?

## Analysis Approach

The report uses a multi-table logistics data model, bringing together customer, load, route, trip, delivery-event, truck, fuel-purchase, maintenance, driver, and safety information. It also includes driver monthly metrics and truck utilization metrics.

The analytical workflow is structured around the following steps:

1. **Organize the data** — bring operational entities and performance metrics into a common reporting model.
2. **Prepare and validate fields** — review data types, missing values, duplicate records, and key fields before drawing conclusions.
3. **Create measures** — calculate or aggregate revenue, load volume, costs, miles, fuel efficiency, utilization, downtime, delivery performance, and incident-related metrics.
4. **Compare performance** — break metrics down by customer, freight type, destination, truck make, maintenance type, driver, city, and month.
5. **Enable exploration** — use slicers, KPI cards, charts, and page navigation to let users investigate performance from different angles.
6. **Translate findings into action** — use the comparisons to identify areas for follow-up rather than treating correlations as proof of cause.

## Key Insights and Business Takeaways

The report is designed to surface the following decision-relevant insights. The specific rankings and numerical conclusions should be confirmed by opening the `.pbix` file and reviewing the current filter context and values.

### Commercial performance
- **Customer and freight mix matter:** Revenue by customer, customer type, and freight type helps identify the sources of commercial contribution and concentration.
- **Revenue potential can guide follow-up:** Comparing load revenue with annual revenue potential can help commercial teams identify customers for account review or growth conversations. Potential should be treated as an estimate, not guaranteed revenue.
- **Destination-level revenue adds context:** Revenue by destination helps managers compare commercial performance across service areas and investigate whether differences reflect demand, freight mix, or operating conditions.

### Load and delivery efficiency
- **Load trends support capacity planning:** Monthly load activity, transported weight, and pieces help managers assess changing demand and plan resources.
- **Detention is an operational signal:** Facility-level detention comparisons can highlight locations for further investigation into waiting time, scheduling, loading, or unloading processes.
- **On-time delivery should be read alongside volume:** Delivery-rate measures are most useful when considered with load activity and operational context, not in isolation.

### Fleet and cost management
- **Fuel and maintenance need to be viewed together:** Comparing fuel cost, MPG, downtime, and maintenance cost can help identify truck groups that deserve a closer efficiency review.
- **Maintenance mix helps prioritize investigation:** Cost by maintenance type and truck make can guide reviews of recurring work and asset-level spending.
- **Utilization and downtime are complementary:** A truck group with low utilization or high downtime may warrant investigation, but the report should be used alongside vehicle age, route demands, and maintenance history before decisions are made.

### Driver performance and safety
- **Productivity is multi-dimensional:** Miles and revenue show different aspects of driver contribution; they should be interpreted alongside workload and route differences.
- **Service quality adds balance to productivity:** Comparing on-time delivery rates with miles and revenue helps avoid judging performance from output alone.
- **Safety costs deserve contextual review:** Incident counts and cargo-damage costs can help identify patterns for follow-up, while considering location, incident type, at-fault status, and injury indicators.
- **Idle time can prompt operational questions:** Differences in idle hours may relate to waiting, routes, scheduling, or other conditions and should be investigated before attributing them to driver behaviour.

## Recommended Business Actions

Based on the questions the report supports, stakeholders could:

1. Review the customers and freight categories that drive revenue, then investigate opportunities to strengthen lower-performing accounts.
2. Investigate facilities with elevated detention time and review their loading, unloading, and scheduling processes.
3. Compare fuel efficiency, maintenance costs, and downtime by truck make before prioritizing fleet interventions.
4. Review driver performance using a balanced set of service, productivity, workload, and safety indicators.
5. Validate key relationships and missing identifiers before using the report for operational or financial decisions.

## Data Quality and Interpretation Notes

- The underlying model includes multiple related operational tables. Measures should be interpreted with attention to relationships and filter context.
- Some source records may contain missing or unmatched truck and driver identifiers. Such records can affect breakdowns by asset or driver and should be investigated before making definitive comparisons.
- Revenue, revenue potential, fuel cost, maintenance cost, and damage cost are different measures and should not be treated as interchangeable.
- This README describes the report structure and the business questions supported by its visuals. It does not claim numerical outcomes that are not stated here. For exact values, interact with the Power BI report itself.
- Remove confidential, personal, or commercially sensitive data before publishing the `.pbix` file in a public repository.

## How to View the Project

1. Download `Logistics Company Dataset.pbix` from this repository.
2. Open it with **Microsoft Power BI Desktop**.
3. Use the report page navigation buttons and available slicers to explore each dashboard.
4. Clear or reset filters when comparing results across different views.

## Repository Contents

- `Logistics Company Dataset.pbix` — interactive Power BI report.
- `README.md` — project overview, business problem, tools, analysis, and key takeaways.
- Optional dashboard screenshots — static previews for visitors who do not have Power BI Desktop.

## Project Goal

This project demonstrates how logistics data can be organized into an interactive reporting experience that connects commercial performance, delivery operations, fleet costs, and driver outcomes. Its goal is to help stakeholders move from disconnected metrics toward clearer questions, focused investigations, and better-informed operational decisions.
