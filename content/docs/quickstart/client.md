---
weight: 1
draft: false
toc: false
title: "API Client"
description: "Technical description about APIs client implementation"
---

If you have decided to make a subscription through our plans on RapidApi, using it will be very simple.

In fact, you have the freedom to make your own client for our APIs, as long as you send the right headers
with every request you make.

In addition to the normal headers of an HTTP request, it's mandatory to include the following headers:
- `X-RapidAPI-Key`, which corresponds to your subscription key, received during plan subscription
- `X-RapidAPI-Host`, which must always contain the value `potaxium-forex-data.p.rapidapi.com`

If the parameters specified in your client are invalid, the request to the target REST API method will most likely fail.

By following the rest of the documentation, you can easily integrate our APIs into your application, checking what
parameters you can pass and the corresponding response examples.
