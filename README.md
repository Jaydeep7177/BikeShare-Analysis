# BikeShare-Analysis
Converting Casual Riders to Members: A Data-Driven Approach

# Introduction
I recently completed a comprehensive data analysis project on Cyclistic, a fictional bike-sharing company, as part of the Google Data Analytics Capstone Certificate. The core business question was: How can Cyclistic convert casual riders into annual members?

With 5.44 million ride records at my disposal, I set out to uncover patterns that would drive a strategic membership conversion strategy. This article walks through my complete analysis journey using Excel, Power Query, and Power BI.

## Phase 1: ASK – Understanding the Business Challenge
### Cyclistic Customer Segments
Cyclistic operates with two customer segments:

* Casual Riders: Pay per ride (35% of all rides)
* Members: Annual subscribers (65% of all rides)

### Business Questions
The executive team wanted to understand:

* Which casual riders are most likely to convert to memberships?
* What are the key behavioral differences between casual riders and members?
* When should marketing efforts target casual riders?
* What membership options would resonate most?

### Hypothesis
The hypothesis: If I could identify distinct casual rider segments through behavioral analysis, I could design targeted membership campaigns with high conversion potential.

## Phase 2: PREPARE – Data Foundation
### Data Source
* 12 months of Cyclistic ride data (December 2024– November 2025)
* 12 separate CSV files (one per month)
* 5.4M ride records

### Initial Exploration in Excel
I started by importing all 12 CSV files into Excel and creating a consolidated view. My first observation revealed a critical insight:

* **Summer (May–September):** 910,726 casual rides
* **Winter (December–February):** 87,770 casual rides
* **Seasonal Swing:** 10.37x difference

This immediately signaled a time-sensitive opportunity. The summer months concentrated nearly half of annual casual traffic—a window I couldn't afford to miss if launching a conversion campaign.

### Initial Metrics
* **Average ride duration (members):** 11.7 minutes
* **Average ride duration (casuals):** 18.1 minutes

**Insight:** Casual riders engage 54% longer, suggesting deeper interest and higher conversion potential

## Phase 3: PROCESS – Data Transformation in Power Query
Raw data isn't analysis-ready. Power Query became my transformation engine.

### Step 1: Consolidating 12 Files into One Table
### Step 2: Data Cleaning & Standardization
### Step 3: Creating 9 New Analytical Columns
This was where raw data transformed into business intelligence:

#### 1. ride_length_minutes

Purpose: Quantify engagement level
Finding: Casual riders = 18.1 min avg (vs members 11.7 min)

#### 2. day_of_week

Purpose: Identify weekly patterns
Finding: Weekends = 38% of casual weekly traffic

#### 3. day_name

Purpose: Create readable day labels
Finding: Saturday & Sunday dominate casual usage

#### 4. month

Purpose: Enable monthly trend analysis
Finding: June, July, August peak (summer season)

#### 5. month_name

Purpose: Display month names in visualizations
Finding: Clear seasonal concentration

#### 6. season

Purpose: Seasonal segmentation
Finding: 47.3% of casual annual traffic in 5 summer months

#### 7. hour_of_day

Purpose: Identify hourly usage patterns
Finding: Casual peak = 5pm (leisure) | Member peak = 5am (commute)

#### 8. is_same_station

Purpose: Identify round-trip vs point-to-point rides
Finding: 10% of casual rides are station-to-station round trips

#### 9. distance_km

Purpose: Understand travel distance behavior
Finding: Casual riders average 2.28 km (vs members 2.19 km)

### Step 4: Data Validation
Before moving to analysis, I validated:

* ✓ All 12 months represented
* ✓ Date range: Jan 1 – Dec 31
* ✓ member_casual only contains: "casual" or "member"
* ✓ hour_of_day range: 0–23
* ✓ ride_length_minutes: all positive values
* ✓ 5,438,000 total records across all months
