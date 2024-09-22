You transform data when you convert it from one format into another. It can be as simple as converting a string to a list, or thousands of lists into dictionaries. Usually, it entails combining different data points. There are many ways to transform data, and ultimately the decisions depend on the type of data and the format you want it in.

Some examples of transforming data:

- Converting a date field format from December 28, 2019 to 28/12/19. 
    
- Converting a money amount in dollars to euros. 
    
- Standardizing email or postal addresses. 
    

For our UK news and communications example, we’ll save all the titles and descriptions from the HTML page into lists of strings. Instead of printing the string information to the console like earlier, we want to save the elements into a list:

```python
titles = soup.find_all("a", class_="gem-c-document-list__item-title")

for title in titles:
    print(title.string)
```

Here we start with an empty list called **titles.** Then we loop through all the elements in the **titles** list and append just the **string** version of the title into our titles list. Now the **titles** list will be a list of strings of all the titles on the HTML page : 

```
Joint Statement from Troika Capitals on South Sudan
Arnhem 80: Stories from the Second World War
Letter from the Secretary of State for Business & Trade on UKEF’s annual priorities
A political solution is urgently needed to bring stability to Syria and to the region: UK statement at the UN Security Council
Nuclear safeguards: AUKUS statement to the IAEA General Conference, September 2024
Nationally Significant Infrastructure Projects: updated advice pages phase two
IBCA Newsletter, 17 September 2024
Law sandwich placements offered at GLD for the first time
UK, US and Canada to collaborate on cybersecurity and AI research
UN Human Rights Council 57: UK Statement on the Right to Development
Fruquintinib approved to treat adult patients with metastatic colorectal cancer   
New protections from rogue energy brokers
Rare “river jelly lichen” discovered in the River Sprint
OPSS sponsored BSI PAS 7770 has been published
UK working to de-escalate and end cycle of violence in Middle East: UK statement at the UN Security Council
UN Human Rights Council 57: UK Statement on human rights situation in Venezuela
The Fourth AEM-UK Consultation
Permit consultation for Portland incinerator reopens
The expansion of Israeli settlements in the West Bank is wholly unacceptable and illegal: UK statement at the UN Security Council
Defence Secretary visits British Army headquarters to thank personnel
```

We going to do the same with description, but we dont want only to print the description string element. We need to save them somewhere!

1) we create an empty list :

```python 
string_titles = []
```

2) then we gonna append the string title in that list 

```python
for title in titles:
...     string_titles.append(title.string)
```

3) now when we want print we can use : "string_titles"

```python
 >>> string_titles

['Joint Statement from Troika Capitals on South Sudan', 'Arnhem 80: Stories from the Second World War', 'Letter from the Secretary of State for Business & Trade on UKEF’s annual priorities', 'A political solution is urgently needed to bring stability to Syria and to the region: UK statement at the UN Security Council', 'Nuclear safeguards: AUKUS statement to the IAEA General Conference, September 2024', 'Nationally Significant Infrastructure Projects: updated advice pages phase two', 'IBCA Newsletter, 17 September 2024', 'Law sandwich placements offered at GLD for the first time', 'UK, US and Canada to collaborate on cybersecurity and AI research', 'UN Human Rights Council 57: UK Statement on the Right to Development', 'Fruquintinib approved to treat adult patients with metastatic colorectal cancer \u202f\u202f', 'New protections from rogue energy brokers', 'Rare “river jelly lichen” discovered in the River Sprint', 'OPSS sponsored BSI PAS 7770 has been published', 'UK working to de-escalate and end cycle of violence in Middle East: UK statement at the UN Security Council', 'UN Human Rights Council 57: UK Statement on human rights situation in Venezuela', 'The Fourth AEM-UK Consultation', 'Permit consultation for Portland incinerator reopens', 'The expansion of Israeli settlements in the West Bank is wholly unacceptable and illegal: UK statement at the UN Security Council', 'Defence Secretary visits British Army headquarters to thank personnel']
```

For the descriptions : 

```python
>>> string_descriptions = []
>>> for description in descriptions:
...     string_descriptions.append(description.string)
...
>>> string_descriptions
["Statement by the Governments of Norway, the United Kingdom and the United States on the announcement by South Sudan’s leaders of an extension of the country's transitional period.", 'The Battle of Arnhem was one of the most audacious endeavours of the Second World War. On the 80th anniversary, discover selected stories from the front line.', 'A letter from the Secretary of State for Business & Trade to UK Export Finance’s Chief Executive on UKEF’s annual priorities.', 'Statement by Fergus Eckersley, Minister Counsellor, at the Security Council meeting on Syria.', 'Statement by Australia, the UK and the US to the International Atomic Energy Agency General Conference on IAEA safeguards and AUKUS', 'The Planning Inspectorate has published the second set of updated advice pages for applicants and others about a range of operational matters under the Planning Act 2008. ', "Infected Blood Compensation Authority's newsletter that was circulated on 17 September 2024.", 'Students will join GLD from September 2024 for 10 months ', 'Military science and technology organisations agree to partner on critical research areas in support of defence and security.  ', 'UK Statement for the Interactive  Dialogue with the Special Rapporteur on the Right to Development. Delivered at the 57th HRC in Geneva. ', '\u202fThe Medicines and Healthcare products Regulatory Agency (MHRA) has today, 20 September, approved the new medicine fruquintinib (Fruzaqla) to treat adult patients with metastatic colorectal cancer (CRC). It is used when othe…', 'New government consultation will investigate introducing regulations for third-party services in the energy retail market\u202fto protect consumers and businesses.', " One of the world's rarest lichens  has been discovered in a Cumbrian River for the first time in memory and represents a significant biodiversity milestone.  ", 'OPSS supports new guidance to reduce the environmental impact of electronic product design.', 'Statement by Ambassador James Kariuki, UK Deputy Permanent Representative to the UN, at the UN Security Council meeting on the situation in the Middle East.', "Interactive Dialogue with the Independent International Fact-Finding Mission on Venezuela. Delivered by the UK's Ambassador to the WTO and UN, Simon Manley. ", 'The Fourth ASEAN Economic Ministers (AEM) – the United Kingdom of Great Britain and Northern Ireland (UK) Consultation was held on the 19th September 2024.\r\n', 'A chance for local people to have their say on waste plans', 'Statement by UK Permanent Representative to the UN, Ambassador Barbara Woodward, at the UN Security Council meeting on the situation in the Middle East.', 'Defence Secretary visited Army headquarters at Andover to meet personnel. It is central to keeping the UK safe at home and secure abroad.\r\n\r\n']
```
