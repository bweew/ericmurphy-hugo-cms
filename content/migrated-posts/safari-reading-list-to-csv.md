---
title: 'safari reading list to csv'
date: 2024-03-05T06:04:00.003-05:00
draft: false
url: /2024/03/safari-reading-list-to-csv.html
---

So you've added a bunch of links to the reading list but now you want to get them all at once out as csv?

1.  open safari on mac
2.  file export bookmarks
3.  it will save as Safari Bookmarks.html
4.  run this python script in that directory

```
from bs4 import BeautifulSoup
import csv

# Open the Safari Bookmarks HTML file
with open('Safari Bookmarks.html', 'r') as file:
    html_content = file.read()

# Parse HTML content
soup = BeautifulSoup(html_content, 'html.parser')

# Find the Reading List section
reading_list_section = soup.find('h3', id='com.apple.ReadingList')

# Check if the Reading List section exists
if reading_list_section:
    # Find all links in the Reading List section
    links = reading_list_section.find_next_sibling('dl').find_all('a')

    # Write links to CSV
    with open('reading_list.csv', 'w', newline='', encoding='utf-8') as csvfile:
        writer = csv.writer(csvfile)
        # Write each link as a row in the CSV without a header
        for link in links:
            writer.writerow([link.get('href'), link.text.strip()])
else:
    print("Reading List section not found in the HTML.") 
```

there's also this one which grabs it from the source  
[https://github.com/smrfeld/export-safari-reading-list?tab=readme-ov-file](plist%20extractor)

a gotcha for this to generate the website you

1.  generate the json
2.  generate the thumbnails folder
3.  git clone the repo and cd into the website folder
4.  python3 website.py 'thejson' 'theimgfolder'
5.  it generates the static file in the website output folder

THE IMAGES DONT WORK!!!  
okay looking at the source i saw the path to the images is wrong in all of them but its an easy fix.  
\- wheen the static site files were created it created an extra folder you dont want its 'readinglistarchives'  
\- once you get rid of that your golden