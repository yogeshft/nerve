# Understandings on Futures, Options, and Option Chain

Based on your raw notes, cleaned and expanded for beginner understanding.

---

## 1) First understand the full picture

In F&O, you usually deal with 3 things:

### A. Spot / Cash Market
This is the actual current market price of the stock or index.

Example:
If NIFTY is trading at **23828.55**, that is the **spot price**.

### B. Futures
A futures contract is a promise with obligation.

You agree to buy or sell something later at a price decided now.

- If you **buy futures**, you expect price to go **up**
- If you **sell futures**, you expect price to go **down**
- Futures use **margin**
- Profit and loss can be **large**
- Many traders exit before expiry

**Easy meaning:**  
**Futures = direct bet on direction with margin**

### C. Options
An option is a **right**, not a compulsion, for the buyer.

Two types:

- **Call option** = bet that price will go **up**
- **Put option** = bet that price will go **down**

In options:

- **Buyer** pays premium and has limited loss
- **Seller** receives premium but can have large risk

**Easy meaning:**  
**Options = you buy or sell a contract whose value changes with the stock/index**

---

## 2) Important words you must know first

### Underlying
The stock, index, or commodity on which the contract is based.

Examples:
- NIFTY
- BANKNIFTY
- Reliance
- Gold

### Contract
A contract is just a tradable agreement.

In F&O, you are usually not trading the actual stock itself.  
You are trading a **contract linked to that stock/index**.

### Expiry
Every futures/options contract has an **expiry date**.

That means the contract cannot live forever.

### Lot Size
F&O contracts are traded in **lots**, not random 1-share quantities.

So actual profit/loss is usually:

**points x lot size**

### Premium
Premium is the **price of the option**.

Very important:
**LTP in option chain = option premium, not spot price**

### Margin
Margin is money blocked by broker/exchange to allow you to trade bigger contracts.

Think of it as a **security deposit**.

Important:
- Margin is **not profit**
- Margin is **not the contract value**
- Margin is money blocked to cover possible losses

If your loss becomes large, broker may ask for more margin. That is called a **margin call**.

---

## 3) What is futures trading?

A futures contract is a trade where both sides have obligation.

### Example:
Suppose NIFTY futures is trading at **23850**.

You **buy** 1 futures contract because you think NIFTY will rise.

### Case 1:
NIFTY futures goes to **23950**
- profit = **100 points x lot size**

### Case 2:
NIFTY futures falls to **23750**
- loss = **100 points x lot size**

### Important points:
- Futures does **not** have premium like options
- It uses **margin**
- Both profit and loss move almost directly with price
- Risk is bigger than option buying because losses can grow fast

**One-line memory:**  
**Long futures = bullish**  
**Short futures = bearish**

---

## 4) What is margin trading?


### In simple cash market language
Margin trading means you use your own money plus borrowed money from broker to take a bigger trade.

Example:
- You have Rs 10,000
- Broker allows 5x exposure
- You trade Rs 50,000 worth

### In derivatives language
In futures and option selling, margin means **blocked money to support the contract**.

So in F&O:
- margin is not exactly "free borrowed money"
- it is more like **required capital to hold the position**

### Very important difference:
- **Cash margin trading** = borrowed buying power
- **Futures/option selling margin** = blocked security deposit

---

## 5) What is option trading?

Options trading means buying or selling contracts that are based on an underlying asset.

You do **not** usually trade the actual stock/index directly.  
You trade the **right** related to it.

There are 2 option types:

### Call Option (CE)
Gives the buyer the right to **buy**

Used when you think the market will go **up**

**Easy memory:**  
**Buy Call = bullish**

### Put Option (PE)
Gives the buyer the right to **sell**

Used when you think the market will go **down**

**Easy memory:**  
**Buy Put = bearish**

---

## 6) Who are the 4 basic option players?

### 1. Call Buyer
- Expects price to go up
- Pays premium
- Max loss = premium paid

### 2. Call Seller
- Usually expects price to stay below strike or not rise much
- Receives premium
- Risk can be large

### 3. Put Buyer
- Expects price to go down
- Pays premium
- Max loss = premium paid

### 4. Put Seller
- Usually expects price to stay above strike or not fall much
- Receives premium
- Risk can be large

**Best beginner rule:**  
**Option buyer = limited loss**  
**Option seller = limited income, larger risk**

---

## 7) What exactly do we trade in options?

You trade **contracts**, not the actual stock or index.

For example:
You are not buying "NIFTY" directly in option trading.  
You are buying:

- NIFTY 23900 CE
- NIFTY 23900 PE
- NIFTY 24000 CE
- etc.

These are all different contracts.

---

## 8) What is an option chain?

An option chain is a live table showing all available option contracts for one underlying.

Example:
For NIFTY, the chain shows many strike prices like:
- 23600
- 23650
- 23700
- 23850
- 23900
- 24000
and so on

For every strike, the chain shows:
- Call data
- Put data
- Greeks
- OI
- LTP
- IV

**Easy meaning:**  
**Option chain = full menu of all option contracts**

---

## 9) How to read the option chain layout

In most dashboards:

### Left side
**CALL data**

### Middle
**Strike price** and sometimes **IV**

### Right side
**PUT data**

So every row means:

**Call of this strike | Strike | Put of this strike**

---

## 10) Strike price vs spot price vs futures price

This is one of the biggest confusions.

### Spot Price
Current real market price of the stock/index right now.

Example:  
NIFTY spot = **23828.55**

### Strike Price
Fixed contract level used in option.

Example:  
23900 strike means the contract is built around 23900.

### Futures Price
Current price of the futures contract.

This may be slightly different from spot.

### Quick memory:
- **Spot** = live market price now
- **Strike** = fixed option contract level
- **Futures price** = current futures contract price

---

## 11) LTP

### LTP = Last Traded Price

In option chain, this means the **premium of that option**.

Example:  
If 23900 CE LTP is **176.40**, that means the option premium is 176.40.

It does **not** mean NIFTY is 176.40.

**Easy memory:**  
**LTP in option chain = option price**

---

## 12) OI

### OI = Open Interest

Open Interest tells how many contracts are still open in the market.

**Easy meaning:**  
It shows how crowded a strike is.

- High OI = lots of traders have positions there
- Low OI = less activity

### Practical use:
Traders often look at:
- high **Call OI** as possible resistance
- high **Put OI** as possible support

But remember:
**OI is a clue, not a guarantee**

---

## 13) Volume vs OI

### Volume
How many contracts traded today

### OI
How many contracts are still open right now

### Easy difference:
- **Volume** = today's activity
- **OI** = open positions still alive

---

## 14) IV

### IV = Implied Volatility

This tells how much movement the market is expecting.

**Easy meaning:**  
Higher IV means options become more expensive.

**Memory:**  
**IV up -> premium usually up**  
**IV down -> premium usually down**

---

## 15) Moneyness: ITM, ATM, OTM

This is very important for reading strikes.

Suppose spot price is:

**NIFTY = 23828.55**

Then nearby strikes are:
- 23800
- 23850
- 23900

### ATM = At The Money
Strike closest to spot

Here:
- **23850** is near ATM

### For Call Options
- Strike **below spot** = ITM
- Strike **near spot** = ATM
- Strike **above spot** = OTM

Example with spot 23828.55:
- 23800 CE = ITM
- 23850 CE = ATM-ish
- 23900 CE = OTM

### For Put Options
Opposite of calls:
- Strike **above spot** = ITM
- Strike **near spot** = ATM
- Strike **below spot** = OTM

Example:
- 23900 PE = ITM
- 23850 PE = ATM-ish
- 23800 PE = OTM

---

## 16) Why ITM options are usually more expensive

Because they already have some "real value".

Example:
If spot is 23828.55, then 23900 PE already has value because the strike is above spot.

That real value is called **intrinsic value**.

---

## 17) Intrinsic value and time value

Option premium has 2 parts:

**Premium = Intrinsic Value + Time Value**

### Intrinsic Value
The real in-the-money value

Example:  
Spot = 23828.55

For **23900 PE**:

Intrinsic value = 23900 - 23828.55 = **71.45**

So this put already has real value of 71.45.

### Time Value
Extra value because time is still left before expiry

If premium is larger than intrinsic value, the extra part is time value.

**Easy meaning:**
- intrinsic value = real value now
- time value = possibility of future movement

---

## 18) Greeks simplified

Greeks tell you how option premium changes.

Do not think of them as scary formulas.  
Think of them as **behavior indicators**.

### Delta = movement power

Delta tells how much option premium changes when the underlying moves by 1 point.

Example:  
If Call Delta = **0.50** and NIFTY goes up by 10 points, option premium may rise by around **5 points**.

**Easy memory:**  
**Delta = engine**

For calls:
- Delta is positive

For puts:
- Delta is negative

ATM options usually have delta near:
- Call: around **0.5**
- Put: around **-0.5**

### Theta = time decay

Theta tells how much premium melts with passing time.

Example:  
If Theta = **-2**, then option may lose about 2 points per day, even if market does not move much.

**Easy memory:**  
**Theta = thief**

This is why option buying is difficult if the market moves slowly.

Important:
- option buyers suffer from theta
- option sellers benefit from theta

### Vega = volatility effect

Vega tells how much option premium changes when IV changes.

Example:  
If Vega = 10, and IV rises by 1, premium may rise by around 10 points.

**Easy memory:**  
**Vega = mood / fear / excitement**

Before big events, IV can go up.

### Gamma = delta booster

Gamma tells how fast delta changes when price moves.

This is more advanced, but simple meaning is:

**Gamma tells how quickly your option becomes more reactive**

**Easy memory:**  
**Gamma = accelerator for delta**

For beginners, gamma is not the first thing to master.

Focus first on:
- spot
- strike
- LTP
- OI
- delta
- theta

---

## 19) Break-even in option buying

This is important.

### Call Buyer Break-even
**Strike + Premium**

Example:  
Buy 23900 CE at 176.40

Break-even at expiry:  
23900 + 176.40 = **24076.40**

That means at expiry, NIFTY must go above 24076.40 for net profit, ignoring charges.

### Put Buyer Break-even
**Strike - Premium**

Example:  
Buy 23900 PE at 236.50

Break-even at expiry:  
23900 - 236.50 = **23663.50**

That means at expiry, NIFTY must go below 23663.50 for net profit, ignoring charges.

---

## 20) Real example using a NIFTY dashboard

Suppose the dashboard shows:

- Spot = **23828.55**
- 23900 CE LTP = **176.40**
- 23900 PE LTP = **236.50**

### Example A: Buy 23900 CE
You are saying:  
"I think NIFTY will go up."

- You pay premium = 176.40
- Max loss = 176.40 x lot size
- Break-even = 24076.40
- If NIFTY does not rise enough, premium can melt due to theta

### Example B: Buy 23900 PE
You are saying:  
"I think NIFTY will go down."

- You pay premium = 236.50
- Max loss = 236.50 x lot size
- Break-even = 23663.50
- This benefits when NIFTY falls

---

## 21) Why call and put premiums move opposite sometimes

If market falls:

- call premiums usually go down
- put premiums usually go up

That is why on a bearish day:
- many call LTPs are red
- many put LTPs are green

Because NIFTY itself is down.

---

## 22) How to read the dashboard in 30 seconds

Whenever you open the option chain, read it in this order:

### Step 1
Check the **underlying**  
Example: NIFTY

### Step 2
Check the **expiry**  
Example: 13 Apr 2026

### Step 3
Check the **spot price**  
Example: 23828.55

### Step 4
Find the **ATM strike**  
Example: around 23850

### Step 5
Look at the call option price and put option price near the at-the-money strike

### Step 6
Look at OI near important strikes

### Step 7
Look at Delta and Theta

### Step 8
Then look at IV and Vega

That is enough for a beginner.

---
## 23) Price alerts simplified

### Active alerts
Alerts that are still waiting for price/condition to hit

### Triggered alerts
Alerts where the condition has already hit

### Possible alert categories
1. stocks (price and quantity)
2. symbols (price)
3. options (price,quantity and geeks)


---

## 24) Best beginner summary of futures vs options

### Futures
- direct directional trade
- uses margin
- no premium
- profit/loss moves almost directly with price
- risk can be large on both sides

### Options buying
- pay premium
- right, not obligation
- max loss limited to premium
- needs correct direction + enough move + enough time

### Options selling
- receive premium
- margin required
- theta helps
- risk can be large

---


## 25) Left side vs right side of the option chain

The option chain is like a mirror:

### Left side
**Call (CE) data**

Look at this side when you think the market may go **up**.

### Right side
**Put (PE) data**

Look at this side when you think the market may go **down**.

### Easy way to remember
- left side = bullish side
- right side = bearish side

---

## 26) What the shading means: ITM vs OTM

Some rows are darker and some are lighter. This is a quick visual clue for **moneyness**.

### Dark shaded rows
These are **In-The-Money (ITM)** options.  
That means they already have some intrinsic value.

### Light shaded rows
These are usually **Out-Of-The-Money (OTM)** options.  
That means they do not yet have intrinsic value.

### Using the spot example 23828.55
- on the **Call side**, strikes below **23828** are ITM
- on the **Put side**, strikes above **23828** are ITM

So the darker area is not random. It shows which strikes are already in-the-money based on the current market price.

---

## 27) Reading a single row: strike 23900 example

When you look at one row in the option chain, each value tells you something different about that strike.

| Column | Value | What it means in plain English |
| --- | --- | --- |
| LTP (Call) | 176.40 | To buy an "up" bet at 23900, you must pay **Rs176.40** per share. |
| OI (Call) | 59.55L | About **59.55 lakh** open contracts exist at this strike on the call side. |
| Delta (Call) | 0.48 | If NIFTY moves up by **Rs1**, this option price may move up by about **Rs0.48**. |
| Theta (Call) | -25 | This option loses about **Rs25** in value over time, even if price does not move. |
| LTP (Put) | 236.50 | To buy a "down" bet at 23900, you pay **Rs236.50** per share. |

This is the easiest way to read one row:
- **LTP** tells you the current option price
- **OI** tells you how many positions are open
- **Delta** tells you how fast the option reacts to price change
- **Theta** tells you how time decay is hurting the option buyer
