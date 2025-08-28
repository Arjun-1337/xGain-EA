# 📈 EMA9/14 Intrabar EA with SMA Trend Filter

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/64/Metatrader_logo.png" width="100" alt="MetaTrader 5 Logo"/>
</p>

<p align="center">
  <b>EMA9/14 Intrabar Crossover Expert Advisor</b>  
  🚀 Smart trade execution | 🎯 Per-trade TP/SL | 📊 SMA trend filter | 💰 Daily PnL guard | ⚖️ Margin-aware lot sizing
</p>

---

## 🔥 Overview

This Expert Advisor (`EMA9_14_Intrabar_TP_SL_SMA200.mq5`) implements a **scalping & intraday trading system** for MetaTrader 5 based on **EMA crossovers** with multiple safety layers and advanced money management.

- **EMA(9/14) crossover logic (intrabar, not only bar-close)**  
- **Optional SMA200 trend filter** for directional bias  
- **Per-trade Take Profit / Stop Loss** in pips  
- **Per-candle pip target** (lock profits & prevent over-trading per bar)  
- **Daily profit/loss guard** (auto stop trading after hitting thresholds)  
- **Margin-aware dynamic lot sizing**  
- **Robust order management** with automatic opposite position closing  

---

## 🛠️ Features

✅ **EMA Intrabar Crossovers** – react faster to short-term shifts  
✅ **SMA200 Trend Filter** – trade only in trend direction  
✅ **Per-Trade Risk Management** – TP & SL in pips  
✅ **Per-Candle Profit Target** – lock gains per candle  
✅ **Daily Profit & Loss Guard** – halt trading when thresholds hit  
✅ **Margin-Aware Lot Calculation** – prevents margin errors  
✅ **Debug Mode** – detailed logs for troubleshooting  

---

## ⚙️ Input Parameters

| Parameter | Default | Description |
|-----------|---------|-------------|
| `InpFastEMA` | 9 | Fast EMA period |
| `InpSlowEMA` | 14 | Slow EMA period |
| `InpUseSMAFilter` | true | Enable SMA trend filter |
| `InpSMAPeriod` | 200 | SMA period for trend filter |
| `InpOpenOnInit` | true | Open trade immediately on EA start if condition met |
| `InpLots` | 0.10 | Fixed lot size |
| `InpTP_Pips` | 100 | Take Profit in pips (0 = disabled) |
| `InpSL_Pips` | 50 | Stop Loss in pips (0 = disabled) |
| `InpPerCandleProfitPips` | 0 | Max profit per candle in pips (0 = disabled) |
| `InpDailyProfitTarget` | 0 | Daily profit target in account currency |
| `InpMaxDailyLoss` | 0 | Max daily loss in account currency |
| `InpNewBarOnly` | false | Trade only on new bar |
| `InpDeviationPoints` | 20 | Slippage allowance (points) |
| `InpMagic` | 900914001 | Magic number (EA identifier) |
| `InpPrintDebug` | false | Enable verbose logging |

---

## 📊 Strategy Logic

1. **Crossover Detection**  
   - **BUY** when EMA(9) > EMA(14)  
   - **SELL** when EMA(9) < EMA(14)  
   - If SMA filter enabled, trade only in trend direction  

2. **Risk & Trade Management**  
   - Opposite trades auto-closed when new signal triggers  
   - TP/SL applied per trade  
   - Margin-aware lot size adjustment  
   - Daily profit/loss guard halts trading  

3. **Profit Locking**  
   - Per-candle pip target halts new trades once profit met  

---

## 🚀 Installation

1. Copy `EMA9_14_Intrabar_TP_SL_SMA200.mq5` into: MQL5/Experts/
2. Restart MetaTrader 5.  
3. Attach EA to chart (`EURUSD M15` recommended).  
4. Configure **Inputs** as per risk appetite.  

---

## 📷 Screenshots (Optional)

*(You can add screenshots of EA settings / performance results here)*

---

## 🏆 Best Practices

- Use **M15 or M30 timeframes** for balanced signals.  
- Enable **SMA200 filter** for trend following.  
- Set **Daily Max Loss** to protect account.  
- Always test in **Strategy Tester** before going live.  

---

## 📜 License

This EA is for **personal & educational use only**.  
Author: **Arjun** (updated & debugged)  

---

<p align="center">
<img src="https://img.shields.io/badge/Platform-MetaTrader%205-blue?logo=metatrader&logoColor=white"/>
<img src="https://img.shields.io/badge/Language-MQL5-orange?logo=c&logoColor=white"/>
<img src="https://img.shields.io/badge/Status-Stable-success"/>
</p>
