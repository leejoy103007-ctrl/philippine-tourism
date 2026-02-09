
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Philippine Tourist Spots</title>

<style>
/* ===== GLOBAL ===== */
body{
    margin:0;
    font-family: 'Segoe UI', Arial, sans-serif;
    background:#eef6fb;
    color:#2c2c2c;
    scroll-behavior: smooth;
    transition: background 0.3s, color 0.3s;
}

/* ===== SECTIONS ===== */
section{
    padding:50px 20px;
}

/* ===== CARD DESIGN ===== */
.card{
    background:white;
    max-width:900px;
    margin:25px auto;
    border-radius:14px;
    overflow:hidden;
    box-shadow:0 8px 20px rgba(0,0,0,0.12);
    opacity:0;
    transform: translateY(30px);
    transition: all 0.6s ease;
}

.card.show{
    opacity:1;
    transform: translateY(0);
}

.card img{
    width:100%;
    height:320px;
    object-fit:cover;
}

.card-content{
    padding:25px;
}

.card h2{
    color:#0077b6;
    margin-bottom:10px;
}

/* ===== FUN FACT ===== */
.fact{
    background: linear-gradient(135deg,#caf0f8,#ade8f4);
    max-width:900px;
    margin:40px auto;
    padding:30px;
    text-align:center;
    border-radius:14px;
    box-shadow:0 6px 15px rgba(0,0,0,0.1);
}

.fact h2{
    color:#023e8a;
}

/* ===== BUTTON ===== */
button{
    padding:12px 25px;
    margin-top:18px;
    background: linear-gradient(135deg,#0077b6,#0096c7);
    color:white;
    border:none;
    border-radius:30px;
    cursor:pointer;
    font-size:16px;
    font-weight:600;
    transition: transform 0.2s, box-shadow 0.2s;
}

button:hover{
    transform: scale(1.05);
    box-shadow:0 5px 15px rgba(0,0,0,0.3);
}

/* ===== FOOTER ===== */
footer{
    background:#03045e;
    color:white;
    text-align:center;
    padding:20px;
    font-size:14px;
}


/* ===== RESPONSIVE DESIGN ===== */
@media (max-width: 768px){
    header h1{font-size:24px;}
    nav a{font-size:14px;}
    .card img{height:220px;}
    .card-content{padding:18px;}
    section{padding:30px 10px;}
}

/* ===== SCROLL TO TOP BUTTON ===== */
#topBtn {
  position: fixed;
  bottom: 30px;
  right: 30px;
  background: #0077b6;
  color: white;
  border: none;
  padding: 12px;
  border-radius: 50%;
  cursor: pointer;
  display: none;
  font-size: 18px;
  z-index: 99;
}
#topBtn:hover {background: #023e8a;}

/* ===== SCROLL ANIMATION ===== */
.card, .section-content{
    opacity: 0;
    transform: translateY(30px);
    transition: all 0.6s ease;
}
.card.show, .section-content.show{
    opacity: 1;
    transform: translateY(0);
}

</style>
</head>

<body>
    
    <section id="loginPage" style="
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    background: linear-gradient(135deg,#00a8cc,#0077b6);
">
  <div style="
      background:white;
      padding:40px;
      border-radius:20px;
      width:320px;
      text-align:center;
      box-shadow:0 10px 30px rgba(0,0,0,0.3);
  ">
    <h2 style="color:#0077b6; margin-bottom:10px;">Welcome 🌴</h2>
    <p style="margin-bottom:20px;">Login to explore the Philippines</p>

    <input type="text" placeholder="Username" required style="
        width:100%;
        padding:12px;
        margin-bottom:15px;
        border-radius:10px;
        border:1px solid #0077b6;
    ">

    <input type="password" placeholder="Password" required style="
        width:100%;
        padding:12px;
        margin-bottom:20px;
        border-radius:10px;
        border:1px solid #0077b6;
    ">

    <button onclick="login()" style="
        width:100%;
        padding:12px;
        border:none;
        border-radius:25px;
        background: linear-gradient(135deg,#ffd166,#ef476f);
        color:white;
        font-size:16px;
        font-weight:600;
        cursor:pointer;
    ">
      Login 🔐
    </button>
  </div>
</section>

  <!-- ===== HEADER & NAVBAR ===== -->
<header style="
    position: sticky;
    top: 0;
    z-index: 100;
    background: linear-gradient(135deg, #00a8cc, #0077b6); /* Soft ocean gradient */
    color: white;
    text-align: center;
    padding: 20px 0;
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    border-bottom-left-radius: 15px;
    border-bottom-right-radius: 15px;
">
    <div style="display:flex; align-items:center; justify-content:center; flex-wrap: wrap; max-width: 1200px; margin:auto;">
        <!-- Logo / Icon -->
        <div style="margin-right:20px; font-size:28px;">🏝️</div>
        <!-- Title -->
        <div style="flex:1; text-align:center;">
            <h1 style="margin:0; font-size:1.8em; letter-spacing:1px;">Philippine Tourist Spots</h1>
            <p style="margin:5px 0 0 0; font-size:0.9em;">Discover the beauty of the Philippines</p>
        </div>
        

    <!-- NAVBAR LINKS -->
    <nav style="
        margin-top:15px;
        display:flex;
        justify-content:center;
        flex-wrap:wrap;
        gap:15px;
    ">
        <a href="#home" style="
            color:white; text-decoration:none; font-weight:600; padding:8px 15px;
            border-radius: 20px; transition: background 0.3s, color 0.3s;
        " onmouseover="this.style.background='rgba(255,255,255,0.2)'; this.style.color='#fff';"
           onmouseout="this.style.background='transparent'; this.style.color='white';">
            Home
        </a>
        <a href="#about" style="
            color:white; text-decoration:none; font-weight:600; padding:8px 15px;
            border-radius: 20px; transition: background 0.3s, color 0.3s;
        " onmouseover="this.style.background='rgba(255,255,255,0.2)'; this.style.color='#fff';"
           onmouseout="this.style.background='transparent'; this.style.color='white';">
            About
        </a>
        <a href="#tourist" style="
            color:white; text-decoration:none; font-weight:600; padding:8px 15px;
            border-radius: 20px; transition: background 0.3s, color 0.3s;
        " onmouseover="this.style.background='rgba(255,255,255,0.2)'; this.style.color='#fff';"
           onmouseout="this.style.background='transparent'; this.style.color='white';">
            Tourist Spots
        </a>
        <a href="#funfacts" style="
            color:white; text-decoration:none; font-weight:600; padding:8px 15px;
            border-radius: 20px; transition: background 0.3s, color 0.3s;
        " onmouseover="this.style.background='rgba(255,255,255,0.2)'; this.style.color='#fff';"
           onmouseout="this.style.background='transparent'; this.style.color='white';">
            Fun Facts
        </a>
        <a href="#contact" style="
            color:white; text-decoration:none; font-weight:600; padding:8px 15px;
            border-radius: 20px; transition: background 0.3s, color 0.3s;
        " onmouseover="this.style.background='rgba(255,255,255,0.2)'; this.style.color='#fff';"
           onmouseout="this.style.background='transparent'; this.style.color='white';">
            Contact
        </a>
    </nav>
    
</header>

<!-- ===== HOME SECTION ===== -->
<section id="home" style="
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, #a8dadc, #457b9d); /* Soft tropical gradient */
    padding: 60px 20px;
    border-radius: 20px;
    max-width: 1200px;
    margin: 40px auto;
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
    color: #1d3557;
    overflow: hidden;
">
    <!-- Text Content -->
    <div style="
        flex: 1 1 400px;
        min-width: 300px;
        padding: 20px;
        animation: fadeInLeft 1s ease forwards;
    ">
        <h2 style="
            font-size: 3em;
            font-weight: 700;
            margin-bottom: 20px;
            text-shadow: 1px 1px 5px rgba(255,255,255,0.3);
        ">
            Welcome to the Philippines 🇵🇭
        </h2>
        <p style="
            font-size: 1.2em;
            line-height: 1.6;
            margin-bottom: 30px;
        ">
            Explore turquoise beaches, majestic mountains, vibrant festivals, and hidden gems across more than 7,600 islands.  
            Plan your adventure and discover the heart of the Philippines.
        </p>
        <button onclick="document.getElementById('tourist').scrollIntoView({behavior:'smooth'})"
            style="
                padding: 15px 30px;
                background: linear-gradient(135deg,#1d3557,#457b9d); /* Soft blue gradient */
                color:white;
                border:none;
                border-radius:30px;
                cursor:pointer;
                font-size:16px;
                font-weight:600;
                transition: transform 0.2s, box-shadow 0.2s;
            "
            onmouseover="this.style.transform='scale(1.05)'; this.style.boxShadow='0 5px 15px rgba(0,0,0,0.3)'"
            onmouseout="this.style.transform='scale(1)'; this.style.boxShadow='none'">
            Explore Now
        </button>
    </div>

    <!-- Image Content -->
    <div style="
        flex: 1 1 400px;
        min-width: 300px;
        padding: 20px;
        text-align:center;
        animation: fadeInRight 1s ease forwards;
    ">
        <img src="/HD wallpaper_ Philippine flag painting, philippines, background, texture, spot.jpg" 
             alt="Philippine Beach"
             style="
                width: 100%;
                border-radius: 20px;
                box-shadow: 0 8px 20px rgba(0,0,0,0.15);
                transition: transform 0.3s;
             "
             onmouseover="this.style.transform='scale(1.03)';"
             onmouseout="this.style.transform='scale(1)';"
        >
    </div>
</section>

<!-- ===== ABOUT SECTION ===== -->
<section id="about" style="
    max-width:900px; 
    margin:50px auto; 
    padding:40px; 
    background: linear-gradient(135deg,#caf0f8,#ade8f4); 
    border-radius:20px; 
    box-shadow:0 8px 25px rgba(0,0,0,0.1);
    text-align:center;
">
    <h2 style="font-size:2.2em; color:#0077b6; margin-bottom:20px;">About Philippine Tourism 🇵🇭</h2>
    <p style="font-size:1.1em; color:#023e8a; line-height:1.8; margin-bottom:25px;">
        The Philippines is a tropical paradise made up of more than 7,600 islands, 
        offering stunning beaches, lush mountains, and rich cultural heritage. 
        From the white sands of Boracay to the mystical waters of the Hinatuan Enchanted River, 
        every corner is a story waiting to be explored. 🌴🌊
    </p>
    <p style="font-size:1.1em; color:#023e8a; line-height:1.8;">
        The country is known for its warm and friendly people, colorful festivals, 
        delicious cuisine, and breathtaking landscapes. Whether you are seeking adventure, 
        relaxation, or cultural experiences, the Philippines offers something unforgettable 
        for every traveler. 🏝️🌋🐠
    </p>
</section>

<!-- ===== FESTIVALS & EVENTS SECTION ===== -->
<section id="festivals" style="max-width:1200px; margin:50px auto; padding:40px;">
    <h2 style="text-align:center; font-size:2.5em; color:#1d3557; margin-bottom:30px;">🎉 Festivals & Events</h2>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap:25px;">
        <!-- Sinulog Festival -->
        <div class="festival-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/FIESTA_ More FUN in the Philippines!.jpg" alt="Sinulog Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Sinulog Festival 🎶</h3>
                <p>Held every January in Cebu City to honor the Santo Niño, featuring street dancing and vibrant parades.</p>
            </div>
        </div>

        <!-- Ati-Atihan Festival -->
        <div class="festival-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Atiatihan festival Aklan, visayas, philippines.jpg" alt="Ati-Atihan Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Ati-Atihan Festival 🥁</h3>
                <p>Celebrated in Kalibo, Aklan, this festival honors the Santo Niño with tribal dancing and colorful costumes.</p>
            </div>
        </div>

        <!-- Panagbenga Festival -->
        <div class="festival-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/download (3).jpg" alt="Panagbenga Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Panagbenga 🌸</h3>
                <p>Baguio's Flower Festival every February showcases giant floats adorned with flowers and street dancing performances.</p>
            </div>
        </div>

        <!-- Pahiyas Festival -->
        <div class="festival-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Pahiyas Festival 2024_ Bountiful harvest festivity in Lucban, Quezon.jpg" alt="Pahiyas Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Pahiyas Festival 🌾</h3>
                <p>Held in Lucban, Quezon every May to celebrate a bountiful harvest, featuring decorated houses with rice, vegetables, and colorful ornaments.</p>
            </div>
        </div>

        <!-- Kadayawan Festival -->
        <div class="festival-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Kadayawan festival 2010_.jpg" alt="Kadayawan Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Kadayawan Festival 🌺</h3>
                <p>Celebrated in Davao City every August, it honors the bountiful harvest and the rich culture of the indigenous people.</p>
            </div>
        </div>

        <!-- Moriones Festival -->
        <div class="festival-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Moriones Festival of Marinduque, Philippines.jpg" alt="Moriones Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Moriones Festival 🏰</h3>
                <p>Takes place during Holy Week in Marinduque, featuring locals in Roman centurion costumes reenacting the story of Longinus.</p>
            </div>
        </div>

        <!-- Dinagyang Festival -->
        <div class="festival-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/How to Get to Iloilo for the Dinagyang Festivities 2016.jpg" alt="Dinagyang Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Dinagyang Festival 🥳</h3>
                <p>Held in Iloilo City in January to honor the Santo Niño, featuring street dancing and cultural competitions.</p>
            </div>
        </div>

        <!-- MassKara Festival -->
        <div class="festival-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Masskara Festival.jpg" alt="MassKara Festival" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">MassKara Festival 🎭</h3>
                <p>Celebrated in Bacolod City every October, famous for smiling masks, street dancing, and colorful costumes.</p>
            </div>
        </div>
    </div>
</section>

<!-- ===== FOOD & CUISINE SECTION ===== -->
<section id="food" style="max-width:1200px; margin:50px auto; padding:40px;">
    <h2 style="text-align:center; font-size:2.5em; color:#1d3557; margin-bottom:30px;">🍲 Filipino Food & Cuisine</h2>
    
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap:25px;">
        <!-- Adobo -->
        <div class="food-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Filipino Chicken Adobo Recipe_ The Best Version You’ll Ever Try - PinoyBites.jpg" alt="Adobo" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Adobo 🍖</h3>
                <p>One of the Philippines' most iconic dishes, made with meat marinated in soy sauce, vinegar, garlic, and spices.</p>
            </div>
        </div>
        
        <!-- Sinigang -->
        <div class="food-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/How to Cook Classic Filipino Sinigang – Step-by-Step Guide.jpg" alt="Sinigang" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Sinigang 🍲</h3>
                <p>A sour tamarind-based soup with pork, shrimp, or fish, and fresh vegetables. Comfort food at its best!</p>
            </div>
        </div>
        
        <!-- Lechon -->
        <div class="food-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/How To Roast Lechon Baboy.jpg" alt="Lechon" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Lechon 🐖</h3>
                <p>Crispy roasted pig, often served during festivals and celebrations — a Filipino crowd favorite!</p>
            </div>
        </div>
        
        <!-- Halo-Halo -->
        <div class="food-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Great Filipino Halo Halo Recipe.jpg" alt="Halo-Halo" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Halo-Halo 🍨</h3>
                <p>A colorful dessert made with shaved ice, evaporated milk, sweet beans, fruits, and ice cream — perfect for tropical heat.</p>
            </div>
        </div>
        
        <!-- Kare-Kare -->
        <div class="food-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Kare Kare.jpg" alt="Kare-Kare" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Kare-Kare 🥘</h3>
                <p>A peanut-based stew with oxtail, tripe, and vegetables, usually served with bagoong (fermented shrimp paste).</p>
            </div>
        </div>
        
        <!-- Balut -->
        <div class="food-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/download (5).jpg" alt="Balut" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Balut 🥚</h3>
                <p>A fertilized duck egg delicacy, often eaten as street food — adventurous eaters only!</p>
            </div>
        </div>
        
        <!-- Bicol Express -->
        <div class="food-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Filipino Bicol Express__🌶️ A deliciously spicy and creamy dish from the Philippines, Bicol Express features tender pork, shrimp, or fish simmered in a rich coconut milk sauce with a hint of heat from chili pepp.jpg" alt="Bicol Express" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Bicol Express 🌶️</h3>
                <p>A spicy dish made from pork, shrimp paste, and coconut milk, hailing from the Bicol region.</p>
            </div>
        </div>
                
         <!-- Lumpia -->
        <div class="food-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Pahiyas Festival 2024_ Bountiful harvest festivity in Lucban, Quezon.jpg" alt="Lumpia" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Lumpia 🌯</h3>
                <p>Filipino spring rolls, either fresh or fried, filled with vegetables, meat, or shrimp — perfect as appetizers or snacks.</p>
            </div>
        </div>

        <!-- Puto -->
        <div class="food-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Easy Puto Cheese Recipe.jpg" alt="Puto" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Puto 🍥</h3>
                <p>Soft, fluffy steamed rice cakes, usually eaten with savory dishes like dinuguan or pancit — a classic Filipino snack.</p>
            </div>
        </div>

        <!-- Longganisa -->
        <div class="food-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Skinless Longganisa Recipe - Kusina Master Recipes.jpg" alt="Longganisa" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Longganisa 🌭</h3>
                <p>Sweet or garlicky Filipino sausages, typically served for breakfast with garlic rice and fried egg.</p>
            </div>
        </div>

        <!-- Taho -->
        <div class="food-card" style="background:#ade8f4; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/Frequently Asked Questions About Taho.jpg" alt="Taho" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Taho 🥄</h3>
                <p>A sweet morning snack made from silken tofu, arnibal (sweet syrup), and sago pearls — sold by street vendors across the Philippines.</p>
            </div>
        </div>

        <!-- Pancit -->
        <div class="food-card" style="background:#caf0f8; border-radius:20px; overflow:hidden; box-shadow:0 8px 20px rgba(0,0,0,0.1); transition: transform 0.3s, box-shadow 0.3s;">
            <img src="/A simple and delicious Filipino noodle dish that's easy to prepare for beginners, featuring rice noodles, chicken, and a variety of vegetables_.jpg" alt="Pancit" style="width:100%; height:200px; object-fit:cover; transition: transform 0.3s;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Pancit 🍜</h3>
                <p>Stir-fried noodles with meat, seafood, and vegetables — a must-have during birthdays for long life and good fortune.</p>
            </div>
        </div>

    </div>
</section>


 <!-- ===== HOVER EFFECTS ===== -->
<style>
.festival-card:hover, .food-card:hover {
    transform: translateY(-8px);
    box-shadow:0 12px 25px rgba(0,0,0,0.2);
}

.festival-card img:hover, .food-card img:hover {
    transform: scale(1.05);
}
</style>
                
<!-- ===== TOURIST SPOTS SECTION ===== -->
<section id="tourist" style="max-width:1200px; margin:50px auto; padding:20px;">
    <h2 style="text-align:center; font-size:2.5em; color:#1d3557; margin-bottom:30px;">Popular Tourist Spots</h2>

    <div style="
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 25px;
    ">
        <!-- Boracay Card -->
        <div class="tourist-card" style="
            background:#caf0f8;
            border-radius:20px;
            overflow:hidden;
            box-shadow:0 8px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        ">
            <img src="/BORACAY ISLAND.jpg" alt="Boracay" style="
                width:100%;
                height:200px;
                object-fit:cover;
                transition: transform 0.3s;
            ">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Boracay 🌴</h3>
                <p>Known for its powdery white sand and crystal-clear waters, one of the Philippines' top destinations.</p>
            </div>
        </div>

        <!-- Chocolate Hills Card -->
        <div class="tourist-card" style="
            background:#ade8f4;
            border-radius:20px;
            overflow:hidden;
            box-shadow:0 8px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        ">
            <img src="/download.jpg" alt="Chocolate Hills" style="
                width:100%;
                height:200px;
                object-fit:cover;
                transition: transform 0.3s;
            ">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Chocolate Hills 🍫</h3>
                <p>Located in Bohol, over 1,200 hills turn brown during dry season, resembling chocolate.</p>
            </div>
        </div>

        <!-- Mayon Volcano Card -->
        <div class="tourist-card" style="
            background:#caf0f8;
            border-radius:20px;
            overflow:hidden;
            box-shadow:0 8px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        ">
            <img src="/download (1).jpg" alt="Mayon Volcano" style="
                width:100%;
                height:200px;
                object-fit:cover;
                transition: transform 0.3s;
            ">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Mayon Volcano 🌋</h3>
                <p>Famous for its perfect cone shape, Mayon Volcano is one of the Philippines' most active volcanoes.</p>
            </div>
        </div>

        <!-- El Nido Card -->
        <div class="tourist-card" style="
            background:#ade8f4;
            border-radius:20px;
            overflow:hidden;
            box-shadow:0 8px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        ">
            <img src="/PHOTOS_ Spectacular El Nido Palawan Philippines Aerial View.jpg" alt="El Nido" style="
                width:100%;
                height:200px;
                object-fit:cover;
                transition: transform 0.3s;
            ">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">El Nido 🏝️</h3>
                <p>Known for limestone cliffs and turquoise waters, part of a protected marine reserve.</p>
            </div>
        </div>

        <!-- Sirao Flower Garden Card -->
        <div class="tourist-card" style="
            background:#caf0f8;
            border-radius:20px;
            overflow:hidden;
            box-shadow:0 8px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        ">
            <img src="/download (2).jpg" alt="Sirao Flower Garden" style="
                width:100%;
                height:200px;
                object-fit:cover;
                transition: transform 0.3s;
            ">
            <div style="padding:20px;">
                <h3 style="color:#0077b6; margin-bottom:10px;">Sirao Flower Garden 🌸</h3>
                <p>Located in Cebu, famous for colorful flower fields and scenic mountain views.</p>
            </div>
        </div>
        
          <!-- Taal Volcano Card -->
  <div class="tourist-card" style="
              background:#caf0f8;
              border-radius:20px;
              overflow:hidden;
              box-shadow:0 8px 20px rgba(0,0,0,0.1);
              transition: transform 0.3s, box-shadow 0.3s;
          ">
    <img src="/Taal Lake, Bohol, Philippines.jpg" alt="Taal Volcano" style="
                  width:100%;
                  height:200px;
                  object-fit:cover;
                  transition: transform 0.3s;
              ">
    <div style="padding:20px;">
      <h3 style="color:#0077b6; margin-bottom:10px;">Taal Volcano 🌋</h3>
      <p>A volcano within a lake within a volcano.</p>
    </div>
  </div>
  
  <!-- Hinatuan Enchanted River Card -->
  <div class="tourist-card" style="
              background:#ade8f4;
              border-radius:20px;
              overflow:hidden;
              box-shadow:0 8px 20px rgba(0,0,0,0.1);
              transition: transform 0.3s, box-shadow 0.3s;
          ">
    <img src="/The Hinatuan Enchanted River, or the Hinatuan Sacred River, located on the east coast of Mindanao, the southernmost island of the Philippines_.jpg" alt="Hinatuan Enchanted River" style="
                  width:100%;
                  height:200px;
                  object-fit:cover;
                  transition: transform 0.3s;
              ">
    <div style="padding:20px;">
      <h3 style="color:#0077b6; margin-bottom:10px;">Hinatuan Enchanted River 💧</h3>
      <p>A deep, mystical blue river known for its crystal-clear waters.</p>
    </div>
  </div>
  
  <!-- Banaue Rice Terraces Card -->
  <div class="tourist-card" style="
              background:#caf0f8;
              border-radius:20px;
              overflow:hidden;
              box-shadow:0 8px 20px rgba(0,0,0,0.1);
              transition: transform 0.3s, box-shadow 0.3s;
          ">
    <img src="/Rice terrasse, Philippines.jpg" alt="Banaue Rice Terraces" style="
                  width:100%;
                  height:200px;
                  object-fit:cover;
                  transition: transform 0.3s;
              ">
    <div style="padding:20px;">
      <h3 style="color:#0077b6; margin-bottom:10px;">Banaue Rice Terraces 🌾</h3>
      <p>Carved by hand over 2,000 years ago, these terraces are called the “Eighth Wonder of the World.”</p>
    </div>
  </div>
  
  <!-- Hundred Islands -->
        <div class="tourist-card" style="background:#caf0f8;">
            <img src="/How Many Islands Make Up the Philippines_ The Surprising Total Will Amaze You!.jpg" alt="Hundred Islands" style="width:100%; height:200px; object-fit:cover;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6;">Hundred Islands 🏝️</h3>
                <p>Located in Pangasinan, a group of 124 islands perfect for island-hopping adventures.</p>
            </div>
        </div>

        <!-- Puerto Princesa Underground River -->
        <div class="tourist-card" style="background:#ade8f4;">
            <img src="/PUERTO PRINCESA, PALAWAN - Travel Guide & What To See And Do In Puerto Princesa.jpg" alt="Puerto Princesa Underground River" style="width:100%; height:200px; object-fit:cover;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6;">Puerto Princesa Underground River 🏞️</h3>
                <p>A UNESCO World Heritage Site, this underground river is one of the longest navigable in the world.</p>
            </div>
        </div>

        <!-- Siargao Island -->
        <div class="tourist-card" style="background:#caf0f8;">
            <img src="/siargao island philippines.jpg" alt="Siargao Island" style="width:100%; height:200px; object-fit:cover;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6;">Siargao Island 🌊</h3>
                <p>Known as the surfing capital of the Philippines with crystal-clear lagoons and palm-lined beaches.</p>
            </div>
        </div>

        <!-- Camiguin Island -->
        <div class="tourist-card" style="background:#ade8f4;">
            <img src="/White Island, Camiguin Island, Philippines.jpg" alt="Camiguin Island" style="width:100%; height:200px; object-fit:cover;">
            <div style="padding:20px;">
                <h3 style="color:#0077b6;">Camiguin Island 🌴</h3>
                <p>Known as the “Island Born of Fire,” it has volcanoes, waterfalls, and hot springs to explore.</p>
            </div>
        </div>
   </div>
  </section>

<!-- ===== STYLES AND HOVER EFFECTS ===== --> <style> .tourist-card:hover { transform: translateY(-8px); box-shadow: 0 12px 25px rgba(0,0,0,0.2); } .tourist-card img:hover { transform: scale(1.05); } </style>

<!-- ===== MAP & TRAVEL TIPS SECTION ===== -->
<section id="travel-info" style="max-width:1200px; margin:50px auto; padding:40px; display:flex; flex-wrap:wrap; gap:30px; justify-content:center;">

<!-- ===== TRAVEL TIPS CARD (UPDATED) ===== -->
<div style="flex:1 1 400px; min-width:300px; background: linear-gradient(135deg,#caf0f8,#ade8f4); border-radius:20px; box-shadow:0 8px 25px rgba(0,0,0,0.1); padding:30px;">
    <h2 style="text-align:center; color:#0077b6; margin-bottom:20px;">📝 Travel Tips</h2>
    <ul style="list-style:none; padding:0; font-size:1.1em; line-height:1.8; color:#023e8a;">
      <li>☀️ Best time to visit: November – May (dry season)</li>
      <li>🧴 Always wear sunscreen to protect your skin</li>
      <li>🌿 Respect local customs and environment</li>
      <li>⛴️ Use ferries and boats for inter-island travel</li>
      <li>📸 Bring a camera to capture stunning landscapes</li>
      <li>🍲 Try local Filipino food and delicacies</li>
      <li>🛏️ Book accommodations in advance during peak season</li>
      <li>🚗 Rent a scooter or motorbike for flexible island exploration</li>
      <li>💧 Stay hydrated, especially in tropical heat</li>
      <li>🧭 Use maps and GPS – some areas have limited signage</li>
      <li>💳 Carry cash – some smaller islands don’t accept cards</li>
      <li>🏊‍♂️ Check water safety and tides before swimming</li>
      <li>🎒 Pack light, breathable clothing for tropical climate</li>
      <li>🦟 Bring mosquito repellent for forested or rural areas</li>
      <li>📅 Plan itineraries but leave room for spontaneous adventures</li>
      <li>🤝 Be friendly – locals are warm and welcoming!</li>
    </ul>
</div>


<!-- ===== FUN FACT SECTION ===== -->
    <section id="funfacts" class="fact">
    <h style="font-size:2.2em; color:#0077b6; margin-bottom:20px;">Did You Know? 🤔</h2>
    <p id="factText" style="
        font-size:1.1em; 
        color:#023e8a; 
        margin-bottom:25px; 
        min-height:40px;
        transition: all 0.4s ease;
    ">
        Click the button to learn a fun fact!
    </p>
    <button onclick="showFact()" style="
        padding:12px 25px; 
        border:none; 
        border-radius:30px; 
        background: linear-gradient(135deg,#0077b6,#0096c7); 
        color:white; 
        font-size:1em; 
        font-weight:600; 
        cursor:pointer; 
        transition: transform 0.2s, box-shadow 0.2s;
    ">
        Show Fun Fact 🎉
    </button>
</section>

<!-- ===== STYLES ===== -->
<style>
/* Button hover effect */
.fact button:hover {
    transform: scale(1.05);
    box-shadow:0 6px 18px rgba(0,0,0,0.3);
}
</style> 

<!-- ===== FUN FACT SCRIPT ===== -->
<script>
function showFact(){
    const facts = [
        "The Philippines has over 7,600 islands. 🏝️",
        "Boracay was once awarded the World’s Best Island. 🌴",
        "Chocolate Hills are a natural geological formation. 🍫",
        "Mayon Volcano has erupted more than 50 times. 🌋",
        "El Nido is part of a protected marine reserve. 🐠",
        "The Hinatuan Enchanted River is crystal-clear and mystical. 💧",
        "Banaue Rice Terraces were carved by hand over 2,000 years ago. 🌾",
        "Siargao is known as the surfing capital of the Philippines. 🏄‍♂️",
    ];
    // Random fact
    const random = facts[Math.floor(Math.random() * facts.length)];
    
    // Animate text fade
    const factText = document.getElementById("factText");
    factText.style.opacity = 0;
    setTimeout(() => {
        factText.textContent = random;
        factText.style.opacity = 1;
    }, 300);
}
</script>

<!-- ===== QUIZ SECTION ===== -->
<section id="quiz" style="max-width:900px; margin:50px auto; padding:40px; background: linear-gradient(135deg,#caf0f8,#ade8f4); border-radius:20px; box-shadow:0 8px 25px rgba(0,0,0,0.1); text-align:center;">
  <h2 style="font-size:2.2em; color:#0077b6; margin-bottom:20px;">🌴 Which Philippine Island Should You Visit?</h2>
  <p style="font-size:1.1em; color:#023e8a; margin-bottom:30px;">Answer a few questions and find your perfect island getaway!</p>

  <!-- Questions -->
  <div id="quizQuestions">
    <div class="question" data-answer="">
      <p style="font-size:1.1em; margin-bottom:15px;">1️⃣ Do you prefer beaches or mountains?</p>
      <button onclick="selectAnswer(this, 'beach')">Beaches 🏖️</button>
      <button onclick="selectAnswer(this, 'mountain')">Mountains ⛰️</button>
    </div>

    <div class="question" data-answer="">
      <p style="font-size:1.1em; margin-bottom:15px;">2️⃣ Do you like adventure or relaxation?</p>
      <button onclick="selectAnswer(this, 'adventure')">Adventure 🧗‍♂️</button>
      <button onclick="selectAnswer(this, 'relax')">Relaxation 😌</button>
    </div>

    <div class="question" data-answer="">
      <p style="font-size:1.1em; margin-bottom:15px;">3️⃣ Do you enjoy vibrant nightlife or peaceful nature?</p>
      <button onclick="selectAnswer(this, 'nightlife')">Nightlife 🎶</button>
      <button onclick="selectAnswer(this, 'nature')">Peaceful Nature 🌿</button>
    </div>
  </div>

  <!-- Result -->
  <div id="quizResult" style="margin-top:30px; font-size:1.2em; font-weight:600; min-height:50px; color:#0077b6;"></div>

  <button onclick="restartQuiz()" style="margin-top:20px; padding:12px 25px; border:none; border-radius:30px; background: linear-gradient(135deg,#0077b6,#0096c7); color:white; font-size:1em; font-weight:600; cursor:pointer; transition: transform 0.2s, box-shadow 0.2s;">
    Restart Quiz 🔄
  </button>
</section>

<!-- ===== QUIZ SCRIPT ===== -->
<script>
let answers = [];

function selectAnswer(button, value) {
    const parent = button.parentElement;
    parent.dataset.answer = value;

    // Highlight selected button
    const buttons = parent.querySelectorAll('button');
    buttons.forEach(b => b.style.background = '');
    button.style.background = 'linear-gradient(135deg,#ffb703,#fb8500)';
    button.style.color = 'white';

    // Save answer
    answers = Array.from(document.querySelectorAll('.question')).map(q => q.dataset.answer);

    // Show result if all answered
    if (!answers.includes('')) {
        showQuizResult();
    }
}

function showQuizResult() {
    let result = '';
    // Simple logic for demo
    const beach = answers.filter(a => a === 'beach').length;
    const mountain = answers.filter(a => a === 'mountain').length;
    const adventure = answers.filter(a => a === 'adventure').length;
    const relax = answers.filter(a => a === 'relax').length;
    const nightlife = answers.filter(a => a === 'nightlife').length;
    const nature = answers.filter(a => a === 'nature').length;

    if (beach >= 1 && adventure >=1) result = "🏄‍♂️ You should visit **Siargao** for surfing adventures!";
    else if (beach >= 1 && relax >=1) result = "🏖️ You should visit **Boracay** for a relaxing beach getaway!";
    else if (mountain >= 1 && nature >=1) result = "🌾 You should visit **Banaue Rice Terraces** for peaceful mountain views!";
    else if (mountain >= 1 && nightlife >=1) result = "🌋 You should visit **Baguio** for cool mountains and vibrant city life!";
    else result = "🏝️ The Philippines has countless islands – try exploring **Palawan** for a mix of adventure and relaxation!";

    document.getElementById('quizResult').innerHTML = result;
}

function restartQuiz() {
    answers = [];
    document.querySelectorAll('.question').forEach(q => q.dataset.answer = '');
    document.querySelectorAll('.question button').forEach(b => {
        b.style.background = '';
        b.style.color = '#0077b6';
    });
    document.getElementById('quizResult').textContent = '';
}
</script>

<!-- ===== QUIZ STYLING ===== -->
<style>
#quiz button {
    padding: 10px 20px;
    margin: 5px;
    border-radius:25px;
    border:none;
    background:#ade8f4;
    color:#0077b6;
    font-weight:600;
    cursor:pointer;
    transition: transform 0.2s, box-shadow 0.2s;
}

#quiz button:hover {
    transform: scale(1.05);
    box-shadow:0 5px 15px rgba(0,0,0,0.3);
}

</style>


<!-- ===== CONTACT SECTION ===== -->
<section id="contact" style="max-width:900px; margin:50px auto; padding:40px; background: linear-gradient(135deg,#caf0f8,#ade8f4); border-radius:20px; box-shadow:0 8px 25px rgba(0,0,0,0.1);">
  <h2 style="text-align:center; color:#0077b6; font-size:2.2em; margin-bottom:20px;">Contact Us 📬</h2>
  <p style="text-align:center; color:#023e8a; font-size:1em; margin-bottom:30px;">
    Have questions or want to share your travel experience? Reach out to us!
  </p>
  
  <!-- Contact Info -->
  <div style="display:flex; flex-wrap:wrap; justify-content:space-around; margin-bottom:30px; gap:20px;">
    <div style="flex:1; min-width:200px; text-align:center;">
      <p style="font-size:1.1em; margin:5px;">✉️ Email</p>
      <p style="color:#0077b6;">PhilTourist@gmail.com</p>
    </div>
    <div style="flex:1; min-width:200px; text-align:center;">
      <p style="font-size:1.1em; margin:5px;">📞 Phone</p>
      <p style="color:#0077b6;">+63 935 392 241</p>
    </div>
    <div style="flex:1; min-width:200px; text-align:center;">
      <p style="font-size:1.1em; margin:5px;">🌐 Social</p>
      <p style="color:#0077b6;">@PhilTourist</p>
    </div>
  </div>
  
  <!-- Contact Form -->
  <form style="display:flex; flex-direction:column; gap:20px;">
    <input type="text" placeholder="Your Name" required style="padding:12px 15px; border-radius:10px; border:1px solid #0077b6; outline:none; font-size:1em;">
    <input type="email" placeholder="Your Email" required style="padding:12px 15px; border-radius:10px; border:1px solid #0077b6; outline:none; font-size:1em;">
    <textarea placeholder="Your Message" rows="5" required style="padding:12px 15px; border-radius:10px; border:1px solid #0077b6; outline:none; font-size:1em;"></textarea>
    <button type="submit" style="padding:12px 20px; border:none; border-radius:25px; background: linear-gradient(135deg,#0077b6,#0096c7); color:white; font-size:1em; font-weight:600; cursor:pointer; transition: transform 0.2s, box-shadow 0.2s;">
      Send Message
    </button>
  </form>
</section>

<!-- ===== HOVER & FOCUS EFFECTS ===== -->
<style>
  form input:focus,
  form textarea:focus {
    border-color: #023e8a;
    box-shadow: 0 0 8px rgba(0, 119, 182, 0.4);
  }
  
  form button:hover {
    transform: scale(1.05);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
  }
</style>

<footer>
    <p>© 2026 Philippine Tourist Spot Information Website</p>
</footer>
</script>

<script>
function login(){
    document.getElementById("loginPage").style.display = "none";
    document.getElementById("mainSite").style.display = "block";
}
</script>

</body>
</html>
