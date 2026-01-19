# Big O Indicator - Notification Sounds Guide

## Overview
The Big O Indicator now includes notification sounds for buy and sell alerts. This feature allows you to receive audio notifications when trading signals are generated.

## Features

### 1. Notification Sounds Toggle
- **Location**: Indicator Settings Menu
- **Name**: "Notification Sounds"
- **Default**: Disabled (unchecked)
- **Purpose**: Enable or disable sound notifications for buy and sell alerts

### 2. Buy Alert Notifications
When a buy signal is generated (green arrow appears below the bar with a white line marker):
- **Sound**: Hand Bell 🔔
- **Trigger**: Plays when the candle closes and the buy condition is met
- **Requirement**: "Notification Sounds" toggle must be enabled

### 3. Sell Alert Notifications
When a sell signal is generated (red arrow appears above the bar with a white line marker):
- **Sound**: Fault ⚠️
- **Trigger**: Plays when the candle closes and the sell condition is met
- **Requirement**: "Notification Sounds" toggle must be enabled

## How to Use

### Step 1: Add the Indicator to Your Chart
1. Open TradingView
2. Add the "Big O Indicator" to your chart
3. The indicator will display with a white moving average line

### Step 2: Enable Notification Sounds
1. Click on the indicator name in the chart
2. Select "Settings" (gear icon)
3. Find the "Notification Sounds" checkbox
4. Check the box to enable sound notifications
5. Click "OK" to apply

### Step 3: Configure Alert Sounds (Optional)
For more control over your alerts, you can create custom alerts:

1. Click the "Alert" button (clock icon) in TradingView
2. Select "Create Alert"
3. Choose the Big O Indicator
4. Select either:
   - "Buy Alert - Hand Bell" for buy signals
   - "Sell Alert - Fault" for sell signals
5. In the alert settings:
   - For Buy Alerts: Select "Hand Bell" from the sound dropdown
   - For Sell Alerts: Select "Fault" from the sound dropdown
6. Configure other alert options as desired
7. Click "Create"

## Signal Conditions

### Buy Signal
A buy signal is generated when:
- Price crosses above the moving average (MA)
- AND the Relative Strength Index (RSI) is in oversold territory

Visual indicators:
- Green triangle (arrow pointing up) below the bar
- White line marker at the signal point

### Sell Signal
A sell signal is generated when:
- Price crosses below the moving average (MA)
- AND the Relative Strength Index (RSI) is in overbought territory

Visual indicators:
- Red triangle (arrow pointing down) above the bar
- White line marker at the signal point

## Customization

The indicator includes several customizable parameters:
- **MA Length**: Length of the moving average (default: 20)
- **RSI Length**: Length for RSI calculation (default: 14)
- **RSI Overbought**: Threshold for overbought condition (default: 70)
- **RSI Oversold**: Threshold for oversold condition (default: 30)

## Technical Notes

- Alerts are triggered once per bar close (`alert.freq_once_per_bar`)
- Sounds only play when both:
  1. A valid signal condition is met
  2. The "Notification Sounds" toggle is enabled
- The indicator uses Pine Script v5
- Original indicator functionality remains unchanged

## Troubleshooting

**Q: I enabled notification sounds but don't hear anything**
- Ensure your device volume is turned up
- Check that TradingView has permission to play sounds in your browser
- Verify the "Notification Sounds" toggle is checked in indicator settings
- Make sure you're on a timeframe where signals are being generated

**Q: Can I change the sounds to something else?**
- In-script sounds are set to "Hand Bell" (buy) and "Fault" (sell)
- You can create custom alerts (Step 3 above) and choose any sound you prefer

**Q: Why do I see arrows but no sounds?**
- The "Notification Sounds" toggle must be enabled for sounds to play
- Check that the `alert()` function calls are working in your TradingView environment

## Version Information
- Pine Script Version: 5
- Feature Added: Notification Sounds with toggle control
- Compatibility: TradingView charts with sound support
