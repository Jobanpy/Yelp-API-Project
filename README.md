# Yelp-API-Project

🗂️ Project Overview

This project utilizes the Yelp Fusion API in combination with Apache Spark, specifically PySpark, to facilitate comprehensive data collection and large-scale analysis of restaurant listings in the Edmonton region. The overarching objective is to replicate the backend processes of a location-aware dining recommendation platform, which delivers personalized suggestions based on user preferences and real-time business attributes.

The initiative addresses a frequently encountered consumer concern: “What is a reliable dining option nearby at this moment?” The solution is designed through an end-to-end data pipeline, leveraging modern big data tools and analytical methods.

🎯 Key Objectives

The primary aim was to construct a functional recommendation engine that delivers user-specific dining suggestions derived from Yelp restaurant data. The project workflow involved programmatically retrieving business data from the Yelp API, followed by transforming and analyzing the data using PySpark. Advanced exploratory analysis was then conducted to detect patterns in restaurant popularity, pricing distribution, and operational status. To ensure stakeholder accessibility and interpretation, the analytical results were visualized using appropriate graphical methods.

📊 Data Collection & Features

The data for this project was obtained from the Yelp Fusion API. The geographic focus included Edmonton and neighboring localities such as Sherwood Park and Beaumont. Business listings were filtered to include only those falling within the categories of restaurants, bars, and cafés. The final dataset comprised over 1,000 distinct entries.

Each entry included relevant attributes such as the business name, rating, price range, customer review count, cuisine category, location and geographic coordinates, and information pertaining to operating hours and status (open or closed).

Several data management challenges were encountered during this stage. These included processing deeply nested JSON responses, addressing rate limitations imposed by the API, and managing incomplete records—particularly with regard to pricing and contact information.

🧠 Data Management & Analysis with PySpark

A local Spark session was configured to enable distributed data processing. The JSON responses collected from the API were structured and imported into Spark DataFrames to facilitate subsequent analytical tasks.

The dataset was filtered to retain only those businesses with ratings of 4.0 or higher. Categories describing cuisine types were extracted and analyzed to determine relative popularity across regions. The data was grouped and aggregated to evaluate metrics such as review volume and average rating. Additionally, complex nested fields, including those associated with geographic and operational data, were flattened for analytical compatibility.

Structured queries were executed using Spark SQL to evaluate various metrics. These included quantifying open versus closed establishments by location, identifying top-rated businesses that received a substantial volume of customer reviews, assessing the frequency of specific cuisine categories, evaluating the average price tier associated with varying rating levels, and categorizing restaurants based on price and review density.

📈 Visualization Highlights

Data visualizations were generated using the Matplotlib and Seaborn libraries. These visual outputs included bar charts that outlined the most common restaurant types, histograms representing the distribution of reviews and ratings, pie charts illustrating the proportion of open versus closed establishments, and heatmaps that explored correlations between pricing tiers and review volumes.

These visualizations contributed significantly to enhancing the interpretability of results and were effective in communicating core insights to both technical and non-technical stakeholders.

⚙️ Tech Stack

The technological tools employed throughout this project included Python for programming, the Yelp Fusion API for data acquisition, Apache Spark and PySpark for large-scale data processing, Spark SQL for structured queries, Matplotlib and Seaborn for visual analysis, and Jupyter Notebook as the primary development and documentation environment.

💡 Key Insights

The findings indicated that highly rated restaurants were most commonly located in central areas of Edmonton. Contrary to expectations, premium pricing was not consistently associated with higher ratings or larger review counts. Cuisine types such as Caribbean, Italian, and Canadian (New) were among the most frequently represented across the dataset. Furthermore, a notable number of highly rated businesses lacked comprehensive contact information or an established online presence.

📞 Contact

Harjoban Singh Jawanda
📧 hjawanda@norquest.ca
📞 +1 (780)-224-0890



🔮 Future Enhancements
Several enhancements could improve the functionality and scope of this project. These include integrating real-time filters for dynamic user queries based on price, rating, and cuisine; deploying the analytical pipeline as a Streamlit-based web application; and incorporating external datasets, such as weather or traffic conditions, to contextualize and refine recommendations. Additionally, automating data retrieval through scheduled API calls would help maintain up-to-date information without requiring manual intervention.

