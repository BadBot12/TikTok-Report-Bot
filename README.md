import requests

ACCESS_TOKEN = "your_access_token_here"
url = "https://open.tiktokapis.com/v2/video/list/"

headers = {
    "Authorization": f"Bearer {ACCESS_TOKEN}",
    "Content-Type": "application/json"
}

response = requests.get(url, headers=headers)
print(response.json())
from selenium import webdriver
from selenium.webdriver.common.by import By
import time

driver = webdriver.Chrome()

driver.get("https://www.tiktok.com/")
time.sleep(5)

# Example: Search for a hashtag
search_box = driver.find_element(By.XPATH, '//input[@placeholder="Search accounts and videos"]')
search_box.send_keys("#python")
search_box.submit()

time.sleep(10)
driver.quit()
