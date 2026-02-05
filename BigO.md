# Big O Notation in TV Indicators

## Overview
Big O notation is used to describe the performance or complexity of an algorithm. In the context of TV Indicators, this refers to the efficiency of various algorithms used to analyze and display trading indicators.

The "Big O" indicator by Anthony Colajezzi detects Fair Value Gaps (FVGs) in price action and provides visual alerts for potential trading opportunities.

## Latest Updates

### Enhanced Notification and Alerting System
The Big O Indicator now includes an enhanced notification system with sound alerts:

- **Notification Sounds Toggle**: Enable/disable sound notifications in indicator settings (default: disabled)
- **Buy Alert Sounds**: "Hand Bell" sound plays when bullish FVG signals are generated (green triangle + FVG box)
- **Sell Alert Sounds**: "Fault" sound plays when bearish FVG signals are generated (red triangle + FVG box)
- **Alert Conditions**: Sounds trigger only when the candle closes, the "Notification Sounds" toggle is enabled, and the corresponding Long/Short alert is active
- **Size Filter Integration**: Sounds respect FVG size filters (won't play for filtered-out signals)

See [NOTIFICATION_SOUNDS_GUIDE.md](NOTIFICATION_SOUNDS_GUIDE.md) for detailed usage instructions.

## Original Big O Indicator Features

The Big O indicator (v6) provides comprehensive Fair Value Gap analysis:

### Core Features
- **Bullish FVG Detection**: Identifies gaps where `low > high[2]`
- **Bearish FVG Detection**: Identifies gaps where `high < low[2]`
- **Visual Boxes**: Projects FVG zones forward with customizable colors
- **50% Retracement Lines**: Marks the midpoint of each FVG
- **Dynamic Updates**: Boxes change color when price trades back into the FVG
- **Invalidation Logic**: Boxes turn gray when FVG is invalidated
- **Broken Open Lines**: White lines appear when price breaks through FVG levels

### Customization Options
- Toggle Long/Short alerts independently
- Customize all colors (triangles, boxes, lines)
- Adjust FVG box projection length (1-400 bars)
- Filter large FVGs by size (points)
- Up to 500 boxes and 500 lines on chart

## Modifications and Add-ons
### Detailed Notification and Alerting Schema
Integrated instructions for detailed notification and alerting schema defined by sound toggling inputs. Users can now receive alerts based on specific trading conditions and can configure the toggling of sounds to represent different signals.

1. **Notification Types**: Users can set alerts for FVG detection, including bullish and bearish Fair Value Gaps.
2. **Sound Toggling Inputs**: Users have the ability to toggle sound notifications on or off for each alert type, providing customization based on personal preferences.
   - Sound On: Alerts will notify with sound.
   - Sound Off: Alerts will notify without sound.

## Conclusion
The improvements to the alerting schema allow for a more versatile and user-friendly experience when utilizing trading indicators. All original Big O indicator functionality remains intact while adding optional sound notifications for enhanced awareness.