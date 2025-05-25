# 🧾 Global Food Trends – Powered by Zomato

### 📌 Objective

To explore and visualize global restaurant trends using the Zomato dataset. This Power BI dashboard uncovers insights into restaurant distribution, cuisine popularity, pricing, ratings, delivery options, and customer engagement across countries and cities.

---

### 📊 Dashboard Highlights

| Section                     | Description                                                                 |
| --------------------------- | --------------------------------------------------------------------------- |
| 🌍 Restaurant Distribution  | Map and bar chart of restaurants by country and city                        |
| 🍽️ Top Cuisines            | Column chart and treemap of most common and city-specific cuisines          |
| 💰 Pricing & Affordability  | Heatmaps of average cost per country/city with price category filters       |
| ⭐ Ratings Overview          | Histogram and bar chart of ratings distribution by rating color and text    |
| 🚚 Delivery & Table Booking | Stacked bars, pie chart, and matrix of online delivery and table bookings   |
| 📈 Votes & Popularity       | Scatter plot and table showing restaurant popularity and rating correlation |
| 🗺️ Location Map            | Interactive map with restaurant name, cuisine, rating & delivery info       |

---

### 📁 Dataset Details

* **Source**: Zomato Restaurant Dataset (Kaggle or provided source)
* **Size**: \~10,000+ restaurants
* **Fields**:

  * Restaurant ID, Name, Country Code, City, Locality
  * Cuisines, Average Cost for Two, Currency
  * Has Online Delivery, Has Table Booking, Is Delivering
  * Price Range, Aggregate Rating, Rating Color/Text, Votes

---

### 🧹 Data Preprocessing (Power Query)

* Mapped `Country Code` to `Country Name` via custom lookup table
* Split `Cuisines` column into multiple rows for granular analysis
* Trimmed whitespace from cuisine names
* Normalized `Currency` via slicers (not converted to a single value)
* Created calculated columns:

  * `IsOnlineDelivery`, `IsTableBooking`, `IsDelivering`
  * `PriceCategory` = Budget / Mid / Premium based on `Price Range`

---

### 📌 Key Insights

* 🇮🇳 **India** has the highest number of restaurants in the dataset
* 🏙️ **New Delhi**, **London**, and **Doha** are top cities by restaurant count
* 🍕 **North Indian**, **Chinese**, and **Fast Food** are globally popular cuisines
* 💸 Average dining cost is highest in **Qatar** and **UAE**, lowest in **India**
* 🟢 Restaurants with **high ratings (4.5+)** tend to get **more votes**
* 🚚 Many cities lack online delivery despite high restaurant density
* 🪑 Table booking is most common in premium restaurants

---

### 🧠 Interactive Features

* **Slicers**: Country, City, Cuisine, Price Category, Rating Text
* **Bookmarks**:

  * Top Cities
  * Top Cuisines
  * Delivery Focused
  * Table Booking
* **Toggle Buttons**:

  * View Switch: Ratings vs Price, Map vs Table
* **Drillthrough Pages**:

  * Click on a city or restaurant to explore detailed stats
* **Tooltips**:

  * Hover over charts to view restaurant details

---

### 🛠 Tools Used

* **Power BI Desktop**
* **Power Query (M Language)**
* **DAX for Calculated Columns and Measures**



