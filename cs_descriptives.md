cs_descriptives
================
Dominique Tzou
2026-11-08

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.2.1     ✔ readr     2.2.0
    ## ✔ forcats   1.0.1     ✔ stringr   1.6.0
    ## ✔ ggplot2   4.0.3     ✔ tibble    3.3.1
    ## ✔ lubridate 1.9.5     ✔ tidyr     1.3.2
    ## ✔ purrr     1.2.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

    ## Rows: 43932 Columns: 75
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr  (8): name, sex, Frmat, formats2, Quality, Cause, code_group, IM_Frmat
    ## dbl (65): country, year, new_pop1, sexid, new_pop0, new_pop7, new_pop8, new_...
    ## lgl  (2): Admin1, SubDiv
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
    ## Rows: 227 Columns: 2
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (1): name
    ## dbl (1): country
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    ## `summarise()` has regrouped the output.
    ## ℹ Summaries were computed grouped by country and covid.
    ## ℹ Output is grouped by country.
    ## ℹ Use `summarise(.groups = "drop_last")` to silence this message.
    ## ℹ Use `summarise(.by = c(country, covid))` for per-operation grouping
    ##   (`?dplyr::dplyr_by`) instead.

**Suicide Mortality by Country**

The average suicide mortality for 2017-2019 and 2020-2022 was used to
calculate pre and post covid suicide mortality rates.

diff_sm1 = the percent change difference between pre and post covid
suicide mortality, formula = (Post - Pre)/ Pre

change_increase = flags whether suicide mortality increased or decreased

| name | country | pre_covid | post_covid | diff_sm1 | change_increase |
|:---|---:|---:|---:|---:|:---|
| Mauritius | 1300 | 0.0000892 | 0.0000988 | 0.1075127 | TRUE |
| Seychelles | 1400 | 0.0000724 | 0.0000606 | -0.1630359 | FALSE |
| South Africa | 1430 | 0.0000064 | 0.0000035 | -0.4541479 | FALSE |
| Antigua and Barbuda | 2010 | NA | 0.0000217 | NA | NA |
| Argentina | 2020 | 0.0000735 | 0.0000659 | -0.1031447 | FALSE |
| Brazil | 2070 | 0.0000619 | 0.0000693 | 0.1190865 | TRUE |
| Canada | 2090 | 0.0001190 | 0.0000998 | -0.1612368 | FALSE |
| Chile | 2120 | 0.0000990 | 0.0000817 | -0.1741297 | FALSE |
| Colombia | 2130 | 0.0000579 | 0.0000569 | -0.0163310 | FALSE |
| Costa Rica | 2140 | 0.0000701 | 0.0000771 | 0.0991280 | TRUE |
| Cuba | 2150 | 0.0001347 | 0.0001504 | 0.1167571 | TRUE |
| Dominica | 2160 | 0.0000146 | NA | NA | NA |
| Ecuador | 2180 | 0.0000704 | 0.0000583 | -0.1716256 | FALSE |
| El Salvador | 2190 | 0.0000402 | NA | NA | NA |
| Grenada | 2230 | 0.0000087 | 0.0000129 | 0.4868843 | TRUE |
| Guatemala | 2250 | 0.0000348 | 0.0000353 | 0.0136332 | TRUE |
| Guyana | 2260 | 0.0002448 | NA | NA | NA |
| Mexico | 2310 | 0.0000544 | 0.0000634 | 0.1649659 | TRUE |
| Nicaragua | 2340 | 0.0000536 | 0.0000634 | 0.1826150 | TRUE |
| Panama | 2350 | 0.0000269 | 0.0000279 | 0.0359581 | TRUE |
| Paraguay | 2360 | 0.0000671 | 0.0000819 | 0.2214204 | TRUE |
| Peru | 2370 | 0.0000150 | 0.0000173 | 0.1569807 | TRUE |
| Puerto Rico | 2380 | 0.0000733 | 0.0000613 | -0.1633517 | FALSE |
| Saint Lucia | 2400 | 0.0000546 | 0.0000393 | -0.2808427 | FALSE |
| Saint Vincent and Grenadines | 2420 | NA | 0.0000097 | NA | NA |
| United States of America | 2450 | 0.0001423 | 0.0001407 | -0.0116408 | FALSE |
| Uruguay | 2460 | 0.0002083 | 0.0002265 | 0.0870942 | TRUE |
| Cyprus | 3080 | 0.0000458 | 0.0000356 | -0.2225617 | FALSE |
| Iran (Islamic Republic of) | 3130 | 0.0000505 | NA | NA | NA |
| Israel | 3150 | 0.0000480 | 0.0000424 | -0.1161127 | FALSE |
| Japan | 3160 | 0.0001609 | 0.0001647 | 0.0236964 | TRUE |
| Jordan | 3170 | 0.0000013 | NA | NA | NA |
| Mongolia | 3260 | 0.0001411 | 0.0001492 | 0.0577234 | TRUE |
| Philippines | 3300 | 0.0000260 | NA | NA | NA |
| Republic of Korea | 3325 | 0.0002595 | 0.0002563 | -0.0124569 | FALSE |
| Saudi Arabia | 3340 | NA | 0.0000147 | NA | NA |
| Singapore | 3350 | 0.0000803 | 0.0000857 | 0.0668162 | TRUE |
| Sri Lanka | 3365 | 0.0001250 | NA | NA | NA |
| Turkey | 3400 | 0.0000387 | 0.0000480 | 0.2380698 | TRUE |
| Armenia | 4007 | 0.0000172 | 0.0000159 | -0.0715498 | FALSE |
| Austria | 4010 | 0.0001338 | 0.0001280 | -0.0431937 | FALSE |
| Belarus | 4018 | 0.0001905 | NA | NA | NA |
| Belgium | 4020 | 0.0001531 | 0.0001463 | -0.0447030 | FALSE |
| Bulgaria | 4030 | 0.0000907 | 0.0000775 | -0.1460126 | FALSE |
| Croatia | 4038 | 0.0001547 | 0.0001438 | -0.0700020 | FALSE |
| Czech Republic | 4045 | 0.0001236 | 0.0001172 | -0.0515262 | FALSE |
| Denmark | 4050 | 0.0001020 | 0.0000965 | -0.0536551 | FALSE |
| Estonia | 4055 | 0.0001551 | 0.0001469 | -0.0531266 | FALSE |
| Finland | 4070 | 0.0001434 | 0.0001323 | -0.0774920 | FALSE |
| France | 4080 | 0.0001310 | 0.0001353 | 0.0328482 | TRUE |
| Georgia | 4084 | 0.0000592 | 0.0000511 | -0.1357538 | FALSE |
| Germany | 4085 | 0.0001114 | 0.0001139 | 0.0228016 | TRUE |
| Greece | 4140 | 0.0000503 | 0.0000438 | -0.1300179 | FALSE |
| Hungary | 4150 | 0.0001650 | 0.0001686 | 0.0218268 | TRUE |
| Iceland | 4160 | 0.0001012 | 0.0001057 | 0.0444147 | TRUE |
| Ireland | 4170 | 0.0000827 | 0.0000883 | 0.0676555 | TRUE |
| Italy | 4180 | 0.0000637 | 0.0000638 | 0.0017666 | TRUE |
| Kazakhstan | 4182 | 0.0001374 | 0.0001050 | -0.2363180 | FALSE |
| Kyrgyzstan | 4184 | 0.0000604 | NA | NA | NA |
| Latvia | 4186 | 0.0001625 | 0.0001367 | -0.1582639 | FALSE |
| Lithuania | 4188 | 0.0002483 | 0.0002016 | -0.1879400 | FALSE |
| Luxembourg | 4190 | 0.0000936 | 0.0000760 | -0.1882175 | FALSE |
| North Macedonia | 4195 | 0.0000536 | 0.0000545 | 0.0162446 | TRUE |
| Malta | 4200 | 0.0000468 | 0.0000546 | 0.1658570 | TRUE |
| Netherlands | 4210 | 0.0001071 | 0.0001063 | -0.0074627 | FALSE |
| Norway | 4220 | 0.0001205 | 0.0001183 | -0.0176713 | FALSE |
| Poland | 4230 | 0.0001186 | 0.0001215 | 0.0241565 | TRUE |
| Portugal | 4240 | 0.0000988 | 0.0000991 | 0.0036405 | TRUE |
| Romania | 4270 | 0.0000962 | NA | NA | NA |
| Russian Federation | 4272 | 0.0001266 | NA | NA | NA |
| Serbia | 4273 | 0.0001382 | 0.0001247 | -0.0973923 | FALSE |
| Slovakia | 4274 | 0.0000706 | 0.0000688 | -0.0255191 | FALSE |
| Slovenia | 4276 | 0.0001868 | 0.0001752 | -0.0620975 | FALSE |
| Spain | 4280 | 0.0000776 | 0.0000857 | 0.1042933 | TRUE |
| Sweden | 4290 | 0.0001234 | 0.0001178 | -0.0449005 | FALSE |
| Switzerland | 4300 | 0.0001200 | 0.0001125 | -0.0628333 | FALSE |
| Ukraine | 4303 | 0.0001501 | NA | NA | NA |
| United Kingdom | 4308 | 0.0000787 | 0.0000847 | 0.0767500 | TRUE |
| Uzbekistan | 4335 | 0.0000709 | NA | NA | NA |
| Australia | 5020 | 0.0001316 | 0.0001246 | -0.0528837 | FALSE |
| New Zealand | 5150 | 0.0001267 | NA | NA | NA |

| change_increase |   n |
|:----------------|----:|
| FALSE           |  36 |
| TRUE            |  28 |
| NA              |  17 |

In 36 countries, suicide mortality decreased. In 28 countries, suicide
mortality increased. In 17 countries, suicide mortality data was
unavailable for either pre or post covid

**Overall Multinational Suicide Mortality**

Average multinational suicide mortality, pre and post covid. formula =
(Post - Pre)/ Pre

Diff_total indicates overall decrease.

| mean_pre_covid | mean_post_covid | diff_total |
|---------------:|----------------:|-----------:|
|        9.8e-05 |         9.2e-05 | -0.0613822 |
