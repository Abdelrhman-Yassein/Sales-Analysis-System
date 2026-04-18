# 📊 Sales Analysis System

## 🚀 Project Overview
This project is a simple **Sales Analysis System** built using Python.  
It demonstrates core data processing and analysis techniques commonly used in **Data Analytics and Business Intelligence**.

The project focuses on analyzing sales data using:
- Functional programming (`map`, `filter`, `lambda`)
- List Comprehensions
- Sorting and aggregation

---

## 🗂️ Dataset

```python
sales = [
    {"id": 1, "customer": "Ali", "city": "Cairo", "amount": 500, "status": "COMPLETE"},
    {"id": 2, "customer": "Sara", "city": "Giza", "amount": 300, "status": "PENDING"},
    {"id": 3, "customer": "Omar", "city": "Cairo", "amount": 700, "status": "COMPLETE"},
    {"id": 4, "customer": "Mona", "city": "Alex", "amount": 200, "status": "CANCELLED"},
    {"id": 5, "customer": "Ahmed", "city": "Cairo", "amount": 1000, "status": "COMPLETE"},
    {"id": 6, "customer": "Laila", "city": "Giza", "amount": 400, "status": "COMPLETE"},
    {"id": 7, "customer": "Hassan", "city": "Alex", "amount": 150, "status": "PENDING"}
]
```

---

## 🎯 Objectives

- Filter completed orders  
- Calculate total sales  
- Identify top 3 customers  
- Transform customer names  
- Filter high-value transactions  
- Sort sales data  
- Aggregate sales by city  
- Count orders by status  

---

## 🧠 Features & Implementation

### ✅ Filter Completed Orders
```python
completed = list(filter(lambda x: x["status"] == "COMPLETE", sales))
```

### ✅ Total Sales Calculation
```python
total_sales = sum(map(lambda x: x["amount"], completed))
```

### ✅ Top 3 Customers
```python
top_customers = sorted(completed, key=lambda x: x["amount"], reverse=True)[:3]
```

### ✅ Convert Names to Uppercase
```python
upper_names = list(map(lambda x: x["customer"].upper(), sales))
```

### ✅ High Value Orders (>500)
```python
big_sales = [x for x in sales if x["amount"] > 500]
```

### ✅ Sort Sales by Amount
```python
sorted_sales = sorted(sales, key=lambda x: x["amount"])
```

### ✅ Sales Aggregation by City
```python
city_sales = {}

for s in completed:
    city = s["city"]
    city_sales[city] = city_sales.get(city, 0) + s["amount"]
```

### ✅ Orders Count by Status
```python
status_count = {}

for s in sales:
    status = s["status"]
    status_count[status] = status_count.get(status, 0) + 1
```

---

## 📊 Sample Output

```
Total Sales: 2600

Top Customers:
[{'customer': 'Ahmed', 'amount': 1000}, ...]

City Sales:
{'Cairo': 2200, 'Giza': 400}

Status Count:
{'COMPLETE': 4, 'PENDING': 2, 'CANCELLED': 1}
```

---

## 🛠️ Technologies Used

- Python 🐍
- Built-in functions (`map`, `filter`, `sorted`)
- Core data structures (lists, dictionaries)

---

## 💡 Key Learnings

- Writing clean and efficient Python code  
- Using functional programming concepts  
- Performing real-world data analysis tasks  
- Data transformation and aggregation  

---

## 👨‍💻 Author

**Abdelrhman**  
Data Engineer & Data Modeler  

## 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdelrhman-yassein/)

---

## ⭐ If you like this project
Give it a star on GitHub ⭐ and feel free to connect!
