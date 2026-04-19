# 📊 Demand Forecasting & Inventory Planning Model

A practical, end-to-end demand planning model built in Excel / Google Sheets that replaces guesswork with data-driven decision-making.

---

## 🚀 Problem Statement

Businesses constantly face two risks:
- ❌ Stockouts → Lost sales and unhappy customers  
- ❌ Overstocking → Cash stuck in inventory  

Most rely on static spreadsheets or gut feeling — leading to repeated costly mistakes.

This model solves that by dynamically calculating:
- When to reorder  
- How much to order  
- How to ship (Air vs Sea)  
- How much space (containers) is required  

---

## 🧠 What This Model Does

Think of it as a **control tower for inventory**.

In one view, you can:
- Identify products at risk of stockout  
- See exact Out-of-Stock (OOS) dates  
- Get reorder recommendations (case-pack adjusted)  
- Decide shipping mode (Air / Sea / Split)  
- Plan container space (CBM-based)  

All outputs update automatically when inputs change.

---

## 🏗️ Model Architecture

The model is structured into 7 interconnected sheets:

| Sheet Name        | Purpose |
|------------------|--------|
| CONFIG           | Central control panel (lead times, policies, rules) |
| SALES_DATA       | Historical sales transactions |
| INVENTORY        | Current stock snapshot (warehouse + pipeline + transit) |
| PO_LOG           | Purchase order tracking with stage-wise visibility |
| DEMAND_MODEL     | Main dashboard with KPIs and recommendations |
| CONTAINER_PLAN   | Converts demand into container requirements |
| SHIP_MODE        | Decides Air vs Sea shipment strategy |

---

## ⚙️ Key Calculations

### 1. Demand Forecasting (Weighted Average)
- 7-day (50%) + 30-day (30%) + 90-day (20%)
- Captures recent trends while maintaining stability

### 2. Days of Stock (DOS)

DOS = Warehouse Stock ÷ Daily Sales Velocity


### 3. Reorder Trigger

Reorder Point = Lead Time + Buffer Days


### 4. Order Quantity

Required Qty = Demand during Lead Time + Buffer - Current Stock - Open Orders

- Rounded to case pack  
- Respects minimum order quantity  

### 5. Safety Stock

Safety Stock = Daily Sales × Buffer Days


### 6. Container Planning (CBM)

CBM = (L × B × H) / 1,000,000


### 7. Ship Mode Decision
- Low stock → Air (urgent)  
- Medium → Split (Air + Sea)  
- High → Sea (cost-efficient)  

---

## 🔄 How It Works (Flow)
Sales Data → Demand Calculation → Inventory Position
→ Reorder Decision → PO Recommendation → Ship Mode → Container Plan


---

## 📈 Business Impact

This model helps:
- Reduce stockouts and lost sales  
- Avoid over-ordering  
- Optimize working capital  
- Improve supply chain visibility  
- Make faster, data-backed decisions  

---

## 🔍 Key Differentiators

| Feature | Basic Spreadsheet | This Model |
|--------|----------------|-----------|
| Demand Forecast | Static | Dynamic (weighted) |
| Reorder Logic | Manual | Automated |
| Pipeline Tracking | ❌ | ✅ |
| OOS Prediction | ❌ | ✅ |
| Case Pack Logic | Manual | Auto |
| Ship Mode Decision | Manual | Rule-based |
| Container Planning | ❌ | Built-in |

---

## ⚠️ Limitations

- Does not account for seasonality (yet)  
- Requires clean and consistent data  
- Manual inventory updates (not real-time)  

---

## 🛠 Tools Used

- Microsoft Excel / Google Sheets  
- Statistical logic (moving averages, weighted averages)  
- Supply chain planning concepts  

---

## 📌 Future Enhancements

- Add seasonality adjustment  
- Build Power BI dashboard  
- Automate using Python  
- Integrate real-time data  

---

## 📸 Preview

<img width="1577" height="188" alt="image" src="https://github.com/user-attachments/assets/ab59ff12-a132-4d03-a387-3797f4cd4177" />

<img width="1080" height="186" alt="image" src="https://github.com/user-attachments/assets/b0bec8f0-5da2-46fe-bce4-053ed7b7d0a8" />

<img width="653" height="185" alt="image" src="https://github.com/user-attachments/assets/23f953c1-608b-4d0f-bffe-1eaeb58ee44b" />


---

## 🤝 Connect

If you're working in supply chain, logistics, or data analytics — feel free to connect or share feedback!

