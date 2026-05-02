# ✈️ Flight Deals Tracker

A Python-based backend system that automatically tracks flight prices and sends alerts when prices drop below a predefined threshold.

## 🚀 Features

* 🔍 Searches flights using SerpAPI (Google Flights engine)
* 📉 Detects cheapest flights (direct & indirect)
* 📊 Stores and updates data using Sheety (Google Sheets)
* 📩 Sends alerts via:

  * Email
  * SMS (Twilio)
  * WhatsApp (Twilio)
* ⏱️ Supports automated periodic execution

---

## 🏗️ Project Structure

```
├── data_manager.py        # Handles Sheety API (prices + users)
├── flight_search.py       # Fetches flight data from SerpAPI
├── flight_data.py         # Processes and finds cheapest flights
├── notification_manager.py # Sends SMS, WhatsApp, Email alerts
├── main.py                # Main orchestration logic
├── requirements.txt
├── .env                   # Environment variables (NOT pushed)
```

---

## ⚙️ How It Works

1. Fetch destination data from Google Sheets
2. Search for flights for each destination
3. Find the cheapest available option
4. Compare with stored lowest price
5. If lower:

   * Update sheet
   * Send notifications

---

## 🛠️ Tech Stack

* Python
* Requests / Requests-Cache
* SerpAPI (Google Flights)
* Twilio API
* SMTP (Email)
* Sheety API

---

## 🔐 Environment Variables

Create a `.env` file:

```
SERPAPI_API_KEY=
SHEETY_PRICES_ENDPOINT=
SHEETY_USERS_ENDPOINT=
SHEETY_USERNAME=
SHEETY_PASSWORD=

EMAIL_PROVIDER_SMTP_ADDRESS=
MY_EMAIL=
MY_EMAIL_PASSWORD=

TWILIO_SID=
TWILIO_AUTH_TOKEN=
TWILIO_VIRTUAL_NUMBER=
TWILIO_VERIFIED_NUMBER=
TWILIO_WHATSAPP_NUMBER=

ORIGIN_CITY_IATA=
```

---

## ▶️ Installation & Run

```bash
pip install -r requirements.txt
python main.py
```

---

## 📌 Future Improvements

* 🌐 Web dashboard (Flask / FastAPI)
* 📊 Price trend visualization
* 🤖 Smart price prediction
* ☁️ Deployment with scheduled jobs (cron)

---

## 💡 Use Case

This project simulates a real-world flight deal tracking system similar to platforms like Skyscanner or Google Flights alerts.

