---
title: Train That Brain
description: A learning app for autodidacts
img: /brainLogoExample.png
---
### The problem 

In 2019, I moved to the beautiful city of Bilbao, Spain.<br>
Since I was born in the Netherlands, I only knew a handful of words in Spanish.<br>
Obviously, it’s not ideal to live in a country where you do not speak the language.<br>

So during my time there I started learning Spanish.<br>
To learn as efficiently as possible, I kept on looking for apps and tools that I could use to improve my Spanish learning.<br>
For me to learn anything, there are two things I need to do.<br>

Firstly, I need to read (this is true for when I learn languages, science, coding or anything else) about the subject, and when it comes to learning languages, I need to read in my target language. 

Secondly, I need to apply the knowledge I gained by reading.<br>
This second step greatly increases how much I remember after a period of not using it.<br>

So, when it comes to learning Spanish, I had to read in Spanish and then try and write and speak as much Spanish as I can.<br>
Language learning apps like Duolingo can work to learn this way, but the premade content that Duolingo uses was not ideal for me.<br>
I prefer reading the stories that I would normally read in English or Dutch.<br>

So, I found some of the books that I like in Spanish and translated the words I didn’t know (spoiler: a lot!) with my phone.<br>
This did work but it certainly wasn’t ideal.<br>

Then a friend pointed me to Learning With Texts (LWT).<br>
This is an open-source app where you can do exactly what I wanted.<br>
You simply import a text to the app, and you start reading.<br>
While reading the text, you can click on any word and it automatically gives you the translation.<br>

You can then easily save this word and its translation to a flashcard-list.<br>
You can practice your saved words (flashcard-style) or export them to a flashcard app like Anki.<br>

Now then, does this mean my problem was solved?<br>
Most certainly not.<br>

The software works, and it is quite good at what it does.<br>
But it had a couple of its own issues:<br>

1) It was made by a single developer that could not maintain it very well. This meant, for example, that the only way you could use it was by hosting it locally on your own pc.<br>
This means that your data was on one device and that it could not be synced with any other devices.<br>
 
2) The UI is old, very old. 
The developer developed an effective tool but did not want to focus on design or styling.<br>
This means that for someone that loves beautiful design (like me) it was not too exciting to use.<br>

 
### The solution 

Since I had been learning HTLM, CSS, JS, and, most recently, Vue.js over the past few years I decided to try and create my own software to tackle the issues I had with LWT. 

There were a few things that I had to figure out before I could start coding. 

1) What do I want this webapp to do? 

After sketching out multiple possible versions, I decided on what the core features should be: 
- Easy to add texts with quick and accurate translations when a word is clicked. 
- Easy to use option to add translated words to flashcard-lists. 
- Option to practice flashcards with spaced repetition. 
- An intuitive UI that makes it easy and pleasant to use. 



2) What technologies will I use to build it? 

This required a lot of research since I was not entirely sure what the app would need. 
These are the main technologies I picked for the project and the reasons why I chose those. 
- Vue.js 
Vue is a JavaScript framework made by Evan You. 
It is easy to get started and has a lot to offer. 
Some of the main features are: 
- Easy to create dynamic webpages 
- Great code reusability by creating components 
- Powerful libraries like Vuex (centralized store), Vue router and Vue Server Renderer (easy server-side rendering).
<br>
<br>

When I wanted to start learning a JavaScript framework, I first did my research.<br>
The main choices boiled down to: Angular, React and Vue.<br>
The main reason I chose Vue was because of how positive people where about the short learning curve.<br>
If you already know HTML, CSS and JS, it is relatively easy to get started with Vue.<br>
It also seemed like the up-and-coming JS framework.<br><br>
While learning this framework, I was extremely impressed with the way it was set up.<br>
After creating a Vue project, it was easy to start playing around and trying out different things.<br>
This has been a huge plus while learning Vue.<br>
 
- Nuxt.js <br>
Nuxt.js is a marvelous Vue.js framework.<br>
Some of the main features are: 
- Server-side rendering with great SEO performance. 
- Middleware to perform actions between route changes. 
- Layouts that you can use on multiple pages. 
- Great Nuxt Modules like Progressive Web App (PWA) and Nuxt Content. 
 <br>
 <br>
- Firebase<br>
Firebase is a “comprehensive app development platform” as google calls it.<br>
It has many great features like Firestore (a NoSQL Database), Firebase Authentication, and Cloud Functions.<br>
Firebase is very easy to get started and it has plenty of documentation (and developers that have written about it) to figure out how it works and how to use it.<br>
It allows for real-time database updates which works great when combined with the Vuex store.<br>
<br>
<br>
- Microsoft Azure Translator 
The translator service of Microsoft Azure is ideal for getting accurate translations for decent pricing.<br>
It works by sending an API post request to their endpoint with the translation as one of the parameters.<br>
As a response you get the translation and some meta-data.<br>
There are also some other options like dictionary lookup, which offers alternate translations, and dictionary examples, which places the translation in a sentence to offer context.<br>
 <br>
 <br> 
- Vuetify<br>
Vuetify is a UI component library that uses the material design system.<br>
There are many different UI components that you can use out of the box.<br>
This means it is very easy to start building a webapp.<br>
Eventually I did run into some issues with limited customizability, but it’s a great library to quickly build a prototype.<br>
 <br>
 <br>
- GitHub<br> 
GitHub is primarily used for version management.<br>
This allows for making changes to your code without losing all the previous versions.<br>
You can have different branches which allows you to have code for development and code for production.<br> 
GitHub is an essential tool for every developer.<br>
<br>
<br>
 
- Figma<br>
Figma is a great tool for making designs for websites and apps for both desktop and mobile.<br>
Because of the intuitive UI, you can quickly create wireframes and early sketches.<br>
With the prototyping function you can add on-hover effects or apply actions on click (like going to different pages or opening sliders).<br>
This way you can create a complete prototype before writing a single line of code.<br>
 
<br>
<br>

### The process 
Making Train That Brain has been quite the journey.<br>
It is the first webapp that I’ve ever made, and I’ve learned a lot!<br>
Building a webapp from scratch on your own like I did here, makes you go through the entire process from an idea to the design, to the actual coding and developing.<br>
This starts with the idea and brainstorming.<br>
I had an idea of what I wanted to create so the main thing to figure out in this stage was what my scope was.<br>
The project had to stay possible for me to build so I could not allow too much scope creep, or I would risk never finishing the project at all.<br>
<br>
Then at some point, after a bunch of brainstorming, it was time to start making something.<br>
Here we enter the design phase.<br>
I did this at first by making rough sketches on paper and putting them up on my wall so I can have an overview of the layouts that I like and dislike.<br>
Then I picked a few designs that I liked, and I started creating them in Figma.<br>
This way I could get a better idea of what it looked like in more detail.<br>
Figma makes it very easy to make quick alterations and different versions.<br>
After creating a few versions that I really liked, it was time to start coding.<br> 
<br>
There were many things that I had to figure out along the way.<br>
A big part was learning how to work with Firebase.<br>
It was very important for me to make my app work flawlessly with the database.<br>
After trying a lot of trial and error I found that I could use Firestore’s onSnapshot listeners when calling nuxtServerInit.<br>
This meant that all the data would be automatically synced when a document in Firestore was added, modified or deleted.<br>
This resulted in great performance within my app.<br>
<br>
Another problem that I had to solve was how to retrieve the correct user data.<br>
For my app this meant retrieving the required flashcard-lists, texts, and user settings when the app is opened.<br>
This is because Firestore is a NoSQL database.<br>
This means that the data does not have relations like in a SQL-database.<br> 
Each document contains a set of key-value pairs.<br>
If you want to link to another document, one of these key-value pairs will have to include the ID of that document.<br>
This is what that looks like in the database of Train That Brain.<br>
<img src="/TTB-database-diagram.png" style="max-width: 100%"></img>
 
It is important to explain how some of these things work.<br>
Let’s start with the user.<br>
The name, email and created_at variables are self-explanatory.<br>
The setting variable is a map that contains more key-value pairs.<br>
Currently it contains
- date_format: desired date format which can be changed from the settings page. 
<br>
<br>

The User ID (UID) is used to retrieve the relevant data to the user.<br>
This also means the user cannot retrieve any data with a UID that is different than the UID in the document the user wants to retrieve.<br>
Then the last_translate and translate_counter.<br>
These variables are used to determine when the user has reached the maximum translations in trial mode (currently 50).<br> 
Every time the user clicks on a word in a text, the app does some checks.<br> 
First it looks at whether the last_translate date is different than the current date.<br> 
If so, it resets the translate_counter to 0 before continuing the translation.<br>
If not, the app checks if the translate_counter is equal to or bigger than 50 (which is the current maximum translations per day). 
If so, the word does not get translated and the user gets a response saying they have reached the maximum translations for today. 
If not, the word gets translated and the translate_counter gets incremented by one. 
 
I implemented this to keep people from making excessive use of the translator API, which could bring a significant price. 
 
 
The card documents contain a few interesting variables as well. 
The front and back variables are there because these cards are meant to simulate flashcards. 
The ID and UID are there to make sure that they are the right flashcards and belong to the currently logged-in user. 
The list_id is used when a user opens a flashcard-list. 
Instead of storing all the card-IDs in the list, the cards themselves contain the id of the list to which they belong. 
 
The ease_factor, interval and repetitions variables are used for the spaced repetition algorithm. 
This is a simple algorithm that calculates when a flashcard needs to be shown again based on how well the user remembers the answer when practicing their flashcards. 
 
 
In the goal document we find two interesting variables. 
The status is a Boolean variable that gets toggled when a user checks the box, as used in a to-do-list. 
The deadline variable contains the UNIX time (milliseconds since January 1, 1970 UTC). 
This variable is used to show the deadline date for this goal. 
This date will be formatted to the user’s preferred format. 
 
Those are the most important variables within the different documents. 

 

### My plans for Train That Brain 
Right now, Train That Brain is working for exactly what I set out to do. 
You can add your own texts and translate those words by clicking on them. 
Then you can add the word and corresponding translation to one of your flashcard lists. 
It is a simple app, but it does the job. 
 
One main component I will implement soon is the payment system. 
Right now, people can only use the trial version (limited to 50 translations per day). 
I am working on using Stripe to add the payment system. 
This will allow users to choose the premium version and get unlimited translations. 
I have chosen Stripe because it works very well with Firebase. 
 
I think the UI is decent, but I plan on making improvements to make the app easier and more pleasant to use. 
I want to add a marketplace as well. 
This feature would allow users to add texts and flashcard-lists that other users made to their own account. 
This way users can easily create material that other users can benefit from. 
One user could, for example, create a flashcard-list called “250 most used Spanish words”, which would be a great start for a Spanish learner to use. 
Other users can go to the Marketplace, look for Spanish lists and add it to their own content. 
Once added, users can change the content all they want. 
If users want to, they can give it anywhere from a 1-star to 5-star rating. 
Lists and texts with higher star ratings will be found higher in searches on the Marketplace. 
 
### My Regrets 
In choosing my tech stack, I don’t really have any regrets. 
I might choose a different UI component library (or none at all) in my next project, because it can be limiting. 
But for this project it was great to get started. 
 
I will certainly use Vue and Nuxt in my upcoming projects. 
The ease of use and the variety of features available is great for quicker and better developing. 
 
Firebase has been great for my purposes in this project and I would really like to use it in my future projects.

All by all, I am very happy with everything I've learned over the last few months and I'm looking forward to learn more about webdevelopment and to improve my skills.
If you have any questions, feel free to send me a <a href="/#contact" style="color: black">message</a>