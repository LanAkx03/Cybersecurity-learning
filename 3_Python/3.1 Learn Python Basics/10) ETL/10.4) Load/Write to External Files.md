To understand writing to external files, let’s go back to our web scraping example. We’ve already written the code to extract and transform the data from the UK government services and information website. We have all the **titles** and **descriptions** saved as lists of strings. Now we can use the  `.writer()`  and  `.writerow()`  functions to write the data into a CSV file.

```python
#Create list for the headers
headers = ["title", "description"]
 
#Open a new file to write to called ‘data.csv’
with open('data.csv', 'w', newline='') as csvfile:
    #Create a writer object with that file
    writer = csv.writer(csvfile, delimiter=',')
    writer.writerow(headers)
    #Loop through each element in titles and descriptions lists
    for i in range(len(titles)):
        #Create a new row with the title and description at that point in the loop
        row = [titles[i], descriptions[i]]
        writer.writerow(row)
```

```python
>>> import requests
>>> import csv
>>>
>>> from bs4 import BeautifulSoup
>>>
>>> url = 'https://www.gov.uk/search/news-and-communications'
>>>
>>> page = requests.get(url)
>>>
>>> soup = BeautifulSoup(page.content, 'html.parser')
>>>
>>> titles = soup.find_all("a", class_="govuk-link govuk-link--no-underline")
>>> descriptions = soup.find_all("p", class_="gem-c-document-list__item-description")
```

```python
Microsoft Windows [version 10.0.19045.4894]
(c) Microsoft Corporation. Tous droits réservés.

C:\Users\lanak>cd documents

C:\Users\lanak\Documents>cd github

C:\Users\lanak\Documents\GitHub>cd python

C:\Users\lanak\Documents\GitHub\Python>dir /B
'Web
favorite_colors.csv
scraping

C:\Users\lanak\Documents\GitHub\Python>cd scraping

C:\Users\lanak\Documents\GitHub\Python\scraping>python
Python 3.12.6 (tags/v3.12.6:a4a2d2b, Sep  6 2024, 20:11:23) [MSC v.1940 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
>>> import requests
>>> import csv
>>>
>>> from bs4 import BeautifulSoup
>>>
>>> url = 'https://www.gov.uk/search/news-and-communications'
>>>
>>> page = requests.get(url)
>>>
>>> soup = BeautifulSoup(page.content, 'html.parser')
>>> 
>>> bs_titles = soup.find_all("a", class_="govuk-link govuk-link--no-underline")
>>>
>>> bs_descriptions = soup.find_all("p", class_="gem-c-document-list__item-description")
>>>
>>> for description in bs_descriptions:
...     print(description.string)
>>>
>>> for title in bs_titles:
...     print(title.string)
>>
>>> string_titles = []
>>> 
>>> for title in bs_titles:
...     string_titles.append(title.string)
...
...
>>> string_descriptions = []
>>> 
>>> for description in bs_descriptions:
...     string_descriptions.append(description.string)
...
>>> string_titles
>>> string_descriptions
>>> 
>>> headers = ["title", "description"]
```