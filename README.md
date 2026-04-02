# FIFA Player Market Value Analysis

## Overview
Exploratory analysis and visualization of factors influencing FIFA player market values across 18,000+ professional football players. This project examines how performance, age, international reputation, nationality, position, and physical traits interact to determine a player's economic value in the global football market.

> **Note:** This was a 5-person group project. My personal contributions are detailed below.

## My Contributions

### 1. Market Value by Overall Rating
Developed a polynomial regression scatter plot examining the relationship between a player's skill level and their market value. Key findings:
- Revealed an **exponential rather than linear** relationship between skill and value
- The most common player (66-70 rating bracket, 5,087 players) is worth a median of €0.92M
- Only 77 players occupy the elite 86+ bracket, yet command a median of €53.5M — a **535x increase** over the lowest bracket
- A polynomial curve fitted on a log scale shows value accelerating sharply past the **Overall Rating 80 threshold**, where the market begins rewarding irreplaceability over improvement

### 2. Market Value by Nationality
Built a choropleth map visualizing median player market value across nationalities, restricted to countries with at least 50 players for statistical reliability. Key findings:
- Brazil and parts of Eastern Europe show higher median market values than expected
- European and South American football ecosystems dominate player valuation globally
- First use of spatial data in R using `rnaturalearth`, ISO country codes, and custom color gradient legends — required significant trial and error to align country codes correctly

### 3. Potential Gap Analysis
Analyzed whether players with the most room to grow (large gap between current and potential rating) command higher market values. Key finding:
- **Counterintuitive result:** Players already near their performance ceiling hold the highest median values
- Raw young talent with large upside sits at the bottom — the market rewards **certainty over possibility**

## Dataset
- **Source:** FIFA player dataset (via Kaggle)
- **Size:** 18,000+ professional football players
- **Key Variables:** Market value, overall rating, potential, age, nationality, position, preferred foot, international reputation, wage

## Tools and Technologies
- **Language:** R
- **Libraries:** ggplot2, tidyverse, rnaturalearth, patchwork, scales, countrycode
- **Visualizations:** Polynomial scatter plots, choropleth maps, box plots, violin plots, histograms

## Key Findings
- Market value increases **exponentially** past an Overall Rating of 80, not linearly
- Players peak economically between **ages 26-30**, mirroring peak performance ratings
- International reputation has a strong positive correlation with market value — level 5 players command medians of €80-100M vs. €500K for level 1
- **Attacking and midfield roles** carry significantly higher market values than defensive roles
- A **scarcity premium** exists for left-footed players in central and creative positions

## Repository Structure
```
fifa-player-market-value-analysis/
├── fifa_market_value_analysis.R     # My visualization code (Overall Rating, Nationality, Potential Gap)
├── fifa_group_final_report.pdf      # Full group report with all visualizations
└── README.md
```

## Author
**Vaishnavi Tiwari** (Individual contributions: Overall Rating, Nationality, Potential Gap visualizations)  
M.S. Data Science, DePaul University  
[LinkedIn](https://www.linkedin.com/in/vaishnavi-tiwari-1a18971ab) · [GitHub](https://github.com/tiwari-vaish)
