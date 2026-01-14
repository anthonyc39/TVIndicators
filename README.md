# TVIndicators

A collection of Pine Script indicators for TradingView, created by Anthony Colajezzi.

## Indicators

### 1. BigO
The BigO indicator is an advanced trading indicator that detects bullish and bearish Fair Value Gaps (FVGs) and reversal patterns.

### 2. SessionLines
A Pine Script v6 indicator that plots horizontal lines for specific trading sessions.

#### Features:
- **Asia Session**: Plots high and low lines for the Asia trading session (default: 6:00 PM to 1:59:59 AM)
- **London Session**: Plots high and low lines for the London trading session (default: 2:00 AM to 6:59:59 AM)
- **New York (AM) Session**: Plots high and low lines for the New York morning session (default: 7:00 AM to 2:59:59 PM)

#### Customization Options:
- Enable/disable each session independently
- Customize colors for each session:
  - Asia Session: Teal (default)
  - London Session: Orange (default)
  - New York (AM) Session: Blue (default)
- Adjust session times (start/end hours and minutes)
- Configure line width (1-5 pixels)
- Choose line style (Solid, Dashed, or Dotted)

#### How to Use:
1. Copy the content of the `SessionLines` file
2. Open TradingView and go to the Pine Editor
3. Create a new indicator and paste the code
4. Save and add to your chart
5. Customize the settings in the indicator settings panel

#### Session Time Handling:
The indicator properly handles sessions that cross midnight (e.g., Asia session starting at 6:00 PM and ending at 1:59 AM the next day).

## Installation

These indicators are Pine Script files that can be used directly in TradingView:

1. Open the indicator file in this repository
2. Copy the entire contents
3. Go to TradingView and open the Pine Editor
4. Create a new indicator
5. Paste the code
6. Save and add to your chart

## License

Created by Anthony Colajezzi.
