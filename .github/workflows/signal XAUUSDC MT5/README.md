# XAUUSD Gold Signal M5
Android WebView project. Includes BUY/SELL/TUNGGU, Entry, SL, TP, ATR, RSI, MACD, EMA and M15 trend confirmation. Demo button uses simulated candles only.

## Build APK from Android using GitHub
1. Create a new GitHub repository and upload all files in this folder, including hidden `.github` folder.
2. Open Actions and run `Build XAUUSD Gold Signal APK` (or push to main).
3. When green, open the run, download artifact `XAUUSD-Gold-Signal-M5-APK`, unzip it, install `app-debug.apk`.

## Real broker MT5 connection
MT5 Android does not expose an API for this app. You need MT5 desktop terminal logged into your broker on Windows/VPS, Python MetaTrader5 package on that same machine, and an authenticated HTTPS API bridge. Enter the bridge URL in app. The API should return JSON:
`{"candles":[{"open":3300.1,"high":3301.2,"low":3299.8,"close":3300.9}, ...], "m15":{"closes":[3300.1, ...]}}`
At least 35 M5 candles required. Use completed candles, HTTPS, authentication and firewall. This project does not include the server bridge. Do not place broker passwords in the app.

Signals are heuristic and not backtested; no profit guarantee. Check broker symbol suffix and contract specs.
