[Published on Linkedin, in July 9, 2018](https://www.linkedin.com/pulse/dynamic-customised-pricing-using-artificial-abdelkrim-alfalah/?trackingId=aMdpC1PzTqGaRwamSktk6g%3D%3D)

The Pricing is one of the most important exercises in Marketing, it’s the final validation of the products value to the customers. We might succeed brilliantly in the acquisition process of customers, using the best SEO, targeted ads, Marketing Automation techniques and yet fail in the step of Customer activation , because the suggested Price is beyond the customer's perceived value for that product.

![](https://media.licdn.com/dms/image/v2/C5612AQEHDxPTGpmBoQ/article-inline_image-shrink_400_744/article-inline_image-shrink_400_744/0/1531141069914?e=1740009600&v=beta&t=qbGBQDBArUaREnXeMd3wEFZ1eXQLUq1K6HbyLxGRkg4)

## **Dynamic and Personalised Pricing**

This relationship between pricing and value, reveals the problem we face : trying to build a Pricing decision , which is a concrete and measurable attribute of the product, based on an intangible, subjective and dynamic concept which is the Value.

In the modern pricing theory, the pricing optimisation problem takes into consideration the consumer surplus hypothesis, where we assume that the buying decision takes place only if the perceived value is higher than the price of the product, and that every customer seeks to maximise his consumer surplus. From that perspective, companies optimise their pricing tactics within the interval between the product cost, and the perceived value of the product, regarding the constraints dictated by the company's Pricing Strategies, whether it’s a skimming, penetration or price war strategy etc..

To build a great Pricing strategy, companies need to develop a deep understanding of the perceived value of their products portfolio to their customers. The value is dynamic, because it keeps changing in regards to the current situation of the customer. Obviously, an umbrella in a rainy day has more value then in a sunny one. The value is also personalised, because it depends of the customer's background and the context of the transaction. A customer operating extensive search for a product at 4a.m does probably not value the product the same as if he was searching the product at 4p.m

In theory, that means that technically, to build a Dynamic and Customised Pricing tactics, we need to take into consideration the timing, the context and the customer profile. And this may result in different prices, in each different timing for each different customer.

## **Big Data fo Pricing and real facts instead of intentions**

One of the most common approaches used in the past to infer the value of a product was based on the use of Survey Data. Where Marketing Analysts show consumers several product profiles, varying Price and other product attributes (ideally orthogonally designed) and asking them to rank these profiles. Then Analysts uses Full profile Conjoint Analysis, Hybrid Conjoint Analysis or Discrete Choice Analysis, to infer the importance of Price (and other product attributes) to the customers and estimate its Price elasticity. The Pricing problem is then framed as an optimisation problem to maximise Revenue or Profit. Tools such as Excel Solver engines (Simplex, GRG and evolutionary) where then used to find the best Price.

Today, the Big Data enable us to be more factual. Indeed, we no longer need to use declarative consumer's intentions about buying or not and at which price. We can simply use server log data, containing detailed informations about the real choices that customers did.

## **Feature engineering for Pricing**

Once we collected all the transactions log data, building the right Dynamic and Customised Pricing tactics is first a matter of Feature Engineering : which means defining and selecting the most important attributes to take into consideration in the Pricing process. Those features could be Product related, such as brand, price, color, technical features of the product. They could be Customer related, such as sociodemographic attributes and customer’s purchase history. The Pricing could also be built using more Advanced features, using the mouse clicks data, the identification of the acquisition channel, and the customer’s interactions with the company's communications campaigns via Direct emails, facebook, twitter etc..

## Machine learning Techniques for Pricing

Once the Feature Engineering is operated, using the available data sources of the Sales Department , comes the Modelling tasks. The Pricing problem can be modelled as a two-step classification problem : At first we predict whether the user will buy the product, and if the prediction is positive, then we predict the price he might be willing to pay. The two classifiers can be trained as a supervised machine learning problem, learning from the historical data and using the engineered features.

Many classifiers can be compared and used, such as Logistic regression, generalized linear model (GLM), Extreme Gradient Boosting (xgboost), Neural Networks. The choice between those techniques depend mainly on the trade-off between the accuracy, scalability of the algorithms we might need.

![](https://media.licdn.com/dms/image/v2/C5612AQGK-9Dk-5kEdQ/article-inline_image-shrink_1000_1488/article-inline_image-shrink_1000_1488/0/1531139978053?e=1740009600&v=beta&t=7k2XPNXVIPZ7-THXp9UwKkjXgeQZ3yC68y0PKdqDgqM)

## **Price discrimination and the trade-off between efficiency and fairness**

In theory, the AI based Pricing Process may provide a technical framework for building an economically efficient Dynamic and Personalised Pricing, capturing the perceived value of the product for every single customer.  In practice, such Pricing tactics might cause some unwanted serious side-effects, and raise huge concerns among customers regarding the fairness of such decisions.

Indeed, in Airline industry, although the time based Pricing discrimination (where companies change prices for all the customers based on remaining time to flight) are today relatively well-acceptable, other experimented Pricing tactics based on the specific OS version of the customer (Mac vs Microsoft) and the use of cookies, were rejected. In other words, the experience of Pricing Optimisation and Revenue Management, developed in the Airline, showed that customers are not radically against the principle of price discrimination but are rather concerned with the discrimination criteria. 

Therefore, the massive use of more and more complicated Machine learning and AI models, such as Ensemble Models and Neural Networks , with a unique objective of capturing the maximum value from each single customer transaction, makes it difficult to interpret and to understand the discrimination criteria. This may be badly perceived by the customers and considered as an ambiguous, arbitrary and unfair decisions.

In order to make this Personalised AI based Pricing more acceptable and reduce it’s perceived unfairness, companies need to put more constraints to those models, regarding their price updates frequency and variance. Also, instead of updating dynamically and publicly product prices, companies may use targeted discounts as a way to implement pricing changes. And above all, companies need to share and communicate in a transparent manner the Pricing and discounting rules to their customers.