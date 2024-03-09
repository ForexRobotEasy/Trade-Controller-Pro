# Trade Controller Pro

Trade Controller Pro is a software developed by the Forex Robot Easy Team. It is designed to enhance trading by providing risk management features. This program can be used in the MetaTrader platform.

## How it Works

The Trade Controller Pro program is written in MQL5 language and consists of several functions and variables. Let's go through each part of the code to understand how it works.

### Importing Necessary Libraries

The program starts by importing necessary libraries for trading operations. These libraries include Trade, PositionInfo, SymbolInfo, and AccountInfo.

### Global Variables

The code declares global variables for trading operations. These variables include CTrade, CPositionInfo, CSymbolInfo, and CAccountInfo objects. These objects are used to perform various trading functions and obtain information about positions, symbols, and account details.

### Risk Percentage Calculation

The code includes a function named `CalculateRiskPercentage` that calculates the risk percentage based on the stop loss and balance. It uses the `Equity` and `MarginFree` methods of the `CAccountInfo` object to obtain the necessary information. The calculated risk percentage is then returned.

### Profit Calculation

The code includes a function named `CalculateProfit` that calculates the profit based on the PIPs and trade volume. It uses the `Point` method of the `CSymbolInfo` object to obtain the PIP value. The calculated profit is then returned.

### Closing Trades for a Specific Symbol

The code includes a function named `CloseAllTradesForSymbol` that closes all open or pending trades for a specific symbol. It uses the `Total` and `SelectByIndex` methods of the `CPositionInfo` object to loop through all positions. If the position symbol matches the specified symbol, the `PositionClose` method of the `CTrade` object is used to close the position.

### Closing All Trades

The code includes a function named `CloseAllTrades` that closes all open or pending trades. It also uses the `Total` and `SelectByIndex` methods of the `CPositionInfo` object to loop through all positions. The `PositionClose` method of the `CTrade` object is used to close each position.

### Entry Point and Initialization

The code includes an `OnInit` function that serves as the entry point of the program. It initializes the `CTrade`, `CPositionInfo`, `CSymbolInfo`, and `CAccountInfo` objects. The expert name is set as 'Trade Controller Pro'. The `Refresh` methods of the objects are used to update their information. The function returns `INIT_SUCCEEDED` to indicate successful initialization.

### Main Program Loop

The code includes an `OnTick` function that serves as the main program loop. It is executed on every tick of the symbol. The function starts by obtaining the bid and ask prices using the `Bid` and `Ask` methods of the `CSymbolInfo` object. It then calculates the spread in pips using the `Spread` and `Point` methods. The calculated values can be displayed in a dashboard or used for further analysis.

Next, the function calculates the risk percentage using the `CalculateRiskPercentage` function. It sets a predefined stop loss value and obtains the balance from the `CAccountInfo` object. The calculated risk percentage can be used for risk management purposes.

The function also calculates the profit based on predefined PIPs and trade volume using the `CalculateProfit` function. The calculated profit can be used for profit calculation and analysis.

The function includes an example of closing all open or pending trades for a specific symbol with a single click. It calls the `CloseAllTradesForSymbol` function and specifies the symbol to close. This can be useful for managing positions for a specific symbol.

Lastly, the function includes an example of closing all open or pending trades altogether with a single click. It calls the `CloseAllTrades` function to close all positions. This can be useful for closing all positions at once.

### Program Termination

The code includes an `OnDeinit` function that is executed when the program terminates. It can be used to perform necessary cleanup operations. The `reason` parameter indicates the reason for termination.

## Product Description

Trade Controller Pro is a powerful risk management software developed by the Forex Robot Easy Team. It enhances trading by providing features to manage risk and calculate profit. With Trade Controller Pro, traders can effectively monitor their trades, calculate risk percentages, and close positions with ease.

This software is designed to work with the MetaTrader platform and can be used by both beginner and experienced traders. It offers a user-friendly interface and intuitive controls, making it easy to navigate and utilize its features.

Trade Controller Pro allows traders to calculate risk percentages based on stop loss and account balance. This helps traders make informed decisions and manage their risk effectively. Additionally, the software provides a profit calculation feature that allows traders to determine their potential profit based on PIPs and trade volume.

One of the key features of Trade Controller Pro is the ability to close all open or pending trades for a specific symbol with a single click. This saves time and simplifies the process of managing positions for a particular symbol. Traders can also close all open or pending trades altogether with a single click, providing a convenient way to exit multiple positions simultaneously.

To learn more about this product, including detailed reviews and trading results, visit the official website of Forex Robot Easy at [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/trade-controller-pro-review-enhance-trading-with-risk-management-software/). Please note that ForexRobotEasy is not the official developer of this product. The provided code is a sample that demonstrates how the product works. For information about the official developer, please refer to the MQL5 platform.
