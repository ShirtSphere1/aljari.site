# aljari.site
aljari<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Al Jari - Topis for Faith</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background: #A78BFA;
        }
        header {
            background: #87CEEB;
            color: sky blue;
            padding: 20px;
        }
        nav ul {
            list-style: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 10px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            padding: 20px;
        }
        .product {
            background: white;
            padding: 20px;
            border-radius: 10px;
            font-weight: bold;
        }
        form input, form textarea {
            width: 80%;
            padding: 10px;
            margin: 10px;
            border: 1px solid #ccc;
        }
        button {
            padding: 10px 20px;
            background: #333;
            color: white;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Al Jari</h1>
        <p>Embracing Faith, One Topi at a Time</p>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <h2>Welcome to Al Jari</h2>
        <p>Discover premium topis designed to reflect your devotion and style.</p>
    </section>

    <section id="products">
        <h2>Our Collection</h2>
        <div class="product-grid">
            <div class="product">Classic White Topi</div>
            <div class="product">Embroidered Faith Topi</div>
            <div class="product">Elegant Black Topi</div>
            <div class="product">Customizable Topi</div>
            <div class="product">Cotton Topi</div>
        </div>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p>"The word 'Al Jari' in Arabic carries a warmth of closeness – it speaks of a neighbor, a companion, a protégé. It is this spirit of fellowship and support that defines the Al Jari brand. We see ourselves as your companion on the beautiful path of Islam.

A topi is a personal article of faith, a constant reminder of our devotion. Recognizing this intimate connection, we at Al Jari are dedicated to crafting topis that are not only aesthetically pleasing but also a source of comfort and tranquility during your prayers. Our designs are a blend of classic elegance and contemporary style, ensuring there is an Al Jari for every individual.

We are a brand built on the values of community and shared identity. When you choose Al Jari, you are not just a customer; you are a neighbor in faith. We are committed to serving you with integrity and excellence, providing you with a product that you can wear with pride and reverence.

Let Al Jari be your trusted companion in every prayer.

Al Jari - With you in Faith."

Al Jari is dedicated to crafting top-quality topis inspired by Islamic tradition and faith.</p>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form id="contactForm">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
           <input type="address" placeholder="Your Address" requird>
            <textarea placeholder="Your Message"></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2025 Al Jari - All Rights Reserved</p>
    </footer>

    <script>
        document.getElementById("contactForm").addEventListener("submit", function(event) {
            event.preventDefault();
            alert("Thank you for your message! We will get back to you soon.");
        });
    </script>
</body>
</html>

<script src="https://www.gstatic.com/firebasejs/9.0.0/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.0.0/firebase-auth.js"></script>
<script>
  const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
  };
  firebase.initializeApp(firebaseConfig);
</script>
<section id="login">
    <h2>Login to Al Jari</h2>
    <input type="email" id="email" placeholder="Email">
    <input type="password" id="password" placeholder="Password">
    <button onclick="loginUser()">Login</button>
    <button onclick="registerUser()">Sign Up</button>
</section>
function registerUser() {
    const email = document.getElementById("email").value;
    const password = document.getElementById("password").value;

    firebase.auth().createUserWithEmailAndPassword(email, password)
        .then((userCredential) => alert("Account Created Successfully!"))
        .catch((error) => alert(error.message));
}

function loginUser() {
    const email = document.getElementById("email").value;
    const password = document.getElementById("password").value;

    firebase.auth().signInWithEmailAndPassword(email, password)
        .then((userCredential) => alert("Logged in Successfully!"))
        .catch((error) => alert(error.message));
}
<div id="editable-section">
    <p id="editable-text">Welcome to Al Jari!</p>
    <input type="text" id="newText" placeholder="Enter new content">
    <button onclick="updateText()">Update</button>
</div>
function updateText() {
    const newText = document.getElementById("newText").value;
    document.getElementById("editable-text").innerText = newText;
    alert("Content Updated Successfully!");
}
<section id="products">
    <h2>Product Collection</h2>
    <div id="product-list">
        <div class="product">Classic White Topi</div>
        <div class="product">Embroidered Faith Topi</div>
    </div>
    <input type="text" id="newProduct" placeholder="Enter Product Name">
    <button onclick="addProduct()">Add Product</button>
</section>
function addProduct() {
    const productName = document.getElementById("newProduct").value;
    const productList = document.getElementById("product-list");

    const newProduct = document.createElement("div");
    newProduct.className = "product";
    newProduct.innerText = productName;
    productList.appendChild(newProduct);
}
function addProduct() {
    const productName = document.getElementById("newProduct").value;
    const productList = document.getElementById("product-list");

    const newProduct = document.createElement("div");
    newProduct.className = "product";
    newProduct.innerText = productName;
    productList.appendChild(newProduct);
}
body {
    background: url('https://www.google.com/search?sca_esv=87b41ab4477c98ab&rlz=1C1SQJL_enPK1090PK1090&sxsrf=AE3TifMcpHD5oF54TfsX_ipVAOxNv21-YA:1749208889351&q=beautiful+background+for+website&udm=2&fbs=AIIjpHxU7SXXniUZfeShr2fp4giZ1Y6MJ25_tmWITc7uy4KIeoJTKjrFjVxydQWqI2NcOha3O1YqG67F0QIhAOFN_ob1aWGQOelbxvw0PKo40QtwvZMGAT8mh52EQduMaEwrkL-OLEnIgHQ7APoKxFV9hua55yCiA1pSqi8NqYaykPBkHQYt8sF3mLIH7UYTHYwhcJqGpMVh&sa=X&ved=2ahUKEwienvPz1tyNAxXmk68BHVEUCkkQtKgLegQIERAB&biw=1366&bih=641&dpr=1#vhid=QDa7Ct68am5O7M&vssid=mosaic') no-repeat center center/cover;
    font-family: 'Poppins', sans-serif;
}
header {
    background: linear-gradient(90deg, #4A90E2, #50C9C3);
    color: white;
    padding: 20px;
}

I’ll generate a content management system (CMS) feature within your website that allows you to edit: ✅ Background (Change colors or images dynamically)
✅ Products & Details (Add/remove products with descriptions and pricing)
✅ Text & Sections (Modify existing content without coding)
How This Works
- Admin Panel: A simple interface where you can edit everything.
- Local Storage: Saves changes without coding (or we can later connect this to a database like Firebase).
- User-Friendly Interface: Click and edit features for easy modifications.

📜 Full Code for Editable Website Features
Insert this inside your existing website, so you can start editing immediately.
🔹 Add an "Edit Mode" Button to Enable Editing
Place this inside your body section:
<button onclick="toggleEditMode()">Enable Edit Mode</button>
<div id="adminPanel" style="display:none;">
    <h3>Customize Your Website</h3>
    
    <label>Change Background:</label>
    <input type="color" id="bgColorPicker">
    <button onclick="changeBackground()">Apply</button><br><br>

    <label>Add Product:</label>
    <input type="text" id="productName" placeholder="Product Name">
    <input type="text" id="productDetails" placeholder="Product Details">
    <button onclick="addProduct()">Add Product</button><br><br>

    <label>Edit Text:</label>
    <input type="text" id="editableText">
    <button onclick="editContent()">Update Text</button>
</div>



🔹 JavaScript to Enable Editing & Updating
Insert this inside your script.js file:
function toggleEditMode() {
    let adminPanel = document.getElementById("adminPanel");
    adminPanel.style.display = adminPanel.style.display === "none" ? "block" : "none";
}

function changeBackground() {
    let color = document.getElementById("bgColorPicker").value;
    document.body.style.backgroundColor = color;
    localStorage.setItem("bgColor", color);
}

function addProduct() {
    let productName = document.getElementById("productName").value;
    let productDetails = document.getElementById("productDetails").value;
    let productList = document.getElementById("product-list");

    let newProduct = document.createElement("div");
    newProduct.className = "product";
    newProduct.innerHTML = `<h3>${productName}</h3><p>${productDetails}</p>`;
    productList.appendChild(newProduct);
}

function editContent() {
    let newText = document.getElementById("editableText").value;
    document.getElementById("editable-section").innerText = newText;
    localStorage.setItem("editableContent", newText);
}

// Load saved settings when the page reloads
document.addEventListener("DOMContentLoaded", function () {
    let savedBgColor = localStorage.getItem("bgColor");
    if (savedBgColor) document.body.style.backgroundColor = savedBgColor;

    let savedContent = localStorage.getItem("editableContent");
    if (savedContent) document.getElementById("editable-section").innerText = savedContent;
});



🔹 How to Use
1️⃣ Click "Enable Edit Mode" to show the editor.
2️⃣ Choose a background color, and the site updates instantly.
3️⃣ Add new products dynamically to the product section.
4️⃣ Edit existing text and update content directly.

🚀 Next Steps
Would you like database integration (Firebase or MySQL) so these edits persist beyond page refresh? Let me know, and I’ll enhance this setup further! 🔥
<button id="editToggle">Enable Edit Mode</button>
<div id="adminPanel" style="display:none;">
    <h3>Customize Your Website</h3>
    
    <label>Change Background:</label>
    <input type="color" id="bgColorPicker">
    <button onclick="changeBackground()">Apply</button><br><br>

    <label>Add Product:</label>
    <input type="text" id="productName" placeholder="Product Name">
    <input type="text" id="productDetails" placeholder="Product Details">
    <button onclick="addProduct()">Add Product</button><br><br>

    <label>Edit Text:</label>
    <input type="text" id="editableText" placeholder="Enter new text">
    <button onclick="editContent()">Update Text</button>
</div>
Got it! I'll make sure the Edit Mode button is positioned at the top-right corner of your website and ensure that all editing features work properly. Here’s the updated code:

🔹 Updated HTML (Place this inside <body>)
<button id="editToggle">🛠 Edit Mode</button>
<div id="adminPanel" style="display:none;">
    <h3>Customize Your Website</h3>
    
    <label>Change Background:</label>
    <input type="color" id="bgColorPicker">
    <button onclick="changeBackground()">Apply</button><br><br>

    <label>Add Product:</label>
    <input type="text" id="productName" placeholder="Product Name">
    <input type="text" id="productDetails" placeholder="Product Details">
    <button onclick="addProduct()">Add Product</button><br><br>

    <label>Edit Text:</label>
    <input type="text" id="editableText" placeholder="Enter new text">
    <button onclick="editContent()">Update Text</button>
</div>



🔹 Updated CSS (Place inside styles.css)
#editToggle {
    position: fixed;
    top: 10px;
    right: 10px;
    background: #007bff;
    color: white;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
    font-size: 16px;
    border-radius: 5px;
}

#adminPanel {
    position: fixed


Got it! I'll make sure the Edit Mode button is positioned at the top-right corner of your website and ensure that all editing features work properly. Here’s the updated code:

🔹 Updated HTML (Place this inside <body>)
<button id="editToggle">🛠 Edit Mode</button>
<div id="adminPanel" style="display:none;">
    <h3>Customize Your Website</h3>
    
    <label>Change Background:</label>
    <input type="color" id="bgColorPicker">
    <button onclick="changeBackground()">Apply</button><br><br>

    <label>Add Product:</label>
    <input type="text" id="productName" placeholder="Product Name">
    <input type="text" id="productDetails" placeholder="Product Details">
    <button onclick="addProduct()">Add Product</button><br><br>

    <label>Edit Text:</label>
    <input type="text" id="editableText" placeholder="Enter new text">
    <button onclick="editContent()">Update Text</button>
</div>



🔹 Updated CSS (Place inside styles.css)
#editToggle {
    position: fixed;
    top: 10px;
    right: 10px;
    background: #007bff;
    color: white;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
    font-size: 16px;
    border-radius: 5px;
}

#adminPanel {
    position: fixed


Got it! I'll make sure the Edit Mode button is positioned at the top-right corner of your website and ensure that all editing features work properly. Here’s the updated code:

🔹 Updated HTML (Place this inside <body>)
<button id="editToggle">🛠 Edit Mode</button>
<div id="adminPanel" style="display:none;">
    <h3>Customize Your Website</h3>
    
    <label>Change Background:</label>
    <input type="color" id="bgColorPicker">
    <button onclick="changeBackground()">Apply</button><br><br>

    <label>Add Product:</label>
    <input type="text" id="productName" placeholder="Product Name">
    <input type="text" id="productDetails" placeholder="Product Details">
    <button onclick="addProduct()">Add Product</button><br><br>

    <label>Edit Text:</label>
    <input type="text" id="editableText" placeholder="Enter new text">
    <button onclick="editContent()">Update Text</button>
</div>



🔹 Updated CSS (Place inside styles.css)
#editToggle {
    position: fixed;
    top: 10px;
    right: 10px;
    background: #007bff;
    color: white;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
    font-size: 16px;
    border-radius: 5px;
}

#adminPanel {
    position: fixed



