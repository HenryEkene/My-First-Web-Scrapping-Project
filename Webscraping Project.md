```python
from bs4 import BeautifulSoup
import requests
url = 'https://en.wikipedia.org/wiki/List_of_largest_companies_in_the_United_States_by_revenue'
page = requests.get(url)
soup = BeautifulSoup(page.text, 'html.parser')
#print(soup)
```


```python
table = soup.find_all('table')[0]
print(table)
```

    <table class="wikitable sortable">
    <caption>
    </caption>
    <tbody><tr>
    <th>Rank
    </th>
    <th>Name
    </th>
    <th>Industry
    </th>
    <th>Revenue <br/>(USD millions)
    </th>
    <th>Revenue growth
    </th>
    <th>Employees
    </th>
    <th>Headquarters
    </th></tr>
    <tr>
    <td>1
    </td>
    <td><a href="/wiki/Walmart" title="Walmart">Walmart</a>
    </td>
    <td><a href="/wiki/Retail" title="Retail">Retail</a>
    </td>
    <td style="text-align:center;">648,125
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 6.0%
    </td>
    <td style="text-align:center;">2,100,000
    </td>
    <td><a href="/wiki/Bentonville,_Arkansas" title="Bentonville, Arkansas">Bentonville, Arkansas</a>
    </td></tr>
    <tr>
    <td>2
    </td>
    <td><a href="/wiki/Amazon_(company)" title="Amazon (company)">Amazon</a>
    </td>
    <td>Retail and <a href="/wiki/Cloud_computing" title="Cloud computing">cloud computing</a>
    </td>
    <td style="text-align:center;">574,785
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 11.9%
    </td>
    <td style="text-align:center;">1,525,000
    </td>
    <td><a href="/wiki/Seattle" title="Seattle">Seattle, Washington</a>
    </td></tr>
    <tr>
    <td>3
    </td>
    <td><a class="mw-redirect" href="/wiki/Apple_Inc" title="Apple Inc">Apple</a>
    </td>
    <td><a href="/wiki/Electronics_industry" title="Electronics industry">Electronics industry</a>
    </td>
    <td style="text-align:center;">383,482
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -2.8%
    </td>
    <td style="text-align:center;">161,000
    </td>
    <td><a href="/wiki/Cupertino,_California" title="Cupertino, California">Cupertino, California</a>
    </td></tr>
    <tr>
    <td>4
    </td>
    <td><a href="/wiki/UnitedHealth_Group" title="UnitedHealth Group">UnitedHealth Group</a>
    </td>
    <td><a class="mw-redirect" href="/wiki/Healthcare" title="Healthcare">Healthcare</a>
    </td>
    <td style="text-align:center;">371,622
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 14.6%
    </td>
    <td style="text-align:center;">440,000
    </td>
    <td><a href="/wiki/Minnetonka,_Minnesota" title="Minnetonka, Minnesota">Minnetonka, Minnesota</a>
    </td></tr>
    <tr>
    <td>5
    </td>
    <td><a href="/wiki/Berkshire_Hathaway" title="Berkshire Hathaway">Berkshire Hathaway</a>
    </td>
    <td><a href="/wiki/Conglomerate_(company)" title="Conglomerate (company)">Conglomerate</a>
    </td>
    <td style="text-align:center;">364,482
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 20.7%
    </td>
    <td style="text-align:center;">396,500
    </td>
    <td><a href="/wiki/Omaha,_Nebraska" title="Omaha, Nebraska">Omaha, Nebraska</a>
    </td></tr>
    <tr>
    <td>6
    </td>
    <td><a href="/wiki/CVS_Health" title="CVS Health">CVS Health</a>
    </td>
    <td>Healthcare
    </td>
    <td style="text-align:center;">357,776
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 10.9%
    </td>
    <td style="text-align:center;">259,500
    </td>
    <td><a href="/wiki/Woonsocket,_Rhode_Island" title="Woonsocket, Rhode Island">Woonsocket, Rhode Island</a>
    </td></tr>
    <tr>
    <td>7
    </td>
    <td><a href="/wiki/ExxonMobil" title="ExxonMobil">ExxonMobil</a>
    </td>
    <td><a href="/wiki/Petroleum_industry" title="Petroleum industry">Petroleum industry</a>
    </td>
    <td style="text-align:center;">344,582
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -16.7%
    </td>
    <td style="text-align:center;">61,500
    </td>
    <td><a href="/wiki/Spring,_Texas" title="Spring, Texas">Spring, Texas</a>
    </td></tr>
    <tr>
    <td>8
    </td>
    <td><a class="mw-redirect" href="/wiki/Alphabet_Inc" title="Alphabet Inc">Alphabet</a>
    </td>
    <td><a href="/wiki/Technology" title="Technology">Technology</a> and cloud computing
    </td>
    <td style="text-align:center;">307,394
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 8.7%
    </td>
    <td style="text-align:center;">182,502
    </td>
    <td><a href="/wiki/Mountain_View,_California" title="Mountain View, California">Mountain View, California</a>
    </td></tr>
    <tr>
    <td>9
    </td>
    <td><a href="/wiki/McKesson_Corporation" title="McKesson Corporation">McKesson Corporation</a>
    </td>
    <td>Health
    </td>
    <td style="text-align:center;">276,711
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 4.8%
    </td>
    <td style="text-align:center;">48,000
    </td>
    <td><a href="/wiki/Irving,_Texas" title="Irving, Texas">Irving, Texas</a>
    </td></tr>
    <tr>
    <td>10
    </td>
    <td><a href="/wiki/Cencora" title="Cencora">Cencora</a>
    </td>
    <td><a href="/wiki/Pharmacy" title="Pharmacy">Pharmacy wholesale</a>
    </td>
    <td style="text-align:center;">262,173
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 9.9%
    </td>
    <td style="text-align:center;">44,000
    </td>
    <td><a href="/wiki/Conshohocken,_Pennsylvania" title="Conshohocken, Pennsylvania">Conshohocken, Pennsylvania</a>
    </td></tr>
    <tr>
    <td>11
    </td>
    <td><a href="/wiki/Costco" title="Costco">Costco</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">242,290
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 6.8%
    </td>
    <td style="text-align:center;">316,000
    </td>
    <td><a href="/wiki/Issaquah,_Washington" title="Issaquah, Washington">Issaquah, Washington</a>
    </td></tr>
    <tr>
    <td>12
    </td>
    <td><a href="/wiki/JPMorgan_Chase" title="JPMorgan Chase">JPMorgan Chase</a>
    </td>
    <td><a href="/wiki/Financial_services" title="Financial services">Financial services</a>
    </td>
    <td style="text-align:center;">239,425
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 54.7%
    </td>
    <td style="text-align:center;">309,926
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>13
    </td>
    <td><a href="/wiki/Microsoft" title="Microsoft">Microsoft</a>
    </td>
    <td>Technology and cloud computing
    </td>
    <td style="text-align:center;">211,915
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 6.9%
    </td>
    <td style="text-align:center;">221,000
    </td>
    <td><a href="/wiki/Redmond,_Washington" title="Redmond, Washington">Redmond, Washington</a>
    </td></tr>
    <tr>
    <td>14
    </td>
    <td><a href="/wiki/Cardinal_Health" title="Cardinal Health">Cardinal Health</a>
    </td>
    <td>Healthcare
    </td>
    <td style="text-align:center;">205,012
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 13.0%
    </td>
    <td style="text-align:center;">47,520
    </td>
    <td><a href="/wiki/Dublin,_Ohio" title="Dublin, Ohio">Dublin, Ohio</a>
    </td></tr>
    <tr>
    <td>15
    </td>
    <td><a href="/wiki/Chevron_Corporation" title="Chevron Corporation">Chevron Corporation</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">200,949
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -18.4%
    </td>
    <td style="text-align:center;">45,600
    </td>
    <td><a class="mw-redirect" href="/wiki/Houston,_Texas" title="Houston, Texas">Houston, Texas</a>
    </td></tr>
    <tr>
    <td>16
    </td>
    <td><a class="mw-redirect" href="/wiki/Cigna" title="Cigna">Cigna</a>
    </td>
    <td>Health insurance
    </td>
    <td style="text-align:center;">195,265
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 8.2%
    </td>
    <td style="text-align:center;">71,413
    </td>
    <td><a href="/wiki/Bloomfield,_Connecticut" title="Bloomfield, Connecticut">Bloomfield, Connecticut</a>
    </td></tr>
    <tr>
    <td>17
    </td>
    <td><a href="/wiki/Ford_Motor_Company" title="Ford Motor Company">Ford Motor Company</a>
    </td>
    <td><a href="/wiki/Automotive_industry" title="Automotive industry">Automotive industry</a>
    </td>
    <td style="text-align:center;">176,191
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 11.5%
    </td>
    <td style="text-align:center;">177,000
    </td>
    <td><a href="/wiki/Dearborn,_Michigan" title="Dearborn, Michigan">Dearborn, Michigan</a>
    </td></tr>
    <tr>
    <td>18
    </td>
    <td><a href="/wiki/Bank_of_America" title="Bank of America">Bank of America</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">171,912
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span><span data-sort-value="7000300000000000000♠" style="display:none"></span> 49.4%
    </td>
    <td style="text-align:center;">212,985
    </td>
    <td><a href="/wiki/Charlotte,_North_Carolina" title="Charlotte, North Carolina">Charlotte, North Carolina</a>
    </td></tr>
    <tr>
    <td>19
    </td>
    <td><a href="/wiki/General_Motors" title="General Motors">General Motors</a>
    </td>
    <td>Automotive industry
    </td>
    <td style="text-align:center;">171,842
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 9.6%
    </td>
    <td style="text-align:center;">163,000
    </td>
    <td><a href="/wiki/Detroit" title="Detroit">Detroit, Michigan</a>
    </td></tr>
    <tr>
    <td>20
    </td>
    <td><a class="mw-redirect" href="/wiki/Anthem_(company)" title="Anthem (company)">Elevance Health</a>
    </td>
    <td>Healthcare
    </td>
    <td style="text-align:center;">171,340
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 9.4%
    </td>
    <td style="text-align:center;">104,900
    </td>
    <td><a href="/wiki/Indianapolis" title="Indianapolis">Indianapolis, Indiana</a>
    </td></tr>
    <tr>
    <td>21
    </td>
    <td><a href="/wiki/Citigroup" title="Citigroup">Citigroup</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">156,820
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 55.1%
    </td>
    <td style="text-align:center;">237,925
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>22
    </td>
    <td><a class="mw-redirect" href="/wiki/Centene" title="Centene">Centene</a>
    </td>
    <td>Healthcare
    </td>
    <td style="text-align:center;">153,999
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 6.5%
    </td>
    <td style="text-align:center;">67,700
    </td>
    <td><a href="/wiki/St._Louis" title="St. Louis">St. Louis, Missouri</a>
    </td></tr>
    <tr>
    <td>23
    </td>
    <td><a class="mw-redirect" href="/wiki/The_Home_Depot" title="The Home Depot">The Home Depot</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">152,669
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -3.0%
    </td>
    <td style="text-align:center;">463,100
    </td>
    <td><a href="/wiki/Atlanta" title="Atlanta">Atlanta, Georgia</a>
    </td></tr>
    <tr>
    <td>24
    </td>
    <td><a href="/wiki/Marathon_Petroleum" title="Marathon Petroleum">Marathon Petroleum</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">150,307
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -16.5%
    </td>
    <td style="text-align:center;">18,200
    </td>
    <td><a href="/wiki/Findlay,_Ohio" title="Findlay, Ohio">Findlay, Ohio</a>
    </td></tr>
    <tr>
    <td>25
    </td>
    <td><a href="/wiki/Kroger" title="Kroger">Kroger</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">150,039
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -3.6%
    </td>
    <td style="text-align:center;">414,000
    </td>
    <td><a href="/wiki/Cincinnati" title="Cincinnati">Cincinnati, Ohio</a>
    </td></tr>
    <tr>
    <td>26
    </td>
    <td><a href="/wiki/Phillips_66" title="Phillips 66">Phillips 66</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">149,890
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -14.7%
    </td>
    <td style="text-align:center;">14,000
    </td>
    <td><a href="/wiki/Houston" title="Houston">Houston, Texas</a>
    </td></tr>
    <tr>
    <td>27
    </td>
    <td><a href="/wiki/Fannie_Mae" title="Fannie Mae">Fannie Mae</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">141,240
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 16.2%
    </td>
    <td style="text-align:center;">8,100
    </td>
    <td><a href="/wiki/Washington,_D.C." title="Washington, D.C.">Washington, D.C.</a>
    </td></tr>
    <tr>
    <td>28
    </td>
    <td><a href="/wiki/Walgreens_Boots_Alliance" title="Walgreens Boots Alliance">Walgreens Boots Alliance</a>
    </td>
    <td>Pharmaceutical industry
    </td>
    <td style="text-align:center;">139,081
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 4.8%
    </td>
    <td style="text-align:center;">268,500
    </td>
    <td><a href="/wiki/Deerfield,_Illinois" title="Deerfield, Illinois">Deerfield, Illinois</a>
    </td></tr>
    <tr>
    <td>29
    </td>
    <td><a href="/wiki/Valero_Energy" title="Valero Energy">Valero Energy</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">139,001
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -18.8%
    </td>
    <td style="text-align:center;">9,987
    </td>
    <td><a href="/wiki/San_Antonio" title="San Antonio">San Antonio, Texas</a>
    </td></tr>
    <tr>
    <td>30
    </td>
    <td><a href="/wiki/Meta_Platforms" title="Meta Platforms">Meta Platforms</a>
    </td>
    <td>Technology
    </td>
    <td style="text-align:center;">134,902
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 15.7%
    </td>
    <td style="text-align:center;">67,317
    </td>
    <td><a href="/wiki/Menlo_Park,_California" title="Menlo Park, California">Menlo Park, California</a>
    </td></tr>
    <tr>
    <td>31
    </td>
    <td><a class="mw-redirect" href="/wiki/Verizon_Communications" title="Verizon Communications">Verizon Communications</a>
    </td>
    <td>Telecommunications
    </td>
    <td style="text-align:center;">133,974
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -2.1%
    </td>
    <td style="text-align:center;">105,400
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>32
    </td>
    <td><a href="/wiki/AT%26T" title="AT&amp;T">AT&amp;T</a>
    </td>
    <td><a href="/wiki/Conglomerate_(company)" title="Conglomerate (company)">Conglomerate</a> and telecommunications
    </td>
    <td style="text-align:center;">122,428
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 1.4%
    </td>
    <td style="text-align:center;">150,470
    </td>
    <td><a href="/wiki/Dallas" title="Dallas">Dallas, Texas</a>
    </td></tr>
    <tr>
    <td>33
    </td>
    <td><a href="/wiki/Comcast" title="Comcast">Comcast</a>
    </td>
    <td>Telecommunications
    </td>
    <td style="text-align:center;">121,572
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 0.1%
    </td>
    <td style="text-align:center;">186,000
    </td>
    <td><a href="/wiki/Philadelphia" title="Philadelphia">Philadelphia, Pennsylvania</a>
    </td></tr>
    <tr>
    <td>34
    </td>
    <td><a href="/wiki/Wells_Fargo" title="Wells Fargo">Wells Fargo</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">115,340
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 39.2%
    </td>
    <td style="text-align:center;">226,000
    </td>
    <td><a href="/wiki/San_Francisco" title="San Francisco">San Francisco, California</a>
    </td></tr>
    <tr>
    <td>35
    </td>
    <td><a href="/wiki/Goldman_Sachs" title="Goldman Sachs">Goldman Sachs</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">108,418
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 57.8%
    </td>
    <td style="text-align:center;">45,300
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>36
    </td>
    <td><a href="/wiki/Freddie_Mac" title="Freddie Mac">Freddie Mac</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">108,050
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 24.6%
    </td>
    <td style="text-align:center;">8,020
    </td>
    <td><a href="/wiki/McLean,_Virginia" title="McLean, Virginia">McLean, Virginia</a>
    </td></tr>
    <tr>
    <td>37
    </td>
    <td><a href="/wiki/Target_Corporation" title="Target Corporation">Target Corporation</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">107,412
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -1.6%
    </td>
    <td style="text-align:center;">415,000
    </td>
    <td><a href="/wiki/Minneapolis" title="Minneapolis">Minneapolis, Minnesota</a>
    </td></tr>
    <tr>
    <td>38
    </td>
    <td><a href="/wiki/Humana" title="Humana">Humana</a>
    </td>
    <td>Health insurance
    </td>
    <td style="text-align:center;">106,374
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 14.5%
    </td>
    <td style="text-align:center;">67,600
    </td>
    <td><a href="/wiki/Louisville,_Kentucky" title="Louisville, Kentucky">Louisville, Kentucky</a>
    </td></tr>
    <tr>
    <td>39
    </td>
    <td><a href="/wiki/State_Farm" title="State Farm">State Farm</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">104,199
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 16.6%
    </td>
    <td style="text-align:center;">65,054
    </td>
    <td><a href="/wiki/Bloomington,_Illinois" title="Bloomington, Illinois">Bloomington, Illinois</a>
    </td></tr>
    <tr>
    <td>40
    </td>
    <td><a class="mw-redirect" href="/wiki/Tesla_Inc" title="Tesla Inc">Tesla</a>
    </td>
    <td>Automotive and energy
    </td>
    <td style="text-align:center;">96,773
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 18.8%
    </td>
    <td style="text-align:center;">140,473
    </td>
    <td><a href="/wiki/Austin,_Texas" title="Austin, Texas">Austin, Texas</a>
    </td></tr>
    <tr>
    <td>41
    </td>
    <td><a href="/wiki/Morgan_Stanley" title="Morgan Stanley">Morgan Stanley</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">96,194
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 45.9%
    </td>
    <td style="text-align:center;">80,006
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>42
    </td>
    <td><a href="/wiki/Johnson_%26_Johnson" title="Johnson &amp; Johnson">Johnson &amp; Johnson</a>
    </td>
    <td>Pharmaceutical industry
    </td>
    <td style="text-align:center;">95,195
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 0.3%
    </td>
    <td style="text-align:center;">131,900
    </td>
    <td><a href="/wiki/New_Brunswick,_New_Jersey" title="New Brunswick, New Jersey">New Brunswick, New Jersey</a>
    </td></tr>
    <tr>
    <td>43
    </td>
    <td><a href="/wiki/Archer_Daniels_Midland" title="Archer Daniels Midland">Archer Daniels Midland</a>
    </td>
    <td><a href="/wiki/Food_industry" title="Food industry">Food industry</a>
    </td>
    <td style="text-align:center;">93,935
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -7.5%
    </td>
    <td style="text-align:center;">41,008
    </td>
    <td><a class="mw-redirect" href="/wiki/Chicago,_Illinois" title="Chicago, Illinois">Chicago, Illinois</a>
    </td></tr>
    <tr>
    <td>44
    </td>
    <td><a href="/wiki/PepsiCo" title="PepsiCo">PepsiCo</a>
    </td>
    <td><a href="/wiki/Drink" title="Drink">Beverage</a>
    </td>
    <td style="text-align:center;">91,471
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 5.9%
    </td>
    <td style="text-align:center;">318,000
    </td>
    <td><a href="/wiki/Purchase,_New_York" title="Purchase, New York">Purchase, New York</a>
    </td></tr>
    <tr>
    <td>45
    </td>
    <td><a href="/wiki/United_Parcel_Service" title="United Parcel Service">United Parcel Service</a>
    </td>
    <td><a class="mw-redirect" href="/wiki/Transportation" title="Transportation">Transportation</a>
    </td>
    <td style="text-align:center;">90,958
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -9.3%
    </td>
    <td style="text-align:center;">382,550
    </td>
    <td><a href="/wiki/Atlanta" title="Atlanta">Atlanta, Georgia</a>
    </td></tr>
    <tr>
    <td>46
    </td>
    <td><a href="/wiki/FedEx" title="FedEx">FedEx</a>
    </td>
    <td>Transportation
    </td>
    <td style="text-align:center;">90,155
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -3.6%
    </td>
    <td style="text-align:center;">446,400
    </td>
    <td><a href="/wiki/Memphis,_Tennessee" title="Memphis, Tennessee">Memphis, Tennessee</a>
    </td></tr>
    <tr>
    <td>47
    </td>
    <td><a href="/wiki/The_Walt_Disney_Company" title="The Walt Disney Company">The Walt Disney Company</a>
    </td>
    <td>Media
    </td>
    <td style="text-align:center;">88,898
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 7.5%
    </td>
    <td style="text-align:center;">199,125
    </td>
    <td><a href="/wiki/Burbank,_California" title="Burbank, California">Burbank, California</a>
    </td></tr>
    <tr>
    <td>48
    </td>
    <td><a href="/wiki/Dell_Technologies" title="Dell Technologies">Dell Technologies</a>
    </td>
    <td>Technology
    </td>
    <td style="text-align:center;">88,425
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -13.6%
    </td>
    <td style="text-align:center;">120,000
    </td>
    <td><a href="/wiki/Round_Rock,_Texas" title="Round Rock, Texas">Round Rock, Texas</a>
    </td></tr>
    <tr>
    <td>49
    </td>
    <td><a href="/wiki/Lowe%27s" title="Lowe's">Lowe's</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">86,377
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -11.0%
    </td>
    <td style="text-align:center;">226,000
    </td>
    <td><a href="/wiki/Mooresville,_North_Carolina" title="Mooresville, North Carolina">Mooresville, North Carolina</a>
    </td></tr>
    <tr>
    <td>50
    </td>
    <td><a href="/wiki/Procter_%26_Gamble" title="Procter &amp; Gamble">Procter &amp; Gamble</a>
    </td>
    <td>Consumer products manufacturing
    </td>
    <td style="text-align:center;">82,006
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span><span data-sort-value="7000300000000000000♠" style="display:none"></span> 2.3%
    </td>
    <td style="text-align:center;">107,000
    </td>
    <td><a href="/wiki/Cincinnati" title="Cincinnati">Cincinnati, Ohio</a>
    </td></tr>
    <tr>
    <td>51
    </td>
    <td><a class="mw-redirect" href="/wiki/Energy_Transfer_Partners" title="Energy Transfer Partners">Energy Transfer Partners</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">78,586
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -12.6%
    </td>
    <td style="text-align:center;">13,786
    </td>
    <td><a class="mw-redirect" href="/wiki/Dallas,_Texas" title="Dallas, Texas">Dallas, Texas</a>
    </td></tr>
    <tr>
    <td>52
    </td>
    <td><a href="/wiki/Boeing" title="Boeing">Boeing</a>
    </td>
    <td><a href="/wiki/Aerospace_engineering" title="Aerospace engineering">Aerospace</a> and <a href="/wiki/Arms_industry" title="Arms industry">defense</a>
    </td>
    <td style="text-align:center;">77,794
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span><span data-sort-value="7000300000000000000♠" style="display:none"></span> 16.8%
    </td>
    <td style="text-align:center;">171,000
    </td>
    <td><a class="mw-redirect" href="/wiki/Arlington_County" title="Arlington County">Arlington County, Virginia</a>
    </td></tr>
    <tr>
    <td>53
    </td>
    <td><a href="/wiki/Albertsons" title="Albertsons">Albertsons</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">77,650
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 8.0%
    </td>
    <td style="text-align:center;">198,650
    </td>
    <td><a href="/wiki/Boise,_Idaho" title="Boise, Idaho">Boise, Idaho</a>
    </td></tr>
    <tr>
    <td>54
    </td>
    <td><a href="/wiki/Sysco" title="Sysco">Sysco</a>
    </td>
    <td>Food service
    </td>
    <td style="text-align:center;">76,325
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 11.2%
    </td>
    <td style="text-align:center;">71,750
    </td>
    <td><a class="mw-redirect" href="/wiki/Houston,_Texas" title="Houston, Texas">Houston, Texas</a>
    </td></tr>
    <tr>
    <td>55
    </td>
    <td><a href="/wiki/RTX_Corporation" title="RTX Corporation">RTX Corporation</a>
    </td>
    <td>Conglomerate
    </td>
    <td style="text-align:center;">68,920
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 2.8%
    </td>
    <td style="text-align:center;">185,000
    </td>
    <td><a href="/wiki/Arlington_County,_Virginia" title="Arlington County, Virginia">Arlington County, Virginia</a>
    </td></tr>
    <tr>
    <td>56
    </td>
    <td><a href="/wiki/General_Electric" title="General Electric">General Electric</a>
    </td>
    <td>Conglomerate
    </td>
    <td style="text-align:center;">67,954
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -11.2%
    </td>
    <td style="text-align:center;">125,000
    </td>
    <td><a href="/wiki/Boston" title="Boston">Boston, Massachusetts</a>
    </td></tr>
    <tr>
    <td>57
    </td>
    <td><a href="/wiki/Lockheed_Martin" title="Lockheed Martin">Lockheed Martin</a>
    </td>
    <td>Aerospace and defense
    </td>
    <td style="text-align:center;">67,571
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 2.4%
    </td>
    <td style="text-align:center;">122,000
    </td>
    <td><a href="/wiki/Bethesda,_Maryland" title="Bethesda, Maryland">Bethesda, Maryland</a>
    </td></tr>
    <tr>
    <td>58
    </td>
    <td><a href="/wiki/American_Express" title="American Express">American Express</a>
    </td>
    <td>Financial
    </td>
    <td style="text-align:center;">67,364
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 21.1%
    </td>
    <td style="text-align:center;">74,600
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>59
    </td>
    <td><a class="mw-redirect" href="/wiki/Caterpillar_Inc" title="Caterpillar Inc">Caterpillar</a>
    </td>
    <td>Machinery
    </td>
    <td style="text-align:center;">67,060
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 12.8%
    </td>
    <td style="text-align:center;">113,200
    </td>
    <td><a href="/wiki/Irving,_Texas" title="Irving, Texas">Irving, Texas</a>
    </td></tr>
    <tr>
    <td>60
    </td>
    <td><a href="/wiki/MetLife" title="MetLife">MetLife</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">66,905
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -4.3%
    </td>
    <td style="text-align:center;">45,000
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>61
    </td>
    <td><a href="/wiki/HCA_Healthcare" title="HCA Healthcare">HCA Healthcare</a>
    </td>
    <td>Healthcare
    </td>
    <td style="text-align:center;">64,968
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 7.9%
    </td>
    <td style="text-align:center;">265,000
    </td>
    <td><a href="/wiki/Nashville,_Tennessee" title="Nashville, Tennessee">Nashville, Tennessee</a>
    </td></tr>
    <tr>
    <td>62
    </td>
    <td><a href="/wiki/Progressive_Corporation" title="Progressive Corporation">Progressive Corporation</a>
    </td>
    <td>Insurance
    </td>
    <td style="text-align:center;">62,109
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span><span data-sort-value="7000300000000000000♠" style="display:none"></span> 25.2%
    </td>
    <td style="text-align:center;">61,432
    </td>
    <td><a class="mw-redirect" href="/wiki/Mayfield_Village,_Ohio" title="Mayfield Village, Ohio">Mayfield Village, Ohio</a>
    </td></tr>
    <tr>
    <td>63
    </td>
    <td><a href="/wiki/IBM" title="IBM">IBM</a>
    </td>
    <td>Technology and cloud computing
    </td>
    <td style="text-align:center;">61,860
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -16.3%
    </td>
    <td style="text-align:center;">296,600
    </td>
    <td><a href="/wiki/Armonk,_New_York" title="Armonk, New York">Armonk, New York</a>
    </td></tr>
    <tr>
    <td>64
    </td>
    <td><a href="/wiki/John_Deere" title="John Deere">John Deere</a>
    </td>
    <td>Agriculture manufacturing
    </td>
    <td style="text-align:center;">61,251
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 16.5%
    </td>
    <td style="text-align:center;">82,956
    </td>
    <td><a href="/wiki/Moline,_Illinois" title="Moline, Illinois">Moline, Illinois</a>
    </td></tr>
    <tr>
    <td>65
    </td>
    <td><a href="/wiki/Nvidia" title="Nvidia">Nvidia</a>
    </td>
    <td>Technology
    </td>
    <td style="text-align:center;">60,922
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 125.9%
    </td>
    <td style="text-align:center;">29,600
    </td>
    <td><a href="/wiki/Santa_Clara,_California" title="Santa Clara, California">Santa Clara, California</a>
    </td></tr>
    <tr>
    <td>66
    </td>
    <td><a class="mw-redirect" href="/wiki/StoneX_Group" title="StoneX Group">StoneX Group</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">60,856
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -7.8%
    </td>
    <td style="text-align:center;">4,137
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>67
    </td>
    <td><a href="/wiki/Merck_%26_Co." title="Merck &amp; Co.">Merck &amp; Co.</a>
    </td>
    <td>Pharmaceutical industry
    </td>
    <td style="text-align:center;">60,115
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 1.4%
    </td>
    <td style="text-align:center;">71,000
    </td>
    <td><a href="/wiki/Kenilworth,_New_Jersey" title="Kenilworth, New Jersey">Kenilworth, New Jersey</a>
    </td></tr>
    <tr>
    <td>68
    </td>
    <td><a href="/wiki/ConocoPhillips" title="ConocoPhillips">ConocoPhillips</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">58,574
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -28.7%
    </td>
    <td style="text-align:center;">9,900
    </td>
    <td><a class="mw-redirect" href="/wiki/Houston,_Texas" title="Houston, Texas">Houston, Texas</a>
    </td></tr>
    <tr>
    <td>69
    </td>
    <td><a href="/wiki/Pfizer" title="Pfizer">Pfizer</a>
    </td>
    <td>Pharmaceutical industry
    </td>
    <td style="text-align:center;">58,496
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -41.7%
    </td>
    <td style="text-align:center;">88,000
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>70
    </td>
    <td><a href="/wiki/Delta_Air_Lines" title="Delta Air Lines">Delta Air Lines</a>
    </td>
    <td><a href="/wiki/Airline" title="Airline">Airline</a>
    </td>
    <td style="text-align:center;">58,048
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000400000000000000♠" style="display:none"></span> 14.8%
    </td>
    <td style="text-align:center;">103,000
    </td>
    <td><a class="mw-redirect" href="/wiki/Atlanta_Georgia" title="Atlanta Georgia">Atlanta, Georgia</a>
    </td></tr>
    <tr>
    <td>71
    </td>
    <td><a href="/wiki/TD_Synnex" title="TD Synnex">TD Synnex</a>
    </td>
    <td><a class="mw-redirect" href="/wiki/Information_Technology" title="Information Technology">Information Technology</a>
    </td>
    <td style="text-align:center;">57,555
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -7.7%
    </td>
    <td style="text-align:center;">28,000
    </td>
    <td><a href="/wiki/Clearwater,_Florida" title="Clearwater, Florida">Clearwater, Florida</a>
    </td></tr>
    <tr>
    <td>72
    </td>
    <td><a href="/wiki/Publix" title="Publix">Publix</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">57,534
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 4.7%
    </td>
    <td style="text-align:center;">253,000
    </td>
    <td><a href="/wiki/Lakeland,_Florida" title="Lakeland, Florida">Lakeland, Florida</a>
    </td></tr>
    <tr>
    <td>73
    </td>
    <td><a href="/wiki/Allstate" title="Allstate">Allstate</a>
    </td>
    <td>Insurance
    </td>
    <td style="text-align:center;">57,094
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000400000000000000♠" style="display:none"></span> 11.1%
    </td>
    <td style="text-align:center;">53,200
    </td>
    <td><a class="mw-redirect" href="/wiki/Northfield_Township,_Cook_County,_Illinois" title="Northfield Township, Cook County, Illinois">Northfield Township, Cook County, Illinois</a>
    </td></tr>
    <tr>
    <td>74
    </td>
    <td><a href="/wiki/Cisco" title="Cisco">Cisco</a>
    </td>
    <td>Telecom hardware manufacturing
    </td>
    <td style="text-align:center;">56,998
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 10.6%
    </td>
    <td style="text-align:center;">84,900
    </td>
    <td><a href="/wiki/San_Jose,_California" title="San Jose, California">San Jose, California</a>
    </td></tr>
    <tr>
    <td>75
    </td>
    <td><a href="/wiki/Nationwide_Mutual_Insurance_Company" title="Nationwide Mutual Insurance Company">Nationwide Mutual Insurance Company</a>
    </td>
    <td>Financial
    </td>
    <td style="text-align:center;">54,609
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 6.1%
    </td>
    <td style="text-align:center;">24,118
    </td>
    <td><a href="/wiki/Columbus,_Ohio" title="Columbus, Ohio">Columbus, Ohio</a>
    </td></tr>
    <tr>
    <td>76
    </td>
    <td><a href="/wiki/Charter_Communications" title="Charter Communications">Charter Communications</a>
    </td>
    <td>Telecommunications
    </td>
    <td style="text-align:center;">54,607
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 1.1%
    </td>
    <td style="text-align:center;">101,100
    </td>
    <td><a href="/wiki/Stamford,_Connecticut" title="Stamford, Connecticut">Stamford, Connecticut</a>
    </td></tr>
    <tr>
    <td>77
    </td>
    <td><a href="/wiki/AbbVie" title="AbbVie">AbbVie</a>
    </td>
    <td>Pharmaceutical industry
    </td>
    <td style="text-align:center;">54,317
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -6.4%
    </td>
    <td style="text-align:center;">50,000
    </td>
    <td><a href="/wiki/Lake_Bluff,_Illinois" title="Lake Bluff, Illinois">Lake Bluff, Illinois</a>
    </td></tr>
    <tr>
    <td>78
    </td>
    <td><a href="/wiki/New_York_Life_Insurance_Company" title="New York Life Insurance Company">New York Life Insurance Company</a>
    </td>
    <td>Insurance
    </td>
    <td style="text-align:center;">54,317
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 14.2%
    </td>
    <td style="text-align:center;">15,384
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>79
    </td>
    <td><a href="/wiki/Intel" title="Intel">Intel</a>
    </td>
    <td>Technology
    </td>
    <td style="text-align:center;">54,228
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -14.0%
    </td>
    <td style="text-align:center;">124,800
    </td>
    <td><a href="/wiki/Santa_Clara,_California" title="Santa Clara, California">Santa Clara, California</a>
    </td></tr>
    <tr>
    <td>80
    </td>
    <td><a class="mw-redirect" href="/wiki/TJX" title="TJX">TJX</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">49,936
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 2.9%
    </td>
    <td style="text-align:center;">329,000
    </td>
    <td><a href="/wiki/Framingham,_Massachusetts" title="Framingham, Massachusetts">Framingham, Massachusetts</a>
    </td></tr>
    <tr>
    <td>81
    </td>
    <td><a href="/wiki/Prudential_Financial" title="Prudential Financial">Prudential Financial</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">53,979
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -10.1%
    </td>
    <td style="text-align:center;">40,366
    </td>
    <td><a href="/wiki/Newark,_New_Jersey" title="Newark, New Jersey">Newark, New Jersey</a>
    </td></tr>
    <tr>
    <td>82
    </td>
    <td><a class="mw-redirect" href="/wiki/HP_Inc" title="HP Inc">HP</a>
    </td>
    <td>Technology
    </td>
    <td style="text-align:center;">53,718
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -14.5%
    </td>
    <td style="text-align:center;">58,000
    </td>
    <td><a href="/wiki/Palo_Alto,_California" title="Palo Alto, California">Palo Alto, California</a>
    </td></tr>
    <tr>
    <td>83
    </td>
    <td><a href="/wiki/United_Airlines" title="United Airlines">United Airlines</a>
    </td>
    <td>Airline
    </td>
    <td style="text-align:center;">53,717
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 19.5%
    </td>
    <td style="text-align:center;">103,300
    </td>
    <td><a class="mw-redirect" href="/wiki/Chicago_Illinois" title="Chicago Illinois">Chicago, Illinois</a>
    </td></tr>
    <tr>
    <td>84
    </td>
    <td><a href="/wiki/Performance_Food_Group" title="Performance Food Group">Performance Food Group</a>
    </td>
    <td>Food processing
    </td>
    <td style="text-align:center;">53,355
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 13.1%
    </td>
    <td style="text-align:center;">34,825
    </td>
    <td><a href="/wiki/Richmond,_Virginia" title="Richmond, Virginia">Richmond, Virginia</a>
    </td></tr>
    <tr>
    <td>85
    </td>
    <td><a href="/wiki/Tyson_Foods" title="Tyson Foods">Tyson Foods</a>
    </td>
    <td>Food processing
    </td>
    <td style="text-align:center;">52,788
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -0.8%
    </td>
    <td style="text-align:center;">139,000
    </td>
    <td><a href="/wiki/Springdale,_Arkansas" title="Springdale, Arkansas">Springdale, Arkansas</a>
    </td></tr>
    <tr>
    <td>86
    </td>
    <td><a href="/wiki/American_Airlines" title="American Airlines">American Airlines</a>
    </td>
    <td>Airline
    </td>
    <td style="text-align:center;">52,788
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 7.8%
    </td>
    <td style="text-align:center;">132,100
    </td>
    <td><a href="/wiki/Fort_Worth,_Texas" title="Fort Worth, Texas">Fort Worth, Texas</a>
    </td></tr>
    <tr>
    <td>87
    </td>
    <td><a href="/wiki/Liberty_Mutual" title="Liberty Mutual">Liberty Mutual</a>
    </td>
    <td>Insurance
    </td>
    <td style="text-align:center;">52,612
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 5.3%
    </td>
    <td style="text-align:center;">45,000
    </td>
    <td><a href="/wiki/Boston" title="Boston">Boston, Massachusetts</a>
    </td></tr>
    <tr>
    <td>88
    </td>
    <td><a class="mw-redirect" href="/wiki/Nike_Inc" title="Nike Inc">Nike</a>
    </td>
    <td>Apparel
    </td>
    <td style="text-align:center;">51,217
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 9.6%
    </td>
    <td style="text-align:center;">83,700
    </td>
    <td><a href="/wiki/Beaverton,_Oregon" title="Beaverton, Oregon">Beaverton, Oregon</a>
    </td></tr>
    <tr>
    <td>89
    </td>
    <td><a href="/wiki/Oracle_Corporation" title="Oracle Corporation">Oracle Corporation</a>
    </td>
    <td>Technology
    </td>
    <td style="text-align:center;">49,954
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000500000000000000♠" style="display:none"></span> 17.7%
    </td>
    <td style="text-align:center;">164,000
    </td>
    <td><a href="/wiki/Austin,_Texas" title="Austin, Texas">Austin, Texas</a>
    </td></tr>
    <tr>
    <td>90
    </td>
    <td><a href="/wiki/Enterprise_Products" title="Enterprise Products">Enterprise Products</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">49,715
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -14.6%
    </td>
    <td style="text-align:center;">7,500
    </td>
    <td><a class="mw-redirect" href="/wiki/Houston,_Texas" title="Houston, Texas">Houston, Texas</a>
    </td></tr>
    <tr>
    <td>91
    </td>
    <td><a class="mw-redirect" href="/wiki/Capital_One_Financial" title="Capital One Financial">Capital One Financial</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">49,484
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 29.0%
    </td>
    <td style="text-align:center;">51,987
    </td>
    <td><a href="/wiki/Richmond,_Virginia" title="Richmond, Virginia">Richmond, Virginia</a>
    </td></tr>
    <tr>
    <td>92
    </td>
    <td><a href="/wiki/Plains_All_American_Pipeline" title="Plains All American Pipeline">Plains All American Pipeline</a>
    </td>
    <td>Petroleum industry
    </td>
    <td style="text-align:center;">48,712
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -15.1%
    </td>
    <td style="text-align:center;">4,200
    </td>
    <td><a class="mw-redirect" href="/wiki/Houston,_Texas" title="Houston, Texas">Houston, Texas</a>
    </td></tr>
    <tr>
    <td>93
    </td>
    <td><a href="/wiki/World_Kinect_Corporation" title="World Kinect Corporation">World Kinect Corporation</a>
    </td>
    <td>Energy trading
    </td>
    <td style="text-align:center;">47,711
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -19.2%
    </td>
    <td style="text-align:center;">5,289
    </td>
    <td><a href="/wiki/Doral,_Florida" title="Doral, Florida">Doral</a>, <a href="/wiki/Florida" title="Florida">Florida</a>
    </td></tr>
    <tr>
    <td>94
    </td>
    <td><a class="mw-redirect" href="/wiki/AIG" title="AIG">AIG</a>
    </td>
    <td>Insurance
    </td>
    <td style="text-align:center;">46,802
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -17.1%
    </td>
    <td style="text-align:center;">25,200
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>95
    </td>
    <td><a class="mw-redirect" href="/wiki/Coca-Cola_company" title="Coca-Cola company">Coca-Cola</a>
    </td>
    <td>Beverage
    </td>
    <td style="text-align:center;">45,754
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 6.4%
    </td>
    <td style="text-align:center;">79,100
    </td>
    <td><a class="mw-redirect" href="/wiki/Atlanta_Georgia" title="Atlanta Georgia">Atlanta, Georgia</a>
    </td></tr>
    <tr>
    <td>96
    </td>
    <td><a href="/wiki/TIAA" title="TIAA">TIAA</a>
    </td>
    <td>Financials
    </td>
    <td style="text-align:center;">45,735
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Increase"><img alt="Increase" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/20px-Increase2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Increase2.svg/40px-Increase2.svg.png 2x" width="11"/></span></span> <span data-sort-value="7000300000000000000♠" style="display:none"></span> 11.8%
    </td>
    <td style="text-align:center;">16,023
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City, New York</a>
    </td></tr>
    <tr>
    <td>97
    </td>
    <td><a class="mw-redirect" href="/wiki/CHS_Inc" title="CHS Inc">CHS</a>
    </td>
    <td>Agriculture cooperative
    </td>
    <td style="text-align:center;">45,590
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -4.6%
    </td>
    <td style="text-align:center;">10,609
    </td>
    <td><a class="mw-redirect" href="/wiki/Inver_Grove_Heights" title="Inver Grove Heights">Inver Grove Heights, Minnesota</a>
    </td></tr>
    <tr>
    <td>98
    </td>
    <td><a class="mw-redirect" href="/wiki/Bristol-Myers_Squibb" title="Bristol-Myers Squibb">Bristol-Myers Squibb</a>
    </td>
    <td>Pharmaceutical industry
    </td>
    <td style="text-align:center;">45,006
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -2.5%
    </td>
    <td style="text-align:center;">34,100
    </td>
    <td><a href="/wiki/New_York_City" title="New York City">New York City</a>, <a href="/wiki/New_York_(state)" title="New York (state)">New York</a>
    </td></tr>
    <tr>
    <td>99
    </td>
    <td><a href="/wiki/Dow_Chemical_Company" title="Dow Chemical Company">Dow Chemical Company</a>
    </td>
    <td><a href="/wiki/Chemical_industry" title="Chemical industry">Chemical industry</a>
    </td>
    <td style="text-align:center;">44,622
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -21.6%
    </td>
    <td style="text-align:center;">35,900
    </td>
    <td><a href="/wiki/Midland,_Michigan" title="Midland, Michigan">Midland, Michigan</a>
    </td></tr>
    <tr>
    <td>100
    </td>
    <td><a href="/wiki/Best_Buy" title="Best Buy">Best Buy</a>
    </td>
    <td>Retail
    </td>
    <td style="text-align:center;">43,452
    </td>
    <td style="text-align:center;"><span typeof="mw:File"><span title="Decrease"><img alt="Decrease" class="mw-file-element" data-file-height="300" data-file-width="300" decoding="async" height="11" src="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/20px-Decrease2.svg.png" srcset="//upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Decrease2.svg/40px-Decrease2.svg.png 2x" width="11"/></span></span> <span data-sort-value="2999450000000000000♠" style="display:none"></span> -6.1%
    </td>
    <td style="text-align:center;">85,000
    </td>
    <td><a href="/wiki/Richfield,_Minnesota" title="Richfield, Minnesota">Richfield, Minnesota</a>
    </td></tr></tbody></table>
    


```python
table_titles = table.find_all('th')
print(table_titles)
```

    [<th>Rank
    </th>, <th>Name
    </th>, <th>Industry
    </th>, <th>Revenue <br/>(USD millions)
    </th>, <th>Revenue growth
    </th>, <th>Employees
    </th>, <th>Headquarters
    </th>]
    


```python
world_table_titles = [titles.text.strip() for titles in table_titles]
print(world_table_titles)
```

    ['Rank', 'Name', 'Industry', 'Revenue (USD millions)', 'Revenue growth', 'Employees', 'Headquarters']
    


```python
import pandas as pd
df = pd.DataFrame(columns = world_table_titles)
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Name</th>
      <th>Industry</th>
      <th>Revenue (USD millions)</th>
      <th>Revenue growth</th>
      <th>Employees</th>
      <th>Headquarters</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
column_data = table.find_all('tr')
for row in column_data[1:]:
    row_data = row.find_all('td')
    individual_row_data = [data.text.strip() for data in row_data]
    length = len(df)
    df.loc[length] = individual_row_data
print(df)
```

        Rank                  Name                    Industry  \
    0      1               Walmart                      Retail   
    1      2                Amazon  Retail and cloud computing   
    2      3                 Apple        Electronics industry   
    3      4    UnitedHealth Group                  Healthcare   
    4      5    Berkshire Hathaway                Conglomerate   
    ..   ...                   ...                         ...   
    395   96                  TIAA                  Financials   
    396   97                   CHS     Agriculture cooperative   
    397   98  Bristol-Myers Squibb     Pharmaceutical industry   
    398   99  Dow Chemical Company           Chemical industry   
    399  100              Best Buy                      Retail   
    
        Revenue (USD millions) Revenue growth  Employees  \
    0                  648,125           6.0%  2,100,000   
    1                  574,785          11.9%  1,525,000   
    2                  383,482          -2.8%    161,000   
    3                  371,622          14.6%    440,000   
    4                  364,482          20.7%    396,500   
    ..                     ...            ...        ...   
    395                 45,735          11.8%     16,023   
    396                 45,590          -4.6%     10,609   
    397                 45,006          -2.5%     34,100   
    398                 44,622         -21.6%     35,900   
    399                 43,452          -6.1%     85,000   
    
                           Headquarters  
    0             Bentonville, Arkansas  
    1               Seattle, Washington  
    2             Cupertino, California  
    3             Minnetonka, Minnesota  
    4                   Omaha, Nebraska  
    ..                              ...  
    395         New York City, New York  
    396  Inver Grove Heights, Minnesota  
    397         New York City, New York  
    398               Midland, Michigan  
    399            Richfield, Minnesota  
    
    [400 rows x 7 columns]
    


```python
df.to_csv(r'C:\Users\user\Desktop\Recovery\KeneDanalyst\_My Dashboard Projects\Web Scrapping\wikipedia_list.csv', index=False)
```


```python

```
