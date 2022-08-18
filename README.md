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
