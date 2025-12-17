# ✈️ Airline Flight Data Analysis Project

A complete **SQL-based Data Analysis project** where raw airline flight data is cleaned, normalized, and analyzed to extract meaningful insights about **airlines, airports, routes, and passenger traffic**.

This project demonstrates strong skills in **SQL, database design, data modeling, and analytical querying**, and is suitable for **LinkedIn, GitHub portfolios, and data analyst interviews**.

---

## 📌 Project Overview

The original dataset was provided as a single raw table (`meta_data`) containing airline, airport, route, and passenger details. The goal of this project was to:

* Design a **normalized relational database**
* Split raw data into **fact and dimension tables**
* Perform **analytical SQL queries** to uncover insights
* Build a **portfolio-ready data analysis project**

---

## 🗂️ Database Schema

### Dimension Tables

* **airline** – Airline details
* **airport** – Airport and geographic information
* **city** – City and state-level data

### Fact Tables

* **flight** – Flight-level transactional data
* **flightmetrics** – Passengers, freight, and mail metrics

### Relationships

* One airline → many flights
* One airport → many origin and destination flights
* One flight → one metrics record

The schema follows **Third Normal Form (3NF)** to reduce redundancy and improve data integrity.

---

## 🛠️ Tools & Technologies

* **MySQL**
* **SQL** (JOINs, GROUP BY, Aggregations, Indexing)
* **Relational Database Design**
* **Data Cleaning & Transformation**
* **Analytical Query Writing**

---

## 🔄 Data Preparation & Cleaning

Key steps performed:

* Renamed raw table to `meta_data`
* Split raw data into multiple normalized tables
* Removed duplicate records using `DISTINCT`
* Fixed datatype inconsistencies (TEXT → numeric)
* Handled origin and destination airports separately
* Applied foreign key constraints for data integrity

---

## 📊 Key Analysis Performed

### 1️⃣ Airport Analysis

* Busiest origin airports
* Busiest destination airports
* Airports ranked by passenger volume

### 2️⃣ Airline Performance

* Passenger share by airline
* Comparison of airlines based on traffic volume

### 3️⃣ Route Analysis

* Most frequently traveled routes
* Origin–destination city pair analysis

### 4️⃣ Time-Series Trends

* Year-wise and month-wise passenger trends
* Seasonal travel patterns

### 5️⃣ Distance Analysis

* Passenger distribution across distance groups

---

## 🧠 Sample SQL Query

```sql
SELECT a.city_name, SUM(fm.passengers) AS total_passengers
FROM flight f
JOIN flightmetrics fm ON fm.flight_id = f.flight_id
JOIN airport a ON a.airport_id = f.dest_airport_id
GROUP BY a.city_name
ORDER BY total_passengers DESC;
```

**Insight:**
Identifies the busiest destination cities based on passenger traffic.

---

## 📈 Key Insights

* A small number of airports handle the majority of passenger traffic
* Certain airlines dominate overall passenger volume
* Passenger demand shows clear seasonal patterns
* Medium-distance flights tend to carry higher average passengers

---

## 📁 Repository Structure

```
Flight-Data-Analysis/
│
├── SQL/
│   ├── table_creation.sql
│   ├── data_insertion.sql
│   └── analysis_queries.sql
│
├── Presentation/
│   └── Airline_Flight_Data_Analysis_Enhanced.pptx
│
├── README.md
```

---

## 🚀 Future Enhancements

* Build interactive dashboards using **Power BI / Tableau**
* Add window-function-based analysis
* Perform predictive analysis on passenger trends
* Optimize queries using advanced indexing

---

## 👤 Author

**Bhumika Kushwah**
Aspiring Data Analyst | SQL | Data Analysis


