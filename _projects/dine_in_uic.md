---
layout: page
title: Dine-in-UIC
description: Dine-In UIC - "Navigate Large Food Halls with Ease"
img: "assets/img/projects/dine_in_uic/thumbnail.png"
importance: 12
category: Other
---

<h4><u>Access this project</u></h4>
<b>GitHub repo:</b> <a href='https://github.com/komar41/uic-dining-hall-navigation'>https://github.com/komar41/uic-dining-hall-navigation</a> <br>
<b>Tools used:</b> React Native, Expo CLI, JavaScript, JSON, Generative AI (for dish images).
<p align='justify'>
This project addresses the challenges faced by university students with dietary restrictions when navigating UIC's United Table in Student Center East. Through user research and iterative design, we developed a mobile application to improve the dining experience for students with specific dietary needs.
</p>
<h4><u>Application Setup</u></h4>
<p align='justify'>
Open a terminal and run the following commands:
</p>
<ol>
    <li>Clone the repository:
        <pre><code>git clone https://github.com/komar41/uic-dining-hall-navigation.git
cd uic-dining-hall-navigation</code></pre>
    </li>
    <li>Install Node.js from <a href="https://nodejs.org/en/download/">https://nodejs.org/en/download/</a></li>
    <li>Install dependencies and start the app:
        <pre><code>npm install
npm start</code></pre>
    </li>
    <li>Download the Expo Go app on your phone to test the app on the development server.</li>
    <li>Scan the QR code on your phone to test the app.</li>
</ol>
<h4><u>Research</u></h4>
<p align='justify'>
Our research involved surveying academic papers to ground our solution in existing knowledge domains. Key insights included:
<ul>
    <li>The influence of information on food choices and the impact of gamification in fostering informed decisions</li>
    <li>The potential of AR-enabled navigation aids, though not directly applicable due to potential task overload</li>
    <li>The efficacy of conversational interfaces in assisting users with nuanced preferences and context-specific requirements</li>
</ul>
These insights informed our approach to integrating planning functionalities, efficient navigation tools, and personalized dietary planning options.
</p>
<br>
<h4><u>Requirements</u></h4>
<p align='justify'>
Based on user interviews, we identified two primary user personas:
</p>
<h5>1. "Irregular visitor" (e.g., John Doe)</h5>
<p align='justify'>
<ul>
    <li>Needs a more organized dining hall experience</li>
    <li>Requires easy location of foods aligning with dietary restrictions</li>
    <li>Desires self-reliance when navigating the space</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/persona1.png" alt="Irregular Visitor Persona" style="width: 80%;">
</p>
<h5>2. "Regular visitor" (e.g., Jane Doe)</h5>
<p align='justify'>
<ul>
    <li>Prioritizes quick and efficient location of suitable foods</li>
    <li>Wants to easily avoid specific food types (e.g., spicy foods, pork)</li>
    <li>Needs clear answers about food options without relying on staff knowledge</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/persona2.png" alt="Regular Visitor Persona" style="width: 80%;">
</p>
<p align='justify'>
Common needs included:
<ul>
    <li>Efficient navigation of dining hall menus</li>
    <li>Detailed ingredient and dietary information</li>
    <li>Clear food labels and efficient navigation tools</li>
</ul>
</p>
<h4><u>Ideation</u></h4>
<p align='justify'>
Our ideation process focused on addressing the needs of both regular and irregular visitors. Key features considered included:
<ul>
    <li>User profile configuration for dietary restrictions</li>
    <li>Personalized meal planning and recommendations</li>
    <li>Efficient map layout for dining hall navigation</li>
    <li>Detailed ingredient lists for food items</li>
</ul>
We prioritized designs that directly addressed key user needs and excluded those that introduced unnecessary complexity.
</p>
<br>
<h4><u>Low-Fidelity Prototype</u></h4>
<p align='justify'>
Our low-fidelity prototypes included sketches of:
<ul>
    <li>A screen for configuring user dietary restrictions</li>
    <li>A recommended meal plan screen based on user preferences</li>
    <li>A map layout screen for efficient navigation</li>
    <li>A screen displaying ingredient lists for selected food items</li>
</ul>
These sketches formed the basis for our initial design concepts.
</p>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/sketches.png" alt="Low-Fidelity Prototype Sketches" style="width: 80%;">
<h4><u>Figma Prototypes</u></h4>
<p align='justify'>
Based on our low-fidelity prototypes, we created more detailed Figma prototypes. These included:
<ul>
    <li>A page for setting dietary restrictions</li>
    <li>A recommended meal plan page with filtered food options</li>
    <li>An interactive map of the dining hall with numbered navigation points</li>
    <li>Detailed food item pages with ingredient lists</li>
</ul>
The Figma prototypes allowed for a more interactive and visually representative model of our final application.
</p>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/figma.png" alt="Figma Prototypes" style="width: 80%;">
<h4><u>Implementation</u></h4>
<p align='justify'>
The application was built using:
<ul>
    <li>React Native and Expo CLI for cross-platform compatibility</li>
    <li>React Components (DishCard.js and PlanCard.js) for reusable UI elements</li>
    <li>React Navigation for seamless navigation between pages</li>
    <li>Local JSON data for quiz questions and options</li>
    <li>React Hooks (useState and useEffect) for efficient state management</li>
</ul>
</p>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/architecture.png" alt="Application Architecture" style="width: 60%;">
<p align='justify'>
Data flow:
<ol>
    <li>Expo CLI initialization</li>
    <li>Component rendering</li>
    <li>User interaction triggering state changes</li>
    <li>Navigation facilitated by React Navigation</li>
</ol>
Menu data is fetched from a public API exposed by the UIC United Table website. Images were collected manually and supplemented with AI-generated images where necessary.
</p>
<br>
<h4><u>Key Features</u></h4>
<p align='justify'>
<ul>
    <li>Personalized dietary restriction settings</li>
    <li>Daily menu recommendations based on user preferences</li>
    <li>Meal planning functionality</li>
    <li>Detailed dish information (ingredients, nutritional info)</li>
    <li>Interactive map for efficient navigation in the dining hall</li>
    <li>Best route generation for collecting chosen meal items</li>
</ul>
</p>
<h4><u>Application Components</u></h4>
<h5>Home Screen</h5>
<p align='justify'>
<ul>
    <li>Central hub for navigation to all other screens</li>
    <li>Starting point for setting up dietary restrictions and meal plans</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/1_home.png" alt="Home Screen" style="display: block; margin-left: auto; margin-right: auto; width: 25%;">
</p>
<h5>Set Dietary Restriction Screen</h5>
<p align='justify'>
<ul>
    <li>Users define their dietary preferences and restrictions</li>
    <li>Redirects users back to the Home screen after setup</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/2_set_diet.png" alt="Set Dietary Restriction Screen" style="display: block; margin-left: auto; margin-right: auto; width: 25%;">
</p>
<h5>Set Up New Plan Screen</h5>
<p align='justify'>
<ul>
    <li>Displays recommended food items based on user's dietary preferences</li>
    <li>Allows users to create and save a meal plan for the day</li>
    <li>Access to Dish Details screen for more information on food items</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/3_create_plan.png" alt="Set Up New Plan Screen" style="display: block; margin-left: auto; margin-right: auto; width: 25%;">
</p>
<h5>My Plan Screen</h5>
<p align='justify'>
<ul>
    <li>Displays the user's saved meal plan for the day</li>
    <li>Option to check dish details and navigate to the Map screen</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/4_my_plan.png" alt="My Plan Screen" style="display: block; margin-left: auto; margin-right: auto; width: 25%;">
</p>
<h5>Dish Details Screen</h5>
<p align='justify'>
<ul>
    <li>Provides detailed information on selected food items</li>
    <li>Includes dish description, ingredient list, and nutrition info</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/5_dish_details.png" alt="Dish Details Screen" style="display: block; margin-left: auto; margin-right: auto; width: 25%;">
</p>
<h5>Map Screen</h5>
<p align='justify'>
<ul>
    <li>Interactive map of the UIC dining hall</li>
    <li>Displays the most efficient route to collect chosen meal items</li>
    <li>Numbered tooltips guide users to specific counters</li>
    <li>Clicking tooltips reveals food items to collect at each counter</li>
</ul>
<img src="https://github.com/komar41/dine-in-uic/raw/main/assets/6_map.png" alt="Map Screen" style="display: block; margin-left: auto; margin-right: auto; width: 25%;">
</p>
<h4><u>Evaluation & Analysis</u></h4>
<p align='justify'>
We conducted a comparative study between our app and the existing "Dine on Campus" application. The study involved:
<ul>
    <li>6 participants performing tasks in the actual dining hall</li>
    <li>Data collection through user estimates, screen recordings, and qualitative feedback</li>
    <li>Use of Hart and Staveland's NASA Task Load Index (TLX) for task assessment</li>
</ul>
Key findings:
<ul>
    <li>Our app received more positive feedback compared to "Dine on Campus"</li>
    <li>Users appreciated features like dish photos and easier navigation</li>
    <li>Statistical analysis showed improvements in perceived efficiency and emotional stability</li>
</ul>
Areas for improvement:
<ul>
    <li>Enhancing map tooltips and favorites functionality</li>
    <li>Improving the dietary restrictions quiz</li>
    <li>Addressing minor usability issues</li>
</ul>
</p>
<h4><u>Future Improvements</u></h4>
<p align='justify'>
<ul>
    <li>Integration of custom dietary restrictions</li>
    <li>Improved matching of dish images with their physical appearance</li>
    <li>Enhanced quality-of-life interactions and bug fixes</li>
</ul>
</p>
<h4><u>Conclusion</u></h4>
<p align='justify'>
This project demonstrates the effectiveness of a user-centric design approach in addressing the challenges faced by students with dietary restrictions in university dining halls. The resulting mobile application offers a comprehensive solution for menu exploration, meal planning, and physical navigation within the dining space.
</p>
<h4><u>Team</u></h4>
<p align='justify'>
<ul>
    <li>Gustavo Moreira</li>
    <li>Kazi Shahrukh Omar</li>
    <li>Shanghao Li</li>
    <li>Farah Kamleh</li>
</ul>
</p>
