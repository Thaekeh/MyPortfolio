---
title: Portfolio
description: My personal portfolio
img: /favicon.ico
date: {
    month: November,
    year: 2020,
}
imageHeight: 50%
---

### Displaying my work 
After working hard on creating my own web app (<a href="https://www.trainthatbrain.app/" style="color: black">Train That Brain</a>) for the past half year, I was ready to start looking for a job as a front-end web developer.<br>
For this I needed a good way to display the projects I’ve worked on, a portfolio website.<br>
First I needed to get an idea of what I wanted to make.<br>
After scouring the internet for a few days, I had a list of websites with the aspects that I liked and disliked written next to them. <br>
The website style I wanted was minimalistic yet elegant. <br>
 <br>

### Designing my website <br>
Before I started coding, I first made some sketches on paper and then created a couple of the sketches I liked with Figma. <br>
Because of my previous projects, I have gotten used to designing this way. <br>
It helps a lot to get a better idea of what it is I want to create. <br>
After settling on one design, I was almost ready to start coding. <br>
 <br>
 
### Selecting the technologies <br>
Since I just finished creating Train That Brain, I was used to using Vue.js and Nuxt.js as my JavaScript frameworks. <br>
To save myself some time and hassle, I decided that I would create my portfolio website with the same technologies. <br>
I would really like to learn React, so that is the framework I will use on my next web development project. <br>
Now however, I would continue with Vue and Nuxt. <br>
As additional tools, I picked Nuxt Content, a headless CMS, and Vuetify, a material UI component library. <br>
 <br>
Nuxt Content is very useful for managing, for example, blog content. <br>
Because I knew I would be writing about the projects that I have done, this was a great addition to my toolkit. <br>
 <br>
With these technologies selected, I was ready to start building. <br>
 <br>

### Writing reusable code <br>
One of the great strengths of Vue is the ability to create components and use those on your pages. <br>
If done right, this allows you to write great reusable code. <br>
Since I wanted to have a list of my finished projects, I knew this would be a perfect opportunity to create a component where the code could be reused. <br>
To make it simpler for me to add new projects, I did a few things: <br>
<ul>
    <li>
        Store all project information in a JSON file. 
    </li>
    <li>
        Write the component code to retrieve and use the information from the JSON file 
    </li>
    <li>
        Style project cards according to the index in the JSON object     
    </li>
</ul>
<br>

Let me explain this a bit further. <br>
For each project that I wanted to add to my portfolio, I would add an object within the JSON array. <br>
This object stores information like:
<ul>
    <li>
        Title    
    </li>
    <li>
        Description 
    </li>
    <li>
        Link to logo     
    </li>
    <li>
        Logo background color    
    </li>
    <li>
        Used technologies with links to their corresponding images     
    </li>
    <li>
        Buttons with links     
    </li>
</ul>
<br>

 <br>
The component then loops over the JSON array and creates a new card for each object found in the array. <br>
It then populates these cards with the information of the object. <br>
 <br>
As you can see on my <a href="/" style="color: black">homepage</a> the cards switch between information on the left to information on the right. <br>
This is done by conditionally rendering some elements depending on the index of the object in the array and on the screen size (because on mobile I wanted all logos to be on top). <br>
 <br>
With all this reusable code, all that I have to do when I want to add a project to my portfolio is to add another JSON object with the relevant information and then the code takes care of the rest. <br>
 <br>

### Contact form 
To enable people to contact me through the contact form, I used EmailJS. <br>
This is an email service that allows you to simply add their JavaScript SDK into your code and start sending emails. <br>
Through the admin panel on their website, you can customize the emails to your preference. <br>
 <br>

### Smooth scrolling 
For smooth navigating on my portfolio website, I used a NPM library called “vue-scrollto”. <br>
This makes it very easy to use smooth scrolling and add extra options if necessary. <br>
Since my navbar is visible on every page of my website, I did add a function that checks whether the user is on the homepage before scrolling. <br>
If the user isn’t on the homepage, the function navigates the user to the homepage and after a one-second timeout, starts scrolling to the right location. <br>
This makes for a very pleasant user experience.<br>