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

# ML Approaches:
NLP, or natural language processing, is one of the numerous uses of machine learning.
NLP can manage text responses, word meaning in context analysis, and human-to-human communication. It enables us to communicate in several ways by making it easier for computers to understand human language.

Google created the well-known method known as BERT (Bidirectional Encoder Representations from Transformers) to extract attributes from text input. It is an open-source machine learning framework for processing natural language (NLP). BERT is a program that uses the text around unclear words in a text to help computers understand what those words mean. The Wikipedia text was used to train the BERT framework, and question and answer datasets may be used to fine-tune it. [3]

I'll employ NLP's BERT technique because my study involves a **multiclass text categorization problem**.

The BERT Technique will be applied in three main steps:

**1. BERT Embedding:** At first, characteristics will be extracte from text data, like word and sentence embedding vectors. To name a few uses, these embeddings are crucial for keyword/search expansion, semantic search, and information retrieval. Based on product details and ingredients, these representations can help in precisely matching expensive products with less expensive options. These vectors are then used as high-quality feature inputs in subsequent models. The inputs for NLP models like LSTMs and CNNs must be numerical vectors, which typically requires transforming variables like vocabulary and portions of speech into numbers. BERT has an advantage over models like Word2Vec in that it generates word representations that are dynamically informed by the words surrounding them, whereas each word in Word2Vec has a fixed representation regardless of the context in which it appears. Context-aware word embeddings gather more sorts of information, improving feature representations and model performance. Python text embedding toolkit "SentenceTransformers" has been used for this.

**2. Finding Cosine Similarity:** After determining the encoding, I obtained the vectors and then looked  for commonalities between them. In order to do this, I used Cosine Similarity, which gives two vectors a score based on how similar they are, with 0 denoting no similarity and 1 denoting complete similarity.

**3. Testing:** Lastly, pricey products were put to the test. The system proposes a relevant product after comparing the user-entered product name to other products. Then I manually checked the pricing column to determine which choice is the least expensive.

# Final Result
The top three categories—cleanser, serum, and cream—have been tested.
The top 5 choices have been examined to determine the outcome. The first picture shows "product recommendation" which refers to the cosine similarity of the products. The first one is the actual product for which we need to look for an affordable alternative.

Then, after printing the top five choices for that product, we selected the one that was most appropriate given its reasonable price and high similarity score. The closer a product is to the original, the greater the similarity score.The least expensive option has been considered the most affordable choice for the pricey product.
These are the outcomes we obtained using the cosine similarity.

### 1.Cream Category

- **The scores for each product's similarity to the specified most expensive cream are listed below. Since the first one is the specified product, it is one.**

![cream_cos](https://user-images.githubusercontent.com/78176162/185469396-d791ffa6-bffa-4878-9ba3-93e3136ca0a1.png)

- **Here are the top 5 similar options for the most expensive cream.**


![cream_recom](https://user-images.githubusercontent.com/78176162/185469397-becc3257-7b01-43dc-90df-fc42ab3cafce.png)

For the cream category, all the top 5 options are affordable compared to the expensive option. For $995 priced “111skin celestial black diamond cream 50ml” cream, the most affordable option from the top 5 highest similarities is the product “Bella aurora Bella multi-perfection day cream combination-oily skin 50ml’ is the cheapest one and the similarity is 87%.

### Cleanser Category

- **The scores for each product's similarity to the specified most expensive cleanser are listed below. Since the first one is the specified product, it is almost one.**

![cleanser_cos](https://user-images.githubusercontent.com/78176162/185469391-130bf6a7-a0f2-4448-be55-12eab7947f75.png)

- **Here are the top 5 similar options for the most expensive cleanser**

![cleanser_recom](https://user-images.githubusercontent.com/78176162/185469393-ba9f0ca4-6bc9-46cb-b6a2-ee07708d2f2e.png)
For the cream category, all the options are affordable compared to the expensive option. The only affordable option from the top 5 highest similarities is the product “Bella aurora Bella multi-perfection day cream combination-oily skin 50ml’ is the cheapest one and the similarity is 87%, it is considered as the best affordable option.


### Serum Category

- **The scores for each product's similarity to the specified most expensive serum are listed below. Since the first one is the specified product, it is almost one.**

![serum_cos](https://user-images.githubusercontent.com/78176162/185469400-1250e956-c6a6-4ce7-a227-84ec044a4f89.png)

- **Here are the top 5 similar options for the most expensive serum**

![serum_recom](https://user-images.githubusercontent.com/78176162/185469402-5c9d6ccc-698a-4328-ae10-f64ce6ba7256.png)
For the serum category, most options are affordable compared to the expensive option. the product 'DCL skincare active mattifying cleanser 125ml' is the not cheapest one but has the similarity of 91%. This is a good affordable option for the expensive product of this category. But there is other cheaper options with nearly 90% similarity. 

# Manually checking the similarities:

These are the similarities I have found. Note that, The model might have detected more similarities. Since I have limited knowledge of these ingredients, I have found these only.

![marked_similarity](https://user-images.githubusercontent.com/78176162/185767945-497dcc02-0591-463d-8331-8abeabe1cb2a.png)



The product " Mila Moursi lifting serum 1 fl. oz" is 92% similar to the product "Mila Moursi rejuvenating serum 1 fl. oz". Let's see some of the similarities:
- Both have the name "mila moursi"
- Both are serum and weigh 1 fl. oz.
- It was good to interpret word representation in the context. for example, POWERFUL (ignore "and anti-aging") CONCENTRATE can be referred to as POWERFUL ELIXIR. Again, REVITALIZE SKIN can be referred to as RESTORE RADIANCE. 
- Some ingredients are exactly similar. for some others, the main ingredient is similar but a different variant has been used. For example: "palmitoyl tetrapeptide-7" and "acetyl hexapeptide-8" are both main components is a peptide. Just two different variants have been used in the two products. 
Another example is- CARBOMER in "Mila Moursi lifting serum 1 fl. oz" and SODIUM PHYTATE in "Mila Moursi rejuvenating serum 1 fl. oz" both are product stabilizer. 
Also, POLYSORBATE 20 is another form of ALCHOL.






# Future work:

- Applying the BERT model to the entire dataset to find the most cost-effective alternative and determining whether it can find its duplicate by looking at the entire dataset rather just categories can be a good work.

- I believe there is scope for improving the product category identification.

- A more accurate method could be used to categorize product sizes. For instance, an eye cream's standard size is often less than 30 grams, however after conversion, it was classified as a small size in our dataset. Therefore, there is room for more work here.




# References:

1. https://www.fortunebusinessinsights.com/skin-care-market-102544
2. https://www.grandviewresearch.com/industry-analysis/skin-care-products-market
3. https://www.techtarget.com/searchenterpriseai/definition/BERT-language-model
4. https://www.freecodecamp.org/news/google-bert-nlp-machine-learning-tutorial/

# Links:

### [PowerPoint Presentation](https://github.com/nazia-noor/nazia_data606/blob/master/presentation/capstone_presentation.pdf) 

### [Youtube Video](https://www.youtube.com/watch?v=YNOof1zlCis)


