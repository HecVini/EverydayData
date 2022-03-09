# EverydayData

## Introduction 
Hi! Welcome to my day-to-day dataset. I have been work a lot with numbers on the enviroment, the economy and production, and maybe it can help you all.
Sources, code lines and final datasets are available. All ata description is listed below. Mostrly done in R. 
All data is divided into four 5 categories: Default Patterns, Greenhouse Gases (GHGs) Emissions, Land-Use and Farming, World Indicators and Brazilian Indicators. 

Tips and comments are totally welcome!
For some dataviz-related work, follow me on Twitter: [@hec_vini](https://twitter.com/hec_vini). Also, connect with me on [LinkedIn](https://www.linkedin.com/in/viniciushpires/)

## Defaut Patterns 
Every scrip follow some rules and often use some structure. Here they are:

#### Packages 
'''
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
'''

#### Price Indeces
| Dateset          | Source           | Column Description   | File Description                                                            |
| ---------------- | ---------------- | -------------------- |---------------------------------------------------------------------------- |
| col 3 is         | right-aligned    | $1600.               |                                                                             |
| col 2 is         | centered         |   $12                |                                                                             |
| zebra stripes.   | are neat         |    $1                |                                                                             |
