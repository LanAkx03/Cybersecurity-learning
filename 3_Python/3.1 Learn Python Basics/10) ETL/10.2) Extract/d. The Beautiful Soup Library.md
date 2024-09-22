
Now that we have the HTML source, we need to parse it. The way to parse the HTML is through the HTML attributes of  `class`  and  `id`  mentioned earlier.

```python
import requests

from bs4 import BeautifulSoup

url = "https://gov.uk/search/news-and-communications"

page = requests.get(url)

  

soup = BeautifulSoup(page.content, 'html.parser')
```

In the terminal :
```python
C:\Users\lanak\Documents>python
Python 3.12.6 (tags/v3.12.6:a4a2d2b, Sep  6 2024, 20:11:23) [MSC v.1940 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import requests
>>> from bs4 import BeautifulSoup
>>> url = "https://www.gov.uk/search/news-and-communications"
>>> page = requests.get(url)
>>> page.content
```


```python
>>> soup = BeautifulSoup(page.content, 'html.parser')
```
Now we have the 'soup' object. We can interact with this object directly in our python consol 

Let get the title of the webpage

```python
>>> soup.title
<title>News and communications - GOV.UK</title>
```

Let get now the titles and the description of the different stories
- to do that we have to identify the specific **identifier** for both of this things to be able to use BeautifulSoup and quary just those items from the HTML code

For the title: 
```html
<div class="gem-c-document-list__item-title">    
```

          

```html
<div class="gem-c-document-list__item-title">          
	<a data-ga4-ecommerce-path="/government/news/joint-statement-from-troika-
	capitals-on-south-sudan" data-ga4-ecommerce-content-id="ce4446b1-d96b-44c1-
	afef-b3239c649eac" data-ga4-ecommerce-row="1" data-ga4-ecommerce-index="1" 
	class="  govuk-link govuk-link--no-underline" href="/government/news/joint-
	statement-from-troika-capitals-on-south-sudan">Joint Statement from Troika 
	Capitals on South Sudan</a>
</div>
```

*class: "govuk-link govuk-link--no-underline"* **AND NOT** "*gem-c-document-list__item-title*"
They changed the site structure. Then : 

```python
soup.find_all("a", class_="govuk-link govuk-link--no-underline")
```

For the description:
```html
<p class="gem-c-document-list__item-description">
```

```html
<p class="gem-c-document-list__item-description ">Statement by the Governments of Norway, the United Kingdom and the United States on the announcement by South Sudan’s leaders of an extension of the country's transitional period.</p>
```

```python
soup.find_all("p", class_="gem-c-document-list__item-description")
```

For more about BeautifulSoup : https://www.crummy.com/software/BeautifulSoup/bs4/doc/
For more abour Requests : https://requests.readthedocs.io/en/latest/
