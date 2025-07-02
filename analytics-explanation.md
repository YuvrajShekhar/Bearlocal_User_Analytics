# Bearlocal Sales Team Analytics for June 2025 Dashboard - Mathematical Analysis
Link : https://bearlocal-user-analytics-ftz8kjf7e-yuvraj-shekhars-projects.vercel.app/

## Table of Contents
1. [All Calls Analytics](#section-1-all-calls-analytics)
2. [Calls Over 1 Minute Analytics](#section-2-calls-over-1-minute-analytics)
3. [Conversion Rate Success Analytics](#section-3-conversion-rate-success-analytics)

---

## Section 1: All Calls Analytics

### 1.1 Profitability Score Calculation

The profitability score is a weighted composite metric that combines three key performance indicators:

**Formula:**
```
Profitability Score = (0.40 × Volume Score) + (0.30 × Efficiency Score) + (0.30 × Quality Score)
```

#### Component Calculations:

**Volume Score:**
- Measures the total output of connected outbound calls
- Formula: `(Employee Connected Calls / Maximum Connected Calls) × 100`
- Example: Janis has 790 connected calls (maximum), so Volume Score = 100%
- Joshua has 572 connected calls, so Volume Score = (572/790) × 100 = 72.4%

**Efficiency Score:**
- Measures calls per hour worked
- Formula: `(Employee Calls per Hour / Maximum Calls per Hour) × 100`
- Calls per Hour = Connected Outbound Calls / Total Hours Worked
- Example: Joshua has 89.4 calls/hour (maximum), so Efficiency Score = 100%
- Janis has 45.1 calls/hour, so Efficiency Score = (45.1/89.4) × 100 = 50.4%

**Quality Score:**
- Measures connection success rate
- Formula: `(Employee Connection Rate / Maximum Connection Rate) × 100`
- Connection Rate = (Connected Calls / Total Attempts) × 100
- Example: Robin has 81.3% connection rate (maximum), so Quality Score = 100%
- Janis has 76.6% connection rate, so Quality Score = (76.6/81.3) × 100 = 94.2%

#### Final Profitability Scores:
- **Joshua: 86.2** = (0.40 × 72.4) + (0.30 × 100) + (0.30 × 90.8)
- **Janis: 83.4** = (0.40 × 100) + (0.30 × 50.4) + (0.30 × 94.2)
- **Robin: 82.2** = (0.40 × 85.4) + (0.30 × 60.1) + (0.30 × 100)
- **Iris: 59.6** = (0.40 × 53.9) + (0.30 × 36.4) + (0.30 × 90.3)

### 1.2 Graph Analytics Explained

#### 1.2.1 Connected Outbound Calls Comparison (Bar Chart)
- **Purpose:** Visual comparison of absolute call volumes
- **Data:** Raw connected call counts per employee
- **Insight:** Janis leads in volume (790), but this doesn't account for efficiency

#### 1.2.2 Connection Rate Analysis (Bar Chart)
- **Calculation:** (Connected Calls / Total Attempts) × 100
- **Results:**
  - Robin: 81.3% (675/830)
  - Janis: 76.6% (790/1,032)
  - Joshua: 73.8% (572/775)
  - Iris: 73.4% (426/580)
- **Insight:** Robin has the highest quality despite not having the highest volume

#### 1.2.3 Weekly Performance Trends (Line Chart)
- **Purpose:** Track performance consistency over time
- **Calculation:** Weekly connected calls for each employee
- **Key Findings:**
  - Week 4 shows significant drop (June partial week)
  - Janis maintains most consistent high volume
  - Joshua shows declining trend

#### 1.2.4 Profitability Score Components (Stacked Bar Chart)
- **Visualization:** Shows contribution of each component to total score
- **Maximum possible:** 100 points (40 + 30 + 30)
- **Insight:** Joshua maximizes efficiency despite lower volume

#### 1.2.5 Call Volume Distribution (Doughnut Chart)
- **Total Calls:** 2,463 connected calls
- **Distribution:**
  - Janis: 32.1% (790/2,463)
  - Robin: 27.4% (675/2,463)
  - Joshua: 23.2% (572/2,463)
  - Iris: 17.3% (426/2,463)

#### 1.2.6 Efficiency Metrics (Radar Chart)
- **Dimensions:** 
  - Calls/Hour (normalized to Joshua's 89.4)
  - Connection Rate (normalized to Robin's 81.3%)
  - Total Volume (normalized to Janis's 790)
  - Efficiency (composite metric)
- **Purpose:** Multi-dimensional performance visualization

### 1.3 Key Metrics Calculations

**Utilization Rate:**
- Formula: `Total Call Hours / (160 hours × weeks worked)`
- Assumes 40-hour work week
- Example: Janis worked 17.5 hours on calls out of ~160 possible = 10.9%

**Failed Calls:**
- Calculation: Total Attempts - Connected Calls
- Percentage: (Failed Calls / Total Attempts) × 100

---

## Section 2: Calls Over 1 Minute Analytics

### 2.1 Modified Profitability Score for Long Calls

The calculation methodology remains the same but focuses only on calls lasting more than 1 minute:

**Formula:**
```
Long Call Profitability = (0.40 × Long Volume Score) + (0.30 × Long Efficiency Score) + (0.30 × Long Quality Score)
```

#### Component Calculations:

**Long Volume Score:**
- Based on calls >1 minute only
- Maximum: Janis with 592 long calls
- Example: Robin = (540/592) × 100 = 91.2%

**Long Efficiency Score:**
- Long calls per hour worked
- Maximum: Joshua with 57.8 long calls/hour
- Example: Janis = (33.8/57.8) × 100 = 58.5%

**Long Quality Score:**
- Connection rate for long calls
- Maximum: Robin with 83.5% long call connection rate
- Example: Janis = (78.5/83.5) × 100 = 94.0%

#### Final Long Call Profitability Scores:
- **Robin: 86.7** = (0.40 × 91.2) + (0.30 × 74.4) + (0.30 × 100)
- **Janis: 84.1** = (0.40 × 100) + (0.30 × 58.5) + (0.30 × 94.0)
- **Joshua: 79.5** = (0.40 × 62.5) + (0.30 × 100) + (0.30 × 90.0)
- **Iris: 65.3** = (0.40 × 57.4) + (0.30 × 45.0) + (0.30 × 90.1)

### 2.2 Long Call Specific Metrics

**Percentage of Long Calls:**
- Formula: (Calls >1 min / Total Connected Calls) × 100
- Results:
  - Robin: 80.0% (540/675)
  - Iris: 79.8% (340/426)
  - Janis: 75.0% (592/790)
  - Joshua: 64.7% (370/572)

**Average Call Duration Analysis:**
- Calculated from total call time / number of calls
- Long call averages:
  - Iris: 2m 11s (highest engagement)
  - Janis: 1m 45s
  - Robin: 1m 21s
  - Joshua: 1m 02s (just over threshold)

### 2.3 Graph Analytics for Long Calls

#### 2.3.1 Long Calls Comparison (Bar Chart)
- Shows absolute numbers of calls >1 minute
- Highlights quality vs quantity trade-off

#### 2.3.2 Long Calls Connection Rate (Bar Chart)
- Higher rates indicate better targeting for meaningful conversations
- Robin's 83.5% suggests excellent qualifying skills

#### 2.3.3 Weekly Long Calls Trends (Line Chart)
- Similar pattern to overall calls but with focus on quality interactions
- Useful for tracking engagement quality over time

#### 2.3.4 Long Calls Distribution (Doughnut Chart)
- Total: 1,842 long calls (74.8% of all calls)
- Shows team's ability to engage customers

---

## Section 3: Conversion Rate Success Analytics

### 3.1 Sales Performance Metrics

**Product Categories:**
- **Object List:** Premium product line (higher value)
- **GNV:** Standard product line (volume-based)

### 3.2 Conversion Effectiveness Formula

```
Conversion Effectiveness = Products Sold / (Call Hours × Call Efficiency)
```

This metric balances sales output against time invested.

### 3.3 Key Sales Metrics

#### 3.3.1 Units per Hour Calculation
- Formula: Total Units Sold / Total Call Hours
- Results:
  - Joshua: 146.9 units/hour (940 units / 6.4 hours)
  - Robin: 27.1 units/hour (342 units / 12.6 hours)
  - Janis: 19.4 units/hour (339 units / 17.5 hours)
  - Iris: 15.3 units/hour (267 units / 13.1 hours)

#### 3.3.2 Sales Efficiency
- Measures conversion quality relative to time spent
- Calculation considers both product mix and volume
- Results:
  - Robin: 91% (best balanced performance)
  - Joshua: 89% (high volume, single product focus)
  - Janis: 83% (good balance)
  - Iris: 78% (lower efficiency)

### 3.4 Graph Analytics for Conversion

#### 3.4.1 Product Sales Comparison (Stacked Bar Chart)
- **Purpose:** Visualize product mix per employee
- **Key Insights:**
  - Joshua: Extreme specialization (25 Object List, 0 GNV)
  - Robin: GNV specialist (12 GNV vs 2 Object List)
  - Janis & Iris: Balanced approach (4-5 of each)

#### 3.4.2 Units Per Call Hour (Bar Chart)
- **Calculation:** Total units / Call hours
- **Joshua's Dominance:** 146.9 units/hour is 5.4× next best
- **Insight:** Specialization yields higher volume

#### 3.4.3 Sales Mix (Doughnut Chart)
- **Total Units:** 1,888 (1,403 Object List + 485 GNV)
- **Distribution:**
  - Joshua Object List: 49.8% (940/1,888)
  - Robin GNV: 14.2% (269/1,888)
  - Others: More balanced contributions

#### 3.4.4 Sales Efficiency vs Call Time (Scatter Plot)
- **X-axis:** Total call hours (effort invested)
- **Y-axis:** Sales efficiency percentage (quality of conversion)
- **Key Finding:** Inverse relationship - less time correlates with higher efficiency
- **Interpretation:** Focused, shorter interactions may be more effective

### 3.5 Comparative Performance Multipliers

**Joshua's Object List Lead:** 5.7×
- Calculation: 25 products / 4.4 average others = 5.7×

**Robin's GNV Units Lead:** 22.4×
- Calculation: 269 units / 12 average others = 22.4×

**Joshua's Units/Hour Lead:** 2.9×
- Calculation: 146.9 / 50.6 team average = 2.9×

**Robin's Efficiency Lead:** 13%
- Calculation: 91% - 78% (vs lowest) = 13 percentage points

### 3.6 Strategic Insights

1. **Specialization vs Diversification:**
   - Joshua's focused approach yields highest volume
   - Robin's GNV focus shows market segment mastery
   - Balanced approach (Janis/Iris) provides flexibility but lower peaks

2. **Time Efficiency Paradox:**
   - Lowest call hours (Joshua: 6.4) → Highest productivity
   - Suggests quality of interaction matters more than quantity

3. **Product-Market Fit:**
   - Different products require different sales approaches
   - Object List may benefit from rapid, high-volume approach
   - GNV may require more relationship building

---

## Conclusion

The three-tiered analytics approach reveals:

1. **Volume ≠ Profitability:** High call counts don't guarantee best results
2. **Efficiency is King:** Calls per hour is the strongest predictor of success
3. **Specialization Wins:** Focused product strategies outperform generalist approaches
4. **Quality Metrics Matter:** Connection rates and call duration indicate engagement quality
5. **Time Optimization:** Less time with higher intensity yields better results

The profitability scoring system successfully identifies top performers by balancing multiple factors, preventing any single metric from dominating the evaluation.