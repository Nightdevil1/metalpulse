# MetalPulse Android-ready PWA prototype — procurement edition

A mobile-first, installable web app prototype customized for brass parts manufacturing and raw-material purchasing across Delhi/NCR and Jamnagar.

## Added for this edition
- Brass, zinc and copper dashboard with manual price entry and source/time fields
- Delhi/NCR vs Jamnagar supplier quote journal, including material/grade, supplier, quote validity and extra per-kg costs
- Landed-cost estimator for quantity, base price, freight and GST
- Transparent rule-based direction indicators based on entered prices
- User-configured target alerts, local history, CSV export and optional browser notifications
- Source desk linking to official MCX zinc information and an indicative brass scrap-rate page

## Critical limitations
- This is a prototype, not a native APK. It has no live market feed, dealer integrations, trained forecasting model, or reliable background push alerts.
- Initial dashboard prices are illustrative demo values. Replace them with verified, timestamped quotes before using any calculations.
- Brass has no single universal exchange price: supplier quotes must be normalized for alloy/grade, product form, taxes, freight, payment terms and delivery point.
- Public scrap prices are indicative context only, not a reliable benchmark for new brass ingot, rod or finished parts.
- Direction indicators are heuristic and not a validated predictive model. Do not treat their score as a calibrated probability or guaranteed forecast.
- Data is stored in the current browser/device and may be lost if browser data is cleared.
- Alerts are checked while the app is open; background alerts require a backend scheduler and push notification service.

## Preview
Open `index.html` in a modern browser. Some PWA functions require HTTPS or localhost.

## Install on Android after hosting
1. Host this folder on an HTTPS static host (e.g. GitHub Pages or Netlify).
2. Open the hosted URL in Chrome on Android.
3. Open Chrome menu → **Install app** or **Add to Home screen**.

## Suggested production build
- Licensed/authorized exchange data source for zinc and copper benchmarks, with clear delay/real-time labels
- Direct supplier quote collection for Delhi/NCR and Jamnagar brass prices
- Backend with timestamped data, source quality flags, historical database and scheduled refresh
- Walk-forward backtesting and calibration before publishing any forecast probabilities
- Firebase Cloud Messaging or equivalent for reliable background alerts
- Secure backend storage for API credentials; never embed secret keys in the Android client

No external service, market feed, notification backend, or API credential is configured by this prototype.
