# n-Tier Architecture

## Requirements

### Background

Commonly projects begin with customer discussions and problem analysis prior to developing a solution. This is known as **capturing originating requirements**.

I keep several of my guitars and other musical instruments in one room of my house, many of which are sensitive to environmental changes. Wood furniture may react to changes in temperature and humidity, but those same changes can have a more profound effect on wooden instruments such as guitars. If the humidity is too low, the wood of the guitar can become dry and brittle, leading to cracks and other damage. If the humidity is too high, the wood can absorb moisture, causing swelling, warping, and other types of damage.

In an attempt to monitor and moderate this, I have **temperature and humidity sensors** located around the room.

To augment the sensors, I can remotely control the temperature (heating and cooling), **fans** for air circulation, and **humidifiers** to regulate the dry air from running the heater or from certain weather events. This can be a problem year-round and especially in the winter. I live in a relatively dry climate so excessive humidity is not a concern. There isn't a need for a de-humidifier.

---

### System Description

I need a cloud-hosted service which will continually monitor multiple IOT sensors in the studio, store and analyze the data, and control power (on/off) switches for the fans and humidifiers in the room.

I would like to see how the temperature and humidity changes over a period of hours, days, weeks, and months both graphically and as tables of data.

An (IOT) thermostat and HVAC should maintain the room temperature between 68 and 75 degrees (Fahrenheit) on its own, but the monitoring system should allow me to set threshold values to alert me if the temperature goes above or below set limits, in which case intervention might be necessary. The proposed solution does not need to control the temperature, just monitor, store and provide (email) alerts.

While the room temperature is controlled by the home's heating and air-conditioning (HVAC) system, and monitored by our software, the system needs to turn the humidifier on or off to maintain the relative humidity between 45% and 55% along with the fans to circulate the air. The system should email alerts if the humidity values exceed user-set limits.

The system should perform periodic system checks and send alerts if the monitors are offline or not reporting regularly. Observation data should be recorded approximately every 5 minutes, and an alert should be sent if the system has not responded after 15 minutes.

I should be able to view this information and control the user-defined thresholds and alert settings from a web page on my computer and also from a mobile device.

An API connecting to a database and serving as the data access layer would make the system extensible and would enable different apps to use the data including web and mobile apps.

---


## 🔧  Instructions 

Design and describe an **n-tier architecture** solution for the **monitoring and control system** described above. Your design does **not need to be implemented**, and **no coding is required**.

Your deliverable will be a **2–4 page document**, and may include **diagrams, tables, or charts** where helpful. The document should include the following **sections**:

---

### 1. 📋 Requirements Table *(15 points)*  
Create a **clear and complete table of system requirements**, organized into:

- **Functional requirements** (e.g., monitor sensor data, control humidifiers, send alerts)
- **Non-functional requirements** (e.g., scalability, availability, responsiveness)
- Optional: Identify **critical requirements** that must be met for success.

---

### 2. 🧱 System Architecture Design *(20 points)*  
Describe your **n-tier architecture**, clearly identifying each **tier or layer** in the system:

- **Presentation Tier** (e.g., web/mobile interfaces)
- **Application/Logic Tier** (e.g., APIs, services)
- **Data Tier** (e.g., databases, cloud storage)

Use a **diagram** to illustrate how components interact. Include data flow if helpful.

---

### 3. 🧩 Component Descriptions *(15 points)*  
List and explain each **major component** in your system. For each component:

- Describe its **role and responsibilities**
- Explain how it **connects** to other components
- Include devices (IoT sensors, controllers), software (API, frontend), and cloud resources

---

### 4. ☁️ Cloud Hosting Strategy *(15 points)*  
Recommend a **cloud hosting strategy** for each component. Address:

- **Which services/platforms** (e.g., AWS, Azure, GCP) you would use and why
- Cost efficiency and **scalability**
- Availability and performance considerations

---

### 5. 🚨 Alerting & Monitoring *(10 points)*  
Describe how the system:

- Monitors sensor values and system health
- Sends alerts when thresholds are crossed or devices go offline
- Allows **user-configurable thresholds** for temperature and humidity
- Ensures reliability (e.g., 5-minute checks, 15-minute timeout detection)

---

### 6. 🔄 Scalability & Extensibility *(10 points)*  
Explain how the system could:

- Be **extended** to include more sensors or rooms
- Support additional **apps** (e.g., native mobile)
- Scale components independently for performance and cost optimization

---

### 7. 🧾 Presentation & Documentation *(10 points)*  
Make sure your document is:

- Well-organized and **easy to read**
- Includes helpful **headings**, **diagrams**, and **visual aids**
- Free from spelling/grammar issues
- Clearly explains all technical terms

---

### 8. 💡 Completeness & Creativity *(5 points)*  
Bonus credit is awarded for:

- Addressing **all requirements** fully
- Offering **creative enhancements or features**
- Using professional formatting or design tools for visual polish

---
