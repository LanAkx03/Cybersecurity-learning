
To extract data from the website, we need to use the **requests** library. Remember that it provides functionality for making HTTP requests. We can use it since we’re trying to get data from a website that uses the HTTP protocol (e.g., [**http:**//google.com](https://google.com/)). 

The requests library contains a **`.get()`**function that we can use to get the HTML from the site.  

To apply this to the web scraping exercise, we’ll use the **requests** library to get the HTML of the UK news and communications page into our Python code. In the code below, we import the library, save the URL we want to web scrape in a  `url`  variable, and then use the  `.get()`  method to retrieve the HTML data. If you run the code below, you'll see the HTML source printed out in the console.

```python
import requests
url = "https://gov.uk/search/news-and-communications"
page = requests.get(url)

print(page.content)
```

