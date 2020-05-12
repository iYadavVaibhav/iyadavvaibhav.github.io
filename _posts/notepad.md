# Mind Dump

To do:
- Plotly Dash +1, Eric Kleppen
- Post to github your flutter finished apps. eg: starred repos
- Flutter ORM
- Python Flask REST API GCP Firebase
- Starred Repos
- Tabs app using BloC.
- flask app with data models integrated, and hosted
- flutter app with data models integrated, and hosted

Intro to:
- Tensorflow +1
- Digital Marketing

Watch
- Startup stories
- Google Channels - cloud for students
- ML Recipies
- 7 steps of ML
- ML zero to hero

- wordpress -> JAM Stack

on-going:
- Flutter architecture samples
- flask restful
- flask todo miguel
- whatsapp analytics
- feedback pwa, qr
- doodh hisab, notification daily
- medi tracker
- firbase ML in Flutter
- Python ETL
- Tableau publish favourites
- Tableau LM tutorial article/git
- Medium articles to be published

Clean up Mac:
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


# Digital Marketing Notes

Instagram page earning:
- original images
- regular posting


# Node JS Notes
- node js is like asp/php/flask
- you can run .js files outside browser
- give ability to use js in backend
- npm is package manager like pip for node js
- pakages are nothing but js libraries.

# Flutter Notes
- Framework to develop mobile/web apps
- Everything is a widget
- uses DART as a programming language
- code gets compiled to java/javascript/swift for native performance.

Initial steps:
- `flutter create --org com.codeo myapp` create a basic app
- `flutter pub get` gets all packages
- `flutter run -d Chrome` runs flutter app on device chrome
- `pod setup` makes ios deploy faster
- `flutter build web/apk` builds app for publishing

Structure:
- assets - hold images/fonts
- lib - all the dart code
  - we can make folders specific for activity
  - models - hold class for data in the app like users.dart, deserialize json
  - pages - hold screens, each .php page or route
  - widgets - component on pages, like progress bar

Architectures (State Management):
- Flutter allows to use many kind of state management architectures like Redux, BLoC, MobX and many more.
- These all are commonly used architecture to layer out UI from Database/WebAPIs.

Basic Workflow:
- make product class, init constructor, add factory, the get and set functions
- link this to sqflite
  - have a db_provider
  - and an init function
  - crud functions
- or firebase
  - get reference of a collection in instance.
  - from ref get the snapshots and build.

BLoC - Business Logic Component
- separates UI from Business logic (Database and Network).
- `Sink<data>` - data in - events
- `Stream<data>` - data out - state

![BLoC diagram](https://www.mobindustry.net/wp-content/uploads/bloc-architecture.jpg "BLoC image")

- BLoC component converts a stream of incoming events into a stream of outgoing states. 
- Close bloc references in despose() methods.
- It has:
  - Bloc
  - BlocBuilder
  - BlocProvider


Redux:
- provides routing as well
- works with store reducer concept

ScopedModel
- Updates only model in scope, not the whole widget tree
- Have to notifyListeners() on each state change

- Links:
  - [Flutter Architecture Samples to build ToDo apps](http://fluttersamples.com/)
  - [The Essential Guide to UI Engineering](https://www.youtube.com/playlist?list=PLS2-V7v1NhNQB66bFNIXlQ_83chw0TgK6)

Development:
- `add(a,b) => a + b` creates function inline and returns valuel, can be without name.
- `setState(){}` - rebuilds the app. usually used in onTap(){}.
- wrapping parameters in {} make them named params and we have to specify the name when passing them in call. eg: `emp({String name, Int age})`, when called, `emp(name: 'Jon', age: 34)`.
- `initState() {}` function gets executed in every State ful widget. can be used to call all what we want to initialize, like db fetch etc.
- `<Future>` needs to be handled. Either we can use `.then((data) {...})` or we can add keywords `async...await` to the functions.
- `factory` before a func declaration makes it accessible outside class just like static.
- To preserve state of app, use mixin keep alive.
- await and async are good to wait for a process to finish and the execute the rest.

Navigation:
- We can generate route on the go with Navigator.pop or push.

Function calling:
- When work needs to be done on call, then pass refrence.
- When function builds/returns then call with ()s.
- Here is the difference:
  - onPressed: \_incrementCounter is a reference to an existing function is passed. This only works if the parameters of the callback expected by onPressed and \_incrementCounter are compatible.
  - onPressed: \_incrementCounter() \_incrementCounter() is executed and the returned result is passed to onPressed. This is a common mistake when done unintentionally when actually the intention was to pass a reference to \_incrementCounter instead of calling it.

External Links:
- appicon.co - app icons
- icons8.com - use icons for free
- vecteezy.com - icons
- canva.com - create own design


# Firebase Notes
- Cloud app backend which helps in:
  - authentication
  - database, firestore_cloud
  - file storage

## Firestore Notes
- It is NoSQL database storage engine in firebase

Initialization:
- create database
- create table, called collection, users
- create rows, called document, doc_id

Connecting apps:
- iOS:
  - add GoogleService-Info.plist in xCode 
  - add reverseClientId in key CFBundleURLSchemes Runner/info.plist
- android:
  - add google-services.josn and 
  - make sure applicationId is correct in app/build.gradle

Reading data (Flutter):
- Create a reference to instance of a collection, `userRef = Firestore.instance.collection('users')`.
- The above has functions to fetch records as snapshot of data
- It returns future which need to be handled.
- use StreamBuilder
- stream: Firestore.instance.collection('users').snapshots(),
- reference object accepts chain of functions like `where()..orderBy()..limit()` etc. for compound queries.
- `FutureBuilder` - reads data in database
- `StreamBuilder` - provides stream to data, shows new user added.

NoSQL Structuting:
- do not nest collections
- keep data flatten
- copy data but mostly stored in the way it is best to be fetched.

Create/Update/Delete data (Flutter):
- onTap: () => record.reference.updateData({'key': new_value})
- now its all linked from front to back
- all sync and updates offline and online.
- reference has function like `add()..updateData()..delete()`. They all return `<Future>`.

Triggers:
- user firestore triggers to listen and act on the change in a collection.
- It uses node js to write and deploy the functions.
- Triggers can be created by using Trigger functions. Steps:
  - `firebase login` - login to your google account to use CLI.
  - `firebase init fucntions` - create fucntions folder in flutter project.
  - `firebase deploy --only functions` - deploy functions to firebase cloud.

# Mac OS (Linux) Notes
- everything global is installed in /usr/local/bin/
- use PostMan for http requests to REST routes

# Google Cloud Platform Notes
- GCP is cloud service from Google just like AWS and Azure.
- It provies [Firebase](#Firebase-notes) as datastoage engine.
- Hands on: https://codelabs.developers.google.com/codelabs/cloud-vision-app-engine/index.html
- Greate and app engine
- App Engine is PaaS for deploying web apps on GCP.
- create storage bucket



# Python Notes

## Web Dev Libs
Flask
- light weight web framework
- FlaskRESTful - extention for REST framework

sqlite3
- store to local db

Shelve
- Persistant object storage library

Pickle
- Dump objects to file and load back

Pandas
- Data maipulation
- Pandas vs Dask vs Spark
  - less than a gb, use pandas
  - upto 100 gb, use pandas with chunk or dask or pyspark
  - more than 100gb, pyspark for sure, upto peta bytes
  - [Pandas, Dask or PySpark - Medium](https://medium.com/datadriveninvestor/pandas-dask-or-pyspark-what-should-you-choose-for-your-dataset-c0f67e1b1d36)
- Superfast Pandas, make data transformation in pandas upto 7237 times faster:
  - use iterrow
  - use apply(lambda)
  - use pandas vectorization, loc(filters here)
  - use numpy vectorization, pass as numpy.array, converts to C code.
  - [Making pandas loop faster](https://towardsdatascience.com/how-to-make-your-pandas-loop-71-803-times-faster-805030df4f06)


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
