# EverydayData

## Introduction 
Hi! Welcome to my day-to-day dataset. <br/> I have been work a lot with numbers on the enviroment, the economy and production, and maybe it can help you all.
Sources, code lines and final datasets are available. All data description is listed below. Mostly done in R. <br/>

All data is divided into four 5 categories: Default Patterns, Greenhouse Gases (GHGs) Emissions, Land-Use and Farming, World Indicators and Brazilian Indicators. 
Dates are always set on YYYY-MM-DD format (if available).

Tips and comments are totally welcome!
For some dataviz-related work, follow me on Twitter: [@hec_vini](https://twitter.com/hec_vini). Also, connect with me on [LinkedIn](https://www.linkedin.com/in/viniciushpires/)

## Defaut Patterns 
Every scrip follow some rules and often use some structure. Here they are:

#### Packages 
```
library(tidyverse) 
library(lubridate) #To work with dates
library(janitor) #To easily manage date, especially Excel dates and clean_names() function. 
library(data.table) #Mainy to use fread() funtion
library(openxlsx) #Work with .xlsx files
library(countrycode) #convert contry names to ISO 3166-1 alfa-3 codes
library(ipeadatar) #IPEA (Brazilian Center for Economics Studies) API package
library(zoo) #mainly to use na.locf() function
library(tidylog) #Feedback on dplyr operations
library(WDI) #World Bank API package
library(httr) #Mostly to download web data
library(geobr) #Brazilian Geographic data
library(textclean) #Useful to clean strings, mostly to trim white spaces
library(ggh4x) #Hacks for ggplot2
library(anytime) #clean time date string
```

#### Inflation
|                                                                        `Dataset`                                                                       |                       `Source`                      | `Col. Description` |           `Coverage`          | `Description`                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------:|:------------------:|:-----------------------------:|---------------------------------------|
|                   [IPCA](https://github.com/HecVini/EverydayData/blob/c11257ff4c8227c1a6ec1020875a29807a29b399/Clean%20Data/ipca.csv)                  | [IPEAData](http://www.ipeadata.gov.br/Default.aspx) |      [Link]()      | 1995-12-01 to <br/>2020-12-01 | Brazilian main CPI index              |
|           [IPCA Monthly](https://github.com/HecVini/EverydayData/blob/c11257ff4c8227c1a6ec1020875a29807a29b399/Clean%20Data/ipca_monthly.csv)          | [IPEAData](http://www.ipeadata.gov.br/Default.aspx) |      [Link]()      | 1995-12-01 to <br/>2020-12-01 | Brazilian CPI monthly change          |
|            [IPCA Yearly](https://github.com/HecVini/EverydayData/blob/c11257ff4c8227c1a6ec1020875a29807a29b399/Clean%20Data/ipca_yearly.csv)           | [IPEAData](http://www.ipeadata.gov.br/Default.aspx) |      [Link]()      |          1996 to 2020         | Brazilian CPI yearly (Jan-Dec) change |
| [BRA GDP Implicit Deflator](https://github.com/HecVini/EverydayData/blob/c11257ff4c8227c1a6ec1020875a29807a29b399/Clean%20Data/deflator_implicito.csv) | [IPEAData](http://www.ipeadata.gov.br/Default.aspx) |      [Link]()      |          1996 to 2020         | Brazilian implicit GDP deflator       |

#### Brazilian Geographic Regions
|                                                                         `Dataset`                                                                        |                                                                                `Source`                                                                                | `Col. Description` | `Coverage` | `Description`                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:------------------:|:----------:|-------------------------------------------------|
| [Municipalies Codes](https://github.com/HecVini/EverydayData/blob/main/Clean%20Data/municipalities_codes.csv)                                            | [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?edicao=30111&t=acesso-ao-produto) | [Link]()           | -          | 5570 Brazilian cities names and 7-number codes  |
| [States Codes](https://github.com/HecVini/EverydayData/blob/main/Clean%20Data/states_codes.csv)                                                          | [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?edicao=30111&t=acesso-ao-produto) | [Link]()           | -          | 27 Brazilian states names and codes             |
| [Immediate Regions Codes](https://github.com/HecVini/EverydayData/blob/89815a1103e612558110f3e7b9a351028309c640/Clean%20Data/immediate_region_codes.csv) | [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?edicao=30111&t=acesso-ao-produto) | [Link]()           | -          | 510 Brazilian immediate regions names and codes |
| [Municipalies Codes 6n](https://github.com/HecVini/EverydayData/blob/89815a1103e612558110f3e7b9a351028309c640/Clean%20Data/municipalities_codes_6n.csv)  | [IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?edicao=30111&t=acesso-ao-produto) | [Link]()           | -          | 5570 Brazilian cities names and 6-number codes  |

#### Other 
|                                                                 `Dataset`                                                                 |                                                     `Source`                                                     | `Col. Description` |   `Coverage`  | `Description`                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------:|:------------------:|:-------------:|------------------------------------------------------------|
| [Income Levels](https://github.com/HecVini/EverydayData/blob/a4dac2074290da6ec134a0807905f0d9288e4936/Clean%20Data/world_bank_income.csv) | [World Bank](https://blogs.worldbank.org/opendata/new-world-bank-country-classifications-income-level-2021-2022) | [Link]             | 217 countries | World Bank countries 4 income levels (in 2021), by country |
| [EU27 ISOs-3c](https://github.com/HecVini/EverydayData/blob/a4dac2074290da6ec134a0807905f0d9288e4936/Clean%20Data/eu27_iso3c.csv)         | [EU](https://european-union.europa.eu/principles-countries-history/country-profiles_en)                          | [Link]             | EU 27         | All ISO3c codes for EU27 (excl. the UK) countries.         |
