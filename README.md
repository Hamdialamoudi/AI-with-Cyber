# AI Network Threat Detection 🚨🤖

**Real-time network monitoring and threat detection system** built with Python. Detects anomalies in network traffic using **machine learning** and sends alerts via Telegram.

---

## Features
- Capture network traffic using `tshark`
- Detect anomalies with **Isolation Forest**
- Send instant **Telegram alerts**
- Flask **dashboard** for real-time monitoring
- Whitelist & cooldown to reduce false positives
- Logs all alerts in `threats.log` for auditing

---

## How It Works
1. Captures network packets and logs source IPs every 10 seconds.
2. Counts IP occurrences and detects anomalies with Isolation Forest.
3. Sends alerts to Telegram and updates the Flask dashboard.
4. Logs all events for review.

---

## Requirements
- Python 3.x  
- pandas  
- scikit-learn  
- Flask  
- requests  
- tshark (Wireshark CLI)

---

## Setup & Run
1. Clone this repo:
   ```bash
   git clone <YOUR_REPO_URL>
   cd <YOUR_REPO_FOLDER>
Install dependencies:

bash
Copy code
pip install pandas scikit-learn flask requests
Update BOT_TOKEN and CHAT_ID in the script.

Run the script:

bash
Copy code
python threat_detection.py
Open dashboard in browser:

cpp
Copy code
http://127.0.0.1:5000/
Tech Stack
Python | pandas | scikit-learn | Flask | requests | tshark

Notes
Ensure tshark is installed and you have the correct network interface.

Add trusted IPs to WHITELIST to avoid false positives.

Alerts are throttled by COOLDOWN_SECONDS to prevent spam.
