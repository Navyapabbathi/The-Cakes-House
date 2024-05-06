<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Navigation Bar with Sliding Images</title>
<style>
  /* Your CSS styles */
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
  }

  header {
    background-color: #333;
    color: white;
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    font-size: 24px;
    font-weight: bold;
    text-transform: uppercase;
    margin: 0;
  }

  .search-bar {
    flex-grow: 1;
    margin: 0 20px;
    display: flex;
    align-items: center;
  }

  .search-bar input[type="text"] {
    width: 100%;
    padding: 8px;
    border: none;
    border-radius: 4px;
    font-size: 16px;
  }

  .track-order,
  .cart,
  .sign-in,
  .more {
    font-size: 20px;
    margin-right: 10px;
    cursor: pointer;
  }

/* Style for the dropdown button */
.dropbtn {
  background-color: #4CAF50;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

/* Container for the dropdown */
.dropdown {
  position: relative;
  display: inline-block;
  margin-right: 20px; /* Add margin between dropdowns */
}

/* Dropdown content */
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

/* Links inside the dropdown */
.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

/* Change background color of dropdown item on hover */
.dropdown-content a:hover {
  background-color: #f1f1f1;
}

/* Show dropdown content on hover */
.dropdown:hover .dropdown-content {
  display: block;
}

/* Change background color of dropdown button on hover */
.dropdown:hover .dropbtn {
  background-color: #3e8e41;
}  

  .slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

* {box-sizing: border-box}
body {font-family: Verdana, sans-serif; margin:0}
.mySlides {display: none}
img {vertical-align: middle;}

/* Slideshow container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

/* Next & previous buttons */
.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -22px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.8);
}

/* Caption text */
.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* The dots/bullets/indicators */
.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active, .dot:hover {
  background-color: #717171;
}

/* Fading animation */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

/* On smaller screens, decrease text size */
@media only screen and (max-width: 300px) {
  .prev, .next,.text {font-size: 11px}
}
.slideshow-container {
  max-width: 1000px;
  margin: auto; /* Center the container horizontally */
  position: relative;
}

.mySlides {
  display: none;
  text-align: center; /* Center the images horizontally */
}
  


  
  
  /* Centered heading */
  .heading {
    text-align: center;
    margin-bottom: 20px;
  }

 .cakes-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
  }



.row {
  display: flex;
}


/* Create three equal columns that sit next to each other */
.column {
  flex: 1;
  margin: 0 1px; /* Adjusted margin */
}

/* Trending cakes heading */
.trending-heading {
  text-align: center;
  margin-bottom: 20px;
}

.trending-row {
  display: flex;
  justify-content: center;
}

.trending-column {
  flex: 1;
  padding: 5px;
}
.location-symbol {
    font-size: 20px;
    margin-right: 5px;
  }

  .deliver-to {
    cursor: pointer;
    text-decoration: underline;
  }
.modal {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.5);
  }
/* Modify the CSS for the slideshow images */
.mySlides {
    display: inline-block; /* Display the slides inline */
    width: 1000px; /* Set a fixed width for each slide */
    overflow: hidden; /* Hide any overflow */
}

  .modal-content {
    background-color: #fefefe;
    margin: 10% auto;
    padding: 20px;
    border: 1px solid #888;
    width: 80%;
    max-width: 600px;
    border-radius: 5px;
  }

  .close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
    cursor: pointer;
  }

  .close:hover {
    color: black;
  }
/* Inside the CSS styles */
.cakes-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

/* Adjusted spacing and curved borders for cake images */
.cake-item {
    width: calc(33.33% - 10px); /* Adjust the width and spacing */
    margin-bottom: 20px;
    text-align: center; /* Center the images */
}

.cake-image img {
    width: 100%;
    border-radius: 15px; /* Curved borders */
}




.cake-caption {
  text-align: center;
  margin-top: 10px;
  font-size: 16px;
}
/* Separate background for the cakes delivery container */
.cakes-delivery-container {
    background-color: #FFB6C1; /* Adjust background color as needed */
    border-radius: 15px; /* Rounded corners for the container */
    overflow: hidden; /* Hide overflowing content */
    padding: 20px; /* Padding for spacing */
    margin-bottom: 20px; /* Added margin for spacing */
}
/* Separate background for the trending cakes container */
.trending-cakes-container {
    background-color: #FFB6C1; /* Same background color as the cakes delivery container */
    border-radius: 15px; /* Rounded corners for the container */
    overflow: hidden; /* Hide overflowing content */
    padding: 10px; /* Padding for spacing */
    margin-bottom: 30px; /* Added margin for spacing */
}
.trending-column {
  flex: 1;
  padding: 5px; /* Adjusted padding for better spacing */
  text-align: center; /* Center the images */
}

.trending-row {
  display: flex;
  justify-content: center;
  flex-wrap: nowrap; /* Prevent wrapping */
}

 .trending-column img {
  width: 70%; /* Set the width to match the cake delivery images */
  max-width: 70%; /* Adjusted max-width to match the desired width */
  margin: 0 auto; /* Center the images */
  display: block; /* Ensure images are centered properly */
}


.dropdown {
    position: relative;
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #333;
    min-width: 160px;
    z-index: 1;
}

.dropdown-content a {
    color: white;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    text-align: left;
}

.dropdown-content a:hover {
    background-color: #ddd;
    color: black;
}

.dropdown:hover .dropdown-content {
    display: block;
}
 
.cakes-by-flavor-container {
    background-color: #FFA07A; /* Adjust background color as needed */
    border-radius: 15px; /* Rounded corners for the container */
    overflow: hidden; /* Hide overflowing content */
    padding: 10px; /* Padding for spacing */
    margin-bottom: 30px; /* Added margin for spacing */
}
</style>
</head>
<body>

<header>

  <div class="logo">
    <img src="bakerlogo.jpg" style="width:90px" alt="Baker Logo">
  </div>
  <div class="location">
    <span class="location-symbol">&#127968;</span> <!-- Location symbol -->
    <span class="deliver-to" onclick="openModal()">Deliver to</span> <!-- Deliver to text -->
  </div>
  <div class="search-bar">
    <input type="text" placeholder="Search...">
  </div>
  <div class="icons">
    <span class="track-order" onclick="window.location.href='track-order.html'">Track Order</span>
    <span class="cart" onclick="window.location.href='cart.html'">Cart</span>
    <span class="sign-in" onclick="window.location.href='sign-in.html'">Sign In</span>
    <span class="more" onclick="window.location.href='more.html'">More</span>
  </div>
</header>


<!-- Container for the first dropdown -->
<center>


<!-- Container for the second dropdown -->
<div class="dropdown">
  <button class="dropbtn">Flowers</button>
  <div class="dropdown-content">
    <a href="roses.html">Roses</a>
    <a href="lilies.html">Lilies</a>
    <a href="orchids.html">Orchids</a>
    <a href="mixed_flowers.html">Mixed Flowers</a>
  </div>
</div>

<!-- Container for the third dropdown -->
<div class="dropdown">
  <button class="dropbtn">Personalized</button>
  <div class="dropdown-content">
    <a href="photo_frames.html">Photo Frames</a>
    <a href="key_chains.html">Key Chains</a>
    <a href="cushions_pillows.html">Cushions & Pillows</a>
    <a href="name_plates.html">Name Plates</a>
    <a href="photo_lamps.html">Photo Lamps</a>
    <a href="mugs.html">Mugs</a>
  </div>
</div>

<!-- Container for the fourth dropdown -->
<div class="dropdown">
  <button class="dropbtn">Gifts</button>
  <div class="dropdown-content">
    <a href="Spiritual_gifts.html">Spiritual Gifts</a>
    <a href="Soft_toys.html">Soft Toys</a>
    <a href="candles.html">Candles</a>
  </div>
</div>
</center>

</div><center>
<div class="mySlides fade">
  <div class="numbertext"></div>
  <img src="mango1cake.jpg" style="width:100%">
  
</div>

<div class="mySlides fade">
  <div class="numbertext"></div>
  <img src="aniversarycake.png" style="width:100%">
  
</div>

<div class="mySlides fade">
  <div class="numbertext"></div>
  <img src="Birthdaycake.jpg" style="width:100%">
 
</div>




</div>
<br>

<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span> 
  <span class="dot" onclick="currentSlide(2)"></span> 
  <span class="dot" onclick="currentSlide(3)"></span> 
</div>
</center>
</div>
<div id="myModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal()">&times;</span>
    <h2>Enter your Pin Code to discover FREE
shipping options</h2>
    <form>
    <center>
        <label for="address">Enter your address:</label><br>
        <div class="inverted-waterdrop"></div><input type="text" id="address" name="address" style="width: 75%; height: 40px;"><br><br>
        <button type="button" onclick="submitAddress()">Submit</button>
    </center>
    <h5>Join our ever-growing family of 10,000+ delighted customers in many cities!</h5>
</form>


  </div>
</div>




<!-- Heading for cakes delivery -->
<h2 class="heading">Cakes Delivery</h2>
<div class="cakes-delivery-container">
<div class="row">
  <div class="column">
<a href="ck1.html">
    <img src="cake1.jpg" alt="Cake 1" style="width:70%">
    <div class="cake-caption">Birthday Cake</div>
  </div>
  <div class="column">
<a href="c2.html">
    <img src="cake2.jpg" alt="Cake 2" style="width:70%">
    <div class="cake-caption">Anniversary Cake</div>
  </div>
  <div class="column">
<a href="c3.html">
    <img src="cake3.jpg" alt="Cake 3" style="width:70%">
    <div class="cake-caption">Designer Cake</div>
  </div>
  <div class="column">
<a href="c4.html">
    <img src="cake4.jpg" alt="Cake 4" style="width:70%">
    <div class="cake-caption">Regular Cake</div>
  </div>
  <div class="column">
<a href="c5.html">
    <img src="cake5.jpg" alt="Cake 5" style="width:70%">
    <div class="cake-caption">Photo Cake</div>
  </div>
  <div class="column">
<a href="c6.html">
    <img src="cake6.jpg" alt="Cake 6" style="width:70%">
    <div class="cake-caption">Eggless Cake</div></a>
  </div>
</div>
</div>



<!-- Trending cakes heading -->
<h2 class="heading">Trending Cakes</h2>
<div class="trending-cakes-container">
<div class="trending-row">
  <div class="trending-column">
    <a href="pmc.html">
    <img src="t1.jpg" alt="Pull me up Cakes" style="width:60%">
      <div class="trending-caption">Pull me up Cakes</div>
    </a>
  </div>
  <div class="trending-column">
    <a href="bbc.html">
      <img src="t2.jpg" alt="Bomb Cakes" style="width:60%">
      <div class="trending-caption">Bomb Cakes</div>
    </a>
  </div>
  <div class="trending-column">
    <a href="pc.html">
      <img src="t3.jpg" alt="Pinata Cakes" style="width:60%">
      <div class="trending-caption">Pinata Cakes</div>
    </a>
  </div>
  <div class="trending-column">
    <a href="dess.html">
      <img src="t4.jpg" alt="Desserts" style="width:60%">
      <div class="trending-caption">Desserts</div>
    </a>
  </div>
</div>
</div>


<!-- Heading for cakes delivery -->
<h2 class="heading">Cakes by Flavour</h2>
<div class="cakes-delivery-container">
<div class="row">
  <div class="column">
<a href="cF1.html">
    <img src="F1.jpg" alt="Cake 1" style="width:70%">
    <div class="cake-caption">Black Forest</div>
  </div>
  <div class="column">
<a href="cF2.html">
    <img src="F2.jpg" alt="Cake 2" style="width:70%">
    <div class="cake-caption">Chocolate</div>
  </div>
  <div class="column">
<a href="cF3.html">
    <img src="F3.jpg" alt="Cake 3" style="width:70%">
    <div class="cake-caption">Friut</div>
  </div>
  <div class="column">
<a href="cF4.html">
    <img src="F4.jpg" alt="Cake 4" style="width:70%">
    <div class="cake-caption">Pineapple</div>
  </div>
  <div class="column">
<a href="cF5.html">
    <img src="F5.jpg" alt="Cake 5" style="width:70%">
    <div class="cake-caption">Butterscotch</div>
  </div>
  <div class="column">
<a href="cF6.html">
    <img src="F6.jpg" alt="Cake 6" style="width:70%">
    <div class="cake-caption">Red Velvet</div>
  </div>
</div>
</div>


<script>
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
}

function openModal() {
  var modal = document.getElementById("myModal");
  modal.style.display = "block";
}

function closeModal() {
  var modal = document.getElementById("myModal");
  modal.style.display = "none";
}

function submitAddress() {
  var address = document.getElementById("address").value;
  // Handle address submission logic here...
}

</script>

</body>
</html>
