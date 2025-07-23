
# ✈️ Airline Operations Dashboard using Power BI


## 📌 Project Overview

This project focuses on analyzing airline operational data using Power BI. The dataset includes details of flights, tickets, and passenger information. The primary objective is to build an interactive, insightful, and visually appealing dashboard to monitor flight performance, passenger flow, and ticket statuses.

<img width="883" height="714" alt="image" src="https://github.com/user-attachments/assets/374591e5-e8a2-4486-9da3-73b401d9dbb7" />

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

<img width="851" height="329" alt="image" src="https://github.com/user-attachments/assets/61c9f095-31e4-47fc-8243-eaa47d1389c8" />


---

## 🔍 3. Enhanced Data Insights 

✅ **Transformations**:
- Created a conditional column `Flight Classification`:
  - `On Time` → “Best”
  - `Delayed` or `Cancelled` → “To Be Improved”
- Extracted numeric flight numbers using *Column From Examples*

📌 **Deliverable**: Updated table with classification and flight number extraction
<img width="720" height="454" alt="image" src="https://github.com/user-attachments/assets/208cf2ed-c74b-4903-a9d8-88bcf9fb5ddf" />

---

## 📊 4. Calculations Using DAX 

✅ **Measures Created**:
- `Total Passengers` per flight
- `Total Tickets Booked`
- Filtered visual for **only “Best” Flights**

📌 **Deliverable**: Screenshot of DAX formulas and output visuals
<img width="813" height="494" alt="image" src="https://github.com/user-attachments/assets/55440c6b-709b-46d1-aabf-db389afc4583" />

<img width="869" height="353" alt="image" src="https://github.com/user-attachments/assets/88145ea1-8a35-4f5c-bb00-971cc784e57b" />

<img width="691" height="602" alt="image" src="https://github.com/user-attachments/assets/b1f8332f-3bb3-444b-8886-4046baa036aa" />

---

## 📈 5. Visualization & Interactivity 

✅ **Visuals Created**:
- Passenger Count by Airline (Bar Chart)
  <img width="514" height="307" alt="image" src="https://github.com/user-attachments/assets/496909b2-258e-4a02-a837-7e64442e39c2" />

- Ticket Booking Status Distribution (Pie Chart)
 <img width="525" height="313" alt="image" src="https://github.com/user-attachments/assets/fcc21c0d-4c71-4b3f-975b-c316c59ca89e" />

- Flights by Airline and Destination (Stacked Chart)
  <img width="687" height="495" alt="image" src="https://github.com/user-attachments/assets/f5ef2dc5-5ad0-40c4-b194-153bbb3ab13b" />


✅ **Interactive Features**:
- Slicers for Airline and Destination
- Buttons with Bookmarks for:
  - Confirmed Tickets
  - Cancelled Tickets
  - Pending Tickets
- Individual airline pages with navigation buttons
  
<img width="510" height="401" alt="image" src="https://github.com/user-attachments/assets/1680847e-e3b5-4d4d-9513-f04b97e1584b" />

📌 **Deliverable**: Screenshots of all visuals with slicers and buttons

---

## 📊 6. Final Dashboard & Power BI Service Deployment 

✅ **Dashboard Components**:
- All key visuals aligned on a single interactive dashboard
- Custom colors and layout for professional design
<img width="711" height="418" alt="image" src="https://github.com/user-attachments/assets/2cb19c66-5c99-47be-8da0-1cad92cf591b" />

<img width="707" height="332" alt="image" src="https://github.com/user-attachments/assets/53563bf1-6350-454c-9990-6223b87f4025" />

<img width="706" height="329" alt="image" src="https://github.com/user-attachments/assets/e9d4245a-74f1-4c00-b619-c4db0c2e889e" />

<img width="435" height="34" alt="image" src="https://github.com/user-attachments/assets/8e0d2884-28a5-4fbd-81e1-bf6d00c77ef5" />

<img width="671" height="254" alt="image" src="https://github.com/user-attachments/assets/11d3383e-cb5a-4cd4-8254-767f73ac6456" />

<img width="671" height="302" alt="image" src="https://github.com/user-attachments/assets/138ea9f9-344e-433a-b420-c99f3cad95c0" />

<img width="650" height="289" alt="image" src="https://github.com/user-attachments/assets/40c79d69-7eef-422d-a039-0ffbb9bd7f06" />

<img width="673" height="381" alt="image" src="https://github.com/user-attachments/assets/a3cd9b3f-e73e-4d8a-9a23-a4c912c15b5a" />



✅ **Power BI Service Features**:
- **Row-Level Security (RLS)** setup for `Airline A`
- Scheduled daily refresh set for 5 PM
- Published to Power BI Service under workspace “Task-6”

📌 **Deliverable**: Screenshot of dashboard, RLS config, and refresh schedule
<img width="932" height="856" alt="image" src="https://github.com/user-attachments/assets/a86b38e5-639d-4a92-9699-555be41f6a85" />

---

## 📽 Video Walkthrough

👉 **[Watch Full Video Explanation](https://drive.google.com/file/d/1i-HFdhkSe1dp3pU-STkSCNq1GKLPe4ZR/view?usp=drive_link)**  
 
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
[LinkedIn]( http://www.linkedin.com/in/ayush-kumar-4137 ) | [GitHub]( https://github.com/CodeWithXayush )
