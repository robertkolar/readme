# Options Trader
- Options trading decision support, risk management and execution system
- Trading equity options, index options, futures options or underlying instruments
- Optimized for options writing delta neutral strategies
- Tick by tick calculation of all relevant risk metrics and option/portfolio Greeks
- Compact web based UI presenting all information in a condensed form
- Realtime update of all information utilizing message queues and websocket technologies
- Predefined risk parameters per underlying like min/max delta
- Automated delta hedging with the underlying futures instruments
- Placing opening/closing option orders from the UI with one click
- Option chains for the underlying, updating on tick by tick basis

### Underlying Fields
- symbol and expiration of the underlying futures contract
- current underlying position
- profit/loss for the open underlying position
- bid size/price
- ask size/price
- last price
- daily traded volume
- daily price change percentage
- option implied volatility for the underlying
- option historical volatility for the underlying
- option volume for the underlying
- option open interest for the underlying
- number of open short put contracts per underlying
- number of open short call contracts per underlying
- portfolio delta per 1% price change of the underlying
- portfolio gamma per 1% price change of the underlying
- combined portfolio delta per underlying
- group delta/average for the underlying group of symbols
- combined portfolio gamma per underlying
- combined portfolio vega per underlying
- combined portfolio theta per underlying
- sum of option positions intrinsic values per underlying
- sum of option positions time values per underlying
- total unrealized profit/loss per underlying
- allocation percentage calculated from the margin requirements of the open option positions

### Order Fields
- TBD

### Position Fields
- TBD

### Option Chain Fields
- TBD

# Trade Analytics
- Trade analytics for options, futures, futures options, stocks and other instruments

