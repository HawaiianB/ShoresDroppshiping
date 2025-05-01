# ShoresDroppshiping
Dropshiping site
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dropship Gold</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #000;
      color: gold;
    }
    header, footer {
      background-color: #111;
      padding: 1em;
      text-align: center;
    }
    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: gold;
    }
    .container {
      padding: 2em;
    }
    .product {
      border: 1px solid gold;
      padding: 1em;
      margin-bottom: 1em;
    }
    .product img {
      max-width: 100%;
      height: auto;
      border: 1px solid gold;
      margin-bottom: 1em;
    }
    form input, form textarea, form button {
      display: block;
      width: 100%;
      margin-bottom: 1em;
    }
    .cart-item {
      border-bottom: 1px solid gold;
      padding: 0.5em 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>Dropship Gold</h1>
    <nav>
      <a href="#products">Products</a>
      <a href="#cart">Cart</a>
      <a href="#contact">Contact</a>
      <a href="#blog">Blog</a>
    </nav>
  </header>  <div class="container" id="products">
    <h2>Products</h2>
    <div class="product" data-name="Product 1" data-price="19.99">
      <img src="https://via.placeholder.com/300x200?text=Product+1" alt="Product 1">
      <h3>Product 1</h3>
      <p>Description of product 1</p>
      <button onclick="addToCart('Product 1', 19.99)">Add to Cart</button>
    </div>
    <div class="product" data-name="Product 2" data-price="29.99">
      <img src="https://via.placeholder.com/300x200?text=Product+2" alt="Product 2">
      <h3>Product 2</h3>
      <p>Description of product 2</p>
      <button onclick="addToCart('Product 2', 29.99)">Add to Cart</button>
    </div>
  </div>  <div class="container" id="cart">
    <h2>Shopping Cart</h2>
    <div id="cart-items">
      <p>Your cart is empty.</p>
    </div>
    <p><strong>Total: $<span id="cart-total">0.00</span></strong></p>
  </div>  <div class="container" id="contact">
    <h2>Contact Us</h2>
    <form onsubmit="event.preventDefault(); alert('Message sent!');">
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Your Email" required>
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
  </div>  <div class="container" id="blog">
    <h2>Blog</h2>
    <article>
      <h3>Welcome to Our Dropshipping Store</h3>
      <p>This is your first blog post. Share tips, updates, and more here!</p>
    </article>
  </div>  <footer>
    <p>&copy; 2025 Dropship Gold. All rights reserved.</p>
  </footer>  <script>
    let cart = [];

    function addToCart(name, price) {
      const item = cart.find(p => p.name === name);
      if (item) {
        item.quantity++;
      } else {
        cart.push({ name, price, quantity: 1 });
      }
      updateCart();
    }

    function updateCart() {
      const cartItems = document.getElementById('cart-items');
      cartItems.innerHTML = '';
      let total = 0;

      if (cart.length === 0) {
        cartItems.innerHTML = '<p>Your cart is empty.</p>';
      } else {
        cart.forEach(item => {
          const div = document.createElement('div');
          div.classList.add('cart-item');
          div.innerText = `${item.name} x ${item.quantity} - $${(item.price * item.quantity).toFixed(2)}`;
          cartItems.appendChild(div);
          total += item.price * item.quantity;
        });
      }

      document.getElementById('cart-total').innerText = total.toFixed(2);
    }
  </script></body>
</html>

<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dropship Gold</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #000;
      color: gold;
    }
    header, footer {
      background-color: #111;
      padding: 1em;
      text-align: center;
    }
    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: gold;
    }
    .container {
      padding: 2em;
    }
    .product {
      border: 1px solid gold;
      padding: 1em;
      margin-bottom: 1em;
    }
    .product img {
      max-width: 100%;
      height: auto;
      border: 1px solid gold;
      margin-bottom: 1em;
    }
    form input, form textarea, form button {
      display: block;
      width: 100%;
      margin-bottom: 1em;
    }
    .cart-item {
      border-bottom: 1px solid gold;
      padding: 0.5em 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>Dropship Gold</h1>
    <nav>
      <a href="#products">Products</a>
      <a href="#cart">Cart</a>
      <a href="#contact">Contact</a>
      <a href="#blog">Blog</a>
    </nav>
  </header>  <div class="container" id="products">
    <h2>Products</h2>
    <div class="product" data-name="Product 1" data-price="19.99">
      <img src="https://via.placeholder.com/300x200?text=Product+1" alt="Product 1">
      <h3>Product 1</h3>
      <p>Description of product 1</p>
      <button onclick="addToCart('Product 1', 19.99)">Add to Cart</button>
    </div>
    <div class="product" data-name="Product 2" data-price="29.99">
      <img src="https://via.placeholder.com/300x200?text=Product+2" alt="Product 2">
      <h3>Product 2</h3>
      <p>Description of product 2</p>
      <button onclick="addToCart('Product 2', 29.99)">Add to Cart</button>
    </div>
  </div>  <div class="container" id="cart">
    <h2>Shopping Cart</h2>
    <div id="cart-items">
      <p>Your cart is empty.</p>
    </div>
    <p><strong>Total: $<span id="cart-total">0.00</span></strong></p>
  </div>  <div class="container" id="contact">
    <h2>Contact Us</h2>
    <form onsubmit="event.preventDefault(); alert('Message sent!');">
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Your Email" required>
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
  </div>  <div class="container" id="blog">
    <h2>Blog</h2>
    <article>
      <h3>Welcome to Our Dropshipping Store</h3>
      <p>This is your first blog post. Share tips, updates, and more here!</p>
    </article>
  </div>  <footer>
    <p>&copy; 2025 Dropship Gold. All rights reserved.</p>
  </footer>  <script>
    let cart = [];

    function addToCart(name, price) {
      const item = cart.find(p => p.name === name);
      if (item) {
        item.quantity++;
      } else {
        cart.push({ name, price, quantity: 1 });
      }
      updateCart();
    }

    function updateCart() {
      const cartItems = document.getElementById('cart-items');
      cartItems.innerHTML = '';
      let total = 0;

      if (cart.length === 0) {
        cartItems.innerHTML = '<p>Your cart is empty.</p>';
      } else {
        cart.forEach(item => {
          const div = document.createElement('div');
          div.classList.add('cart-item');
          div.innerText = `${item.name} x ${item.quantity} - $${(item.price * item.quantity).toFixed(2)}`;
          cartItems.appendChild(div);
          total += item.price * item.quantity;
        });
      }

      document.getElementById('cart-total').innerText = total.toFixed(2);
    }
  </script></body>
</html>
