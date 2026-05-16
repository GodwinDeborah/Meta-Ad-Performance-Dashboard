# Meta Ad Performance Dashboard | Business Requirements Document (BRD)

## Business Objective
The objective of this project is to design and develop an interactive marketing analytics dashboard that enables stakeholders to evaluate campaign effectiveness across the digital marketing funnel and optimize advertising spend based on engagement, conversion performance, and overall campaign efficiency.

This project focuses on advertising performance analysis across Meta platforms, specifically Facebook and Instagram.

The dashboard should provide clear visibility into:
- Campaign reach and engagement
- Audience behavior and responsiveness
- Conversion efficiency across the funnel
- Opportunities for budget optimization and improved ROI


## Problem Statement
Marketing teams often lack a unified analytical view of the digital marketing funnel, making it difficult to understand how impressions translate into engagement and ultimately conversions. This results in inefficient budget allocation, unclear audience targeting, and suboptimal campaign performance.

Although raw metrics exist across platforms, there is no consolidated view connecting impressions, engagement, and conversion outcomes, limiting effective strategic decision-making.

## Stakeholders
The dashboard is intended for:
- **Marketing Managers** — Monitor campaign performance and optimize strategy
- **Performance Analysts** — Analyze trends and identify inefficiencies
- **Business Executives** — Evaluate ROI and overall campaign effectiveness

## Key Business Questions
The dashboard should answer the following questions:
- Which campaigns generate the highest engagement?
- Which audience segments are most responsive and convert best?
- Which ads and platforms drive the highest conversions?
- Where do users drop off within the marketing funnel?
- Which campaigns generate the highest return relative to budget?
- Which audience segments deliver the lowest cost per conversion?
- What time periods yield the best campaign performance?

## Dashboard Requirements

### Key Performance Indicators (KPIs)

#### Awareness Metrics
- **Impressions** — Total number of times ads are displayed

#### Engagement Metrics
- **Clicks** — Number of user interactions with ads
- **Shares** — Content redistribution metric
- **Comments** — User feedback and engagement indicator
- **Total Engagements** = Clicks + Shares + Comments
- **Engagement Rate** = (Engagements ÷ Impressions) × 100

#### Conversion Metrics
- **Purchases** — Total conversions
- **Conversion Rate** = (Purchases ÷ Clicks) × 100
- **Purchase Rate** = (Purchases ÷ Impressions) × 100

#### Efficiency Metrics
- **Click-Through Rate (CTR)** = (Clicks ÷ Impressions) × 100
- **Total Budget** — Total spend across campaigns
- **Average Budget per Campaign** — Budget allocation efficiency

## Chart Requirements

### 1. Target Gender — Donut Chart
Use a donut chart to visualize performance distribution by target gender from the ads table.

- The displayed metric (e.g., Impressions, Clicks, Purchases) should update dynamically using a parameter.
- Purpose: Identify which gender segment contributes most to the selected metric.

### 2. Age Group — Bar Chart
Use a bar chart to display engagement across age groups defined in the ads table.

- Each bar represents a single age group.
- The displayed metric should update dynamically.
- Purpose: Highlight which age group is most responsive to campaigns.

### 3. Country — Map Visualization
Use a map visualization to display campaign performance by country from the users table.

- Bubble size or color intensity should represent the selected metric.
- Purpose: Provide a geographic view of campaign reach and engagement.

### 4. Calendar Month — Calendar Heat Map
Use a calendar heat map to visualize monthly performance trends based on the timestamp field in the `ad_events` table.

- Darker shades indicate higher activity levels.
- Purpose: Identify seasonal patterns, peak campaign periods, and low-activity months.

### 5. Weekly Trend — Stacked Column Chart by Ad Type
Use a stacked column chart to display weekly performance trends.

- **X-axis:** Week number (from the Date Table linked to `ad_events`)
- **Stacks:** Different `ad_type` values from the ads table
- **Y-axis:** Selected metric
- Purpose: Compare ad type contributions across weeks.

### 6. Hourly Trend — Area Chart
Use an area chart to display campaign activity by hour of day using `ad_events[time_of_day]`.

- **X-axis:** Hour of the day (0–23)
- **Y-axis:** Selected metric
- Purpose: Understand user activity patterns throughout the day.

### 7. Ad Type — Matrix
Use a matrix visualization to compare performance across ad formats and platforms.

- **Rows:** Ad Types
- **Columns:** Platforms or campaign dimensions
- **Values:** Selected metric
- Purpose: Compare ad performance side by side across multiple dimensions.

## Success Criteria
The project will be considered successful if:
- Stakeholders can clearly identify top-performing and underperforming campaigns
- Funnel drop-off points are visible and actionable
- High-converting audience segments are clearly identifiable
- Campaign performance can be evaluated across engagement and efficiency metrics
- Marketing teams can use insights to improve budget allocation decisions

## Assumptions & Limitations

### Assumptions
- The dataset accurately represents campaign and user interactions
- Event tracking is consistent across platforms
- KPIs such as clicks, impressions, and purchases are reliably recorded

### Limitations
- The dataset is simulated and may not reflect real-world advertising complexity
- Cost and revenue data are limited, restricting full ROI analysis
- Attribution modeling is not included
- External factors such as seasonality and market competition are not captured

## Future Enhancements
- Integrate cost-per-click (CPC) and cost-per-acquisition (CPA) metrics for deeper ROI analysis
- Implement attribution models such as first-touch, last-touch, and multi-touch attribution
- Introduce predictive modeling for campaign performance forecasting
- Enable real-time data integration for live campaign monitoring
- Develop advanced behavioral segmentation and cohort analysis capabilities

