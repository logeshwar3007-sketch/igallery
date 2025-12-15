# Ex.08 Design of Interactive Image Gallery
## Date:15/12/2025
## Ref.No:25014493
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
photo.html
~~~
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Image Gallery</title>
  <link rel="stylesheet" href="photo.css">
</head>
<body>
  <h1> My  Gallery </h1>

  <div class="gallery">
    <img src="1.jpeg" alt="player 1" onclick="openImage(this)">
    <img src="2.jpg" alt="player 2" onclick="openImage(this)">
    <img src="3.jpg" alt="player 3" onclick="openImage(this)">
    <img src="4.jpg" alt="player 4" onclick="openImage(this)">
    <img src="5.avif" alt="player 5" onclick="openImage(this)">
    
    <img src="6.avif" alt="player 5" onclick="openImage(this)">

  </div>

  <!-- Popup Image View -->
  <div id="popup" class="popup" onclick="closeImage()">
    <img id="popupImage" src="">
  </div>

  <script src="photo.js"></script>
</body>
</html>
~~~
photo.css
~~~
body {
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ffe6f0, #e6f7ff);
  text-align: center;
  padding: 20px;

}

h1 {
  color: #333;
  margin-bottom: 30px;
}

.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 15px;
}

.gallery img {
  width: 250px;
  height: 170px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s, box-shadow 0.3s;
  cursor: pointer;
}

.gallery img:hover {
  transform: scale(1.1);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
}

/* Popup image styling */
.popup {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  justify-content: center;
  align-items: center;
}

.popup img {
  max-width: 90%;
  max-height: 90%;
  border-radius: 10px;
  box-shadow: 0 0 20px #fff;
}

~~~
photo.js
~~~
function openImage(imgElement) {
  const popup = document.getElementById("popup");
  const popupImage = document.getElementById("popupImage");
  
  popupImage.src = imgElement.src;
  popup.style.display = "flex";
}

function closeImage() {
  document.getElementById("popup").style.display = "none";
}
~~~

## OUTPUT:
<img width="1917" height="964" alt="Screenshot 2025-12-15 154410" src="https://github.com/user-attachments/assets/6de17c64-9b6b-4232-9646-791b95858dae" />


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
