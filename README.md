
# ✈️ Airline Operations Dashboard using Power BI

(<img width="883" height="714" alt="image" src="https://github.com/user-attachments/assets/374591e5-e8a2-4486-9da3-73b401d9dbb7" />
)

## 📌 Project Overview

This project focuses on analyzing airline operational data using Power BI. The dataset includes details of flights, tickets, and passenger information. The primary objective is to build an interactive, insightful, and visually appealing dashboard to monitor flight performance, passenger flow, and ticket statuses.



---

## 📁 Dataset Details

The project utilizes three main tables:
- `Flight_Information`
- `Ticket_Information`
- `Passenger_Information`

Each dataset contains structured details like FlightID, PassengerID, BookingStatus, Airline, Destination, and more.

---

## 🧹 1. Data Preparation & Cleaning

✅ **Tools Used**: Power Query Editor in Power BI

- Loaded all Excel sheets into Power BI
- Verified and corrected data types:
  - `FlightID`, `TicketID`, `PassengerID` → Whole Number
  - `FlightNumber`, `Airline`, `Destination`, `Status` → Text
- Trimmed unnecessary spaces in text columns
- Ensured consistency in status values (e.g., standardizing “Delayed” vs “delayed”)
- Removed duplicate records from key columns
- Final step: Applied all transformations using **Close & Apply**

📌 **Deliverable**: Power Query Editor screenshots showing cleaned data

---

## 🔗 2. Data Modeling 

✅ **Steps Followed**:
- Defined `FlightID` as the Primary Key
- Created One-to-Many relationships:
  - `Flight_Information[FlightID] → Ticket_Information[FlightID]`
  - `Flight_Information[FlightID] → Passenger_Information[FlightID]`
  - `Ticket_Information[TicketID] → Passenger_Information[PassengerID]`
- Set single-direction filter propagation
- Renamed columns for better readability
- Hid redundant fields in relationships
- Tested model with basic visuals like tables and bar charts

📌 **Deliverable**: Screenshot of model view with relationships

---

## 🔍 3. Enhanced Data Insights 

✅ **Transformations**:
- Created a conditional column `Flight Classification`:
  - `On Time` → “Best”
  - `Delayed` or `Cancelled` → “To Be Improved”
- Extracted numeric flight numbers using *Column From Examples*

📌 **Deliverable**: Updated table with classification and flight number extraction

---

## 📊 4. Calculations Using DAX 

✅ **Measures Created**:
- `Total Passengers` per flight
- `Total Tickets Booked`
- Filtered visual for **only “Best” Flights**

📌 **Deliverable**: Screenshot of DAX formulas and output visuals

---

## 📈 5. Visualization & Interactivity 

✅ **Visuals Created**:
- Passenger Count by Airline (Bar Chart)
- Ticket Booking Status Distribution (Pie Chart)
- Flights by Airline and Destination (Stacked Chart)

✅ **Interactive Features**:
- Slicers for Airline and Destination
- Buttons with Bookmarks for:
  - Confirmed Tickets
  - Cancelled Tickets
  - Pending Tickets
- Individual airline pages with navigation buttons

📌 **Deliverable**: Screenshots of all visuals with slicers and buttons

---

## 📊 6. Final Dashboard & Power BI Service Deployment 

✅ **Dashboard Components**:
- All key visuals aligned on a single interactive dashboard
- Custom colors and layout for professional design

✅ **Power BI Service Features**:
- **Row-Level Security (RLS)** setup for `Airline A`
- Scheduled daily refresh set for 5 PM
- Published to Power BI Service under workspace “Task-6”

📌 **Deliverable**: Screenshot of dashboard, RLS config, and refresh schedule

---

## 📽 Video Walkthrough

👉 **[Watch Full Video Explanation](https://drive.google.com/file/d/1i-HFdhkSe1dp3pU-STkSCNq1GKLPe4ZR/view?usp=drive_link)**  
Duration: ~7 minutes  
Covers all operations from cleaning to dashboard deployment.

---

## 🛠 Tools Used

- **Power BI Desktop**
- **Power Query Editor**
- **DAX**
- **Power BI Service**

---

## 📎 How to Run

1. Clone this repo
2. Open the `.pbix` file in Power BI Desktop
3. Check the "Transform Data" to view cleaning logic
4. Go to “Model” view to analyze relationships
5. Use “Report” view to explore visuals
6. Publish to Power BI Service for deployment features

---

## 🧑‍💻 Author

**Ayush Kumar**  
B.Tech CSE | Data Analyst Enthusiast  
[LinkedIn](https://www.linkedin.com/in/ayush-kumar-41374a272) | [GitHub](https://github.com/your-profile)
