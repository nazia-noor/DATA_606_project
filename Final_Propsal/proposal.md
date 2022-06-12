![fb097060ae15d3b22d8e037f96a1532b](https://user-images.githubusercontent.com/78176162/173253781-b5678b87-6213-4ffe-bc0c-70cc659f4493.jpg)

# Capstone Project

### Affordable Product Recommendation of Luxury Skincare Products Using NLP Bert Technique


**Name:** Nazia Noor

**Course:** DATA606

**Instructor:** Dr. Chaojie (Jay) Wang

### Keywords: 

*NLP, BERT Technique, Recommendation System, Skincare Industry*

# Introduction:
The skincare industry has been booming for the last couple of years. The global skincare market was projected to grow by $100.13 billion in 2021 and the market size was originally valued at USD 130.50 billion in 2021 more than the projection. It is forecasted to grow to $145.82 billion in 2028 at a CAGR of 5.52% in the forecast period, 2021-2028.[1]

Increased demand for face creams, sunscreens, and body lotions around the world is likely to boost market growth during the forecast period. Furthermore, the thriving e-commerce sector is expected to enhance market growth even more.[2]

Because the market is so competitive, there are a lot of brands functioning in stores and on the internet right now. How skincare businesses price their products appears to be a well-guarded secret. On the La Mer skincare's official website, a 16-ounce container of La Mer cream costs USD 2,475, but the considerably cheaper Nivea Creme moisturizer has a nearly identical ingredient list. The Ordinary is another brand that has gained a lot of traction because of its low-cost skincare products and no-nonsense ingredients. The Ordinary can keep costs down by spending less on marketing than other skincare brands and just employing products that have been proven to work. This makes me wonder: what are we paying for when we buy a skincare product?

# Importance & Motivation:

When people spend a lot of money on skincare, they want high-quality products and formulations that work. Luxury skincare firms have a vested interest in perpetuating the myth that a higher price tag equals higher-quality ingredients and effectiveness.

However, this is not always the case. The total cost of the product includes not only the ingredients but also the brand value and marketing. So, even though the product constituent is nearly equal to that of a less expensive product, we pay a premium for the brand name.

People want to indulge themselves with high-quality things, but high-quality products do not have to be expensive. It is preferable to save money if an affordable product has identical ingredients and benefits as a high-end product. We can use effective products within our budget.

Although some people can afford to pay $100-$1000 for a face cream, most others, particularly teenagers and students, cannot afford it.

As a student, I want to use a product that will give me almost the same skincare result but at a fraction of the price. Even though we can search on YouTube videos, read articles, and do online blog research to see which products are affordable and could be a decent substitute for a more expensive one, it requires time and effort to look for an effective product.

# Objective:

I believe that creating a model where I can locate alternative premium skincare product options would be a fantastic approach to saving time and money.

**Problem statement:** Find the affordable option for luxury skincare products with skin concerns wise.

Since there are not a lot of studies have been done on this topic, I would like to find the answer to some skincare product-related questions.

**EDA-related question:**

1.  What are the cheapest to most expensive products in each skincare category?
  
2. Are much correlated are the price and size of the product?
 
3. how is price category distribution distributed?

# DATA Source & Description:

There are no skincare dataset options available, specifically for my issue. As a result, I decided to scrape my data from a cosmetics e-commerce website.

I will scrape the LOOKFANTASTIC website. [Click](https://us.lookfantastic.com/) for the website link.

*Reasons behind choosing this website are:*

- They sell a wide range of skincare products on their website.
- This e-commerce site sells products at every price level, from cheap to most expensive.
- They have great variation in product brands.

There are many different sorts of skincare products on the market, such as cleansers, moisturizers, toners, sunscreens, serums, and so on. I will choose only the following items:
- Moisturizer
- Cleanser
- Exfoliants
- Face mask

I am choosing only these four skincare categories because a huge price gap can be noticed among these.

### Data description


**Attributes:** 7

These are-
- Product name
- Product Type
- Ingredients
- Product details
- Price
- Size
- Skin type/concern.

 **Number of instances:** 4000 (Approximately). 
 
 **Size:** Unknown [**N.B.** *I don't know how big the dataset will be because I haven't scraped the data yet. But I'm assuming the dataset won't be much bigger than 1GB]*
 
 
# ML Approaches:
Natural language processing, known as NLP, is one of the many applications for machine learning.
Text responses, determining the meaning of words in context, and conversing with humans are all handled by NLP. It aids computers in comprehending human language, allowing us to communicate in a variety of ways.

BERT (Bidirectional Encoder Representations from Transformers) is a well-known technique developed by google to extract characteristics from text data. It is a machine learning framework for natural language processing that is open source (NLP). BERT is a program that uses surrounding text to help computers grasp the meaning of ambiguous words in a text. The BERT framework was trained using Wikipedia text and may be fine-tuned using question and answer datasets.[3] 

Since our study is a **multiclass text classification problem**, I will use NLP's BERT technique.

There will be three major steps in applying the BERT Technique:

**1. BERT Embedding:** At first, I will extract characteristics from text data, such as word and sentence embedding vectors. These embeddings are important for keyword/search expansion, semantic search, and information retrieval, to name a few applications. These representations can assist in accurately retrieving results to match pricey products with affordable products based on product information and ingredients. Then these vectors are fed into downstream models as high-quality feature inputs. NLP models like LSTMs and CNNs require numerical vector inputs, which usually entails converting variables like vocabulary and portions of speech into numerical representations. BERT has an advantage over models like Word2Vec in that, while each word in Word2Vec has a fixed representation regardless of the context in which it appears, BERT generates word representations that are dynamically informed by the words around them.Context-aware word embeddings collect additional types of data, resulting in more accurate feature representations and, as a result, higher model performance[. I will use "SentenceTransformers" which is a Python text embedding framework. 

**2. Finding Cosine Similarity:** As a next step, I will acquire the vectors after calculating the encoding and I need to detect commonalities between them. To accomplish so, I'll utilize Cosine Similarity, which assigns a score to two vectors based on their resemblance, with 0 indicating no similarity and 1 indicating total similarity.

**3. Testing:** Then I can put the name of the expensive goods to the test. The system compares the user's entered product name score to other ratings and suggests a related product. Then I can then choose the cheapest option by glancing at the price column.

# References:

1. https://www.fortunebusinessinsights.com/skin-care-market-102544
2. https://www.grandviewresearch.com/industry-analysis/skin-care-products-market
3. https://www.techtarget.com/searchenterpriseai/definition/BERT-language-model
4. https://www.freecodecamp.org/news/google-bert-nlp-machine-learning-tutorial/

 






