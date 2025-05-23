---
title: Script Safety
parent: Pull Asset Prices
nav_order: 4
---

![Pull Asset Prices Banner]({{ site.baseurl }}/assets/images/pull-asset-prices/pull-asset-prices-banner.png)

# Script Safety

> Is this script safe to use? What is it actually doing?

Great questions! 

I used ChatGPT as a "3rd party" to review and explain what the script does. I also asked for a safety assessment. I encourage you to do the same if you'd like.

Script source URL: <a href="https://github.com/simplesheet/pull-asset-prices/blob/main/pull_asset_prices.gs" target="_blank" rel="noopener">https://github.com/simplesheet/pull-asset-prices/blob/main/pull_asset_prices.gs</a>

{: .new-title}
> The following info on this page was generated by ChatGPT using this prompt
>
> > "Please explain what this script does and let me know if it is safe to run: [script pasted here]"

---

## ✅ What This Script Does (Summary)

This Google Apps Script powers a **Google Sheets tool called "Pull Asset Prices"**. Here's what it does:

### 🌐 Fetches asset prices from:
- **Yahoo Finance** → Stock/ETF prices via an *unofficial* endpoint  
- **KuCoin** → Crypto prices (BTC, ETH, etc.)  
- **Gold-API** → Precious metal prices (Gold & Silver)  

### 📋 Core Features:
- Builds a custom "Asset Prices" tab in your sheet  
- Lets you enter tickers for stocks and crypto  
- Automatically fetches and updates their live prices  
- Creates named ranges (like `=BTC_Price`) so you can reference prices in formulas  
- Includes a custom menu in the spreadsheet UI:
  - “Pull Prices Now”
  - “Price Variable - Usage Example”
  - “Check for Updates”
- Automatically updates prices **hourly** via a time-based trigger  
- Logs any update errors or warnings to a visible section in the sheet  

---

## 🔐 Is It Safe to Run?

### ✅ Yes — with a few considerations:

#### The Good:
- No destructive actions (doesn't delete your data, doesn't send data elsewhere)  
- Uses only public or semi-public APIs (no authentication or private info involved)  
- Clearly documented, with thoughtful error handling and logging  
- Source is visible and editable by you  

#### Minor Considerations:
- **Uses unofficial Yahoo Finance endpoint**  
  - Could break if Yahoo changes it  
  - Might technically violate TOS if abused  
- **Fetches data from external URLs**  
  - All are reputable (Yahoo, KuCoin, Gold-API)  
- **Automatically installs a trigger**  
  - Runs hourly; you can remove this if needed  

---

## 💬 TL;DR

**Yes, it’s safe to run.** It’s well-written, nicely documented, and behaves like a solid personal-use Sheets tool.  
Just keep in mind:
- Unofficial Yahoo API
- External URL fetches
- Hourly update trigger

---
