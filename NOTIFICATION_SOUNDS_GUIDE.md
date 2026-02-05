# Big O Indicator - Notification Sounds Guide

## Overview
The Big O Indicator (with FVG detection) now includes notification sounds for buy and sell alerts. This feature allows you to receive audio notifications when trading signals are generated based on Fair Value Gap (FVG) detection.

## Features

### 1. Notification Sounds Toggle
- **Location**: Indicator Settings Menu under "NOTIFICATION SOUNDS" section
- **Name**: "Notification Sounds"
- **Default**: Disabled (unchecked)
- **Purpose**: Enable or disable sound notifications for buy and sell alerts

### 2. Buy Alert Notifications (Bullish FVG)
When a bullish Fair Value Gap is detected (green triangle appears below the bar):
- **Sound**: Hand Bell 🔔
- **Trigger**: Plays when the candle closes and a bullish FVG is detected
- **Requirement**: "Notification Sounds" toggle must be enabled
- **Respects**: Size filters (if "Hide Large Bullish FVG" is enabled)

### 3. Sell Alert Notifications (Bearish FVG)
When a bearish Fair Value Gap is detected (red triangle appears above the bar):
- **Sound**: Fault ⚠️
- **Trigger**: Plays when the candle closes and a bearish FVG is detected
- **Requirement**: "Notification Sounds" toggle must be enabled
- **Respects**: Size filters (if "Hide Large Bearish FVG" is enabled)

## How to Use

### Step 1: Add the Indicator to Your Chart
1. Open TradingView
2. Add the "Big O" indicator to your chart
3. The indicator will display FVG boxes, triangles, and midlines

### Step 2: Enable Notification Sounds
1. Click on the indicator name in the chart
2. Select "Settings" (gear icon)
3. Find the "NOTIFICATION SOUNDS" section at the top
4. Check the "Notification Sounds" checkbox
5. Click "OK" to apply

### Step 3: Configure Alert Sounds (Optional)
For more control over your alerts, you can create custom alerts:

1. Click the "Alert" button (clock icon) in TradingView
2. Select "Create Alert"
3. Choose the Big O Indicator
4. Select either:
   - "Buy Alert - Hand Bell" for bullish FVG signals
   - "Sell Alert - Fault" for bearish FVG signals
5. In the alert settings:
   - For Buy Alerts: Select "Hand Bell" from the sound dropdown
   - For Sell Alerts: Select "Fault" from the sound dropdown
6. Configure other alert options as desired
7. Click "Create"

## Signal Conditions

### Bullish FVG (Buy Signal)
A bullish FVG is detected when:
- Current bar's low is higher than 2 bars ago high: `low > high[2]`
- Creates a gap indicating potential buying opportunity

Visual indicators:
- Green triangle below the bar
- Blue FVG box projected forward
- White 50% retracement line through the box
- Box turns green when price trades back into the FVG
- Box turns gray if FVG is invalidated (price closes below FVG bottom)

### Bearish FVG (Sell Signal)
A bearish FVG is detected when:
- Current bar's high is lower than 2 bars ago low: `high < low[2]`
- Creates a gap indicating potential selling opportunity

Visual indicators:
- Red triangle above the bar
- Orange FVG box projected forward
- White 50% retracement line through the box
- Box turns darker orange when price trades back into the FVG
- Box turns gray if FVG is invalidated (price closes above FVG top)

## Original Big O Indicator Features (Preserved)

All original functionality remains intact:
- **FVG Detection**: Bullish and Bearish Fair Value Gap detection
- **Visual Elements**: Triangles, boxes, midlines, broken open lines
- **Customization**:
  - Long/Short alert toggles
  - Customizable colors for all visual elements
  - FVG box projection length (1-400 bars)
  - FVG size filters to hide large gaps
- **Dynamic Updates**: FVG boxes change color when traded into or invalidated
- **Broken Open Lines**: White lines when price breaks through FVG levels

## Customization

The indicator includes several customizable parameters organized in sections:

**NOTIFICATION SOUNDS**
- Notification Sounds toggle (NEW)

**LONG ALERT**
- Long Alerts toggle
- Triangle color
- Broken line color
- FVG box colors (bullish, traded, invalid)
- FVG box projection length
- 50% retracement line color

**SHORT ALERT**
- Short Alerts toggle
- Triangle color
- Broken line color
- FVG box colors (bearish, traded, invalid)
- FVG box projection length
- 50% retracement line color

**FVG SIZE FILTER**
- Hide large bullish FVG toggle
- Max bullish FVG size (points)
- Hide large bearish FVG toggle
- Max bearish FVG size (points)

## Technical Notes

- Alerts are triggered once per bar close (`alert.freq_once_per_bar`)
- Sounds only play when:
  1. A valid FVG signal is detected
  2. The corresponding alert toggle is enabled (Long/Short Alerts)
  3. The "Notification Sounds" toggle is enabled
  4. FVG size filters don't exclude the signal
- The indicator uses Pine Script v6
- Original indicator functionality remains completely unchanged
- Uses advanced data structures (type FVGBox with arrays)

## Troubleshooting

**Q: I enabled notification sounds but don't hear anything**
- Ensure your device volume is turned up
- Check that TradingView has permission to play sounds in your browser
- Verify the "Notification Sounds" toggle is checked
- Verify that "Long Alerts" or "Short Alerts" are enabled
- Make sure you're on a timeframe where FVG signals are being generated
- Check if FVG size filters are excluding the signals

**Q: Can I change the sounds to something else?**
- In-script sounds are set to "Hand Bell" (buy) and "Fault" (sell)
- You can create custom alerts (Step 3 above) and choose any sound you prefer

**Q: Why do I see triangles but no sounds?**
- The "Notification Sounds" toggle must be enabled for sounds to play
- The corresponding "Long Alerts" or "Short Alerts" toggle must also be enabled
- Check that the `alert()` function calls are working in your TradingView environment

**Q: What happened to the simple MA/RSI indicator?**
- The Big O indicator is the original FVG-based indicator by Anthony Colajezzi
- Notification sounds have been added to the existing FVG detection logic
- All original features remain fully functional

## Version Information
- Pine Script Version: 6
- Original Author: Anthony Colajezzi
- Feature Added: Notification Sounds with toggle control
- Compatibility: TradingView charts with sound support
