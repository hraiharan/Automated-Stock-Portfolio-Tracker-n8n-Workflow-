# Automated-Stock-Portfolio-Tracker-n8n-Workflow-
This project is an automated stock tracking workflow built using n8n. It fetches live stock prices daily from Yahoo Finance, calculates portfolio value changes, and sends a summary update to Telegram. It also logs the data to Google Sheets for historical tracking.






Here’s a clean and professional **README** you can use for your GitHub project. I wrote it based on your `stock.json` workflow – which tracks stock prices daily using **n8n**, **Yahoo Finance API**, and sends portfolio updates via **Telegram** and **Google Sheets**.

---

# 📈 Automated Stock Portfolio Tracker (n8n Workflow)

This project is an **automated stock tracking workflow built using n8n**. It fetches **live stock prices daily from Yahoo Finance**, calculates **portfolio value changes**, and sends a **summary update to Telegram**. It also logs the data to **Google Sheets** for historical tracking.

---

##  Features

 Fetches live stock prices daily using Yahoo Finance
 Tracks custom stock portfolio with quantities
 Calculates price change and percentage gain/loss
 Sends daily stock summary to Telegram
 Logs data to Google Sheets
 Fully customizable and extendable

---

## 🛠️ Tech Stack & Tools Used

| Tool / Service       | Purpose                          |
| -------------------- | -------------------------------- |
| n8n Automation Tool  | Workflow orchestration           |
| Yahoo Finance API    | Fetch stock market data          |
| Telegram Bot API     | Send stock updates               |
| Google Sheets        | Store daily tracking history     |
| JavaScript Functions | Data formatting and calculations |

---

## ⚙️ Workflow Overview

The workflow includes these main steps:

1. **Cron Trigger** – Runs every day at 9 AM IST
2. **Set Stock Symbols** – List of stocks to track (e.g. `IOB.NS`, `SAKHTISUG.NS`)
3. **Split Stock List** – Splits the stock list for individual processing
4. **Fetch Stock Price** – Fetches stock data from Yahoo Finance
5. **Format Result** – Extracts current price, change, percentage, timestamp
6. **Compose Telegram Message** – Creates a summary for all stocks
7. **Send to Telegram** – Sends the report to your Telegram chat
8. **Save to Google Sheets** *(optional)* – Appends data to Sheets

---

##  Example Telegram Output

```
 Daily Indian Stock Portfolio Update

 IOB.NS (Holdings: 20 shares)
   Current: ₹68.40 | Value: ₹1368.00
   Change: ₹+1.20 (+1.68%)
   Previous Close: ₹67.20

 SAKHTISUG.NS (Holdings: 400 shares)
   Current: ₹38.50 | Value: ₹15400.00
   Change: ₹-0.80 (-2.04%)
   Previous Close: ₹39.30

Last Updated: 29 Oct 2025, 9:00 AM IST
```

---

##  Prerequisites

Before using this workflow, make sure you have:

* n8n installed (`npm install n8n -g`)
* A Telegram bot token (from @BotFather)
* Yahoo Finance stock symbols
* Google Sheets credentials (OAuth2)

---

##  Setup Instructions

### 1. Clone this repo

```bash
git clone https://github.com/your-username/your-repo.git
```

### 2. Import workflow

* Open n8n (`n8n start`)
* Import the file `stock.json` into n8n
* Edit nodes as needed

### 3. Configure Credentials

* Add Google Sheets OAuth credentials
* Add Telegram Bot API key
* Add stock list to `Set Stock Symbols` node

---

## 🛠️ Customization

You can modify:

| Custom Item          | Where to edit                   |
| -------------------- | ------------------------------- |
| Stock list           | `Set Stock Symbols` node        |
| Run schedule         | `Cron` node                     |
| Portfolio quantities | In `Combine Telegram Data` node |
| Output message style | JS code in message compose node |

---

##  Future Enhancements

*  Email report support
*  Historical chart tracking
*  Portfolio gain/loss tracking over time
*  Dashboard integration

---

 
