# Web Scraping with Selenium and Pandas
**Overview**

This repository contains Python scripts for scraping data from GitHub and LinkedIn using Selenium and Pandas libraries.

# GitHub Scraper

The GitHubBot class in github_bot.py scrapes repository data from a GitHub user's profile.

**Usage**

- Instantiate the GitHubBot class.

- Open the GitHub profile URL.

- Click on the "Repositories" tab.

- Scrape the repository titles and programming languages.

bot = GitHubBot()

bot.open_url('https://github.com/CrystalEFernandes')

bot.click_repositories_tab()

titles, languages = bot.scrape_repositories_data()

# LinkedIn Scraper

The LinkedInBot class in linkedin_bot.py scrapes profile data, including title, experiences, education, activities, and certifications, from a LinkedIn user's profile.

**Usage**

- Instantiate the LinkedInBot class.
  
- Open the LinkedIn profile URL.

- Scrape the profile data.

bot = LinkedInBot()

bot.open_url('https://www.linkedin.com/in/crystal-fernandes-752347263/')

linkedin_profile = bot.scrape_data() 

experiences_text = bot.scrape_experience()

education_text = bot.scrape_education()

activities_text = bot.scrape_activities()

certifications_text = bot.scrape_certifications()

# Flipkart(2023)

The Flipkart class in flipkart_bot.py scrapes product data from Flipkart, including product name, price, image URLs, seller information, specifications, reviews, and size chart (if available).

**Usage**

Instantiate the Flipkart class.

Pass the Flipkart search URL to the control method to scrape data.

url = 'https://www.flipkart.com/search?q=dunder+mifflin+t+shirt&otracker=AS_Query_HistoryAutoSuggest_5_0&otracker1=AS_Query_HistoryAutoSuggest_5_0&marketplace=FLIPKART&as-show=on&as=off&as-pos=5&as-type=HISTORY'

flipkart = Flipkart()

merged_df = flipkart.control(url)

# Amazon(2023)
The Amazon class in amazon_bot.py scrapes product data from Amazon, including product name, price, image URLs, about information, features, technical information, product ratings, and size chart (if available).

**Usage**

Instantiate the Amazon class.

Pass the Amazon search URL to the control method to scrape data.

url = 'https://www.amazon.in/s?k=t-shirt+below+50&ref=nb_sb_noss'

amazon = Amazon()

merged_df = amazon.control(url)

# Requirements

Python 3.x

Selenium

Pandas

Numpy

Fake User-Agent

# Setup

Install the required packages:

Copy code

pip install selenium pandas numpy fake-useragent

Download the appropriate ChromeDriver and specify the path in the respective bot classes.
