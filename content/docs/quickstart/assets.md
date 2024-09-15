---
weight: 2
draft: false
toc: false
title: "Assets"
description: "Description of Assets resource in the API"
---

An asset is the fundamental element on which our API is based,
and represents any type of asset listed in global markets, with its own price.

We decided to divide the assets into 3 different categories:
- currencies
- cryptocurrencies
- materials

Below we have added some tables with the assets supported by our API.

The assets below are indicative only and may not represent all the available ones, please call our availability API
to check for new assets that aren't listed here.

> If the realtime rate of an asset isn't marked as available in the tables below, the maximum precision for the rate of
> the conversion pair is **1 minute**.

Do you need an asset that is not listed here? [Contact us](/docs/support) and let us know, we will do our best to
make it available.

### Currencies
{{< table "table-striped table-responsive" >}}
|      Listing Code    |   Name       | Realtime |
|:--------------------:|:-------------|:--------:|
| ADP | Andorran peseta | |
| AED | United Arab Emirates dirham | |
| AFA | Afghan afghani (old) | |
| AFN | Afghan afghani | |
| ALL | Albanian lek | |
| AMD | ArmenianDram | |
| ANG | Netherlands Antillean guilder | |
| AOA | Angolan kwanza | |
| AOR | Angolan kwanza reajustado | |
| ARS | Argentine peso | |
| ATS | Austrian schilling | |
| AUD | Australian dollar | ✔️       |
| AWG | Aruban Florin | |
| AZM | Azerbaijani manat (old) | |
| AZN | Azerbaijani manat | |
| BAM | Bosnia and Herzegovina convertible mark | |
| BBD | Barbadian dollar | |
| BDT | Bangladeshi taka | |
| BEF | Belgian franc | |
| BGL | Bulgarian lev (1962 - 1999) | |
| BGN | Bulgarian lev | |
| BHD | Bahraini dinar | |
| BIF | Burundian franc | |
| BMD | Bermudian dollar | |
| BND | Brunei dollar | |
| BOB | Boliviano | |
| BRL | Brazilian real | |
| BSD | Bahamian dollar | |
| BTN | Bhutanese ngultrum | |
| BWP | Botswana pula | |
| BYN | Belarusian ruble | |
| BYR | Belarusian ruble (2000 - 2016) | |
| BZD | Belize dollar | |
| CAD | Canadian dollar | ✔️       |
| CDF | Congolese franc | |
| CHF | Swiss franc | ✔️       |
| CLP | Chilean peso | |
| CNY | Renminbi | |
| COP | Colombian peso | |
| CRC | Costa Rican colon | |
| CUC | Cuban convertible peso | |
| CUP | Cuban peso | |
| CVE | Cape Verdean escudo | |
| CYP | Cypriot pound | |
| CZK | Czech koruna | ✔️       |
| DEM | German mark | |
| DJF | Djiboutian franc | |
| DKK | Danish krone | ✔️       |
| DOP | Dominican peso | |
| DZD | Algerian dinar | |
| ECS | Ecuadorian sucre | |
| EEK | Estonian kroon | |
| EGP | Egyptian pound | |
| ERN | Eritrean nakfa | |
| ETB | Ethiopian birr | |
| EUR | Euro | ✔️       |
| FIM | Finnish markka | |
| FJD | Fiji dollar | |
| FKP | Falkland Islands pound | |
| FRF | French franc | |
| GBP | British pound | ✔️       |
| GEL | Georgian lari | |
| GGP | Guernsey pound | |
| GHC | Ghanaian cedi (old) | |
| GHS | Ghanaian cedi | |
| GIP | Gibraltar pound | |
| GMD | Gambian dalasi | |
| GNF | Guinean franc | |
| GRD | Greek drachma | |
| GTQ | Guatemalan quetzal | |
| GYD | Guyanese dollar | |
| HKD | Hong Kong dollar | ✔️       |
| HNL | Honduran lempira | |
| HRK | Croatian kuna | |
| HTG | Haitian gourde | |
| HUF | Hungarian forint | ✔️       |
| IDR | Indonesian rupiah | |
| IEP | IrishPound | |
| ILS | Israeli new shekel | ✔️       |
| IMP | Manx Pound | |
| INR | Indian rupee | |
| IQD | Iraqi dinar | |
| IRR | Iranian rial | |
| ISK | Icelandic króna | |
| ITL | Italian lira | |
| JEP | Jersey pound | |
| JMD | Jamaican dollar | |
| JOD | Jordanian dinar | |
| JPY | Yen | ✔️       |
| KES | Kenyan shilling | |
| KGS | Kyrgyzstani som | |
| KHR | Cambodian riel | |
| KID | Kiribati dollar | |
| KMF | Comoro franc | |
| KPW | North Korean won | |
| KRW | South Korean won | |
| KWD | Kuwaiti dinar | |
| KYD | Cayman Islands dollar | |
| KZT | Kazakhstani tenge | |
| LAK | Laos kip | |
| LBP | Lebanese pound | |
| LKR | Sri Lankan rupee | |
| LRD | Liberian dollar | |
| LSL | Lesotho loti | |
| LTL | Lithuanian litas | |
| LUF | Luxembourg franc | |
| LVL | Latvian lats | |
| LYD | Libyan dinar | |
| MAD | Moroccan Dirham | |
| MCF | Monégasque franc | |
| MDL | Moldovan leu | |
| MGA | Malagasy ariary | |
| MGF | Malagasy franc | |
| MKD | Macedonian denar | |
| MMK | Myanmar kyat | |
| MNT | Mongolian tögrög | |
| MOP | Macanese pataca | |
| MRU | Mauritanian ouguiya | |
| MTL | Maltese lira | |
| MUR | Mauritian rupee | |
| MVR | Maldivian rufiyaa | |
| MWK | Malawian kwacha | |
| MXN | Mexican peso | ✔️       |
| MYR | Malaysian ringgit | |
| MZM | Mozambican metical (old) | |
| MZN | Mozambican metical | |
| NAD | Namibian dollar | |
| NGN | Nigerian naira | |
| NIO | Nicaraguan córdoba | |
| NLG | Dutch guilder | |
| NOK | Norwegian krone | ✔️       |
| NPR | Nepalese rupee | |
| NZD | New Zealand dollar | ✔️       |
| OMR | Omani rial | |
| PAB | Panamanian balboa | |
| PEN | Peruvian sol | |
| PGK | Papua New Guinean kina | |
| PHP | Philippine peso | |
| PKR | Pakistani rupee | |
| PLN | Polish złoty | ✔️       |
| PTE | Portuguese escudo | |
| PYG | Paraguayan guaraní | |
| QAR | Qatari riyal | |
| RON | Romanian leu | |
| RSD | Serbian dinar | |
| RUB | Russian ruble | |
| RWF | Rwandan franc | |
| SAR | Saudi riyal | |
| SBD | Solomon Islands dollar | |
| SCR | Seychelles rupee | |
| SDD | Sudanese dinar | |
| SDG | Sudanese pound | |
| SEK | Swedish krona | ✔️       |
| SGD | Singapore dollar | ✔️       |
| SHP | Saint Helena pound | |
| SIT | Slovenian tolar | |
| SKK | Slovak koruna | |
| SLE | Sierra Leonean leone | |
| SLL | Sierra Leonean leone (old) | |
| SML | San Marinese lira | |
| SOS | Somali shilling | |
| SRD | Surinamese dollar | |
| SRG | Surinamese guilder | |
| STD | São Tomé and Príncipe dobra (old) | |
| STN | São Tomé and Príncipe dobra | |
| SVC | Salvadoran colón | |
| SYP | Syrian pound | |
| SZL | Swazi lilangeni | |
| THB | Thai baht | |
| TJS | Tajikistani somoni | |
| TMM | Turkmenistan manat (old) | |
| TMT | Turkmenistan manat | |
| TND | Tunisian dinar | |
| TOP | Tongan paʻanga | |
| TRL | Turkish lira (old) | |
| TRY | Turkish lira | ✔️       |
| TTD | Trinidad and Tobago dollar | |
| TVD | Tuvaluan dollar | |
| TWD | New Taiwan dollar | |
| TZS | Tanzanian shilling | |
| UAH | Ukrainian hryvnia | |
| UGX | Ugandan shilling | |
| USD | Dollar | ✔️       |
| UYU | Uruguayan peso | |
| UZS | Uzbekistani sum | |
| VAL | Vatican lira | |
| VED | Venezuelan digital bolívar | |
| VEF | Venezuelan bolívar fuerte (2008 - 2018) | |
| VES | Venezuelan sovereign bolívar | |
| VND | Vietnamese đồng | |
| VUV | Vanuatu vatu | |
| WST | Samoan tala | |
| XAF | CFA franc BEAC | |
| XCD | East Caribbean dollar | |
| XOF | CFA franc BCEAO | |
| XPF | CFP franc | |
| YER | Yemeni rial | |
| ZAR | South African rand | ✔️       |
| ZMK | Zambian kwacha (old) | |
| ZMW | Zambian kwacha | |
| ZWD | Zimbabwean dollar (old) | |
| ZWG | Zimbabwe Gold | |
| ZWL | Zimbabwean dollar | |
{{< /table >}}

### Cryptocurrencies
{{< table "table-striped table-responsive" >}}
|      Listing Code    |   Name       | Realtime |
|:--------------------:|:-------------|:--------:|
| ADA                  | Cardano      | ✔️       |
| BCH                  | Bitcoin Cash | ✔️       |
| BTC                  | Bitcoin      | ✔️       |
| DOGE                 | Doge         | ✔️       |
| DOT                  | Polkadot     | ✔️       |
| ETH                  | Ethereum     | ✔️       |
| LTC                  | Litecoin     | ✔️       |
| LINK                 | Chainlink    | ✔️       |
| LUNA                 | Terra        |          |
| UNI                  | Uniswap      | ✔️       |
| XLM                  | Stellar      | ✔️       |
| XRP                  | Ripple       | ✔️       |
{{< /table >}}

### Materials
{{< table "table-striped table-responsive" >}}
|      Listing Code    |   Name      | Quantity | Realtime |
|:--------------------:|:------------|----------|:--------:|
| XAU                  | Gold        | Ounce    | ✔️       |
| XAG                  | Silver      | Ounce    | ✔️       |
| XPT                  | Platinum    | Ounce    | ✔️       |
| XPD                  | Palladium   | Ounce    | ✔️       |
{{< /table >}}