
# ISB Marketing Analytics

Marketing analytics is done on CRM database to market more effectively. It is done to optimize the costs associated with marketing products and costs for customer acquiring and retention.

Outbound means company calling a customer, Inbound means customer reaching out to company for service or product.

## Session 3:

Ad Copy - we can optimize the ad copy with text keyword that has less bid rate and can still get good click thru. this can be done using text mining and a model can be built for the same.

Since htese keywords are infrequent hence less users type to comeup with thtat we have to find thousands of unfrequent keyworkds 

$$ Clicks = \alpha [1 - e^{-\beta b}] $$

$\alpha$ = Traffic x CTR for the #1 ad

$\beta$ = inversely related to competition intensity

b = bid amount

Using this we can start finding the conversion rate for different keywords.

If LTV and ConversionRate is high then we can go for max bid amount and be #1 on the ad page. Else, we will have to find an optimal point.

If the budget is lower than the optimal value for keywords, then do optimization with function to be sum of profits and constraint to be less than max expenditure.


------------------------------------------------

# ISB ML SL2

https://www.youtube.com/watch?v=lowavG2SXsQ

https://www.youtube.com/watch?app=desktop&v=4b5d3muPQmA



# ISB FP

Soundfile is a package to read and write files. Every SoundFile has a specific sample rate, data format and a set number of channels.
- `sf.read('filename.wav')` returns data and samplerate.
- Sound file can also be opened as SoundFile Objects `f`.
  - `f.read()` gives data
  - `f.write()` writes the file
  - `f.samplerate` returns sample rate.

librosa - A python package for music and audio analysis. `librosa.feature` is used to extract features from a wav file. These are usally 2D arrays.

MFCC is a 2D matrix format with MFCC bands on the y-axis and time on the x-axis, representing the MFCC bands over time. To simplify things, what we're going to do is take the mean across each band over time.

MLP Classifier - MLPClassifier stands for Multi-layer Perceptron classifier which in the name itself connects to a Neural Network. Unlike other classification algorithms such as Support Vectors or Naive Bayes Classifier, MLPClassifier relies on an underlying Neural Network to perform the task of classification.

PLP or perceptual linear prediction is a feature 

Links:
- [PyPi with basic steps](https://pypi.org/project/SoundFile/)
- [Read The Docs](https://pysoundfile.readthedocs.io/en/latest/)





---------------------------------------------------------------

# Dairy Farm

Animal|Milk|SP|Expense
-|-|-|-
HF Horisten Frisher|20litre|550|10kg Rs.300 + cal min dr green dry labour
Desi|6ltr year avg|Rs 30 per ltr, Rs. 150 | 5/6 green
Bhains|7ltr avg|Rs 42 | 15kg food

Difficulties:
- Peak season
- Cow dry period
- Cow not milking forever

Also:
- Sell Gobar and Gau Mutra

Requirements:
- Area
- Shed Gaushala, Covered open, roam area
- Water

Before buying:
- max 3rd preg cow
- see three time milk
- cow with bachiya
- feed baby 1/10 milk for 90 days, then chara
- cow (300kg) should at least min, else sick
  - 5kg bhoosa per day
  - 35-50kg green chaara
  - 1kg daana, 1kg pe 300gm daana
  - daana is rashan, ann ka mishrad, protien, carbs, calcium
  - 1quintal daana is, 50kg chota genhu, 40kg rice polish, 8kg daal ki choori, 1kg mineral mixture, 1kg namak iodine.
  - daana subh bhigao, shaam do. Serve it well.
  - naadi should be gol like a bowl.
  - 20 days no calicum after baby birth
  - calcium 100gm daily for 20days and then not 20 days
- maintain all in and out, milk, medicine, feed.
- keede ki dwai every 6 month
- cow drinks 80-100ltr pr day.

Breeds:
- HF - 60k cost, 8 mahine milk, 25-30kg chaara
- Jersey

60% kharcha

75 gay 500-500ltr

aseem rawat hetha

Archit Auro Milk

--------------------------------------------

ISB 


--------------------------------------------

# ML Supervised Learning
- by Sailesh Kumar

Session 1:

## Inroduction to Machine Learning SL

FORMULATION is the Key Skill in Data Science. It is the art of converting busines prob to ML.  “Our technology, our machines, is part of our humanity. We created them to extend ourselves, and that is what is unique about human beings!” -- Ray Kurzweil. Everything is evolving, tools, products, tech, skills etc. 


Products are evolving, emergent intelligence - let the technology emerge. Then learn thru unsupervised learning. Don;t make it pre intelligent, but let it evolve. Dont define classes on its own but let ML find the patterns and clusters.

Philosophy of AI, understanding the Nature of the Mind. ML Goal is to unravell the nature of mind.  What is INTELLIGENCE? Generalization: Ability to predict or assign a label to a “new” observation based on the model built from past experience.

## Driving Better Decisions

ML is to learn how to make better decisions, from broadcaste to peronalized decisions. tata sky vs netflix, this will apply to health n agri. From batch sms to realtime, e.g. no sundays offers but event based poersonlized offers. From data rich to AI first. ML is continuous learning, continuous improvement. It has evolved from BI to ML to DS to AI and is still progressing.

Data - Insights - Features - Models - Predictions - Decisions - Feedback - Data

Here, same paradigm can solve many problems, it can be a classification, recommendation, outlier detection or retrival. Every ML Paradigm is an OPTIMIZATION Problem



We work by taking sample from reality, eg customer buying, rides taken.

- clustering algo, outlier detection algo/method.

- rediction paradigm, is cust about to churn, car to breakdoiwn based onbserved data.

pattern recognition - usl, 

recommndatin engn - 

resoning alogo - its sequence of actions, not onlu 1, chatbot, solving math ptob

reinforcement - laern to rason, explore an exploit, 

deep learning - not everyhting is deep learning


Architecture of Ai 
- stimulus to state, then state to action? how we do this is SL/USL.

AI for industrial IoT
- DOmain knowlege is faaaaarr more imp that stats and python

- how does on think about AI, 
  - metrics to be max/minimized
  - domain knowledge
  - stimulus - sensors data, 
  - state - featured vectors
  - response - actions or predictions, classes etc
  - eg, RETAIL, AGRICULTURE, EDU

Democratizing AI for ALL
- making AI available
- lot of apps/models/apis/services are developed
- AI market place for India, all upload their model, and anyone can consume via API. it coneects product thinkeers with AI

- Ariculture, now I can tell what is gown an dant what stage, so no wrong growth neither import, no wastegae

Super vises:
- regresion, prediction
- clas - time here, 
- recommnedation - what are you going to do in future based on past, tell fav 4 movie and we will recommend based on that.
- retrival - entity to a query.

Supervised learning paradigm:
- numerical prediction the regression
- categorical then classification, crop is  classification cz it is not based on recommendation of past dta
- recommendation - top 4 recommendation
- retrival - 

eg: 
- ad position is retrival based on query u show ad
- credit card is classification
- youtube - recommendation, also retrival for your query in seatch box. 
- google images, - retrival n then, gif/clipart/sketch based on classification it filters.
- connect/follow on linkedIn via recommendation, seach is retrival, 
- product next - recommendation
- android prce, profit model
- medicine/tereatmment classification
- resumne for Job ID - retrival, based on JD or query we provide resume.
- where to sell new prods, like jio all in one media
- like barclays new product
- MRI cancer? classification, class has interprtation and prediction. curent data vs future
- Stock regression
- credit limit, regression, cz of number
- customer churn, classifier, give data, i'll interpret.
 -stealing/shopping clss, interpretaiton
- objects - classification, detection(interpret) and recognition(predictin).
- iPads in mumbai - regression, demand forecasting
- Tweet - classification
- rhowuse  -regression, price forecasting
- song humming - retrival, 
- shaadi - retrival, also can be recommendatuib vased ib your activity. this exercise is classification as we give a class label to every prob


From data to decisions:
- 

Outlier detection paradigm
- 


session 2:

- data nuance1 - fourier transform?
- noise vs signal, every data has it, eg, some vibrations in aeroplane are noise in xyz coordinates, while take off and landing is signal. Same for voice data, ocean heights. we need to distinguish bw noise and signal

- covida data has noise, like some tests are not trust worthy. count is not the true representation. not i=enought tests, not testing in the right places, flase postve and true nregative sis alo noise, reporting err isnoise. so we take the data and create model, then model predictions remove noise.

- ML is used to find signal in noise.

Data Nuance 2:
- nobody is buying the complete logical set of things.

- grammar data - there is mixture of projection, means different products might be purchased from different baskets, eg, keyboard mouse with hammer and screw driver

Data nuance 3:
- degree of variabliluty in images is very high e.g., due to pose, light etc. 
- making system invariant to the variance is what we need. eg, making system invariant to different accent of speech

DN 3 Invariance:
- ignore the variance in all kind of data. ML is art of invariance learning, what matters and what doesn't matter

DN 4 |  Missing Data
- many reasons and we need to be logical in filling missing data. like mean, averange, median or model based, predict the missing values.

DN 5 | Not so normal dist
- to use stats methods and math priciple like aucledian distnace, we need normal dist assumption and or uniform distn. 
- else, we can take log, or other transformations. 

DN 6 | heterogenious mixture :
- once column may have different unit values, eg, blood test 
- min max may not work, because of outliers. it may work some time and not other time.

DN 7 | Multi-modality features:
- 2D, 3D,  TIme-series, 
- need to normalize, reduce dimentionality, 

Importance of labelled data-
- scaling can be done using cloud
- AIML can be done using tensor, SparkML etc libs
- big data can be done using spark, hadoop, kafka etc.
- these doesn;t make u special, or super.

- to make a super powerful company you need labelled data, then you can make more accurate predictions, eg, google has more labelled data than bing. google images, maps, capcha.

- it has to be kept sage, no leakage

what are you trying to predict?

### Machine Learning Feature Engineering

What variables are important for you?

Insights + Domain = Feature

- Fitbit to cardiac
- Bank tranactions to CIBL score

Two ways to do DS:
- simple features, complex model
- complex features, simple model

Here, complex model with neurons have latency and if you need fast predictions then use complex features, that;s what Google does.

While modellling we need to consider the limitations of models like we cannot do multiplication or division in some models then we might need to take log or other such tranasformations.

Model the variables that matter:

- **NOTE:** Try to never use raw number in ML, it may have noise and other things, e.g., dont use balance for creadit score, normalize it with other facts like expense, frequency of expense, (total debts)/(total income) etc.
- remove exp nature by taking log, remove senstivity of varibales

Model Deviations from Expected:
- Model to predict total_sales, demand forecasting model, then modelling just for a number like sales is not important, you need to model it;s deviation from mean, that tells weather we have met expectation or not.

"Bugs" in Feature Engineering
- Its like when telling a lie, then explaination goes complex, like Johnny Jhonny, yes papa...
- So if model is getting complicated and then too not acheiving accuracy then there is possibilty of a feature bug that the model is trying to compensate, e.g., 0 for not found and first value in field or variable having garbage values.
- 
















##Session 3:

- Feature engg is exploring all features and trasnforming them
- impoertance of dimentions, eg, 23675, here 2 is most imp because of units we have. it is 10s thousands, similarly we need to find imp eg color, size etc. if we remove the thing, eg, remove 2 and make 0, then max loss of information is most imp feature.
- now, if we check, is the number divisible by 2, then, last digit becomes most important.
- many features will be there, then many feature will be engineered. task is to determine most imp feature.
- which is better? - same feature, but different class, A B are class, dengu non dengu, if sigma is high it is worse. Seperation of mean should be high and variance within the class should overlapp minimum, variance within class should be low


study, fisher distribution, selection of feature, projection of features

We reduce the dimentions into 1D, we compute w, the weigths which can be multiplie with dimensions to maximise a values:
- PCA maximizes variation in data
- Fisher maximizes separation in classes

We use fishers formula to compute the separation of classes nin numeric way. Which dimension separates the classes maximum out of 1000s columns/dimntions.

We use another method to find which projection separates the classes the max, diff in the means.

clustering is done, then we get casses and it becomes classification problem from clustering problem. In real world new classes keep emerging.

There are both clssifiers, discriminative and descriptive. once defines withing and another differentiates the classes.





now, classifier world, model:
- classifiers describe the class , such that it does not overlap each other
- discriminative classifiers dicriminate and we know the classes.



Partitioning into pure region
- cannot be 100% boundary, because of noise
- complexity of classifier can only be linear for now.then which is the best fir line to distinguish the classes is the optimization. which linear classifier maximises the purity.
- medium decision boundary is having a polynimial, all curves are degree of polynomial
- 100% accuracy on training data, is all pure region, is very complex.
- out of these, something in b/w is good, region should be as pure as possible.

Toy dataset
- art, start with feature engg, color, shape, lights, sounds
- collect the data, get sales data, then see number of times it was sold/not
- art, create labelled data, check video of toys, take interview of sample kids
- we have categorical data, shape and color. We make matrix to find probabilies/region. This is classifying a toy, as in to which cell a toy belongs to. 
- Now if we increase the features then the matrix increases hence we will use decision tree.





## Session 4:

Recap:

We create contingency table from categorical variables nd then try to find the pure region which the goal of ML Classifier.

- each row, column or cell is a region.

- purity is the probability of the majority class in a region

- when the data is noisy, 55-45 then we don not use majority class, we use GINI measure, we find the expected accuracy. 

### 3rd measure of purity

requires entropy of distribution, used by communication sattelites. 

Information Theory 101:
- rare letter vs frequent letter and its importance. rare ahve more importance.

- entropy means chaos and uncertainity.  

purity is high then entorpy is low.

uniform ditn has workst entorpy

Accuracy can be mesured by 
- purity
- entorpy, or
- ginin index.               

Decision tree works by dividing data by class then findinf the purity of region. 

Size X Purity for a region is score, it is basis of decision tree. As we get more and more deeper in a tree shape emerges and purity incereases.

### Greedy decision tree

- if A turne dout ot be the best feature then we keep it on top of tree, then further look down to partition, all rows ahving 'a1' and remaining 25 fetures.

- we stop growing when we reach a pure partiiton, need not partition futher, they are pure above a parameter threshold., eg, c1 and e1.

- in case of numeric attributes, sort and do all possible partitions. then we get n-1 partitions.

- for numeric, we can only go horiontally or diagonally, then for diagnol we do feature engineering. 

- logistic regression is good for numerical variable.

- so we cna combine ML techniques an not get stuck with one, this is wehere we can do programming in it and cnannot use library. for eg, embed logistic regression at a leaf of decision tree.

- facbook, for eg, ignore numerical var and use only cat var to make decision tree, then partitions on numberical var.


Recap:
- fisher discriminant SV tech, for feature selectiion, importance, projection
- rule based classifier, pre set of classifier, based on few features, 
- learn rules based on data, birth of decision tree, hence birth of ML. DT is first algo of ML.


### K-Nearest Neighbors
- carc - classification and regression cheat
- for 2 classes we use odd k
- as we inc k, the complexity decreases
- parameter is nothing, this is non-parametric classifier
- given the hyper param what are the params
- hyper is used to control the complexity
- param is the tree lenght or the partitions
- no training time
- scoring complexity depends on k 

### Kernel density function:
- points are like magnets and thy have influence on the validation data. They influence distn is called 'Density Estimate'
- magnets can be +ve or -ve, then each influence is calculated, then the data belongs to the class whcoh has high influence.
- density function is influence on x by all other points.
- Thsi is Parsean Window.

### Bayesian Classifiers
- Based on Bayes Rule.
- P(Data|Class) is based on old data where you know the class or result of diagnosis.
- P(Class) is probability of such dicease occuring
- P(Data) is probability of such patients coming
- RHS is all labelled data,m that is history
- LHS is for new data that has yet to come.
- P(Class|Data) is for new data that has not been seen previously.
- Learinig on RHS , inference on LHS.
- **Comes in interview think like a Bayesian**

Multivariate data:
- we can start simple by using similar covariance matrix for all dimentions
- then inc complexity by allowing different covariance
- then by different degree of freedom
- then by increasing dimesion freedom as well.












------------------------------------

# FA - Forecasting Analysis

Ninary process are only yes or no

point process tells us only occurance.

forecasting is based on past data.

predicting might not be associated with time, but forecasting is, 

in timeseries, the value is correlated with the previous observations.

deterministic vs stochastic
- there are a lot of fluctuations in stochastic series

- temporal correlation is relation to the previous year, scatter pliot of values this year vs last year

- notation, T + h|T is how many periods into the future you are going to forecast.

- frequency of seasonality is important, it depends on data granularity and how often the seasonality repeats.

- cyclicality is not that it will occur at regular interval but it is random, like pandemic or recession.

- seasonality occurs at regular interval while cyclicality is random in time interval.



## FA Session 2:


------------------------------------

# Unsupervised Learning

- No labels in data but we try to find patterns within, eg:
  - Clustering – grouping data, inferring labels from the data
  - Rule-mining – interesting relation b/w varibales, finding patterns based on purchase information
  - Recommendation-system – suggesting new items based on usage
  - Dimension reduction – Inferring structure from the data

USL is first arrow on data but underlyting assumptions shuld be validated in EDA, then followed by Epicyclic procss.

Association Rule Mining
- how to combine things, market basket ananlysis
- txns could be a few days of purchase as well.

Terminology:
- I is all items in store
- X is one basket/txn, called item
- D is dataset, table having each row as txn.

- Association rule is, X => Y, if X then Y, X and Y have nothing in common
X is called antecedent, LHS or body
Y is called consequent, RHS or head

How to evalueate:
- Support: how often they occur tohether in store,
  - sigma is count, txns in store
  - s is pct, count/total
- Confidence, once you buy X how often you buy Y
  - given X, X => Y, c = S(X => Y)/S(X)
- Lift, they occur vs they randomly occur., 
  - s(X => Y) / s(X)\*s(Y)
  - how much X lifts prob of buying Y.
  - lift = 0.4/0.6\*0.6 = 1.11, thsi says that you expect X adn Y 30% of time but they occur 40% of the time, hence has more lift.
- leverage is diff of occured and random, lift is ratio, 𝐿𝑒𝑣𝑒𝑟𝑎𝑔𝑒 𝑋→𝑌 =𝑠 𝑋→𝑌 −𝑠 𝑋 ∗𝑠(𝑌)
- conviction is ratio with diff from 1. 𝑐𝑜𝑛𝑣𝑖𝑐𝑡𝑖𝑜𝑛 𝑋 → 𝑌 = (1−𝑠(𝑌))/ ( 1−𝑐(𝑋→𝑌) )

Rules are discovered using Apriori algo. It tries to improve the efficiency by managing the frequently occuring items. 
Phase 1 - Join, support, exhaustive search, 2^n itemsets, if an itemset is frequent, then all its subsets are also frequent
Phase 2 - Prune, confidence

Improving, Hash-based technique, When scanning for 1-itemsets, create a hash for 2- itemsets, and remove hash buckets that do not have enough support.
Reduce the transactions, Prune the transactions that do not contain any k-itemset, when scanning for (k+1)-itemset. Partitioning, Divide the transactions into non-overlapping datasets, Find “local” frequent patterns, Verify if these local frequent patterns have enough support in the entire data.

Adv FP-Growth, Improves the efficiency of not scanning the database multiple times for the generation of candidate itemsets, Minimizing the number of frequent items considered, Multi-level or multidimensional pattern mining, Sequential and time-series patterns.




## Session 2: Recommendations

Collaborative filtering:

- filter itmes/users based on similarity from collaboration

- user-based - find similar users to focal user based posts liked, both like car and pizza hence similar
- item-based - find similar items based on users liking them, u1, u2 like a post then other posts liked by u1 are similar and can be recommended to u2

𝑈 is the set of users: |U| = n.  𝑢1,𝑢2,...,𝑢𝑛
𝐼 is the set of items: |I| = 𝑝. 𝑖1,𝑖2,...𝑖𝑝
- Ratings data is matrix 𝑟, with 𝑛 rows (users) and 𝑝 (columns), r_jk is the rating of the user 𝑢 for the item 𝑖

User-based CF: Step 1
- We need to define a distance metric between the focal user and other users.
- Two popular metrics
  - Pearson correlation between ratings
  - Cosine similarity between ratings
- Once we decide on a metric, we can find the neighbors using k-nearest-neighbors (knn) approach.

- Correlation proximity
- Ratings by user 𝑢1 on items 𝑖1,...,𝑖𝑝
- r11....r1p avf r1_
- r21....r2p avg r2_
  𝐶𝑜𝑟𝑟 𝑢1,𝑢2 =
∑ (𝑟1i − 𝑟1_) ∗ (𝑟2i − 𝑟2_)
/ 
sqrt( ∑(𝑟1i −𝑟1_)^2 ) ∗ sqrt( ∑(𝑟2i −𝑟2_)^2 ) 

C𝑜𝑠𝑆𝑖𝑚 𝑢1,𝑢2 = ∑𝑟1i ∗ 𝑟2i / (  sqrt(∑𝑟1i^2) * sqrt(∑𝑟2i^2) )


Itembased CF use same metrics

Disadvantages of Collaborative Filtering
- Coldstart - When a new user who has not rated any item - When a new item is introduced into the market
- Serendipity- There are no surprises in the recommendations.- This can be modeled into the collaborative filtering framework
- Sparsity - Most of the ratings matrix is empty! 
- Biased data (rating stickiness) - Popularity bias - Unique tastes of users is lost. - Over time the data can be biased - Is the rating the actual rating or the recommendation has biased it?
- Privacy related issues
 
Association rule can bundle items, Recommendation is often a single or a set of items with no apparent relationship.


The idea in matrix factorization is discover these latent features that the users and items can be aligned with,    Latent factors It is a general concept that can describe a user and an item.

  Singular Value Decomposition (SVD)  Fill (impute) the empty cells with average rating
 Non-negative Matrix Factorization (NMF)NMF can be applied when 𝑅 has only non- negative values

## Dimensionality Reduction

Dangers of Dimensionality Reduction
Reducing dimensionality can distort data (and, hence, data mining results) in misleading ways

## Outlier and Anomaly Detection

The set of data points that are considerably different than the remainder of the data

Detection schemes - Graphical , Statistical/model-based, Distance/proximity - based.

 Graphical Approaches
- Simple examples
- Boxplot (1D)
- Scatter plot (2D)
- Spinning scatterplot (3D)
- Benefits
- Intuitive, use powers of human cognition
- Limitations
- Time-consuming
- Subjective
- Difficult to use with higher dimensionality
 
  Statistical Approaches
- Statistical methods (also known as model-based methods) assume that the regular data follow some statistical model (a stochastic model)
- The data not following the model are outliers
- Lots of different models are available
- Effectiveness of statistical methods highly depends on whether the assumption of statistical model holds in the real data
- Many statistical techniques have been developed
- E.g., parametric vs. non-parametric

### Data is represented as a vector of features
- Three major approaches - Nearest-neighbor-based
- Density-based
- Clustering-based

 Nearest-Neighbor-Based Approach
- Simple idea:
- Compute the distance between every pair of data points and use the information about k nearest neighbors of each point

 Density-Based Approach
- Finds local outliers, i.e., by comparing data points to their local neighborhoods, instead of looking at the global data distribution
- Intuition: The density around an outlier object is significantly different from the density around its neighbors
- Method: Use the relative density of an object against its neighbors as the indicator of the degree of the object being outliers

Density-Based Approach: Local Outlier Factor (LOF)
- Basic idea:
- For each object (data point), compute the density of its local neighborhood (defined by the k nearest neighbors)
- Compute local outlier factor (LOF) of a given object as the ratio between its local density and the local densities of its nearest neighbors
- Outliers are objects with largest LOF value
- A number of further variations and refinements have been proposed

 Clustering-Based Approaches

- Regular data belongs to large and dense clusters, whereas outliers belong to small or sparse clusters, or do not belong to any clusters

Strengths
- Many clustering techniques available
- Work for many types of data
- Clusters can be regarded as summaries of the data
- Once the cluster are obtained, need only compare any object against the clusters to determine whether it is an outlier (fast)
- Weaknesses
- Effectiveness depends highly on the clustering method used – it
may not be optimized for outlier detection
- High computational cost
- I.e., need to first find clusters
- There are some techniques that try to mitigate this cost

## Challenges of Outlier Detection
- Modeling regular objects and outliers properly
- Hard to enumerate all possible regular behaviors in an application - The border between regular and outlier objects is often a gray area - More complex outlier behavior: collective outliers, contextual outliers
- Application-specificity in outlier detection
- Choice of distance measure among objects and the model of relationship
among objects are often application-dependent
- Handling noise in outlier detection
- Noise may distort normal objects, blurring the difference between regular objects and outliers
- Understandability
- Why these are outliers? (I.e., justification of the detection)
- E.g., poor data quality, measurement malfunctions, manual entry errors, correct but abnormal data
- Specify the degree of an outlier
- The unlikelihood of the object being generated by a normal mechanism
- Supervised outlier detection methods
- Can be used, if descriptions (labels) of anomalous data are available - Otherwise, it is typically an unsupervised (exploratory) learning task

## Visualizing Data using t-SNE1
- t-SNE is mainly a non-linear dimensionality reduction technique for visualization
- t-SNE stands for t-distributed Stochastic Neighbor Embedding
- The main idea is to project high-dimensional objects to a low-dimensional objects such that there is high probability that
- t-SNE minimizes the divergence between - a distribution of pairwise similarities in high-
dimensional space
- a distribution of pairwise similarities in low- dimensional space

## Spatial and temporal anomaly detection
Report any observed value that is significantly above or below its expected value (e.g., using GESD).
Time series data Spatially distributed data
One simple case of model-based anomaly detection is when we are monitoring a single real-valued quantity over time and/or space


###Anomalous pattern detection
 
Main goal of pattern detection: to identify and characterize relevant subsets of a massive dataset, i.e. groups of records that differ from the rest of the data in an interesting way.
 


###Subset scanning
 
We can scan over subsets of the dataset in order to find those groups of records that correspond to a pattern.
 
Step 2: Consider the highest scoring potential patterns (S, P) and decide whether each actually represents a pattern.
 
Step 1: Compute score F(S, P) for each subset S = {xi} and for each pattern type P, where higher score means more likely to be a pattern.
 
###Linear-time subset scanning
 
Given a score function F(S) which satisfies the linear-time subset scanning property, we can optimize F(S) over the exponentially many subsets of data records, while evaluating only O(N) regions instead of O(2N).
Just sort the locations from highest to lowest priority according to some function, then search over groups consisting of the top-k highest priority locations (k = 1..N). The highest scoring subset will be one of these!

## Why Bayesian networks?
- An easily interpretable graphical representation of the relationships between a set of variables.
- Bayes Nets can be specified manually or learned automatically from data, and enable computationally efficient probabilistic inferences.
- Many practical and successful applications in medicine, manufacturing, failure diagnosis:
- Diagnosis: infer Pr(problem type | symptoms)
- Prediction: infer probability distributions for values that are
expensive or impossible to measure.
- Anomaly Detection: detect observations that are very unlikely (i.e. have low probabilities given the model).
- Active Learning: choose the most informative diagnostic test to perform given these observations.

“X and Y are conditionally independent given Z”: Pr(X, Y | Z) = Pr(X | Z)\*Pr(Y | Z)
or
Pr(X | Z) = Pr (X | Y, Z) and Pr(Y | Z) = Pr(Y | X, Z)


Make a truth table listing all combinations of values of your variables. If there are M binary variables, the table has 2M rows.



## The many uses of Bayes Nets
Bayes Nets provide a useful graphical representation of the probabilistic relationships between many variables.
Automatic learning of Bayes net structure can be used for exploratory analysis of datasets with many attributes.
We can often improve the performance of model-based classification by moving from Naïve Bayes to Bayes Nets.
We can also use Bayes Nets to detect anomalies, by finding points with low probabilities given the Bayes Net.
Bayes Nets provide a compact structure which enables us to efficiently compute probability distributions for any unobserved variables given observations of other variables.






















------------------------------------

















--------------------------------------------------------

# CT3: Fraud Analytics

Frauds: Fake insurance, wrong medical claims and invalid transactions.

Money Laundering: Hide the origin of money by passing from complex transactions.

Why ML here: It can detect fraud using behaviours in data.

[C5.0](https://cran.r-project.org/web/packages/C50/vignettes/C5.0.html) is a classification algorithm. This was used to create a model which detected Money Laundering. It reduced number of transactions reported from 30% to 1%.

Based on behavioural data ML model can detect **anomalies**. It shows a row of data that stands out, like, too many txns on online shopping.

We use supervised learning, where based on each columns (attributes) we assign a class to the data. Data has to be labbeled.

- **Deep Neural Network (DNN)** can be used for classification. **Neural Networks** has hidden layers where we use transform functions, DNN has 100s of hidden layers.

- **Perceptron** is the simplest neural network possible: a computational model of a single neuron. A perceptron consists of one or more inputs, a processor, and a single output. It defines decision boundary between classes by defining the **hyper planes** in higher dimensions.

- **SVM or Support Vector Machines** can be used for classification. It uses a technique called the kernel trick to transform your data and then based on these transformations it finds an optimal boundary between the possible outputs. It finds several hyperplanes to minimize the classification error.

- **K-Nearest Neighbours or KNN** uses simplicity metrics to group samples into classed in featured space. New data is assigned to the class which is nearest to the class.

- **Random Forests** breaks data in many samples and makes decision tree from each. New data is passed from trees and then picks the majority vote to assign data to class. This outperforms others but has issues of overfitting.

Financials fraud data is generally skewed.

**Exploratory Data Visualization** is used to view how our classes differentiate. Find patterns of differentiation in data.

- **Andrews Plot** shows curves and usually classes are well seperated in the curves.

- **Parallel Lines** each attribute is vertical line, each row is ||el line, classes can be seen separated.

In summary:

- Class labels are needed for supervised learning
- Perceptron learning lays the foundation for many of the neural network architectures
- Financial fraud data is singularly characterized by the skewed nature of the data 
- Overfitting in neural networks is a generic issue
- Very powerful algorithms exist for supervised learning

t-SNE t-Distributed Stochastic Neighbor Embedding (t-SNE) is an unsupervised, non-linear technique primarily used for data exploration and visualizing high-dimensional data. It gives you a feel or intuition of how the data is arranged in a high-dimensional space. t-SNE is a powerful visualization tool that preserves topological structures in the higher dimensional space

Chernoff Faces, each attribute is specific feature on face, can have upto 17 attributes.

Plot Histo, box plot, andrew, parallel, t-SNE, chernoff, pair plot, pareto of eigen values, scatter of pca and visualize. t-SNE, reduces 6D to 2D.









ML

Dimentionality Reduction

Examples Datasets




Machine learning for Fraud Analytics

Fraud Stats:
- $26b fraud
- CNP 82% reason

Examples of Fraud:


Potential for ML use:
- banks legacy systems use about 300 rules to approve a txn
- ML algos can use other attributes of user like IP, device, day of time etc to detect fraud.
- We will use supervised learning.
- *80% time in EDA and DC.*

Anomaly Detection:
- 
















------------------------------------

# SA4 - Term 4

Kaggle

**Linear Regression** is relation in **observations** ($x_i$ : set of variables) and **outcome** ($y$ : variable of interest) which tells us how x variables explain y. It is a line which has shortest distance to all possible outcomes from observation.

## Covariance and Correlation

**Covariance** is variation of data from the mean. The value depends on unit and is not standardized. 

To calculate, find variation of each point from mean and then the product of variations. Then sum these variations and divide by n-1: 

$$Cov(Y,X) = \frac{1}{n-1}\sum_{i=1}^{n} (y_i - \bar{y})(x_i - \bar{x})$$

Here, +/- tells us relation but value does not tell the strenght as it varies with the unit of measure. We standardise values to find strength, in correlation.

**Correlation** is how variables are linearly related to each other. It is standardized and does not change with the unit of X. The sign tells us +/- relation and the value tells us the strength. $cor(Y,X) = 0$ does *not* mean that they are not related, it only means that they are *not linearly* related as they may have non-linear relation, like, $ Y = 50 - X^2 $.

To calculate divide the diff from mean by standard deviation:

$$ Cor(Y,X) = \frac{Cov(Y,X)}{S_xS_y} = \frac{1}{n-1}\sum_{i=1}^{n}\left (\frac{y_i - \bar{y}}{S_y}  \right )\left (\frac{x_i - \bar{x}}{S_x}  \right ) = \frac{\sum(y_i - \bar{y})(x_i - \bar{x})}{\sqrt{\sum(y_i - \bar{y})^2\sum(x_i - \bar{x})^2}}  $$

## Use of Linear Regression

- **Relation**: To understand relation between X and Y, e.g. is sales related to advertisement, location, color etc? If so how, +/-, less/more.

- **Prediction**: To make predictions about Y variable, once we train the model (equation) from test data we can then predict Y from new X varables.

## Steps in Linear Regression

We often do, modelling, estimation, inference, prediction and evaluation. And them may be repeat the cycle with corrections.

### Modelling (define): Develop a regression model

The initial step in doing linear regression is to model the data. In this, we **identify** the variables of interest that we think are of importance in expaining y. This is usually based on past experienece. The variables are **not exhaustive**. Simple linear regression is formulated by following equation.

$$ Y = \beta_0 + \beta_1 X + \varepsilon  $$

$\beta_k$ are called **regression coefficients**. We estimate these using the sample data.

$\epsilon$ is the **random error**. This occurs because we might be missing some important x variable or x and y variable might not be linearly related. This is difference of actual point from the fitted point. This is also measure of **goodness of fit** of the regression model.

Modelling should take 95% of time, thinking about variables, x variables. The remaining steps below, estimation, inference and prediction, should take 5% of the time.

For example, 
price/advertising cost/promotion costs
- e.g. $UnitsSold = \beta_0 + \beta_1 Price + \beta_2 AdExp + \beta_3 PromExp + \epsilon$


### Estimation (fit): Using software to estimate the model

Prior data is required for each X, it could be collected over time. Use excel/r/python to fit the model. Linear regression gives **estimates** of regression coefficients, or **predicted weights**, denoted by $b_0, b_1, ..., b_r$. We use **least squares method**, min sum of vertical distances, 

$$ \hat\beta_1 = \frac{Cov(Y,X)}{Var(X)} = Cor(Y,X)\frac{S_y}{S_x} $$

Here, we have an **assumption** that Y and X are *linearly related* hence the estimated coefficient we got needs to be checked against this assumption before drawing any conclusion..

It gives us **estimated regression function**

$$ y = f(X) = b_0 + b_1x_1 + ... + b_kx_k $$

Now for each i'th observations, or i'th row, we can put in the function to get **estimated** or **predicted response**, $f(X_i)$. This should be as close to actual reponse $y_i$. The difference, $y_i - f(X_i)$ is called **residuals**. Now our aim is always to predict the beta estimates such that it minimizes the residuals, or deviation from actual y.

To get best predicted weights we minimize the **sum of squared residuals (SSR)**. for all i observations.

$$ SSR = \sum_i(y_i - f(X_i))^2 $$

For one x it is called simple linear regression, for more than one x, it is called **multiple linear regression**. In multiple linear regression with **two** x, it represents a **regression plane in a three-dimensional space**. The goal of regression is to determine the values of the weights $b_0, b_1 and b_k$ such that this plane is as close as possible to the actual responses and yield the minimal SSR. 

We also get **regression output**.Also here, we should get expected sign of estimators, else there might be some **problem**, like, multi-colinearity.


### Inference: Interpreting the estimated regression model

Inference in unerstanding the estimators and other stats from linear regression summary output. $\beta_1$ is, when the $X_1$ variable **increases by one unit** then the Y variable **increases by $\beta_1$ units**, all other variables in the model being kept at constant. So on for other betas.

For eg, $SalesUnits = -25096.83 - 5055.27Price + 648.61AdExp + 1802.61PromExp$. Here, $\beta_0$ is fixed cost of production, without making any unit.

$\beta_0$ is the value of Y when all X are 0. **All $x_i$ are 0**  needs to be relevant. It can be relevant when we talk about fixed cost of production. So units produced can be 0 but still b0 would be fixed cost. But in our sales model, we cannot infer that when price of product is 0, then b0 is number of untis sold. We need to make **managerally relevant interpretation** of $beta_0$. To **improve $\beta_0$ estimation** we need to adjust data. We can change data by, say, x* = x - mean of x. This will keep all coefficients same but will change $b_0$. In this case all x* will be 0 only if x is equal to mean of x. Hence, we are saying that, when our ad expediture is equal to average of ad expenditure in past two years then units sold is $b_0$. Rather than saying that when ad expenditre is zero in the original case. When we cannot make x equal to 0, for eg, $Income = b_0 + b_1Age$, here $b_0$ is **only to fit the beta** to the model but we **cannot make inference** that it is the minimum income, no!

**Regression line through Origin** means that model has **no intercept** or $b_0$. The residuals do not necessarily add up to zero. SST != SSE + SSR and $R^2$ identities are also not true.


### Prediction: Making predictions about Y variable

We can make predictions of Y value based on Xs, put value of Xs and beta estimators to get predicted Y value. For eg, create 3rd scenarios, how much to set price, how much to spend on ad and promotions, based on these scenarios we get Y that can help us decide on how to increase sales/profit. The farther the X is from the X-bar mean, the larger is the Std Err. So we should take precaution if predicting value farther from our observations.

### Evaluate: Determine how accurate the model's predictions are.

**Quality of Fit** or goodness of fit tells us how good our model predicts. **Larger t, or smaller p**, means **strong** linear relationship b/w x and y, use it to keep/remove observations in model. The scatter plot of Y and Ycap can also tell us the strength. The closer the stronger, this is same as Cor(Y,Ycap).

Needs update.. We can also measure by computing,

- SST, total sum of squared deviations
- SSR, sum of squares due to regression
- SSE, smu of squared errors (residuals)
- They are related: SST = SSR + SSE

$$R^2 = SSR/SST = 1 - SSE/SST = Cor(Y,X)^2 = Cor(Y,Yhat)^2 = R^2$$

0 < R^2 < 1, SSE<SST. Higher R^2 means strong linear relationship.

Repeat steps, modelling, estimation, inference & prediction, again to improve the model.


#### Standardizing

We might need to standardize the variables when we want to compare them for their effect on expaining Y. Standardizing makes them unit free, hence we can compare them. they can be standardized by doing $(x-\mu)/\sigma$ for all X and Y. Then we can run the regression model and interpret the coefficients. Here, **one std dev change in X changes Y by b1 std dev**.

#### Missing Values

We need to handle missing missing values in the data. THere are many techniques to do this. **Delete** if you have lots of data.


## Assumptions

There are a few assumptions that we have considered when we have estimated the coefficients. One of them is that all $\sum \hat{y} - y$ or $\epsilon$ is normally distributed around 0. The more we deviate from this assumption, the bad would our model fit.

$$\epsilon \sim N(0,\sigma)$$

Since we have this assumption and we have estimated betas, we can do a hypothesis test around this.

Now, CLT says that sample mean has Normal distribution with mean is population mean, and std is pop sd / root n, $ \bar{x} \sim N(\mu,\sigma/\sqrt{n}) $ . We actually never know the population mean. We estimate it from sample. Similarly we never know actual betas, we only estimate the bees from sample training data. Hence, all bees follow a norml distn with mean beta and std is std of beta.

$$b_k \sim N(\beta_k, std_{b_k})$$

Skipping lot of derivations, leads us to below equation that we can use for hypothesis testing.

$$\frac{b_0 - \beta_0}{S_{b_0}} \sim t_{n-k-1}$$

Here, $S_{b_0}$ is std err of $b_0$, n is observations, k is number of x variables. 


### Hypothesis Tests

Hypothesis test is done to handle the uncertainities of the estimates from sample. $b_0$ is estimate of beta, hence it is not a true value and we need to  have a confidence interval around it. 

For eg, Toy example, for ad_expense impact on units sold, the coefficient estimate is 600 but sales people say it should be around 300, then we have to check. The estimate is from sample, hence estimate and is uncertain, it is a belief, and it can be accepted or rejected. Hence, Hypothesis test. We need to **formulate a hypothesis test** for this. If SME says 1000 dollar increase in ad increses units sold by 300 units. Then, 

Ho: beta2 = 300, this is claim made, hence mu
Ha: beta2 != 300

Method 1: $x = b_2 = 648.6 ; \mu = \beta_2 = 300 ; \sigma = S_{b_2} = 209$ from regression output. Now it get back to std value and t-distribution.
Our estimated coeff, b2, follows a t-dist, its std value = (x-mu)/sigma, this is **t-statistic**. It is 1.67, or 1.67 std to the right of mu. Now on the graph, check if this lies in **rejection region** for a certain confidence level. Here, conf level is 95%, so alpha = 0.05, and it is two tail test, so we will use $\alpha/2=0.025$, deg of freedom is n-k-1, residuals. Use T.INV to get std value from probablity and deg of freedom, using `T.INV(0.025,20)` it gives cutoff value as -2.71. So if t-statistic is beyond +-2.71 then we are in rejection region, but as t-statistic does not lie in either region hence we fail to reject the NULL hypothesis. Thus, our data does not has enough evidence to not reject the NULL hypothesis. Hence, the claim may be true. Out data has much noise.

Method 2: **p-value** is probability that the sample mean would be >= sample mean, given NULL hypothesis (mean is somevalue) is true. Here, p-value is twice the value cutoff by t-statistic in two tail test. Use the t-statistic found above to calculate the p-value. if p-value is lower than alpha then we can reject the NULL hypothesis, p-value = 2X(1-T.DIST(1.67,20,TRUE)) = 0.11, since .11 > 0.05 alpha. Hence, we fail to reject the NULL hypothesis. Remember: **When p is low the NULL has to go**.

Method 3: Use **confidence interval** in regression output. If the claim in in CI, then we fail to reject the claim.


## Regression Output
Every statistical software nowadays produces regression summary or output. This can answer many questions related to variables.

#### R-Square
It tells how much percentage of Y is explained by the observations. Rsq may be low, then also model may have value as coefficients tell us the marginal impact. Rsq is imp but we should also consider the algebric signs of coefficients, their magniture should be plausible, they should be precisely estimated, and also check if you have missed any imp right-hand-side variable.

#### P-Values
The p-values in regression output are the values for a hypothesis test in which we say that the true value of the **coefficient is 0**, i.e., weather one unit change in x has 0 impact on y. By looking at them, we can tell which observation is **significant in explaining** my Y variable. Usually, if p-value if **higher than 0.05** then the variable becomes **insignificant** in explaining Y.

#### Coefficients
They are unit dependent, their magnitude cannot be used for comparision. They tell us the change in Y variable for one unit change in them. If you need to compare then stanrdize them.

#### Confidence Intervals
They tell us CI at a certain confidence percentage. They are CI for estimates of betas.

## Anomalies of Regression
There are many problems, like 

#### Multi-Colinearity
We might get high Rsq which means model is good fit, but also high p-value which makes observations insignificant or unexpected signs of coefficients, this might be **problem of multicollinearity**. It occurs when there is a nearly linear relationship among a set of explanatory variables, i.e., they are highly correlated, usually more than 90%. To solve it do a **pair-wise correlation** and just drop one of the correlated variable.

It might not be a problem when we only have to predict but not understand individual observation effect.

















------------------------------------

# Focused Session on Big Data Analytics

Find a polar bear in images from cameras in forest.
- use azure iot to get images from camera
- `devices.json` has camera lat, long, key and id.
- create cloud-shell, this gives bash shell on azure.
- create a resource group (project) on azure., 'streaminglab-rg'
- create storage account 'mysamg1'
- create storage account keys to allow camera to store files to your account.
- create disk space(container) named photos(dir)
- create 'azure iot hub'AIH to recieve photos in realtime. AIH can listen to multiple IOT devices at the same time. 'myhubmg1'
- get connection string to the hub, to access the cameras.
- deploy 10 camera array to AIH, they will send camera snap in some interval.
- On laptop, use node.js for sending photos (simulated cam, else cam kernel will talk to AIH)
- npm install AIH
- create devices.json has {lat: "", long: "", key: "", device_id: "").
- create deploy.json
- node deploy.js, read devices.json, the register to AIH
- key is populated for each devices once it is registered on AIH.
- to store photos, you need `azure-storage` pkg, install using node.
- create `test.js` to upload an image to AIH with camera device id, lat, long, timestamp details.
- Create 'stream analytics job'SAJ under IOT, 'polar_bear_analytics', this will take input from AIH and send the image to 'Vision Analytics'
- stream, clean, not all photo to ml
- In SAJ we can query based on window, timestamps, camera or other dimentions of data.
- SAJ -> Computer Vision APi (CVA), for this use cloud-functions
- go to function app, make func, (streaminglab-rg)
- create 'http trigger func' 
- now cretae 'run.js' that simulates real time, it uploads in random time interval.
- start SAJ
- SAJ sends filtered data to clout function which at the moment logs to console.

## Custom Vision 
- Create resource 'polar bear r1'
- kind: CognitiveServices
- the upload training images with tags.
- do quick training of the model.
- now publish this model to get a web-api. 
- we can use this web-api in our cloud ml function, then save the perdiction result to sql server.
- create sql server, myservermg1,
- configure the server to allow zure services, create db and table.
- update the function with js code to read preds from web-api and store results in db.

For counting, use regression model.

------------------------------------

# ML Classes:

ML in practise:
- most of the time goes in ML model building
- Auto ML does not works always
- data -> model -> predict
- Learning - 
- p-value tell if the model is correct. it is confidence
- missing values and outliers k liye seek domain guy/customer
- touch more on inference side.
- number has no value, inference has value in corp.

K-means algorithm, hands on:
1. decide number of cluster, k=2
2. initialize random data points as c1(x1, y1), c2(x2, y2).
3. now find eucladian distance (ED) between between all the points and all the centroids.
4. ED = [x1-x2)^2 + (y1-y2)^2]^0.5
5. now the point belongs to centroid to which they have minimum distance.
6. now calculate new c1, c2 by finding average of all new points belonging to the cluster.
7. repeat step 3 to 6, until you get same c1,c2 as in last iteration.

K-Means Variations:
- logic and flow remains same, but we can change the way we calculate the distance, hamming, manhattan etc. This changes the centroid and the point belonging to it.

Business Scenario 💼 :
- Client may say that no, point A belongs to other cluster
- Change clustering method/k value/etc
- so no clustering is best, it can only be acceptable, by client.

Hierarchical Clustering:
- Find dist of each point with everyother point. 5C2.
- create a 5X5 matrix with values as distance bw points
- in dendogram, y-axis is ED between points and x-axis is points.
- This is agglomerative clustering.
- Now any cut on Y axis gives us the clusters.
![Hierarchical Clustering](../images/hierarchical_clustering.png "Hierarchical Clustering")

Uber Case Study:
- Kmeans clustering to find centroid as place from where all rides can be catered. 

## Knowledge Graphs

Patters:
- How different subjects are related, find the connections, eg, Trump Boeing, Binny Bansal and Infosys.
- if business prob requires connections then build graphs
- Subject is node, edge is relationship.
- we can analyse customer care text data, and get insights
- 

-------------------------------------------

only ISB above ^

-------------------------------------------


# Mind Dump

-------------------------------------------


------------------------------------
# History:

Indus valley
- building cities and bath
- exchanged goat and crops
- had a language

Egypt
- around the river NIle
- rich in resources
- advancement in trade and military

Perians and Greeks
- 

-------------------------------------------

# Blogging and Notes Decisions:


## Bookdown:

Quick [getting started](http://seankross.com/2016/11/17/How-to-Start-a-Bookdown-Book.html).

Steps:
- `mkdir bookdown`
- `cd bookdown/`
- `git clone https://github.com/seankross/bookdown-start`
- `cd bookdown-start/`
- `r`
- `bookdown::render_book("index.Rmd")`

- all `# heading 1` are chapters.
- Add `Part I` before a chapter to make it part in a book, `# (PART) Data Science {-}`
- `> options(bookdown.render.file_scope = FALSE);` to use parts in diff directories.

To support GitHub flavoured MarkDowm, you need to add the following line to `_output.yml` file:

`md_extensions: +lists_without_preceding_blankline+pipe_tables+raw_html+emoji`


References:
- Bookdown [cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/rmarkdown-anatomy.html)
- [Bookdown](https://bookdown.org/yihui/bookdown/html.html)
- Rafalab [dsbook](https://rafalab.github.io/dsbook/introduction-to-productivity-tools.html)
- Rafalab book [source github](https://github.com/rafalab/dsbook/blob/master/_bookdown.yml).
- Bookdown data science notes [book](https://bookdown.org/mpfoley1973/data-sci/)
- Python Visualizations in [bookdown](https://bookdown.org/jamie/python_visualisation/)
- Using [Python Environments](https://bookdown.org/yihui/rmarkdown/language-engines.html)
- Show plotly html js in Rmarkdown [stackoverflow](https://stackoverflow.com/questions/50191208/display-python-plotly-graph-in-rmarkdown-html-document)
- code options [cheat sheet](https://rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf)
- publishing on [github](https://bookdown.org/yihui/bookdown/github.html)
- pandoc markdown [formats](https://pandoc.org/MANUAL.html).


-------------------------------------------


------------------------------------------------

------------------------------------------------

# Digital Marketing Notes

Instagram page earning:
- original images
- regular posting


------------------------------------------------

# Plotly D3 Vizs

- poltly built on top of D3
- python api uses plotly.js


Plotly Library:
- data - result of go.chartType(x=, y=, others=....)
- layout - title, axis, annotations
  - has param `updatemenus`
  - There are four possible update methods:
    - "restyle": modify data or data attributes
    - "relayout": modify layout attributes
    - "update": modify data and layout attributes
    - "animate": start or pause an animation
- frames: used for animations
  - we can add different frames to a chart
  - this can be used to produce the animations
  - Example can be found [here](https://plotly.com/python/animations/#frames).
- figure - final object combining data and layout.

Dash is putting and linking many plotly charts together.

## Other plotly products

Dash:
- Dash is Python framework for building *analytical web applications*.
- It is built on Flask, Plotly.js and React.js
- Just like flask, we define `app = dash.Dash()` and then at end `app.run_server()`
- We can create complete site with links.
- It has intractable story.

Chart Studio 
- is like Tableau web edit and public.
- Can create and host data, charts and dashboards.
- can explore other people's work.
- charts are interactable and linked together.
- can be reverse engineered.
- can host notebooks as well.

ObservableHQ:
- Live, web edit, d3 notebooks.
- markdown and JS blocks
- lots of d3 features. like counts, action buttons etc
- can make dasboard as well.


References:
- [How and why I used Plotly (instead of D3)](https://www.freecodecamp.org/news/how-and-why-i-used-plotly-instead-of-d3-to-visualize-my-lollapalooza-data-d48345e2ca68/)
- [4 interactive Sankey diagrams made in Python](https://medium.com/plotly/4-interactive-sankey-diagram-made-in-python-3057b9ee8616)

# D3

Add D3 library. Then specific module.
- it is collection of module that work together
- data is bounded to the selections, it join-by-index
- By default, the data join happens by index: the first element is bound to the first datum, and so on. Thus, either the enter or exit selection will be empty, or both. If there are more data than elements, the extra data are in the enter selection. And if there are fewer data than elements, the extra elements are in the exit selection.
- selectAll() data() enter() append() - to add elements, SDEA.
https://observablehq.com/@d3/d3-hierarchy?collection=@d3/d3-hierarchy


------------------------------------------------


# Flutter Notes
------------------------------------------------



------------------------------------------------

# GCP Firebase Notes

------------------------------------------------

# Mac OS (Linux) Notes

------------------------------------------------

# Google Cloud Platform Notes





------------------------------------------------

# Flask Notes



------------------------------------------------

# Web Server Notes




------------------------------------------------


# Python Notes

## Anaconda and Conda Notes with Jupyter and R Studio

**Anaconda** is toolkit for Data Science.
- it includes ds and ml libraries along with conda, and 
- other tools like jupyter, rstudio etc.

**Conda** is package manager and environment manager, like pip,
- it can install packages and 
- can manage envs 
- It is a CLI

**Anaconda Navigator** is GUI to use conda.

Conda Basic Commands:
- `conda config --set auto_activate_base false` disables autoload base
- `conda update conda` updates conda
- `conda install PACKAGENAME ` installs pkg to default/active env
- `conda update PACKAGENAME ` updated pkg
- `pip install pkg` aslo intalls to active env

Conda Env Commands:
- `conda create --name py35 python=3.5` created new env and installs py 3.5
- `conda activate py35` activates
- `conda list` lists all akgs installed ina ctive env.

**Jupyter** name comes from Julia, Python and R,
- formerly known as *IPython Notebook*
- it is pkg, same as flask
- `pip install jupyter` or it comes installed in Anaconda dist.
- `jupyter notebook` runs a server to server jupyter notebooks at http://localhost:8888/tree

**R and RStudio** are statistical language and IDE,
- `r` or `R` - R console in terminal
- `Rscript my.r` - executes file in terminal
- `Rscript -e "getwd()"` - executes cmd in terminal, can quickly install a library.
- `R CMD BATCH my.r` runs R script and saves output to `my.r.Rout`
- To make R Script executable like `./my.r` then:
  - set permission to 755
  - add correct `#!` to top of file

```r
#!/usr/bin/env Rscript
sayHello <- function(){
   print('hello')
}

sayHello()
```



## Regex Notes:

Remove single line comments // from code:
- `\/\/.*$\n` - Finds all single line comments starting with //.
  - `\/\/` - string has //
  - `.*` - then has anything after that
  - `$\n` - then matches next line as well.
- Check and Validate on [Regex101](https://regex101.com/)
------------------------------------------------

# AI image generator Notes:
- GAN is used to genrete original like images
- Deep Convolutional Generative Adverserial Networks (or DCGAN) are a deep learning architecture that generate outputs similar to the data in the training set.
- This person does not exist.com
- nVidea research lab, start with low resolution and keep training to make a full resolution image.
- two ai neural network work against each other to generate and eveluate the images.
- fake images, fake media
- computing power is still issue
- lip syncing image to audio
- dataGrid, deepFake AI models


------------------------------------------------

# Ayurveda

Earth is governed by sun and moon, they change its movement which changes day-night and seasons which changes other things, we are also made of earth, hence sun and moon change us.

Routine:
- 5:30 Wake up in last phase of darkness, Bramha Muhurat, because, vata is active, which is why we remember dreams of this time, meditate and study time.
- Freshen up
- Work out till sweat
- Bath
- Meditate
- Breakfast, lunch
- Evening recreation
- dinner 2 hours before sleep
- sleep for 8 hours.

Parpancha, five elements, Akash, bhoomi, vayu, agni, jal

Three dosha, defines body and behaviour:
- 05, Vata - vayu aakash
- 80, Pitta - agni jal
- 15, Kapha - bhoomi jal





------------------------------------------------


# Agriculture

What went wrong:
- Punjab destroyed
- Debt suside
- Water level

Important people:
- Aacharya Devvrat, Rajyapal, Himachal Pradesh
- Subhash Palekar, noble price winner
- Vandana Shiva, nobel price winner
- Binay Kumar, art of living
- Prem Singh, Ecological farmer, activist

Cow Breeds
- A2 cow is desi and amrit

Where money goes?
- Monsento
- Syngencha
- SBI
- Bill Gates - failed gmo project

## Zero Budget Natural Farming (ZBNF):
- Farming technique in which we do not use raw materials like pesticide, urea etc.
- Belief is that soil needs to be living with microorganisms and worms
- Itegrating cow dung and urine make it living and this everything flourishes.

- Benifits:
  - Long live of plants
  - 90% less water
  - Climate resistant

- Products:
  - Ghan Jivamrit (fertilizer)

- Important people:
  - Aacharya Devvrat, Rajyapal, Himachal Pradesh
  - Subhash Palekar, noble price winner

## Permaculture
- Karne se zada hone do kaam ko
- Sustainability will come
- greed drives life, show money to farmers in prmcltr

- Health
  - Soild needs skin, leves, grss etc.
  - Value organic matter.




------------------------------------------------



# Astrology and Vedic Life
- hormones control body
- planets control hormones
- stones link to planets
- stones filter light and inc/dec effect of planet
- stones also have vibrations
- Law of Vibration, ‘everything in the universe moves or vibrates’.
- birth snap of planets effect you

## Taurus
- Auspicious
  - Saturn is on your side.
  - Mercury helps you communicate effectively.
  - Mars is also a blessing for Taurus. 
  - Sun is ideal for a Taurus to achieve success in life.

- Malefic 
  - Jupiter can harm you if you’re a Taurus. 
  - Venus can make you unhappy and dissatisfied in life.
  - Moon is also malefic for a Taurus and can deter you from destiny. 

## Om Theory
- Om is originator vibration, 
- https://www.one-mind-one-energy.com/theuniversallaws.html
- from om five elemental vibrations emerged.
  – Jupiter for Ether, 
  - Saturn for Air, 
  - Mars for Fire, 
  - Mercury for Earth, and 
  - Venus for Water.
