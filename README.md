![Skincare1](https://user-images.githubusercontent.com/78176162/185502216-1b8d313c-8763-4454-acbf-1f080bc88b67.jpg)


# Capstone Project

### Affordable Product Recommendation of Luxury Skincare Products Using NLP's BERT Technique


**Name:** Nazia Noor

**Course:** DATA606

**Instructor:** Dr. Chaojie (Jay) Wang

### Keywords: 

*NLP, BERT Technique, Recommendation System, Skincare Industry*

# Abstract:
The market for premium skincare products is strong. However, a significant section of the clients cannot afford expensive skincare products. The aim of this study was to identify cost-effective alternatives for high-end skincare items. I applied NLP's BERT model for this (Bidirectional Encoder Representations from Transformers). This is a well-known method that Google developed to extract traits from text data.

The data was extracted from the "Look Fantastic" e-commerce website.13 attributes in total were obtained from the website. The final dataset was created after deleting, adding additional columns, and eliminating and imputing null values. The final dataset has nine attributes. Data from three columns—"name," "product details," and "ingredients"—were combined for modeling purposes, and the BERT model was used to analyze the results. The first stage involved utilizing BERT's pre-trained sentence transformer "bert-base-nli-mean-tokens" to obtain the sentence embeddings. Finding the cosine similarity of the text was the second stage. The last stage was to choose the most expensive item from the top three skincare categories—cream, cleanser, and serum and find out the most reasonably priced product which is similar to the expensive product.

The following summarizes the outcome:
![summary](https://user-images.githubusercontent.com/78176162/185504892-e3919cd5-d370-4b61-9885-a21e4d182cd8.png)


Overall, the outcome was quite favorable. An economical products match with almost 90% similarity were discovered.

# Introduction:
The last few years have seen tremendous growth in the skincare sector. The market size for skincare products worldwide was initially estimated at USD 130.50 billion in 2021, which was higher than the expectation of a growth of $100.13 billion in that year. It is expected to increase to $145.82 billion in 2028. [1]

During the forecast period, increased demand for body lotions, sunscreens, and face creams etc are anticipated to drive market expansion. Additionally, it is anticipated that the booming e-commerce industry would further accelerate market expansion. [2]

There are many brands currently operating in shops and online due to the intense competition in the market. Pricing practices used by skincare companies seem to be well guarded trade secrets. A 16-ounce jar of La Mer cream costs USD 2,475 on the official La Mer skincare website, however the Nivea Creme moisturizer is far less expensive and has almost the same ingredient list. Another company that has been very popular is The Ordinary, which is known for its affordable skincare products.  The Ordinary can keep expenses down by using only products that have been shown to work and spending less on marketing than other skincare firms. This raises the question: What do we get for our money when we purchase skincare products?

# Importance & Motivation:

When individuals spend a lot of money on skincare, they expect effective high-quality products. Luxury skincare companies have a clear interest in upholding the fallacy that more expensive products always include better ingredients and work more efficiently.

This isn't always the case, though. Along with the ingredients, the product's overall cost also accounts for branding and marketing. We therefore pay a premium for the brand name even though the product's components are almost identical to that of a less expensive offering.

High-quality ingredients in a product is not that pricey compared to the price luxury brands charge. It is preferable to save money if an inexpensive product has the same components and benefits as a pricey one. Within our budget, we can purchase quality products.

While some people can afford to spend $100 to $1,000 on a face cream, the majority of people, especially teenagers and students, cannot.

It takes time and effort to find an effective product online after going through lots of article, exploring for cheap alternatives from YouTube videos, reading articles, and researching on web blogs.As a student, I want to use a product that will provide me with skincare results that are almost identical but cost much less. 

# Objective:

The goal of this project is to find affordable alternatives of high-end skincare products so that people who cannot afford them or who wish to save money but still enjoy identical products can benefit.

**1. Determine whether there is a relationship between pricing and quantity of the product.**

**2. Determine which products are the most and least expensive (from whole dataset as well as from each category)**

**3. Analysis of each individual price, product size, quantity, and brand**

# Data Source & Description:

For my particular problem, there are no proper dataset options available. So the data have been scraped from an online cosmetic retailer.

I scraped the LOOKFANTASTIC website. [Click](https://us.lookfantastic.com/) for the website link.

*Reasons behind choosing this website are:*

- This e-commerce site sells products at every price level, from the least expensive to the most expensive. 

- They sell a large variety of skincare products.

- There is a wide range of product brands available.

The dataset includes several different categories for skincare products, including cleansers, moisturizers, toners, lip products, serums, and so on.
According to value counts, the top three categories overall are "cream," "cleanser," and "serum," respectively.

# Data description
### Raw Dataset

This dataset has been scraped from an e-commerce website name "LookFantastic". [Click](https://us.lookfantastic.com/) for the website link.
The whole skincare option has been downloaded. It included a variety of skin care products such as cleansers, moisturizers, serum, etc. The dataset's size is **7.7 MB**. The total number of instances is **4580** 

**Attributes:** The dataset consists of the following 13 attributes-

**1. Web-scraper-order**

**2. Web-scraper-start-url**

**3. All**

**4. All-href**

**5. Page**

**6. Page-href**

**7. Name**

**8. Price**

**9. Product_details**

**10. Ingredients**

**11. Brand**

**12. Size**

**13. Review_star**

### Final Dataset

This is the dataset we got after cleaning and processing it.

**Instances:** 2838 

**Attributes:** 9

**1. name**

**2. price**

**3. product_details**

**4. ingredients**

**5. brand**

**6. product_amount**

**7. measurement_unit**

**8. product_type**

**9. product_size**

# Data Cleaning & Preprocessing:
Since the data has been scraped, a lot of cleaning and processing were required. This part is divided into 2 section:

**1. Handling null values**

**2. Removing and adding new column**

A major challenge is in cleaning was to distinguish skincare product to skincare tools and remove skincare tools variables.  To differentiate between skincare tools and products, extensive observation was carried out. For instance, if "components" and "size" are both null, it is clear that the observation is a skincare tool because such a tool cannot have any ingredients and typically lacks information on the quantity of the product. However, because some items' ingredients were listed in the "product details" column, we could not delete the null values of the "ingredients" column. Therefore, a lot of little details were attended to throughout the cleaning and preparation stage.

New columns like product category has been added and the category options were extracted from “name” and “product details” column to improve dataset's effectiveness. The product sizes were then uniformed by being converted to grams. Based on that product size, such as large, small, etc., information was extracted, and a new  column was added.

The final dataset has only taken into account single products. Observations that had numerous products, such as three masks in a single packet, were eliminated.

Data types were later modified for EDA purposes.

# EDA:
In order to comprehend the many variables and their relationships, we have carried out various EDA.

**1.Correlation between "price" and "product_amount":** Size or quantity of the product may contribute to a greater price. Checking whether there is a correlation between piece and product amount is one of our objectives.
![corr_price_amount](https://user-images.githubusercontent.com/78176162/184214131-b1af5bdf-4be4-4133-8b40-cdad9f13b09e.png)
As we can see the correlation between “price” and “product_amount” is “-0.09” , there is no correlation between these two variables. So we can interpret that products' amount does not affect their price.

**2. Size distribution:** Below is the distribution of different size product in the dataset. 
![product_size](https://user-images.githubusercontent.com/78176162/184214127-ac9aa53a-9e78-405e-ae39-e212622a4586.png)
There are more small size products in our dataset than standard size product. Large products are the least in the category. 


**3.Average price of each category:** Let’s have a look at the average price of each category products. 

![avg_price](https://user-images.githubusercontent.com/78176162/184214126-206a04a6-5df4-4dc7-b729-f445af53dc5a.png)

Serum has the greatest average price and exfoliant has the lowest average price.

**4.Brands' average product price:** Below is the bar graph of the brands in ascending order based on their average product price.

![brand](https://user-images.githubusercontent.com/78176162/184214124-10d14db2-05e4-4ec7-9d71-3486507129bd.png)

The most expensive brand is “Skin Point Eight” and the least expensive brand is “Vaseline”.

**5.Most and least priced product:** Let’s see the 5 most expensive and the 5 cheapest product in the dataset.

![exp](https://user-images.githubusercontent.com/78176162/184214123-b45ede6d-bd70-43a8-85fa-a25738288bca.png)

![least_exp](https://user-images.githubusercontent.com/78176162/184214121-cca551a3-12d3-4b48-a067-0a6ed3abd293.png)


The most expensive product is almost UDS 1500 which is a face cream and the least expensive products is a little bit less than USD 3 dollar which is a lip balm.




