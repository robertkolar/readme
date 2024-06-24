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
- Instrument filtering by underlying symbol root, instrument symbol, security type, currency, multiplier
- Option chain filtering by symbol root, expiration from/to, right - put/call/none, strike from/to

### Technology Stack
- Backend: Java 21+, Spring WebFlux 3+, Project Reactor, RSocket, WebSockets, Hazelcast, Hibernate/JPA, PostgreSQL
- Frontend: Angular v18+, Angular Material
- DevOps/deployment: GitHub + Actions, AWS EC2 + VPC + ECR, Ubuntu, Docker

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
- underlying symbol root
- symbol of the trading instrument
- security type - futures option, future, option, stock, cfd
- option or future expiration date
- option right, put/call
- option strike
- bid size/price
- ask size/price
- last size/price
- order source - underlying, position, option chain, delta hedge
- order id
- order permId
- order action - buy, sell
- order quantity
- order limit price
- fill price
- commission paid
- order heartbeat
- order ib status - submitted, filled, canceled

### Option Position Fields
- underlying symbol root
- option or future expiration date
- dte - days to expiration
- option right - put/call
- option strike
- position size
- margin requirement for the position
- profit/loss for the position
- percentage distance to the at-the-money strike
- intrinsic value points of the position contract
- time value points of the position contract
- intrinsic value of the position
- time value of the position
- time value percentage yield
- delta of the position contract
- position delta
- position gamma
- position theta
- option model price
- bid size/price
- ask size/price
- daily traded volume
- option open interest
- previous day close
- option implied volatility

### Order History Fields
- record id
- order submit date
- underlying symbol root
- symbol of the trading instrument
- security type - futures option, future, option, stock, cfd
- instrument currency
- trading exchange - e.g. cme, cbot, nymex, comex
- instrument multiplier
- order source - underlying, position, option chain, delta hedge
- order permId
- order action - buy, sell
- order quantity
- order limit price
- fill price
- commission paid
- order status date
- order ib status - submitted, filled, canceled

### Delta Hedge Fields
- delta hedge event id
- delta hedge event date
- underlying symbol root
- symbol of the trading instrument
- security type - futures option, future, option, stock, cfd
- instrument currency
- instrument multiplier
- delta hedge algo parameters
- underlying last price
- group delta
- group delta average
- delta hedge threshold
- threshold break
- delta hedge triggered
- trading time condition met
- time between orders condition met
- position size condition met
- delta hedge order action - buy, sell
- delta hedge order quantity
- delta hedge order id

### Underlying Snapshot Fields
- snapshot id
- snapshot date
- underlying symbol root
- symbol of the trading instrument
- instrument currency
- instrument multiplier
- underlying last price
- number of puts short
- number of puts long
- number of calls short
- number of calls long
- portfolio delta per 1% price change of the underlying
- portfolio gamma per 1% price change of the underlying
- combined portfolio delta per underlying
- group delta/average for the underlying group of symbols
- combined portfolio theta per underlying
- sum of option positions intrinsic values per underlying
- sum of option positions time values per underlying
- total unrealized profit/loss per underlying
- allocation percentage calculated from the margin requirements of the open option positions

### Option Chain Fields
- underlying symbol root
- symbol of the option instrument
- security type - futures option, option
- option expiration date
- dte - days to expiration
- option right - put/call
- option strike
- percentage distance to the at-the-money strike
- intrinsic value points of the option contract
- time value points of the option contract
- time value percentage yield
- option delta
- option model price
- bid size/price
- ask size/price
- last size/price
- daily traded volume
- option open interest
- previous day close
- daily percentage change
- option implied volatility

# Trade Analytics
- Trade analytics for options, futures, futures options, stocks and other instruments
- Statistics calculation interval - days, weeks, months, years
- Executions/Trades filtering by symbol root, symbol, security type, option right, currency, instrument multiplier
- Statistics filtering by symbol root, symbol, security type, option right, currency, multiplier, trade type, interval

### Technology Stack
- Backend: Java 21+, Spring WebFlux 3+, Project Reactor, RSocket, WebSockets, Hazelcast, Hibernate/JPA, PostgreSQL
- Frontend: Angular v18+, Angular Material
- DevOps/deployment: GitHub + Actions, AWS EC2 + VPC + ECR, Ubuntu, Docker

### Executions Fields
- execution id
- fill date
- execution reference
- execution action - buy, sell
- quantity traded
- underlying symbol root
- symbol of the instrument traded
- security type - futures option, future, option, stock, cfd
- underlying security type - future, stock
- option right - put/call
- instrument currency
- instrument multiplier
- fill price
- option intrinsic value
- proceeds in the currency of the instrument traded
- option time value
- instrument notional value - stock, futures
- trade id

### Trades Fields
- trade id
- trade type - long, short
- underlying symbol root
- symbol of the instrument traded
- security type - futures option, future, option, stock, cfd
- option right - put/call
- instrument currency
- instrument multiplier
- cumulative quantity traded
- last position size
- trade open date
- trade close date
- trade cumulative open price
- trade cumulative close price
- trade points sum
- traded proceeds sum
- trade time value sum
- trade notional value sum
- closed trade profit/loss
- number of trade executions
- trade status

### Statistics Fields
- statistics id
- number of executions for the period
- number of open trades
- number of closed trades
- number of winners
- number of losers
- percentage of winners
- biggest winner
- biggest loser
- winners profit
- losers loss
- proceeds bought
- proceeds sold
- proceeds sum
- time value bought
- time value sold
- time value sum
- profit/loss for the period
- profit/loss percent for the period
- profit/loss for the tax report
- cumulative profit/loss