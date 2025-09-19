# qai4_divar_project
# Real Estate Data Analysis & Machine Learning Project  

## 📌 Project Overview  
This project focuses on analyzing and modeling the **Divar Real Estate dataset**, which contains over one million real estate listings from across Iran. The dataset includes detailed information about residential and commercial properties such as:  

- 📍 **Geographical data**: city, neighborhood, latitude/longitude  
- 🏠 **Property details**: size, rooms, year built, amenities  
- 💰 **Financial details**: rent, deposit, sale price, and combined values  
- 📑 **Ownership and documentation**  
- 👤 **Advertiser type** (owner, agent, etc.)  

The project consists of three main parts: **statistical analysis**, **machine learning clustering**, and **price prediction**.  

---

## 📂 Dataset Description  
The dataset contains a wide range of features. Some of the most important include:  

- **city_slug** → City name  
- **neighborhood_slug** → Neighborhood name  
- **price_value / credit_value / rent_value** → Financial details of properties  
- **land_size / building_size** → Land and building size  
- **rooms_count, floor, total_floors_count** → Structural details  
- **has_parking, has_elevator, has_balcony, …** → Amenities  
- **construction_year / is_rebuilt** → Property age and renovation status  
- **location_latitude / location_longitude** → Geographic coordinates  

⚠️ Prices in real estate ads can appear in different formats (sale, rent, mortgage, or combined). To allow fair comparisons, the dataset provides **transformed values** (e.g., `transformable_price`, `transformed_rent`) where rent and mortgage values are normalized into comparable financial units.  

---

## 📊 Part 1: Statistical Analysis  
In this section, you will explore the dataset to answer key questions and test hypotheses about the housing market.  

- **Descriptive Statistics**  
  - Distribution of ads across categories (level 2 & 3)  
  - Histogram of construction years  
  - Seasonal trends in rent vs sale ads  
  - Price distribution across categories  
  - Heatmap of ad density on a geographic map  
  - Trends of rent & sale prices over time (adjusted for inflation)  
  - Correlation matrix between numerical features  

- **Hypothesis Testing**  
  - Are average property sizes smaller in big cities compared to smaller towns?  
  - Are older houses generally larger than newer ones?  
  - Does having a **business deed** affect the average price of commercial properties?  
  - Do luxury amenities (pool, sauna, jacuzzi, barbecue) significantly increase property prices compared to non-luxury features?  

---

## 🤖 Part 2: Machine Learning  

### Task 1: Recommender System (Clustering)  
- Select key features to cluster real estate listings meaningfully.  
- Apply **K-Means clustering** with `k=10` and visualize clusters (using UTM coordinates + price).  
- Use the **Elbow method (WCSS)** to determine the best `k`.  
- Apply **DBSCAN clustering** with transformed price and UTM coordinates to form 3 meaningful clusters.  

### Task 2: Price Prediction  
- Train a supervised ML model to **predict property prices** (sale, rent, or mortgage) based on property attributes.  
- Use metrics such as **R² score, MAE, and MSE** for evaluation.  
- Ensure correct train/validation/test data splitting to avoid data leakage.  
- Feature engineering is encouraged (but be careful not to leak target information).  
