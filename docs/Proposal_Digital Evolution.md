# Digital Evolution in Great Britain: Insights into Internet Penetration, User Behaviors, and Trust from 2015-2020

- **Author:** Alisha Minj
- **Prepared for UMBC Data Science Master Degree Capstone by:** Dr. Chaojie (Jay) Wang
- **GitHub Profile:** [Alisha Minj's GitHub](#)
- **LinkedIn:** [Alisha Minj's LinkedIn](#)
- **PowerPoint Presentation:** [To be updated]
- **YouTube Video:** [To be updated]

## Background

### What is it about?

The dawn of the digital age brought forth a transformative force: the internet. Over the years, what began as a novel tool for a select few has burgeoned into a global phenomenon, deeply intertwined with the daily lives of billions. This project embarks on a rigorous exploration of Great Britain's journey through this digital evolution, spanning from the rapid growth of internet accessibility in households to the multifaceted online behaviors exhibited by its citizens. Specifically, we probe into the realms of e-commerce, digital financial activities, and the ever-pertinent concerns of online security and trust.

### Why does it matter?

As the internet's tendrils extend further into our personal, professional, and societal domains, the significance of understanding its implications magnifies. A nuanced grasp of internet behaviors doesn't merely offer a mirror to societal trends; it equips businesses with invaluable insights, guides policy-making, and fosters an informed citizenry. In an era where commerce, communication, and even concerns of privacy are increasingly digital, a comprehensive understanding of these patterns holds the promise of a more secure, efficient, and connected future.

### Research Questions:

1. **Digital Evolution:** How has the landscape of internet penetration in Great Britain transformed from 2015 to 2020, and what implications does this trajectory hold for the future?
2. **E-commerce Exploration:** As e-commerce platforms burgeon, what patterns of behavior can we discern amongst users? How have shopping habits evolved with increasing digitization, and what does this reveal about modern consumer preferences? 
    - *E-commerce and Online Behavioral Analysis:* Beyond shopping, what online patterns emerge as users engage with the vast digital realm? This encompasses e-commerce trends, financial activities, and more.
3. **Digital Trust and Security Landscape:** In a world that's increasingly online, how do perceptions of privacy, data protection, and online security manifest amongst the populace? Are there discernible shifts in trust, and if so, what factors might be influencing them?

## Data

### Data Source:

- **Dataset Name:** Internet Access - Households and Individuals.
- **Description:** This dataset provides an annual assessment of internet usage in Great Britain. It encompasses areas such as frequency of internet use, the array of activities individuals engage in while online, and the evolving patterns in online purchasing.
- **Source:** [Office for National Statistics (ONS)](https://www.ons.gov.uk/)

### Data Size:

The cumulative size of the data for all years (from 2015 to 2020) is approximately 2.937 MB. The individual file sizes are as follows:

- 2015: 512 KB
- 2016: 547 KB
- 2017: 502 KB
- 2018: 453 KB
- 2019: 235 KB
- 2020: 188 KB

### Tables of Focus:

- **Households with Internet Access (1998 - 2020):** The percentage of households with internet access in a given year.
- **Frequency of Internet Use (2006 to 2020):** Provides insights into how often individuals access the internet in a given year.
- **Internet Activities (2007 to 2020):** Highlights various activities people engage in while online for each year.
- **Demographic Insights into Online Shopping Trends (2008 - 2020):** Offers a demographic breakdown of online shopping trends.
- **Online Purchases, By Age Group, Sex, And Disability Status (2018 - 2020):** Breaks down online purchases based on specific categories and demographics.

## Digital Evolution: Deciphering E-commerce Behavior

### Datasets:

**Online Shopping Trends (2008-2020)** and **Online Purchases (2018-2020)**

| Feature/Variable | Data Type | Description |
|---|---|---|
| Year | Integer | The year for which data is collected (from 2008 to 2020) |
| All | Float | Percentage of all individuals who have shopped online in the last 12 months |
| Men | Float | Percentage of men who have shopped online in the last 12 months |
| Women | Float | Percentage of women who have shopped online in the last 12 months |
| Age Group (16-24) | Float | Percentage of individuals aged 16-24 who have shopped online in the last 12 months |
| Age Group (25-34) | Float | Percentage of individuals aged 25-34 who have shopped online in the last 12 months |
| ... | ... | ... |
| Equality Act disabled | Float | Percentage of individuals who are disabled (as per the Equality Act) who have shopped online in the last 12 months |
| Not Equality Act disabled | Float | Percentage of individuals who are not disabled (as per the Equality Act) who have shopped online in the last 12 months |
| Product/Service (e.g., Clothes, Deliveries from restaurants) | String | The category of the product/service purchased online |

**Target Variable/Label:** 

- Percentage of a specific demographic (e.g., Men, Women, Age Group, etc.) who have shopped online in the last 12 months for a given year.
- Percentage of a specific demographic or the overall population who have made a certain type of purchase online within the last 3 months.

**Potential Features/Predictors:** 

- Year, Percentage values from different demographic groups from previous years.
- Product/Service Category, Percentage values from different demographic groups from previous months/years, and overall online shopping trends from the "Online_Shopping_Trends_2008_2020.csv" dataset.
