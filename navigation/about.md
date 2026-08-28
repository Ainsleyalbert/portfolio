---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Here are some places I have lived or visited.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - forever"},
        {"flag": "f/f7/Flag_of_Florida.svg", "greeting": "Hello", "description": "Florida, Disneyworld"},
        {"flag": "2/22/Flag_of_Wisconsin.svg", "greeting": "Hey there", "description": "Wisconsin, Go Badgers"},
        {"flag": "e/ef/Flag_of_Hawaii.svg", "greeting": "Aloha", "description": "Hawaii - Maui and Alani"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

Here is what I did at those places

- 🏠 Lived my whole life in San Diego.
- 🏠 My family lives in San Diego
- 🪄 Disneyland, Disneyworld, and Alani are places i visit every year.
- 🌎 I have never left the Country.
- ❤️ My sister is going to Wisconsin Madison this fall.
- 🎓 Promotedform OAk Valley middle school 2025.
- 🎾 I play Vrsity Tennis and run Varsity Track and Feild.
- 🦴 I hang out with my dog and take him on walks.
- 🚙 I am learning how to drive.

### Culture, Family, and Fun

Everything for me, as for many others, revolves around family, friends, and food.

- My mother told me that I was Irish, welsh. and Hungarian.
- My family is pretty Small becuse it is just me, my mom, my dad, my sister, and my dog.
- The gallery of pics has some of my family, friends, and my dog.

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/1.jpeg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/1FB882DD-D216-436D-8A71-31090745E21E_1_102_o.jpeg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/DF5EF092-F841-4E0C-8E93-6C515D8A9A4F_1_105_c.jpeg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/580B6F07-6F42-4CCF-810B-C342675F913F_1_102_o.jpeg" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/DDB37387-B688-4B7A-99E7-9E55783C6A3C_1_102_o.jpeg" alt="Image 5">
</div>
