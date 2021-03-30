# Amazon-Web-Scrapping

## The goal of this scrapper is to use web crawling techniques to gather and represent product listing information from the Amazon websit and analyzing the manufacturer's online marketplace position in terms of the best deals available and conducting a text analysis of the features

It consists of three phases: 

Phase 1: The first component is a utility that connects to the Amazon website using the user's input product, collects the unique identifiers of all similar products listed on this page, loops through similar pages, and saves the information to a text file. 

Phase 2: The scrapper's second component iterates through this text file, connects to all of Amazon's product listings, and extracts and stores the gathered data into a database using web scraping techniques. 

Phase 3: Using the information extracted and stored in the database, this phase involves doing a quadrant analysis (similar to a brand map) for analyzing a manufacturer's position with respect to discount and original prices. This can help consumers understand on what discount points an the product from the same manufacturer be available. This phase also involves doing a text analysis and creating a word cloud of the features that are listed by the sellers. Consumers can get a better understanding of what are the important/similar features across products of the same category. 


## Key features extracted 
1. Unique ID given by Amazon to a product
2. URL of the product
3. Name of the product
4. Current Price of the product
5. List Price of the product
6. List of features (Each list pointer separated by ||)
7. Primary category of the product
8. Secondary category of the product
9. Seller's Name
10. Manufacturer's Name
11. Rank of the Product
12. Star rating of the product (floating point decimal with one digit after the decimal)
13. Total number of Rating given
14. Number of reviews for the product
15. Number of questions answered
16. Availability of the product as described in words
                              

Limitation: Product listings in Amazon, often differ a lot in terms of the structure in which the details are stored. Price is often saved in several tags, including "priceblock_dealprice" and "priceblock_saleprice," to name a few. This code relies on these names, as well as the tags in which they are stored. If Amazon captures data in different formats across pages or if these unique identifiers are changed in the future, the code will no longer be able to fetch results. Also, headless browser or Amazon API has not been used to extract details, hence running multiple times may results in CAPTCHA issues. 
