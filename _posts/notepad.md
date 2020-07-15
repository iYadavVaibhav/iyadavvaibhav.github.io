Handover
- [x] api is working via domain and wsgi
- [x] add basic auth, followed by user auth
- [x] create tasks rest
- [ ] add process starter, miguel modern deployment.


------------------------------------

# SA4

## Linear Regression 

Relation in Y and X such that X variables explain Y

Why do LR:
- Relation: Understand relation between X and Y, e.g.
  - Relation of sales on profit
- Prediction: To make predictions about Y variable

**Problem:** Anita wants to predict the number of toys she can sell in coming half year.

Step 1: Modeling: Develop a regression model
- identify the variables: proce/advertising cost/promotion costs
- Variables are not exhaustive
- SalesUnits = $\beta_0 + \beta_1 Price + \beta_2AdExp + \beta_3PromExp$
- Beta_s are coefficients,
- signs expected are: b1 -ve, b2 +ve, b3 +ve

Step 2: Estimation: Using software to estimate the model
- prior data, collected over time
- use excel/r/python and get refgression output
- this gives coeffiecients, the betas
- get expected signs of betas

Step 3: Inference: Interpreting the estimated regression model
- $SalesUnits = -25096.83 - 5055.27Price + 648.61AdExp + 1802.61PromExp$
- beta means when X increase by **one unit** y increases by beta times, keeping others constant.
- beta0 is Y when all X are 0.
- beta0 is fixed cost of production, without making any unit.

Step 4: Prediction: Making predictions about Y variable
- put value of Xs and betaS and get Y value.
- create 3 scenarios, how much to set price, how much to send on ad and promotions, based on these scenarios we get Y that can help us decide.

Results:
95% time on Modeling, 5% on rest steps.

Assumptions:
- Hypothesis testing on the regressions:
- $Y = \beta_0 + \beta_1X_1 + \epsilon$
- here e is the error.
- these errors are normally distributed around avg value 
- avg of errors is 0, $\epsilon_i ~ N(0,\sigma)$

- in regression output we do have result of hypothesis test, as p-values

Why is p-value imp:
- tells significance of X in explaining Y,
- *when p is low, null has to go*


# Session 2

Problem a): Test the Hypothesis that price has no effect on sales

Answer: Check hypothesis on beta1 ehich is coefficient of Price.

$H_0: \beta_1=0$
$H_1: \beta_1 \neq 0$

- Check this using confidence interval from refression output.
- lower 95% = -6153.32 and upper 95% = -3957.22
- hecne, beta1 != 0
- also, p value = 6.2E.09, which is low, null has to go.
- We reject the NULL Hypothesis, Ho, so sales is dependent on price.

Problem b): Company would agree to proposal of 25 cents drop in toy price if there is evidence that price reduction would lead to *at least* an increse of 1500 unit sales.

Answer:
- When price inc by 1 then Sales inc by $\beta_1$ units.
- when price dec by 1 then Sales inc $-\beta_1$ units.
- when price dec by .25 then => Sales inc $-\beta_1/4$ units.

$=> H_0: -\beta_1/4 \geq 1500$ and $H_1: H_0$ not true

$=> H_0: -\beta_1 \geq 6000$ and $H_1: \beta_1 < 6000$

$=> H_0: \beta_1 \leq -6000$ and $H_1: \beta_1 > -6000$

- This single tail test, solve using CI in summary table.

- to do

Problem: Car

Answer: 
- Y variable is gasoline required for 100 miles.
- Y column = 100/MPG
- Run regression, from output,

- Weight - for every 1000 lb increase in weight of car, the gasoline required to travel a 100 miles increases by 1.56 gallons, all other varibales kept at the same level.
- Horsepower 
  - since p-value is more than alpha hence it is not significant in explaining Y. 
  - This seems wrong and is a pitfall of regression, will be covered in multi-co-linearity.
  - this should be checked as, from common sense, horsepower effects mileage.
- R square 
  - the variance explained by residuals is 92%, 
  - there is variation in Y variable because some have high efficiency some low.
  -  It can explain 92% of this variablility in fuel efficiency, 
  - how much variation gets explained is R-square. 
  - 92% is high, hence, model will make good predictions.
- What impacts fuel efficiency the most?
  - we cannot depend on coefficient as it is unit dependent.
  - p-value are used as cut-offs to rule out the coefficient.
  - 1sd change in weight, has coeff sd change in Y, 1sd change in weight is 1.01 sd change in Y. hence weight has more impact.


------------------------------------



vy tk
- beer mug viz
- payments getting back in sector
- kiran flask following on conv .2 for ds plz let me know
- gone down the storm
- send link

Partnerships:
- change filter label, grp = partner type, and partner name.
- on all pages.
- add same filters on single merch p&L.
- wed morning.


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

# Mind Dump

To do:
- [ ] Plotly Dash +1, Eric Kleppen
- [x] Post to github your flutter finished apps. eg: starred repos
- Finder is slower
- speed up terminal startup time.
- Flutter ORM
- [x] Python Flask REST API GCP Firebase
- Starred Repos
- Tabs app using BloC.
- todo app in flask RESTful completed, decide backend to be sqlite or firebase?
- flutter ui for todo [app](https://github.com/devinsays/laravel-react-bootstrap)
- flask app with data models integrated, and hosted
- flutter [app](https://wptheming.com/2019/11/flutter-todo-app/) with data models integrated, and hosted

- Intro to- Tensorflow +1
- intro to Digital Marketing

Watch
- Startup stories
- Google Channels - cloud for students
- ML Recipies
- 7 steps of ML
- ML zero to hero

- wordpress -> JAM Stack

on-going:
- Flutter architecture samples - [BloC](https://medium.com/flutterpub/architecting-your-flutter-project-bd04e144a8f1)
- flask restful
- flask todo miguel
- whatsapp analytics
- feedback pwa, qr
- doodh hisab, notification daily
- medi tracker
- firbase ML in Flutter
- Python ETL notebook
- Tableau publish favourites
- Tableau Live Monitor tutorial article/git
- Medium articles to be published

Clean up Mac:
- Used GrandPerspective.dmg
- Win 10 image
- ISB Cludera clarify backup folder
- Files in documents
- remove and delete vagrant
- Pictures- backup and delete
- Music in iTunes
- android avds Library/Android
  - .andoird
- code/Video Tutorials
- code/clients and docs - zip them
  - mongo db - up and running
  - elastic - up and running
  - native - completely remove
  - infy online trainigs - review remove

# Do what I want to do
- dont wait for a miracle to happen.
- be consistent to see result
- get out of comfort zone and 
- no short term pleasures
- If you want to shine like a sun, then first burn like a sun

## identify the pattern, start a journal.
- Identified - laptop/mac not in morning
- Start small, one exercise, picking gradually

## How:
- Goal oriented, break, stick, achieve, reward
  - Goal - fit and look good
  - Break - one exercise
  - Stick - just one, but daily
  - Achieve - Doing
  - Reward - in the mirror.

------------------------------------------------

# Digital Marketing Notes

Instagram page earning:
- original images
- regular posting

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

- password for apps is apps

- 




------------------------------------------------


# Python Notes


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
