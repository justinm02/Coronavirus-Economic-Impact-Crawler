# Coronavirus-Economic-Impact-Crawler

The goal of this task was to generate at least 1000 pages/URL's that relate to COVID-19's economic impact within a 6 hour period. 

My approach for this task was to consider the String content of URL's from CommonCrawl data and determine if any contained key words along the lines of 
"Coronavirus" and "Economy." If the URL matched these key words, then I simply added the URL and its associated publish date to a dictionary.

I attempted several optimizations to this approach in order to allow for a faster runtime with a greater number of results, but I unfortunately was unable to make
them working efficiently by the end of the 6 hour period. 

The first optimization I attempted was to consider the actual title and text information for each of the
pages by processing the WET response formats. However, I realized that even though the text content within each page is a better indicator than the limited 
information in a simple URL, the amount of time that it would take to process all the textual information greatly exceeded the time taken to process a URL. If I had
more time to continue experimenting with this approach, I would have tried to obtain just the title information in amortized O(1) time, which would on average seem 
to take around the same time to process a URL while yielding a greater quantity of valid pages.

The second optimization that I would make to my code would be to only consider relevant data that is known to contain a significant amount of Coronavirus related 
pages. I did try to make a small attempt at this by focusing on 2020 data from March through April due to the greater fear and national attention the virus
epidemic had on the US and other western countries during that time, but it simply wasn't enough to decrease runtime. Given more time, I would conduct a lot more
research on the given CommonCrawl data and see if there is a way to look at the main focus of each WARC segment.

Overall, I am very pleased with my results, especially for my first time ever working with any form of data scraping. I may not have been able to produce 1000 
results within the allotted 6 hours, but my code does at the very least have the potential to produce a significantly large quantity of valid results: 
it would just require a lot of computing time that I unfortunately did not have. 
