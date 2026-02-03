# BNF Signal 🚥

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Financial Strategy](https://img.shields.io/badge/Strategy-Mean--Reversion-green)](#-the-signal-logic)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**BNF Signal** is a quantitative market-observation engine designed to identify extreme mean-reversion events. It is a technical tribute to **Takashi Kotegawa** (alias: BNF), the legendary Japanese trader who mastered the art of buying market capitulation.

---

## 🎯 The Signal Logic

The engine monitors the divergence between a security's spot price and its **25-day Simple Moving Average (SMA)**. This specific metric was the cornerstone of BNF’s early success in the Japanese markets.



### Mathematical Threshold
A signal is triggered when the price-to-SMA deviation of a stock meets the following condition:

$$\text{Price} \le \text{SMA}_{25} \times 0.80$$

### Strategy Pillars:
* **Capitulation Detection:** Identifying points where retail panic creates an "overstretched" rubber band effect.
* **High Liquidity Focus:** By default, the scanner targets S&P 500 constituents to ensure efficient exits.
* **Mean Reversion:** Anticipating a violent "snap back" toward the 25-day average once the selling pressure is exhausted.

---

## 🚀 Features

* **Real-time Scanning:** Fetches the most recent daily closes for the S&P 500.
* **Automated Ticker Ingestion:** Dynamically updates the watch list via Wikipedia's S&P 500 records.
* **Telegram Integration:** Delivers actionable telemetry directly to your mobile device.
* **Batch Processing:** Optimized `yfinance` calls to prevent IP rate-limiting.

---

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/yourusername/bnf-signal.git](https://github.com/yourusername/bnf-signal.git)
cd bnf-signal
```

### 2. Install Dependencies
```bash
pip install yfinance pandas requests

```
### 3. Telegram configuration
```To receive alerts, you must provide your Bot Token and Chat ID:
Create a bot via @BotFather to get your API_TOKEN.
Get your CHAT_ID from @userinfobot.
Update the configuration section in bnf_signal.py.
