# Flipkart-Product-Tracker
 
Flipkart Product Availability Tracker
Overview
This is a simple Python script that allows you to track the availability of a product on Flipkart and receive notifications via email when the product becomes available. It uses the ScraperAPI service to scrape product information from Flipkart's website.

Prerequisites
Before using this script, make sure you have the following prerequisites installed:

Python 3.x
Requests library: pip install requests
BeautifulSoup library: pip install beautifulsoup4
The send_email module for sending email notifications (You may need to implement this module yourself).
Usage
Import the required libraries at the beginning of your Python script:
python
Copy code
import requests
from bs4 import BeautifulSoup
import time
from send_email import send_info
Define your Flipkart product URL and recipient email address:
python
Copy code
product_url = input("Enter the Flipkart product URL: ")
recipient_email = input("Enter your email address: ")
Run the script, and it will prompt you to choose whether to automate availability checking and receive email notifications. You can choose to automate the process or not.

If you choose to automate checking, the script will continuously monitor the product's availability and send you an email notification when the product becomes available.

Functions
check_product_availability(product_url, recipient_email)
This function checks the availability of the specified product on Flipkart and sends an email notification when the product is available.

product_url: The URL of the Flipkart product you want to track.
recipient_email: Your email address to receive availability notifications.
get_product_price(soup)
This function extracts the product price from the product page.

soup: The BeautifulSoup object containing the HTML of the product page.
get_product_ratings(soup)
This function extracts the product ratings from the product page.

soup: The BeautifulSoup object containing the HTML of the product page.
get_product_reviews(soup)
This function extracts the product reviews from the product page.

soup: The BeautifulSoup object containing the HTML of the product page.
Note
The script uses ScraperAPI to bypass any anti-scraping measures on the Flipkart website. You will need to sign up for ScraperAPI and obtain an API key to use this service.
You may need to implement the send_info function to send email notifications with the product details.
License
This script is provided under the MIT License. Feel free to modify and use it as needed.

Disclaimer: This script is for educational and personal use only. Please review Flipkart's terms of service and scraping policies before using this script, and use it responsibly.
