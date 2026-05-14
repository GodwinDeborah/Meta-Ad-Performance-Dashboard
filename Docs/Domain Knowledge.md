# Meta ad Performance Dashboard | Domain Knowledge

## Introduction
This project analyzes paid social media advertising performance using a Meta Ads dataset, focusing on how campaigns drive user engagement and conversions across different audience segments.
The analysis is structured around the marketing funnel:

**Impressions → Clicks → Engagement → Purchases**

This framework is used to identify drop-off points, evaluate campaign effectiveness, and uncover opportunities to improve targeting, creative performance, and conversion efficiency.
Each stage of the funnel represents a key decision point in the user journey, and inefficiencies at any stage directly impact overall campaign performance and return on advertising spend.

## Data Model Overview
The project integrates four relational datasets structured into a simple star schema:

### Fact Table
-	Ad_Events: Captures all user interaction events such as impressions, clicks, shares, comments, and purchases.

### Dimension Tables
-	Ad: Contains ad-level attributes such as format, platform, and targeting details
-	Campaign: Contains campaign-level information such as budget and duration
-	Users: Contains demographic and behavioral attributes such as age, gender, location, and interests

### Relationships
-	Ad_Events → Ad via Ad_ID
-	Ad_Events → Campaign via Campaign_ID
-	Ad_Events → Users via User_ID

These relationships enable cross-dimensional analysis of performance across campaign structure, ad creatives, and user segments.

## Key Metrics Explained

### Impressions
The number of times an advertisement is displayed to users.
-	Represents reach and visibility
-	High impressions alone do not indicate success without engagement

### Clicks
The number of times users interact with an ad.
-	Indicates initial interest and relevance
-	Used as a key input for CTR and conversion analysis

### Shares
The number of times users share an ad.
-	Indicates content virality and organic amplification
-	Extends reach beyond paid exposure

### Comments
User responses or feedback on ads.
-	Provides qualitative insight into engagement
-	Helps understand sentiment and user perception

### Purchases
The number of completed conversions resulting from ad interaction.
-	Represents final business value
-	Primary success indicator for campaign effectiveness

## Derived Performance Metrics (KPIs)
These metrics provide deeper insight into funnel efficiency and campaign effectiveness.

### Click-Through Rate (CTR)
CTR = (Clicks ÷ Impressions) × 100
-	Measures how compelling an ad is
-	High CTR indicates strong targeting and creative relevance

### Engagement Rate
Engagement Rate = (Engagements ÷ Impressions) × 100
-	Measures overall interaction relative to reach
-	Evaluates content quality and audience resonance

### Conversion Rate
Conversion Rate = (Purchases ÷ Clicks) × 100
-	Measures how effectively engagement translates into conversions
-	Key indicator of funnel efficiency and landing page effectiveness

### Purchase Rate
Purchase Rate = (Purchases ÷ Impressions) × 100
-	Measures end-to-end funnel performance
-	Reflects combined effectiveness of targeting, engagement, and conversion

## Analytical Perspective

This dataset enables analysis across three core dimensions:

1. **Funnel Efficiency**  
Examines user progression from impressions to purchase, highlighting key drop-off points and conversion bottlenecks across the marketing funnel.

2. **Audience Performance**  
Evaluates how different demographic and interest-based segments respond to campaigns in terms of engagement and conversion behavior.

3. **Campaign Effectiveness**  
Compares campaign performance using engagement, conversion, and efficiency metrics to identify both high-performing and underperforming initiatives.

## Conclusion
This domain model enables a structured analysis of digital advertising performance by connecting user-level interactions with campaign and ad-level attributes. By applying a funnel-based analytical approach, the project identifies inefficiencies in user conversion paths and supports data-driven optimization of marketing strategies.
