# Ex02 Commercial Website
## Date: 16-05-2026
## Name: Adarsh Chowdary R
## Reg No: 212223040166
## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css) 

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
## index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NovaCart</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>

        <div class="logo">NovaCart</div>

        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>

        <button class="account-btn" onclick="openPopup()">
            Create Account
        </button>

    </header>

    <section id="home" class="hero-section">

        <div class="hero-content">

            <h1>Discover Smart Shopping Experience</h1>

            <p>
                Explore premium gadgets, modern accessories and trending
                technology products with exciting offers.
            </p>

            <a href="#products">
                <button class="shop-btn">Explore Products</button>
            </a>

        </div>

        <div class="hero-image">
            <img src="https://images.unsplash.com/photo-1519389950473-47ba0277781c" alt="shopping">
        </div>

    </section>

    <section id="products" class="products-section">

        <h2>Trending Products</h2>

        <div class="product-container">

            <div class="card">

                <img src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9" alt="phone">

                <h3>Smart Phones</h3>

                <p>
                    Powerful smartphones with stylish design and high speed performance.
                </p>

                <button>View Product</button>

            </div>

            <div class="card">

                <img src="https://images.unsplash.com/photo-1496181133206-80ce9b88a853" alt="laptop">

                <h3>Modern Laptops</h3>

                <p>
                    Lightweight and high performance laptops for students and professionals.
                </p>

                <button>View Product</button>

            </div>

            <div class="card">

                <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e" alt="headphone">

                <h3>Wireless Audio</h3>

                <p>
                    Enjoy immersive sound quality with premium wireless headphones.
                </p>

                <button>View Product</button>

            </div>

        </div>

    </section>

    <section id="about" class="info-section">

        <h2>About NovaCart</h2>

        <p>
            NovaCart is a modern commercial platform designed to provide
            stylish technology products with better quality, affordable pricing
            and customer satisfaction.
        </p>

    </section>

    <section id="contact" class="contact-section">

        <h2>Contact Us</h2>

        <p>Email : support@novacart.com</p>
        <p>Phone : +91 9876543210</p>
        <p>Location : Chennai, India</p>

    </section>

    <footer>

        <div class="social-links">
            <a href="#">Instagram</a>
            <a href="#">Facebook</a>
            <a href="#">Twitter</a>
            <a href="#">LinkedIn</a>
        </div>

        <p>© 2026 NovaCart. All Rights Reserved.</p>

    </footer>

    <div class="popup" id="popup">

        <div class="popup-content">

            <span class="close-btn" onclick="closePopup()">&times;</span>

            <h2>Create Account</h2>

            <form>

                <input type="text" placeholder="Full Name" required>

                <input type="email" placeholder="Email Address" required>

                <input type="password" placeholder="Password" required>

                <input type="password" placeholder="Confirm Password" required>

                <button type="submit" class="create-btn">
                    Create Account
                </button>

            </form>

        </div>

    </div>

    <script>

        function openPopup(){
            document.getElementById("popup").style.display = "flex";
        }

        function closePopup(){
            document.getElementById("popup").style.display = "none";
        }

    </script>

</body>
</html>
```

## style.css
```
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Verdana, Geneva, Tahoma, sans-serif;
}

html{
    scroll-behavior:smooth;
}

body{
    background:
    radial-gradient(circle at top left, #dbeafe, transparent 30%),
    radial-gradient(circle at bottom right, #ede9fe, transparent 30%),
    linear-gradient(to right, #f8fafc, #eef2ff);

    color:#222;
    min-height:100vh;
}

header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:18px 50px;

    background:rgba(255,255,255,0.55);

    backdrop-filter:blur(12px);

    position:sticky;
    top:0;
    z-index:1000;

    border-bottom:1px solid rgba(255,255,255,0.3);

    box-shadow:0 4px 20px rgba(0,0,0,0.08);
}

.logo{
    font-size:38px;
    font-weight:bold;
    font-family:'Trebuchet MS', sans-serif;
    letter-spacing:3px;
    text-transform:uppercase;

    background:linear-gradient(to right,#4f46e5,#7c3aed,#06b6d4);
    background-clip:text;
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;

    text-shadow:2px 2px 10px rgba(79,70,229,0.3);
}

nav ul{
    display:flex;
    list-style:none;
    gap:25px;
}

nav ul li a{
    text-decoration:none;
    color:#333;
    font-size:17px;
    font-weight:500;
    transition:0.3s;
}

nav ul li a:hover{
    color:#4f46e5;
}

.account-btn{
    padding:10px 18px;
    border:none;
    border-radius:25px;
    background:linear-gradient(to right,#4f46e5,#7c3aed);
    color:white;
    cursor:pointer;
    font-size:15px;
    transition:0.3s;
}

.account-btn:hover{
    transform:scale(1.05);
    box-shadow:0 4px 15px rgba(79,70,229,0.4);
}

.hero-section{
    min-height:90vh;
    display:flex;
    justify-content:space-around;
    align-items:center;
    padding:50px;
    flex-wrap:wrap;
    gap:40px;
}

.hero-content{
    max-width:550px;
}

.hero-content h1{
    font-size:60px;
    line-height:1.2;
    margin-bottom:20px;

    background:linear-gradient(to right,#1e1b4b,#4f46e5,#06b6d4);
    background-clip:text;
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

.hero-content p{
    font-size:20px;
    line-height:1.8;
    margin-bottom:30px;
    color:#555;
}

.shop-btn{
    padding:14px 28px;
    border:none;
    border-radius:30px;
    background:linear-gradient(to right,#4f46e5,#7c3aed);
    color:white;
    font-size:18px;
    cursor:pointer;
    transition:0.3s;
}

.shop-btn:hover{
    transform:translateY(-3px);
    box-shadow:0 5px 18px rgba(79,70,229,0.4);
}

.hero-image img{
    width:450px;
    border-radius:25px;
    box-shadow:0 10px 30px rgba(0,0,0,0.2);
    transition:0.4s;
}

.hero-image img:hover{
    transform:scale(1.03);
}

.products-section{
    padding:70px 40px;
    text-align:center;
}

.products-section h2{
    font-size:42px;
    margin-bottom:50px;
    color:#1e1b4b;
}

.product-container{
    display:flex;
    justify-content:center;
    gap:35px;
    flex-wrap:wrap;
}

.card{
    width:320px;
    background:rgba(255,255,255,0.8);
    backdrop-filter:blur(10px);
    border-radius:22px;
    overflow:hidden;
    transition:0.4s;
    box-shadow:0 8px 25px rgba(0,0,0,0.08);
}

.card:hover{
    transform:translateY(-12px);
    box-shadow:0 12px 30px rgba(79,70,229,0.18);
}

.card img{
    width:100%;
    height:230px;
    object-fit:cover;
}

.card h3{
    margin:20px 0 10px;
    color:#4f46e5;
    font-size:24px;
}

.card p{
    padding:0 20px;
    line-height:1.7;
    color:#555;
}

.card button{
    margin:20px 0 25px;
    padding:10px 22px;
    border:none;
    border-radius:20px;
    background:linear-gradient(to right,#4f46e5,#7c3aed);
    color:white;
    cursor:pointer;
    transition:0.3s;
}

.card button:hover{
    transform:scale(1.05);
}

.info-section,
.contact-section{
    margin:40px auto;
    width:85%;
    background:rgba(255,255,255,0.8);
    backdrop-filter:blur(10px);
    padding:45px;
    border-radius:22px;
    box-shadow:0 6px 20px rgba(0,0,0,0.08);
    text-align:center;
}

.info-section h2,
.contact-section h2{
    margin-bottom:20px;
    font-size:35px;
    color:#1e1b4b;
}

.info-section p,
.contact-section p{
    font-size:18px;
    line-height:1.8;
    color:#555;
}

footer{
    margin-top:50px;
    background:linear-gradient(to right,#1e1b4b,#312e81);
    color:white;
    text-align:center;
    padding:30px;
}

.social-links{
    margin-bottom:15px;
}

.social-links a{
    text-decoration:none;
    color:white;
    margin:0 12px;
    transition:0.3s;
}

.social-links a:hover{
    color:#c4b5fd;
}

.popup{
    width:100%;
    height:100vh;
    background:rgba(0,0,0,0.5);
    position:fixed;
    top:0;
    left:0;
    display:none;
    justify-content:center;
    align-items:center;
    z-index:2000;
}

.popup-content{
    width:380px;
    background:white;
    padding:35px;
    border-radius:22px;
    position:relative;
    animation:popupAnimation 0.4s ease;
    box-shadow:0 10px 30px rgba(0,0,0,0.2);
}

.popup-content h2{
    text-align:center;
    margin-bottom:25px;
    color:#1e1b4b;
}

.popup-content form{
    display:flex;
    flex-direction:column;
    gap:18px;
}

.popup-content input{
    padding:13px;
    border:1px solid #ccc;
    border-radius:10px;
    font-size:15px;
}

.create-btn{
    padding:13px;
    border:none;
    border-radius:25px;
    background:linear-gradient(to right,#4f46e5,#7c3aed);
    color:white;
    font-size:16px;
    cursor:pointer;
    transition:0.3s;
}

.create-btn:hover{
    transform:scale(1.03);
}

.close-btn{
    position:absolute;
    top:15px;
    right:20px;
    font-size:28px;
    cursor:pointer;
    color:#555;
}

.close-btn:hover{
    color:red;
}

@keyframes popupAnimation{

    from{
        transform:scale(0.7);
        opacity:0;
    }

    to{
        transform:scale(1);
        opacity:1;
    }
}

@media(max-width:768px){

    header{
        flex-direction:column;
        gap:15px;
    }

    nav ul{
        flex-wrap:wrap;
        justify-content:center;
    }

    .hero-section{
        text-align:center;
    }

    .hero-content h1{
        font-size:42px;
    }

    .hero-image img{
        width:100%;
        max-width:350px;
    }

    .products-section h2{
        font-size:34px;
    }

    .card{
        width:100%;
        max-width:330px;
    }

    .popup-content{
        width:90%;
    }
}
```
## OUTPUT
<img width="1872" height="963" alt="image" src="https://github.com/user-attachments/assets/d2186e2b-3c9b-4754-8577-55f9950e8fe5" />
<img width="1875" height="962" alt="image" src="https://github.com/user-attachments/assets/ffad006e-470d-4553-ba28-d0e32c897afa" />
<img width="1874" height="966" alt="image" src="https://github.com/user-attachments/assets/d398c239-3908-45c6-ae57-93c44c2b9150" />
<img width="1871" height="960" alt="image" src="https://github.com/user-attachments/assets/79aff60d-457a-4cd2-adfa-bd3428d2695a" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
