---
weight: 3
draft: false
toc: false
title: "What is the Midmarket Rate?"
description: "Explanation of midmarket rate calculation"
---

### Market
The values returned by our API refer to the average midmarket rate available from different sources in real time.
Being a normal financial market, each currency exchange has sellers and buyers (e.g. if the pair is EUR/USD, there is
someone who wants to sell EUR in exchange for USD and someone who wants to buy EUR using USD).

Taking the EUR/USD exchange rate as an example, we therefore have two prices at any given time, the Bid Price (the maximum
USD amount that any entity is willing to pay for EUR in the given moment) and the Ask Price (the minimum USD amount that
any entity is willing to receive to sell EUR in the given moment).
When the prices of the buyer and of the seller coincide, the actual financial transaction on the broker takes place.

At any given time, the two price values may have some difference, called spread, and to try to return the most
representative value, we decided to use the midmarket rate in our APIs, which is nothing but the average between
the Bid price and the Ask price.

| Bid Price | Ask Price | Midmarket Rate |
|:---------:|:---------:|:--------------:|
|  1.7908   |  1.7910   |     1.7909     |
|  1.7907   |  1.7908   |    1.79075     |

### Decentralization
The forex market is decentralized and therefore is open 24 hours a day, because there is no single source that returns all
current prices on worlwide currency exchange, but instead there are many brokers each independent of the other.

This is also why today it's virtually impossible to get reliable data in real time, if it's necessary to check
hundreds of different data, each in a different format.

Indeed, it isn't enough to take the midmarket rate exclusively from one source and trust it blindly; to get a value
as accurate as possible, it's necessary to aggregate several midmarket rate values into one, making a weighted average
of them.

| Midmarket Rate Provider 1 | Midmarket Rate Provider 2 | Average Midmarket Rate |
|:-------------------------:|:-------------------------:|:----------------------:|
|          1.79075          |          1.79077          |        1.79076         |
|           1.79            |           1.791           |         1.7905         |

### Outliers filtering
Not all price values taken from different providers are equally reliable.
If a broker has a low volume of transactions at a certain time, for example, it is very likely that its value
will deviate from what the actual forex market prices are.

If we want to get an accurate result, we cannot afford to include these prices that don't meet current
market values (outliers) and we must therefore do what we can to identify and eliminate them from our
calculations, using the data available to us (not only the raw midmarket rates).

| Midmarket Rate Provider 1 | Midmarket Rate Provider 2 |  Midmarket Rate Provider 3  | Average Midmarket Rate |
|:-------------------------:|:-------------------------:|:---------------------------:|:----------------------:|
|           1.79            |          1.7905           |          ~~1.803~~          |        1.79025         |

### It's... difficult
> After seeing how complicated it's to handle all this properly on your own, we can tell you that you won't have to worry
about these details... because we already do.
