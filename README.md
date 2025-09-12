# Airbnb Listings EDA Project: New York 2024  

---

## Project Overview
This project performs an Exploratory Data Analysis (EDA) on Airbnb listings in New York City (2024) to identify trends, patterns, and actionable insights that can support data-driven business decisions.

The analysis explores:

1. Price distribution and removal of extreme outliers.
2. Neighbourhood group-wise trends and their impact on pricing.
3. Room type comparisons (Entire home/apt, Private room, Shared room).
4. Availability patterns to understand seasonality and occupancy potential.
5. Review patterns and their relationship with pricing and demand.
6. Geospatial distribution of listings across NYC. 

We use libraries like **Pandas, Numpy, Matplotlib and Seaborn**for cleaning, visualization, and analysis. 

![](https://github.com/najirh/Python-Project-P2-New-York-AirBnb-Listing-2024/blob/main/New-York-City-Brooklyn-Bridge-Panorama-Juergen-Roth-2.jpg)

---

## Business Problem Statement

*Problem:*
Airbnb’s management team wants to **optimize pricing and availability strategies to increase revenue** while maintaining customer satisfaction in New York City. However, they currently lack insights into how neighbourhood location, room type, availability, and reviews impact price and demand.

*Business Goal:*
Analyze Airbnb listings to identify:
1. Which neighbourhood groups and room types yield the highest revenue potential.
2. The relationship between reviews, availability, and pricing.
3. Optimal price ranges to reduce outliers and attract more bookings.
4. Recommendations for better inventory distribution (e.g., room types in high-demand areas).

---

## Dataset
The dataset contains **20,765 entries and 22 features**, including:
- **id**: Unique identifier for each listing  
- **name**: Title of the Airbnb listing  
- **host_name**: Name of the host  
- **neighborhood_group**: Group (borough) where the listing is located  
- **latitude/longitude**: Geolocation of listings  
- **price**: Nightly rental price  
- **room_type**: Type of accommodation (e.g., entire home, private room)  
- **reviews_per_month**: Average monthly reviews for the listing  
- **availability_365**: Number of days available in the year  

---

## Steps and Workflow

### 1. Data Cleaning
- **Handle missing data**: `price`, `neighborhood`, and `beds` columns had null values.
- **Fix data types**: Converted `last_review` to a **datetime** object.
- **Remove outliers**: Listings with prices > $1,000 were capped to avoid skewed visualizations.

### 2. EDA (Exploratory Data Analysis)
1. **Room type distribution**: 
   - Visualized the count of each room type using **bar plots**.
   - Identified **Entire home/apt** as the most common room type.

2. **Neighborhood group insights**:
   - Analyzed **price variations by boroughs**.
   - Manhattan had the **highest average prices**.

3. **Availability trends**:
   - Used **heatmaps** to show correlations among `price`, `availability_365`, `number_of_reviews`, and `beds`.

4. **Price distribution**:
   - Used **histograms** to show the distribution of prices.
   - Majority of the listings were priced between **$50 - $300**.

5. **Host listings**:
   - Analyzed hosts with multiple listings using **boxplots** to identify key contributors.

6. **Review behavior**:
   - Used **pair plots** to show relationships between number of reviews, price, and availability.

### 3. Data Visualization
- **Pairplot**: To see correlations among `price`, `availability`, and `number of reviews`.
- **Heatmap**: Showing correlations among numerical features.
- **Histograms and Boxplots**: To detect outliers in `price`.
- **Bar Charts**: Displaying room types and neighborhood group distributions.

---

## Key Insights & Conclusions from the Analysis

### Price Distribution & Outliers

-   The dataset showed several extreme price outliers (very high-priced
    listings).
-   After filtering prices below \$1500, the majority of listings
    clustered around a much lower price range, suggesting most customers
    prefer budget-to-midrange stays.
-   Outlier removal improves pricing recommendations and prevents skewed
    analysis.

### Neighbourhood Group Impact

-   Certain neighbourhood groups (like Manhattan) have significantly
    higher average prices than others (e.g., Staten Island).
-   This indicates a strong location-based pricing model, meaning
    pricing strategy must be geographically optimized.

### Room Type Insights

-   Entire homes/apartments are priced much higher compared to
    private/shared rooms, but they may have lower booking frequency.
-   Private rooms could be an entry-level offering to attract budget
    travelers.

### Availability Trends

-   Availability distribution suggests some hosts list properties
    year-round, while others are seasonal.
-   Listings with higher availability and balanced pricing could achieve
    better occupancy rates.

### Reviews & Price Relationship

-   Listings with a moderate number of reviews tend to have more
    competitive prices.
-   Extremely high review counts may correlate with lower pricing
    (possibly budget options), while high-price luxury stays have fewer
    reviews.

### Geographical Insights

-   Manhattan and Brooklyn dominate the listing density and higher price
    range.
-   Visual maps reveal clusters of high-priced listings, useful for
    understanding competition and adjusting pricing dynamically.

### Correlation Findings

-   Weak-to-moderate correlation between price and most numerical
    variables, meaning price is not solely dependent on beds, reviews,
    or minimum nights, but location and room type play bigger roles.




## Recommendations
- **For Guests**: 
   - Look for listings with high availability and good reviews for a better experience.
   - **Private rooms** in Brooklyn offer affordable stays compared to Manhattan.

- **For Hosts**:  
   - Improve **availability** and **review response rates** to attract more bookings.
   - Manage pricing effectively to compete within the borough's market.

---

## Future Work
- Use **machine learning** to predict prices based on room type and location.
- Perform **sentiment analysis** on reviews to better understand guest experiences.
- Create an **interactive dashboard** using Plotly or Tableau for live monitoring.

---

## Conclusion
This project offers valuable insights into the New York Airbnb market, helping both guests and hosts make informed decisions. By using **EDA techniques**, we identified key trends and developed actionable recommendations. Future improvements can involve advanced analytics and predictive modeling to further enhance the findings.

---


---
