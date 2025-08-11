# bitcoin_price_alert
It's a software that will fetch bitcoin price at that particular instant only.
# 🪙 Bitcoin Price Alert (Web Scraper)

A simple Python script that scrapes the current Bitcoin (BTC) price from [CoinMarketCap](https://coinmarketcap.com/currencies/bitcoin/) and sends an email alert if the price exceeds a specified threshold.

---

## 📌 Features
- Scrapes live Bitcoin price using **BeautifulSoup**
- Sends an email alert via **Gmail SMTP**
- Customizable price threshold
- Lightweight and fast — runs in seconds

---

## ⚙️ Requirements
- Python 3.x  
- Internet connection  
- Gmail account with **App Password** enabled (not your regular password)

---

## 📦 Installation
1. **Clone or Download** this repository  
   ```bash
   git clone https://github.com/YOUR_USERNAME/web-scraping-projects.git
   cd web-scraping-projects/bitcoin_price_alert
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up Gmail App Password**  
   - Go to [Google App Passwords](https://myaccount.google.com/apppasswords)  
   - Select *Mail* and *Your device* → Generate password  
   - Use that in the script

---

## 🛠️ Usage
1. Open `btc_alert.py`  
2. Set:
   ```python
   FROM_EMAIL = "your_email@gmail.com"
   APP_PASSWORD = "your_google_app_password"
   TO_EMAIL = "receiver_email@gmail.com"
   THRESHOLD = 120000  # USD
   ```

3. Run the script:
   ```bash
   python btc_alert.py
   ```

---

## 📤 Output Example
```
Current BTC Price: $113456.78
Price below 120000, no alert sent.
```
or if above threshold:
```
Current BTC Price: $121000.50
Email alert sent!
```

---

## ⚠️ Notes
- CoinMarketCap HTML structure may change; update the scraping logic accordingly.
- Gmail may block sign-in attempts if you don’t use an App Password.
- For frequent checks, schedule with **cron** (Linux) or **Task Scheduler** (Windows).

---

## 📜 License
This project is open-source and available under the [MIT License](LICENSE).
