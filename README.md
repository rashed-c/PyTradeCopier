# Trading Application

A robust PyQt5-based desktop application for real-time trading with Databento market data integration, take-profit management, and automated trade execution.

## Features

- Real-time market data streaming through Databento API
- Advanced order management system
- Multiple take-profit levels with automated execution
- Dynamic stop-loss management (Fixed, Trailing, Break-even)
- Support for both micro and mini futures contracts
- Historical data replay mode for backtesting
- OHLCV-1m data archiving capability
- ATR-based stop loss calculations
- Customizable trade timer with automatic actions

### Supported Instruments
- Micro E-mini S&P 500 (MES)
- Micro E-mini Nasdaq-100 (MNQ)
- Micro Gold (MGC)
- Micro Crude Oil (MCL)
- E-mini S&P 500 (ES)
- E-mini Nasdaq-100 (NQ)
- Gold Futures (GC)
- Crude Oil Futures (CL)

## Requirements

```
Python 3.x
PyQt5
requests
databento
pandas
pytz
```

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd trading-app
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Set up your configuration:
   - Create a `settings.json` file with your API credentials
   - Configure your Databento API key
   - Set up your webhook URL for order execution

## Configuration

Create a `settings.json` file with the following structure:
```json
{
    "api_url": "your-webhook-url",
    "databento_key": "your-databento-key",
    "archive_key": "your-archive-key",
    "atr_period": 14,
    "atr_lookback": 390
}
```

## Usage

1. Start the application:
```bash
python trading_app.py
```

2. Select your trading instrument and contract type (Micros/Minis)

3. Configure your trade parameters:
   - Quantity
   - Stop Loss amount and type
   - Take Profit levels
   - Break-even settings

4. Use the trading buttons to:
   - Enter long positions (BUY)
   - Enter short positions (SELL)
   - Exit all positions (EXIT ALL)
   - Manage individual take-profit exits

## Features in Detail

### Stop Loss Types
- **Market**: Standard stop loss order
- **Limit**: Stop limit order
- **Trailing**: Dynamic trailing stop
- **Trail after 1st TP**: Converts to trailing stop after first take-profit hit

### Take Profit Management
- Multiple TP levels with individual quantity settings
- Automatic execution at target prices
- Break-even stop loss automation after first TP hit

### Price Data
- Real-time streaming through Databento
- Historical data replay mode for testing
- OHLCV-1m data archiving
- ATR-based volatility calculations

### Trade Management
- Position sizing
- Trade timer with automatic actions
- Trade reversal capability
- Break-even automation

## Advanced Features

### ATR-Based Stop Loss
- Dynamic stop loss calculation based on Average True Range
- Customizable ATR period and multiplier
- Automatic updates based on market volatility

### Historical Replay Mode
- Test strategies with historical data
- Configurable date range
- Simulated real-time price updates

### Data Archiving
- Automated OHLCV-1m data storage
- Continuous data collection
- Local file management

## Error Handling

The application includes comprehensive error handling for:
- Network connectivity issues
- API communication errors
- Invalid user inputs
- Data stream interruptions

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Databento for market data API
- PyQt5 for the GUI framework
- All contributors and users of the application

## Support

For support, please:
1. Check the existing issues
2. Create a new issue with detailed information about your problem
3. Include relevant log files and screenshots

---

**Note**: This application requires valid API credentials and appropriate market data subscriptions to function properly. Please ensure all necessary accounts and permissions are set up before using the application.