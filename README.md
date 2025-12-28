# 🚦 Road Accident Analysis Dashboard (Power BI)

An interactive **Power BI dashboard** that visualizes and analyzes road accident data to uncover trends, hotspots, and key contributing factors. Ideal for transportation planners, safety analysts, and decision-makers looking to explore accident patterns and improve road safety outcomes.

---

## 📌 Overview

This project uses real accident data to build a rich, interactive dashboard in **Microsoft Power BI**. The dashboard highlights:

- Accident trends over time  
- Geographic accident hotspots  
- Severity and casualty breakdowns  
- Patterns by vehicle type, road type, weather, and time

Users can filter and drill down into the data to gain deeper insights that support evidence-based planning and road safety strategies.

---

## 📊 Features

### 🔢 Key Performance Indicators (KPIs)

Quick snapshot metrics including:

- **Total Number of Accidents**
- **Total Casualties**
- **Accidents by Severity (Fatal, Serious, Slight)**
- **Year-on-Year Trends**

---

### 📈 Trend Analysis

Visualizes accident data over time to show:

- Monthly and annual trends
- Comparative trends between years
- Patterns based on time of day or day of week

---

### 🛞 Category Breakdown

Drill down into accident causes by:

- **Vehicle Type** (car, bike, bus, etc.)
- **Road Type** (single vs dual carriageways, roundabouts, etc.)
- **Weather Conditions**
- **Light Conditions**

---

### 📍 Geographic Mapping

An interactive map that displays accident frequency and severity by location. Users can:

- Zoom to high-accident regions
- Filter by state/city
- Identify geographic patterns

---

### ⚙️ Interactivity

Built-in features include:

- Slicers for filtering (year, severity, region, weather, etc.)
- Drill-through to focused analyses
- Cross-filtering between visuals

---

## 🧠 Data & Modeling

### 📦 Data Source

Accident dataset containing attributes such as:

| Field               | Description                             |
|--------------------|-----------------------------------------|
| `Accident_Index`   | Unique accident identifier              |
| `Date`             | Accident date                           |
| `Location`         | Geographic coordinates or region        |
| `Vehicle_Type`     | Type of vehicle(s) involved             |
| `Number_of_Casualties` | Total casualties                  |
| `Severity`         | Accident severity level                 |
| `Weather_Condition`| Weather during accident                 |
| `Light_Condition`  | Light conditions at time of accident    |

*(Update these to match your dataset fields.)*

---

### 🛠 Data Preparation

- Data is preprocessed using **Power Query**
- Cleans missing or inconsistent records
- Builds relationships between tables (e.g., dates, geography)

---

### 📊 DAX Metrics

Common measures used in reports:

```dax
Total Accidents = COUNT('Accidents'[Accident_Index])

Total Casualties = SUM('Accidents'[Number_of_Casualties])

Accidents This Year = CALCULATE([Total Accidents], YEAR('Accidents'[Date]) = YEAR(TODAY()))

YoY Change = ([Accidents This Year] - [Accidents Last Year]) / [Accidents Last Year]


📄 Report Pages

Typical dashboard sections include:

Executive Summary – Top-level metrics & trends

Severity Analysis – Breakdown by severity levels

Category Insights – Vehicle, weather, and road type analysis

Geographic Hotspots – Map visualization of accident density

Interactive Filters – Slicers for dynamic exploration

🧾 Conclusion

The Road Accident Analysis Dashboard provides a comprehensive and intuitive visualization of accident and casualty trends across regions, vehicle types, and environmental conditions. By combining spatial mapping with time series and categorical breakdowns, this dashboard delivers meaningful insights that support informed decision-making for road safety initiatives.

📌 Key Takeaways

Accident and Casualty Trends:
There were 144.4K accidents and 195.7K casualties in the current year (CY). While overall figures have declined compared to the previous year, specific categories such as serious casualties remain significant, highlighting areas for deeper investigation.

Severity Insights:
The dashboard shows 2.9K fatal casualties this year — a 33.3% decrease — indicating potential improvements in safety measures, yet continued focus is necessary.

Vehicle Type Distribution:
Passenger cars and bikes account for the majority of casualties, with 155,804 and 15,610 respectively. This emphasizes the need for targeted interventions for these road users.

Temporal Trends:
The monthly comparison of casualties indicates fluctuating patterns that may align with seasonal travel or weather variations. This assists planners in anticipating peak periods requiring enhanced safety measures.

Urban vs Rural:
The majority of casualties occur in urban environments (61.95%), though rural areas still contribute substantially, suggesting a need for varied safety strategies adapted to context.

Road and Lighting Conditions:
Single carriageways dominate casualty counts, while daylight conditions account for nearly 74% of casualties, likely reflecting higher traffic volumes during the day.

Geographic Hotspots:
The interactive map highlights clusters of accidents across the UK, enabling stakeholders to pinpoint high-risk areas for targeted interventions, infrastructure improvements, or enforcement actions.

📊 Strategic Insights

Target Enforcement and Education
Focus on high-casualty vehicle categories such as cars and bikes through awareness campaigns and driving safety programs.

Improve High-Risk Zones
Use map visualizations to identify and prioritize infrastructure enhancements in accident hot-spots.

Seasonal Safety Planning
Tailor safety campaigns and patrols to periods with higher casualty counts derived from monthly trends.

Urban Safety Policies
Urban areas, despite better infrastructure, still exhibit higher casualty numbers. This suggests that policies addressing congestion, speed management, and pedestrian safety could provide impactful benefits.

This conclusion synthesizes the dashboard’s insights and transforms visual analytics into actionable narrative points that can be included in your GitHub README, report summary, or executive presentation. If you want, I can also help draft bullet points for slides or executive summaries.

