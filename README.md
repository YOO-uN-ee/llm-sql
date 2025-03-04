# Writing and Executing SQL Queries
In this task, you will use n SQL database management system of your choice (e.g., MySQL, PostgreSQL) to construct and execute queries that answer the given questions.

## Data Description
In this task, we will imagine an alternate universe that hosts a global sporting event called Aolympics, held every three years. Aolympics features the same sports as the Olympics; however, all details—including athlete names, event years, host cities, and countries—are entirely fictional. There are four datasets provided to you: `athlete_event`, `nac_regions`, `cities`, `countries`

### athlete_event
The following describes the schema of the data
- `name`: name of the participating athelete
- `sex`: biological sex
- `age`: age of the participating athelete at the year they have participated
- `team`: country name of which the participating athelete is representing
- `NAC`: the NAC code of which the athelete is representing
- `games`: official name of the Aolympic
- `city`: host city of the Aolympic
- `sport`: sport in which the athelete is particpating in
- `event`: subdivision sport name of the event the athelete is participating in
- `medal`: status of medal. can only be Gold, Silver, Bronze, or NA

### nac_regions
The following describes the schema of the data
- `NAC`: three character NAC code that uniquely represents each country
- `name`: name of the country

### cities
The following describes the schema of the data
- `name`: name of the city
- `country_id`: id of the country in which the city is located
- `country_name`: name of the country in which the city is located

### countries
The following describes the schema of the data
- `name`: name of the country
- `iso3`: ISO3 code of the country
- `capital`: capital of the country
- `phonecode`: phone extension code of the country


## Questions 1
List all distinct cities that have ever hosted an Aolympic. Also provide the official name of the Aolympic. Sort in alphabetical order or city name.
### True Answer
| city | games |
| --- | --- |
| Bihmore | 3141 Summer |
| Boiyrith | 3120 Winter |
| Bulvine | 3195 Summer |
| Caupolis | 3162 Winter |
| Chimmond | 3240 Winter |
| Chouhron | 3135 Summer |
| Chuuncester | 3216 Winter |
| Cirta | 3159 Summer |
| Claapbert | 3168 Winter |
| Ecuystead | 3243 Summer |
| Elifhull | 3180 Winter |
| Eploson | 3174 Winter |
| Ewreburgh | 3126 Winter |
| Floxsa | 3219 Summer |
| Frexver | 3231 Summer |
| Frixrith | 3108 Winter |
| Greapdiff | 3189 Summer |
| Haanby | 3177 Summer |
| Haitding | 3150 Winter |
| Isunsea | 3129 Summer |
| Iyremouth | 3225 Summer |
| Izadsea | 3144 Winter |
| Kihham | 3147 Summer |
| Koixson | 3153 Summer |
| Leayrora | 3246 Winter |
| Ledgow | 3234 Winter |
| Miahgan | 3165 Summer |
| Muotfield | 3093 Summer |
| Nuupling | 3087 Summer |
| Opruabus | 3081 Summer |
| Ostrifvine | 3063 Summer |
| Oyluxby | 3123 Summer |
| Phoumton | 3183 Summer |
| Phupson | 3186 Winter |
| Praukport | 3111 Summer |
| Pruiswell | 3192 Winter |
| Qouklens | 3132 Winter |
| Qraihbert | 3069 Summer |
| Quipmore | 3156 Winter |
| Saarrith | 3171 Summer |
| Soiygas | 3105 Summer |
| Stiyhull | 3204 Winter |
| Troudsea | 3213 Summer |
| Ublitland | 3222 Winter |
| Ushuihta | 3210 Winter |
| Vrualsas | 3207 Summer |
| Vuedson | 3075 Summer |
| Yhinphia | 3201 Summer |
| Yreelphia | 3198 Winter |
| Zhessall | 3237 Summer |
| Zhonwell | 3228 Winter |
| Zhoyford | 3114 Winter |
| Zlopchester | 3138 Winter |
| Zrefville | 3099 Summer |
| Zrehphia | 3117 Summer |

### LLM Executed Answer
| Chat GPT | Le Chat | DeepSeek |
| --- | --- | --- |
| &check; | &check; |  |

## Question 2
Who earned the most Gold medal throughout the history of Aolympic. Give the count of gold medals

### True Answer
| name | gold_count |
| --- | --- |
| Tomoya Suzuki | 23 |

### LLM Result
| Chat GPT | Le Chat | DeepSeek |
| --- | --- | --- |
| &#x58; | &#x58; | &#x58; |

## Questions 3
Give the information (Name, Sex, Birth Year, NAC) of the oldest Aolympic participant.

### True Answer
| Name | Sex | Birth Year | NAC |
| --- | --- | --- | --- |
| Isaac Kindle | M | 3141 | ATR |

### LLM Results
| Chat GPT | Le Chat | DeepSeek |
| --- | --- | --- |
| &#x58; | &#x58; | &#x58; |

- ChatGPT uses a line of code that uses the 'actual' current date
- Le Chat uses a line of code that uses the 'actual' current date
- DeepSeek: syntax error

## Question 4
List the top 5 nations (by country name) that had the most representing atheletes throughout the history of the Aolympics. For each of these nations, report the total number of medals won across all Aolympic events and the number of athelete who have represented them.

### True Answer
| country_name | medal_count | participants |
| --- | --- | --- |
| Keglus | 5692 | 9577 |
| Glia Crain | 2132 | 6292 |
| Aprana | 1825 | 6132 |
| Bagrales | 1678 | 4936 |
| Gliedor | 1395 | 4837 |


### LLM Results
| Chat GPT | Le Chat | DeepSeek |
| --- | --- | --- |
| &#x58; | &#x58; | &#x58; |

- ChatGPT reports in country NAC code instead of country name, incorrect participants
- Le Chat: Correct country info, incorrect medal_count, participants
- DeepSeek: Incorrect order

## Question 5
Determine which country has hosted the most Aolympic events and provide the total number of medals awarded by that country. Also, identify the country that received the highest number of medals from all Aolympics hosted by that nation. Report all countries using their NAC codes.

### True Answer
| host_country | medal_count | highest_received | 
| --- | --- | --- |
| KEG | 5361 | KEG |

### LLM Results
| Chat GPT | Le Chat | DeepSeek |
| --- | --- | --- |
| &check; | &#x58; |  |

- ChatGPT requires manual processing of the code. It does not perform this task in one code block.
- Le Chat: Not executed

## Question 6
A nation’s final ranking is determined by prioritizing the number of Gold medals won. If there is a tie, Silver medals are considered, followed by Bronze medals. Identify the country that ranked fourth in the Aolympics held in the year 3213. Give the name of the country, count of gold, silver, and bronze medals.

### True Answer
| Country Name | Gold Count | Silver Count | Bronze Count |
| --- | --- | --- | --- |
| Clef Flana | 37 | 9 | 26 |

### LLM Results
| Chat GPT | Le Chat | DeepSeek |
| --- | --- | --- |
| &#9651; | &check; | &#x58; |

- ChatGPT reports the NAC code of the country instead of the country name.
- DeepSeek does not execute