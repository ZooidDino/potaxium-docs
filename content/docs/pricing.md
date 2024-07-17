---
weight: 2
draft: false
toc: false
icon: "sell"
title: "Pricing"
description: "Check our pricing model"
---

### Partner
We collaborate with RapidAPI to easily provide our API service to end users, and subscription management and monthly
payment are handled directly by them.

### Subscribe
If you would like to subscribe to a customized plan, please email us directly at [support@potaxium.com](mailto:support@potaxium.com),
and we will try to get back to you as soon as possible.

However, if you just want a regular subscription, click on the corresponding link in the next table, and you will be redirected
to the RapidAPI website to make the subscription.

### Plans
{{< table "table-striped table-responsive" >}}
|                       |   Free               |  Minimal   |  PRO     | Business | Custom |
|:----------------------|:--------------------:|:--------:|:--------:|:--------:|:------:|
| Price/month           | `$0.00`              | `$7.50`  | `$25.99` | `$59.99` |   |
|                       | [Subscribe](https://rapidapi.com/ErikPelli/api/potaxium-forex-data) | [Buy](https://rapidapi.com/ErikPelli/api/potaxium-forex-data) | [Buy](https://rapidapi.com/ErikPelli/api/potaxium-forex-data) | [Buy](https://rapidapi.com/ErikPelli/api/potaxium-forex-data) | [Contact us](/docs/support)
| Monthly HTTP Requests | 500 | 25,000 | 400,000 | 1,200,000 | Infinite |
| HTTPS                 | Yes | Yes    | Yes     | Yes       | Yes      |
| Rate Limit            | 50 requests/minute   | 100 requests/minute  | No | No | No |
| Commercial Use        | No                   | Yes | Yes | Yes | Yes |
| Refresh Period `*`    | 3 hours              | 30 minutes | 1 minute | Instant | Instant |
| Technical Support `**`    |                  | Email | Email | Email | Custom group chat |
| Rate History API `***`    |                  | Yes | Yes | Yes | Yes | 
| Asset Conversion API      |                  |     | Yes | Yes | Yes |
| SLA `****`                |                  |     | API (`99.9%`)  | API (`99.9%`) | API & custom asset pairs (`99.99%`)
| Custom Features           |                  |     |     |     | Contact us |
| Websocket Updates `*****` |                  |     |     |     | Contact us |
{{< /table >}}

`*` Refresh Period is the time period between each update of conversion rate data; if the plan is *BUSINESS* or *CUSTOM*,
    the value is calculated in realtime for each API request using currently available data

`**` Since payment and subscriptions aren't handled by us in plans different from the custom one, we can't directly help
     you with this kind of problem, but we are happy to solve your technical issues

`***` Historical data APIs don't contain all the assets available in the Realtime APIs, and some values may be missing
      for some dates in the past

`****` In the custom plan it's possible to agree on a Service Level Agreement on individual forex pairs used by the
      customer, for real-time rates, to make sure the API will always have them available and with the correct values

`*****` In the custom plan it's possible to ask for a websocket that returns realtime rates updates for a specific
       assets pair

### Different names
RapidAPI uses different names for the plans, so we decided to add here the mappings
between our API plans and their API marketplace plan names:
{{< table "table-striped table-responsive" >}}
|       API Plan        |   RapidAPI Name      |
|:---------------------:|:--------------------:|
| FREE                  | BASIC                |
| MINIMAL               | PRO                  |
| PRO                   | ULTRA                |
| BUSINESS              | MEGA                 |
{{< /table >}}

<a href="https://rapidapi.com/ErikPelli/api/potaxium-forex-data" target="_blank">
	<img src="https://storage.googleapis.com/rapidapi-documentation/connect-on-rapidapi-dark.png" width="215" alt="Connect on RapidAPI">
</a>
