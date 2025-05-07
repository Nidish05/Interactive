# Ex.08 Design of Interactive Image Gallery


## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
home.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>AVENGERS</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="captain.jpg" height="200px" width="350px">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="iron-man.jpg"  height="200px" width="350px" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="thor.jpg" height="200px" width="350px" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="hulk.jpg" height="200px" width="350px" >
        </div>
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="style.js"></script>
</body>
</html>

style.css

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    text-align: center;
    padding: 20px;
    background-color: #f4f4f4;
}

.gallery {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;         
    gap: 10px;               
    padding: 20px;
}

.gallery-item img {
    width: 200px; 
    height: 150;
    cursor: pointer;
    border: 2px solid #ccc;
    border-radius: 5px;
    transition: transform 0.3s ease;
}

style.js

function openModal(element) {
    const modal = document.getElementById("modal");
    const modalImage = document.getElementById("modalImage");
    const caption = document.getElementById("caption");

    modal.style.display = "flex";
    modalImage.src = element.querySelector("img").src;
    caption.textContent = element.querySelector("img").alt;
}

function closeModal() {
    const modal = document.getElementById("modal");
    modal.style.display = "none";
}
```

## OUTPUT:
![Screenshot 2025-05-07 183150](https://github.com/user-attachments/assets/03726700-913f-4297-bd10-dd805815735d)
![Screenshot 2025-05-07 183227](https://github.com/user-attachments/assets/c3b0eeb9-63d3-4669-95d9-54340b2196d1)






## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
