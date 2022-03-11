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
| `Dateset`                       | `Source` | `Col. Description` | `Coverage`    | `File Description`                      |                  
| :-----------------------------: | :------- | ------------------ | ------------- |---------------------------------------- |
| [IPCA Monthly](../blob/master/LICENSE)                    | IBGE     | Link               | 2020-12-01    |Brazilian monthly main CPI Index         |
| IPCA Yearly                     | IBGE     | Link               | 2020-12-01    |Brazilian yearly (Jan-Dec) main CPI Index|
| Brazilian Implicit GDP Deflator | IBGE     | Link               | 2020          |Brazilian inplicit GDP Deflator          |

#### Brazilian Geographic Regions
| `Dateset`                  | `Source`   | `Col. Description`   | `Last Update`   | `File Description`                         |          
| :------------------------: | :--------: | -------------------- | --------------- |--------------------------------------------- |
| Municipalities ID Codes    | IBGE       | Link                 | 2020            |5570 Brazilian cities IDs and names           |
| States ID Codes            | IBGE       | Link                 | 2020            |27 Brazilian states IDs and names             |
| Immediate Regions ID Codes | IBGE       | Link                 | 2020            |510 Brazilian immediate regions IDs and names |
| Municipalities Biomes.     | IBGE       | Link                 | 2020            |5570 Brazilian cities biomes                  |

