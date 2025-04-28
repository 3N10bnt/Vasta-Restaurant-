<!DOCTYPE html>
<html lang="en">

<head>
  <title>VASTA Restaurant | Elegant Filipino Menu</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    /* General Styles */
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f8f8f8;
      color: #333;
      line-height: 1.6;
    }

    h1,
    h2,
    h3 {
      color: #2c3e50;
      font-weight: 600;
      margin-top: 1rem;
      margin-bottom: 0.5rem;
      line-height: 1.2;
    }

    a {
      color: #e74c3c;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    a:hover {
      color: #c0392b;
    }

    /* Header Styles */
    header {
      background-color: #fff;
      color: #2c3e50;
      padding: 2rem 0;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    header h1 {
      font-size: 2.5rem;
      margin-bottom: 0.5rem;
    }

    header p {
      font-size: 1.2rem;
      color: #777;
    }

    /* Navigation Styles */
    nav {
      background-color: #2c3e50;
      color: #fff;
      padding: 1rem 0;
      text-align: center;
    }

    nav a {
      color: #fff;
      padding: 0.75rem 1.5rem;
      display: inline-block;
      transition: background-color 0.3s ease;
    }

    nav a:hover {
      background-color: #34495e;
    }

    /* Content Styles */
    .content {
      padding: 2rem;
      max-width: 1200px;
      margin: 2rem auto;
      background-color: #fff;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
      border-radius: 8px;
      display: none; /* Hidden by default, shown by Javascript */
    }

    .content h2 {
      font-size: 2rem;
      margin-bottom: 1.5rem;
      color: #e74c3c;
      border-bottom: 2px solid #e74c3c;
      padding-bottom: 0.5rem;
    }

    .content p {
      font-size: 1.1rem;
      color: #555;
    }

    /* Menu Styles */
    section {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }

    table {
      background-color: #f9f9f9;
      border-radius: 8px;
      box-shadow: 0 1px 5px rgba(0, 0, 0, 0.1);
      padding: 1.5rem;
      transition: transform 0.3s ease;
    }

    table:hover {
      transform: translateY(-5px);
    }

    table img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 8px;
      margin-bottom: 1rem;
    }

    table h2 {
      font-size: 1.5rem;
      margin-bottom: 0.75rem;
      color: #34495e;
    }

    table h1 {
      font-size: 1.3rem;
      margin-bottom: 0.5rem;
      color: #e74c3c;
    }

    table h3 {
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
      color: #777;
    }

    table h5 {
      font-size: 1rem;
      color: #555;
      line-height: 1.4;
    }

    table button {
      background-color: #e74c3c;
      color: #fff;
      padding: 0.75rem 1.25rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      font-size: 1rem;
    }

    table button:hover {
      background-color: #c0392b;
    }

    /* Cart Styles */
    #cart-items {
      margin-bottom: 1rem;
    }

    #cart-total h3 {
      font-size: 1.4rem;
      color: #2c3e50;
    }

    /* Contact Styles */
    .contact-info {
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
    }

    .contact-info p {
      font-size: 1.1rem;
      color: #555;
    }

    /* Footer Styles */
    footer {
      background-color: #34495e;
      color: #fff;
      text-align: center;
      padding: 1rem 0;
      position: relative;
      width: 100%;
      bottom: 0;
    }

    /* Utility Classes */
    .text-center {
      text-align: center;
    }

    .hidden {
      display: none;
    }

    .active {
      display: block;
    }

    /* Order Confirmation Styles */
    #order-confirmation {
      display: none;
    }

    #order-confirmation h2 {
      color: #2c3e50;
    }

    #order-summary {
      margin-bottom: 1rem;
    }

    #order-summary p {
      font-size: 1.1rem;
      color: #555;
    }

    #customer-info-form label {
      display: block;
      margin-top: 0.5rem;
      font-weight: 500;
    }

    #customer-info-form input,
    #customer-info-form select {
      width: 100%;
      padding: 0.75rem;
      margin-top: 0.25rem;
      border: 1px solid #ddd;
      border-radius: 5px;
      font-size: 1rem;
    }

    #customer-info-form button {
      background-color: #e74c3c;
      color: #fff;
      padding: 0.75rem 1.25rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      font-size: 1rem;
      margin-top: 1rem;
    }

    #customer-info-form button:hover {
      background-color: #c0392b;
    }

    /* Receipt Styles */
    #receipt {
      display: none;
    }

    #receipt h2 {
      color: #2c3e50;
    }

    #receipt-details {
      margin-bottom: 1rem;
    }

    #receipt-details p {
      font-size: 1.1rem;
      color: #555;
    }

    /* Verification Styles */
    #verification-code-form {
      display: none;
    }
  </style>
</head>

<body>
  <header>
    <h1>VASTA RESTAURANT</h1>
    <p>Elegant Filipino Dining</p>
  </header>

  <nav>
    <a href="#home" onclick="showPage('home')">Home</a>
    <a href="#menu" onclick="showPage('menu')">Menu</a>
    <a href="#about" onclick="showPage('about')">About</a>
    <a href="#contact" onclick="showPage('contact')">Contact</a>
    <a href="#cart" onclick="showPage('cart')">Cart</a>
  </nav>

  <div class="content" id="home">
    <h2>Welcome to VASTA Restaurant!</h2>
    <p>Experience the heart of Filipino cuisine in an elegant and inviting atmosphere. We are dedicated to providing you with exceptional service and dishes that capture the true essence of Filipino flavors.</p>
  </div>

  <div class="content" id="menu">
    <section>
      <table>
        <tr>
          <td>
            <h2>Chicken Dishes</h2>
            <img src="https://www.eatwithcarmen.com/wp-content/uploads/2022/09/chicken-adobo_.jpg" alt="Adobo">
            <h1>Adobo</h1>
            <h3>About Adobo:</h3>
            <h5>Adobo is a dish that is usually made with meat (chicken, pork, or beef) marinated in vinegar, soy sauce, garlic, and other spices. The meat is slowly cooked until it becomes tender and flavorful. Adobo is often served with rice and is a staple dish in many Filipino households.</h5>
            <button onclick="addToCart('Adobo', 150)">Php 150 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Chicken Dishes</h2>
            <img src="https://www.allrecipes.com/thmb/WSSoRAz2IygrMPkiJxHPbt9gqMg=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/8635-southern-fried-chicken-ddmfs_4x3-90736ab31a7a4bb59eb04e2380ccebe7.jpg" alt="Fried Chicken">
            <h1>Fried Chicken</h1>
            <h3>About Fried Chicken:</h3>
            <h5>Fried chicken is a dish consisting of chicken pieces that have been coated with seasoned flour or batter and pan-fried, deep fried, pressure fried, or air fried. The breading adds a crisp coating or crust to the exterior of the chicken while retaining juices in the meat.</h5>
            <button onclick="addToCart('Fried Chicken', 120)">Php 120 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Chicken Dishes</h2>
            <img src="https://travellingfoodie.net/wp-content/uploads/2022/03/Exotic-Filipino-Food-Bizarre-Food-Philippines-Travelling-Foodie-8-1024x683.jpg.webp" alt="Isaw">
            <h1>Isaw</h1>
            <h3>About Isaw:</h3>
            <h5>Isaw is a street food made from barbecued pig or chicken intestines. It is a type of inihaw. The intestines are cleaned several times and are then either boiled, then grilled on sticks. For presentability, the intestines are usually applied with orange food coloring.</h5>
            <button onclick="addToCart('Isaw', 180)">Php 180 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Chicken Dishes</h2>
            <img src="https://assets.unileversolutions.com/recipes-v2/110276.jpg" alt="Tinola">
            <h1>Tinola</h1>
            <h3>About Tinola:</h3>
            <h5>Tinolang manok is a Filipino chicken soup. It can consist of various chicken cuts and internal organs cooked in a flavorful broth alongside green papaya and chili pepper or malunggay leaves. The broth is usually generously seasoned with ginger, garlic, and fish sauce, and the soup is often served over plain white rice.</h5>
            <button onclick="addToCart('Tinola', 160)">Php 160 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Pork Dishes</h2>
            <img src="https://panlasangpinoy.com/wp-content/uploads/2021/08/Killer-Pork-Sinigang-jpg.webp?fbclid=IwAR0Q1gApG_7o1GLTr6S0AkKGmuw4xuNM-gx7D7vQthsX5MPw11Sx9mXNAy0" alt="Sinigang">
            <h1>Sinigang</h1>
            <h3>About Sinigang:</h3>
            <h5>Sinigang is a Filipino soup or stew characterized by its sour and savory taste. It is most often associated with tamarind (Filipino: sampalok), although it can use other sour fruits and leaves as the souring agent. It is one of the more popular dishes in Filipino cuisine. The soup is usually accompanied by rice.</h5>
            <button onclick="addToCart('Sinigang', 140)">Php 140 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Pork Dishes</h2>
            <img src="https://assets.unileversolutions.com/v1/85775930.jpg" alt="Kare-kare">
            <h1>Kare-kare</h1>
            <h3>About Kare-Kare:</h3>
            <h5>Kare-kare is a stew (kare derives from "curry") that features a thick savory peanut sauce. It is generally made from a base of stewed oxtail, beef tripe, pork hocks, calves' feet, pig's feet or trotters, various cuts of pork, beef stew meat, and occasionally offal.</h5>
            <button onclick="addToCart('Kare-kare', 200)">Php 200 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Pork Dishes</h2>
            <img src="https://i0.wp.com/www.angsarap.net/wp-content/uploads/2017/02/Pinakbet-Wide.jpg?fit=1080%2C720&ssl=1" alt="Pinakbet">
            <h1>Pinakbet</h1>
            <h3>About Pinakbet:</h3>
            <h5>Pinakbet (also called pakbet) is an indigenous Filipino dish from the northern regions of the Philippines. Pinakbet is made with a variety of mixed vegetables flavored with bagoóng. The word is the contracted from the Ilokano word pinakebbet, meaning "shrunk" or "shriveled."</h5>
            <button onclick="addToCart('Pinakbet', 180)">Php 180 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Pork Dishes</h2>
            <img src="https://th.bing.com/th/id/OIP.YqNdU65X0vEdL4G7Wk6NaQHaFj?w=230&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7.jpg" alt="Lechon kawali">
            <h1>Lechon kawali</h1>
            <h3>About Lechon Kawali:</h3>
            <h5>Lechon kawali, also known as lechon de carajay or litsong kawali in Tagalog, is a Filipino recipe consisting of pork belly slabs deep-fried in a pan or wok (kawali). It is seasoned beforehand, cooked then served in cubes.</h5>
            <button onclick="addToCart('Lechon kawali', 250)">Php 250 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Beef Dishes</h2>
            <img src="https://www.thespruceeats.com/thmb/BJnw-h62SdxnpnI4ynYSrHVSpxI=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/garlicky-filipino-bistek-3030379-hero-01-f916301cac884a309b4ead5ed8bee443.jpg" alt="Bistek">
            <h1>Bistek</h1>
            <h3>About Bistek:</h3>
            <h5>Bistek also known as bistek tagalog or karne frita, is a Filipino dish consisting of thinly-sliced beefsteak braised in soy sauce, calamansi juice, garlic, ground black pepper, and onions cut into rings.</h5>
            <button onclick="addToCart('Bistek', 190)">Php 190 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Beef Dishes</h2>
            <img src="https://pilipinasrecipes.com/wp-content/uploads/2017/05/Pork-Afridata-Recipe.jpg" alt="Balbacua">
            <h1>Balbacua</h1>
            <h3>About Balbacua:</h3>
            <h5>Balbacua is a Filipino beef stew made from beef, collagen-rich beef parts (oxtail, skin, and joints), and various spices cooked for several hours until very tender.</h5>
            <button onclick="addToCart('Balbacua', 210)">Php 210 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Beef Dishes</h2>
            <img src="https://panlasangpinoy.com/wp-content/uploads/2019/03/Beef-Kaldereta.jpg" alt="Kaldireta">
            <h1>Kaldireta</h1>
            <h3>About Kaldireta:</h3>
            <h5>Kaldereta or caldereta is a goat meat stew from the Philippines. Variations of the dish use (beef, chicken, or pork.)Commonly, the goat meat is stewed with vegetables and liver paste. Vegetables may include tomatoes, potatoes, olives, bell peppers, and hot peppers.</h5>
            <button onclick="addToCart('Kaldireta', 200)">Php 200 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Beef Dishes</h2>
            <img src="https://www.pinoyrecipe.net/wp-content/uploads/2021/03/Chicken-Afritada.jpg" alt="Afritada">
            <h1>Afritada</h1>
            <h3>About Afritada:</h3>
            <h5>Afritada is a Philippine dish consisting of chicken, beef, or pork braised in tomato sauce with carrots, potatoes, and red and green bell peppers.</h5>
            <button onclick="addToCart('Afritada', 180)">Php 180 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Cold Drinks</h2>
            <img src="https://www.encopadebalon.com/3493-large_default/coca-cola-pack-24-cans-33-cl.jpg" alt="Cola">
            <h1>Cola</h1>
            <button onclick="addToCart('Cola', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Cold Drinks</h2>
            <img src="https://media.pickaroo.com/media/thumb/variant_photos/2022/5/17/PaHzqjhAMKm6WcCwjDZ6Hi_watermark_400.jpg" alt="7 Up">
            <h1>7 Up</h1>
            <button onclick="addToCart('7 Up', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Cold Drinks</h2>
            <img src="https://ucccafe.mugengroup.ph/wp-content/uploads/sites/4/2023/09/SPRITE-min.jpg" alt="Sprite">
            <h1>Sprite</h1>
            <button onclick="addToCart('Sprite', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Cold Drinks</h2>
            <img src="https://amici.ph/cdn/shop/products/mug-rootbeer-can_1200x.jpg?v=1518899304" alt="Root Beer">
            <h1>Root Beer</h1>
            <button onclick="addToCart('Root Beer', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Cold Drinks</h2>
            <img src="https://frostingandfettuccine.com/wp-content/uploads/2022/12/Caramel-Iced-Coffee-6.jpg" alt="Ice Coffee">
            <h1>Ice Coffee</h1>
            <button onclick="addToCart('Ice Coffee', 70)">Php 70 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Cold Drinks</h2>
            <img src="https://www.alphafoodie.com/wp-content/uploads/2020/11/Orange-Juice-1-of-1.jpeg" alt="Juice">
            <h1>Juice</h1>
            <button onclick="addToCart('Juice', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Hot Drinks</h2>
            <img src="https://thehealthytart.com/wp-content/uploads/2017/03/Ginger-and-Lemon-tea.jpg" alt="Malunggay Tea">
            <h1>Malunggay Tea</h1>
            <button onclick="addToCart('Malunggay Tea', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Hot Drinks</h2>
            <img src="https://thehealthytart.com/wp-content/uploads/2017/03/Ginger-and-Lemon-tea.jpg" alt="Ginger Tea">
            <h1>Ginger Tea</h1>
            <button onclick="addToCart('Ginger Tea', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Hot Drinks</h2>
            <img src="https://img.jakpost.net/c/2023/09/12/2023_09_12_142304_1694508173._large.jpg" alt="Blue Ternatea Tea">
            <h1>Blue Ternatea Tea</h1>
            <button onclick="addToCart('Blue Ternatea Tea', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>

      <table>
        <tr>
          <td>
            <h2>Hot Drinks</h2>
            <img src="https://i.pinimg.com/564x/f5/6d/19/f56d19b0a266c645ffceb6c6588b5a85.jpg" alt="Kalamansi Tea">
            <h1>Kalamansi Tea</h1>
            <button onclick="addToCart('Kalamansi Tea', 35)">Php 35 Add to Cart</button>
          </td>
        </tr>
      </table>
    </section>
  </div>

  <div class="content" id="cart">
    <h2>Your Cart</h2>
    <div id="cart-items">
    </div>
    <div id="cart-total">
      <h3>Total: <span id="total-amount">Php 0</span></h3>
    </div>
    <button onclick="showOrderConfirmation()">Checkout</button>
  </div>

  <div class="content" id="about">
    <h2>About VASTA Restaurant</h2>
    <p>We are passionate about serving delicious, high-quality meals in a welcoming and comfortable atmosphere. Our menu is carefully crafted to offer a variety of dishes that cater to different tastes and dietary preferences.</p>
    <p>We invite you to come and experience the best of Filipino cuisine with us!</p>
  </div>

  <div class="content" id="contact">
    <h2>Contact Us</h2>
    <div class="contact-info">
      <p>Address: One Victoria Plaza 3rd Floor, A. Mabini St. Brgy. Kapasigan, Pasig City 1630 Pasig, Philippines</p>
      <p>Phone: (63+) 994 752 2520</p>
      <p>Email: info@vastarestaurant.com</p>
    </div>
  </div>

  <!-- Order Confirmation Section -->
  <div class="content" id="order-confirmation">
    <h2>Confirm Your Order</h2>
    <div id="order-summary">
      <!-- Order items will be listed here -->
    </div>
    <h3>Total: <span id="confirmation-total">Php 0</span></h3>
    <button onclick="editCart()">Edit Cart</button>
    <button onclick="showCustomerInfoForm()">Confirm Order</button>
  </div>

  <!-- Customer Information Form -->
  <div class="content" id="customer-info">
    <h2>Customer Information</h2>
    <form id="customer-info-form">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required>

      <label for="contact">Contact Number:</label>
      <input type="tel" id="contact" name="contact" required>

      <label for="address">Address:</label>
      <input type="text" id="address" name="address" required>

      <label for="payment-method">Payment Method:</label>
      <select id="payment-method" name="payment-method" required>
        <option value="">Select Payment Method</option>
        <option value="cash">Cash on Delivery</option>
        <option value="gcash">GCash</option>
      </select>

      <button type="button" onclick="verifyContact()">Submit Order</button>
    </form>
  </div>

  <!-- Verification Code Form -->
  <div class="content" id="verification-code-form">
    <h2>Verify Your Contact Number</h2>
    <p>A verification code has been sent to your contact number. Please enter it below.</p>
    <label for="verification-code">Verification Code:</label>
    <input type="text" id="verification-code" name="verification-code" required>
    <button type="button" onclick="submitOrder()">Verify</button>
  </div>

  <!-- Receipt Section -->
  <div class="content" id="receipt">
    <h2>Thank You for Your Order!</h2>
    <div id="receipt-details">
      <!-- Receipt details will be populated here -->
    </div>
  </div>

  <footer>
    <p>&copy; 2023 VASTA Restaurant</p>
  </footer>

  <script>
    let cart = {};
    let verificationCode = '';

    // Function to generate a random verification code
    function generateVerificationCode() {
      return Math.floor(100000 + Math.random() * 900000).toString();
    }

    // Initially show the home page
    showPage('home');

    function addToCart(itemName, price) {
      if (cart[itemName]) {
        cart[itemName].quantity += 1;
      } else {
        cart[itemName] = {
          price: price,
          quantity: 1
        };
      }
      updateCartDisplay();
    }

    function updateCartDisplay() {
      const cartItemsDiv = document.getElementById('cart-items');
      const totalAmountSpan = document.getElementById('total-amount');
      let cartItemsHTML = '';
      let total = 0;

      for (const itemName in cart) {
        const item = cart[itemName];
        const itemTotal = item.price * item.quantity;
        cartItemsHTML += `<p>${itemName} - Php ${item.price} x ${item.quantity} = Php ${itemTotal} </p>`;
        total += itemTotal;
      }

      cartItemsDiv.innerHTML = cartItemsHTML;
      totalAmountSpan.innerText = 'Php ' + total;
    }

    function showOrderConfirmation() {
      // Populate order summary
      const orderSummaryDiv = document.getElementById('order-summary');
      const confirmationTotalSpan = document.getElementById('confirmation-total');
      let orderSummaryHTML = '';
      let total = 0;

      for (const itemName in cart) {
        const item = cart[itemName];
        const itemTotal = item.price * item.quantity;
        orderSummaryHTML += `<p>${itemName} - Php ${item.price} x ${item.quantity} = Php ${itemTotal} </p>`;
        total += itemTotal;
      }

      orderSummaryDiv.innerHTML = orderSummaryHTML;
      confirmationTotalSpan.innerText = 'Php ' + total;

      // Show order confirmation and hide other sections
      showPage('order-confirmation');
    }

    function editCart() {
      // Go back to the cart page
      showPage('cart');
    }

    function showCustomerInfoForm() {
      // Show customer info form and hide other sections
      showPage('customer-info');
    }

    function verifyContact() {
      const contact = document.getElementById('contact').value;

      // Generate a verification code
      verificationCode = generateVerificationCode();

      // Simulate sending a text message (replace with actual SMS API call)
      alert(`Sending verification code: ${verificationCode} to ${contact}`);

      // Show the verification code form
      showPage('verification-code-form');
    }

    function submitOrder() {
      const enteredCode = document.getElementById('verification-code').value;

      if (enteredCode === verificationCode) {
        // Collect customer information
        const name = document.getElementById('name').value;
        const contact = document.getElementById('contact').value;
        const address = document.getElementById('address').value;
        const paymentMethod = document.getElementById('payment-method').value;

        // Prepare receipt details
        let receiptDetailsHTML = `
              <p><strong>Name:</strong> ${name}</p>
              <p><strong>Contact Number:</strong> ${contact}</p>
              <p><strong>Address:</strong> ${address}</p>
              <p><strong>Payment Method:</strong> ${paymentMethod}</p>
              <h3>Order Summary:</h3>
          `;

        let total = 0;
        for (const itemName in cart) {
          const item = cart[itemName];
          const itemTotal = item.price * item.quantity;
          receiptDetailsHTML += `<p>${itemName} - Php ${item.price} x ${item.quantity} = Php ${itemTotal} </p>`;
          total += itemTotal;
        }

        receiptDetailsHTML += `<h3>Total: Php ${total}</h3>`;

        // Populate receipt
        const receiptDetailsDiv = document.getElementById('receipt-details');
        receiptDetailsDiv.innerHTML = receiptDetailsHTML;

        // Show receipt and hide other sections
        showPage('receipt');

        // Clear the cart
        cart = {};
        updateCartDisplay();
      } else {
        alert('Verification code is incorrect. Please try again.');
      }
    }

    function sendOrderToRestaurant(orderDetails) {
      // Replace with your actual endpoint
      const restaurantEndpoint = 'https://example.com/restaurant/orders';

      // Use fetch API to send data to the restaurant
      fetch(restaurantEndpoint, {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json',
          },
          body: JSON.stringify(orderDetails),
        })
        .then(response => {
          if (response.ok) {
            alert('Thank you for your order! The restaurant has been notified.');
          } else {
            alert('There was an error processing your order. Please try again.');
          }
        })
        .catch(error => {
          console.error('Error:', error);
          alert('There was an error processing your order. Please try again.');
        });
    }

    function showPage(pageId) {
      // Hide all content divs
      const contentDivs = document.querySelectorAll('.content');
      contentDivs.forEach(div => div.style.display = 'none');

      // Show the selected content div
      const selectedDiv = document.getElementById(pageId);
      if (selectedDiv) {
        selectedDiv.style.display = 'block';
      }

      if (pageId === 'cart') {
        updateCartDisplay();
      }

       // Show the home page by default
      if (pageId === 'home') {
      selectedDiv.style.display = 'block';
        }
    }

  // Show the home page on initial load
  showPage('home');
  </script>

</body>

</html>
