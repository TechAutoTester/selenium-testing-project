# selenium-testing-project.
# My first selenium testing project using python for opening the chrome browser with selenium 4 version.
# Download latest chrome web driver  and read the path.
# Installing the selenium package
pip install selenium
# importing the web driver from selenium.
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
serv_obj=Service(path)      # path of the chrome driver extention.
driver=webdriver.Chrome(service=serv_obj)  # driver object creation with Chrome class.
driver.implicility_wait(10)                    
driver.get(https://www.google.com)    # url: google search page
driver.maximize_window()                # maximize the browser window
expected_title=driver.title()
actual_title="Google"
if actual_title==expected_title:
  print("test passed")
else:
  print("test failed")
driver.close()
driver.quit()
