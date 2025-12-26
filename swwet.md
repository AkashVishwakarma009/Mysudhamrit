<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Sudhamrit</title>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet" />
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" rel="stylesheet" />
    <link href="/img/111.png" rel="icon">

    <style>
      /* General Styles */
      body {
          font-family: 'Poppins', sans-serif;
          margin: 0;
          padding: 0;
          background: #f6f6f6; /* Light gray background */
          color: #333;
      }
  
      /* Header Styles */
      header {
          background: linear-gradient(90deg, #f79d00, #fbcaff);
          box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
          padding: 10px 20px;
          position: sticky;
          top: 0;
          z-index: 1000;
      }
  
      .navbar {
          display: flex;
          justify-content: space-between;
          align-items: center;
          max-width: 1200px;
          margin: 0 auto;
          
          
      }
  
      .logo img {
          height: 50px;
          width: auto;
      }
  
      .nav-links {
          list-style: none;
          display: flex;
          gap: 20px;
          margin: 0;
          padding: 0;
      }
  
      .nav-links a {
          text-decoration: none;
          color: #333;
          font-size: 18px;
          font-weight: 500;
          transition: color 0.3s;
      }
  
      .nav-links a:hover {
          color: #ff6f61; /* Coral color for hover */
      }
  
      .menu-toggle {
          display: none;
          flex-direction: column;
          cursor: pointer;
      }
  
      .menu-toggle .bar {
          width: 25px;
          height: 3px;
          background: #333;
          margin: 4px 0;
          transition: all 0.3s;
      }
  
      /* Products Section */
      .products {
          padding: 60px 20px;
          background: linear-gradient(90deg,#ffe6b3, #fdeaff); /* White background for the products section */
      }
  
      .container {
          max-width: 1200px;
          margin: 0 auto;
      }
  
      .section-header {
          text-align: center;
          margin-bottom: 40px;
      }
  
      .section-header h2 {
          font-size: 36px;
          color: #333; /* Dark gray for headings */
          margin-bottom: 10px;
          font-weight: 600;
      }
  
      .section-header p {
          font-size: 18px;
          color: #666; /* Light gray for subtext */
      }
  
      /* Product Grid */
      .product-grid {
          display: grid;
          grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
          gap: 20px;
      }
  
      .product-box {
          background: #ffffff;
          border-radius: 10px;
          overflow: hidden;
          box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
          transition: transform 0.3s, box-shadow 0.3s;
      }
  
      .product-box:hover {
          transform: translateY(-10px);
          box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      }
  
      .product-card {
          padding: 20px;
          text-align: center;
      }
  
      .product-image img {
          width: 100%;
          height: 200px;
          object-fit: cover;
          border-radius: 10px;
          transition: transform 0.3s;
      }
  
      .product-box:hover .product-image img {
          transform: scale(1.05); /* Zoom effect on hover */
      }
  
      .product-info h3 {
          font-size: 22px;
          color: #333;
          margin: 15px 0 10px;
          font-weight: 600;
      }
  
      .product-info p {
          font-size: 16px;
          color: #666;
          margin: 0;
      }
  
      /* Add a gradient button effect */
      .product-box .btn {
          display: inline-block;
          margin-top: 15px;
          padding: 10px 20px;
          background: linear-gradient(45deg, #ff6f61, #ff9a9e); /* Gradient coral to pink */
          color: #fff;
          border-radius: 5px;
          text-decoration: none;
          font-weight: 500;
          transition: background 0.3s;
      }
  
      .product-box .btn:hover {
          background: linear-gradient(45deg, #ff9a9e, #ff6f61); /* Reverse gradient on hover */
      }
  
      /* Responsive Design */
      @media (max-width: 768px) {
          .nav-links {
              display: none;
              flex-direction: column;
              background: #fff;
              position: absolute;
              top: 70px;
              left: 0;
              width: 100%;
              box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
          }
  
          .nav-links.active {
              display: flex;
          }
  
          .menu-toggle {
              display: flex;
          }
      }
  
      /* Add a subtle animation to the header */
      @keyframes fadeInDown {
          from {
              opacity: 0;
              transform: translateY(-20px);
          }
          to {
              opacity: 1;
              transform: translateY(0);
          }
      }
  
      header {
          animation: fadeInDown 0.5s ease-out;
      }
  
      /* Add a gradient background to the section header */
      .section-header h2 {
          background: linear-gradient(45deg, #050505, #ff9a9e);
          -webkit-background-clip: text;
          -webkit-text-fill-color: transparent;
      }
  </style>
</head>
<body>
    <header>
        <nav class="navbar">
            <div class="logo">
                <img src="img/111.png" alt="Sudhamrit Logo" />
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="index.html"><strong> Home </strong></a></li>
            </ul>
            <div class="menu-toggle" id="menuToggle">
                <span class="bar"></span>
                <span class="bar"></span>
                <span class="bar"></span>
            </div>
        </nav>
    </header>

    <!-- Products Section -->
    <section id="products" class="products">
        <div class="container">
            <div class="section-header">
                <h2>Our Products</h2>
                <p>
                    Explore our delicious treats, handcrafted to perfection, and made
                    with the finest ingredients.
                </p>
            </div>
            <div id="productsContainer" class="product-grid">
                <!-- Static Products -->
                <div class="product-box">
                    <div class="product-card">
                        <div class="product-image">
                            <img src="img/product-01.jpg" alt="Rasgulla" />
                        </div>
                        <div class="product-info">
                            <h3>Ras Malai</h3>
                            <p>Soft, syrupy, and melt-in-your-mouth Indian delicacy.</p>
                        </div>
                    </div>
                </div>
                <div class="product-box">
                    <div class="product-card">
                        <div class="product-image">
                            <img src="img/product-02.jpg" alt="Gulab Jamun" />
                        </div>
                        <div class="product-info">
                            <h3>Kaju Katli</h3>
                            <p>Smooth, diamond-shaped cashew fudge infused with pure nuts.</p>
                        </div>
                    </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/product-03.jpg" alt="Barfi" />
                    </div>
                    <div class="product-info">
                      <h3>Kaju Barfi</h3>
                      <p>Luxuriously creamy cashew fudge with cardamom.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/product-04.jpg" alt="Jalebi" />
                    </div>
                    <div class="product-info">
                      <h3>Gulab jamun</h3>
                      <p>Soft milk-based dumplings in aromatic sugar syrup.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/product-05.jpg" alt="Ladoo" />
                    </div>
                    <div class="product-info">
                      <h3>Mysore Pak</h3>
                      <p>Rich sweet made with gram flour, ghee, and sugar.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/product-06.jpg" alt="Sandesh" />
                    </div>
                    <div class="product-info">
                      <h3>Besan Laddu</h3>
                      <p>Traditional sweet made from roasted gram flour and ghee.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/73 jALebi-2.jpg" alt="Jalebi" />
                    </div>
                    <div class="product-info">
                      <h3>Jalebi</h3>
                      <p>
                        Crispy, syrupy spirals with a perfect blend of sweet and tangy
                        flavors.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/76 rasgulla-3.jpg" alt="Rasgulla" />
                    </div>
                    <div class="product-info">
                      <h3>Rasgulla</h3>
                      <p>Soft, spongy cheese balls soaked in light sugar syrup.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img
                        src="img/112 motichoor ladoo-4.jpg"
                        alt="Motichoor Laddu"
                      />
                    </div>
                    <div class="product-info">
                      <h3>Motichoor Laddu</h3>
                      <p>
                        Tiny gram flour balls sweetened and combined into a delightful
                        sphere.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/93 malai ghevar-1.jpg" alt="Milk Cake" />
                    </div>
                    <div class="product-info">
                      <h3>Malai Ghevar</h3>
                      <p>Dense, rich milk-based sweet with a caramelized texture.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/120 paneer barfi-10.jpg" alt="Soan Papdi" />
                    </div>
                    <div class="product-info">
                      <h3>Paneer Barfi</h3>
                      <p>
                        Flaky, melt-in-mouth sweet made with gram flour and cardamom.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/118 kalakand-2 copy.jpg" alt="Kalakand" />
                    </div>
                    <div class="product-info">
                      <h3>Kalakand</h3>
                      <p>Grainy milk cake garnished with nuts and cardamom.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/71 kesar peda-3.jpg" alt="Kesar Peda" />
                    </div>
                    <div class="product-info">
                      <h3>Kesar Peda</h3>
                      <p>Saffron-flavored milk fudge with rich, creamy texture.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/85 dryfruit ladoo-2.jpg" alt="Badam Halwa" />
                    </div>
                    <div class="product-info">
                      <h3>Dry Fruit ladoos</h3>
                      <p>Rich dry fruits pudding made with pure ghee and cardamom.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/106 chocolate barfi-1.jpg" alt="Gajar Ka Halwa" />
                    </div>
                    <div class="product-info">
                      <h3>Coconut Barfi</h3>
                      <p>Traditional coconut pudding with nuts and cardamom.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/66 cham cham-2.jpg" alt="Malai Cham Cham" />
                    </div>
                    <div class="product-info">
                      <h3>Malai Cham Cham</h3>
                      <p>Cream-filled oval-shaped sweet topped with coconut.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/111 besan barfi-2.jpg" alt="Khoya Burfi" />
                    </div>
                    <div class="product-info">
                      <h3>Besan Burfi</h3>
                      <p>Dense milk fudge squares with cardamom flavor.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img
                        src="img/107 chocolate kaju katli-1.jpg"
                        alt="Pista Roll"
                      />
                    </div>
                    <div class="product-info">
                      <h3>Chocolate KajuKatali</h3>
                      <p>
                        Chocolate kajukatli is a delicious fusion of traditional
                        kajukatli and rich chocolate, sweet, nutty flavor of cashews
                        with the indulgence of cocoa.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/148 anjeer barfi-3.jpg" alt="Anjeer Barfi" />
                    </div>
                    <div class="product-info">
                      <h3>Anjeer Barfi</h3>
                      <p>Fig and milk fudge with chopped nuts.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/177 pal payasam-2.jpg" alt="Kaju Roll" />
                    </div>
                    <div class="product-info">
                      <h3>Payasam</h3>
                      <p>
                        Pal Payasam is a creamy, sweet South Indian rice pudding made
                        with milk, sugar, and flavored with cardamom, offering a
                        comforting and rich dessert experience. .
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/134 mango cupcake-2.jpg" alt="Mango Barfi" />
                    </div>
                    <div class="product-info">
                      <h3>Mango cupcake</h3>
                      <p>Mango-flavored milk fudge with real fruit pulp.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/83 coconut barfi-3.jpg" alt="Coconut Laddu" />
                    </div>
                    <div class="product-info">
                      <h3>Coconut Laddu</h3>
                      <p>Sweet spheres made with fresh coconut and condensed milk.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/85 dryfruit ladoo-2.jpg" alt="Dry Fruit Laddu" />
                    </div>
                    <div class="product-info">
                      <h3>Dry Fruit Laddu</h3>
                      <p>Mixed nuts and dried fruits formed into sweet balls.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img
                        src="img/108 kesar kaju katli-2.jpg"
                        alt="Kesar Rasmalai"
                      />
                    </div>
                    <div class="product-info">
                      <h3>Kesar kajukatli</h3>
                      <p>Saffron-flavored kajukatli in creamy milk.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/200 imarti.jpg" alt="Malai Peda" />
                    </div>
                    <div class="product-info">
                      <h3>imarti</h3>
                      <p>Cream-based sweet discs with cardamom flavor.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/116 darbari khaaja-5.jpg" alt="Rose Sandesh" />
                    </div>
                    <div class="product-info">
                      <h3>Darbari Khaja</h3>
                      <p>Crispy-flavored khaja sweet with pistachios.</p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/97 swiss albania -1.jpg" alt="Badam Pista Roll" />
                    </div>
                    <div class="product-info">
                      <h3>awiss albania</h3>
                      <p>
                        Swiss Albania refers to the unique blend of Swiss and Albanian
                        cultures, often highlighting the picturesque landscapes and
                        strong traditions that unite both countries. .
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img
                        src="img/82 peanut date delight.jpg"
                        alt="Chocolate Barfi"
                      />
                    </div>
                    <div class="product-info">
                      <h3>peanut date delight</h3>
                      <p>
                        Makevit is a versatile, nutritious food supplement made from
                        wheat flour, often used to boost energy and provide essential
                        vitamins and minerals. .
                      </p>
                    </div>
                    nuts
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/122 kaju nankhatai-6.jpg" alt="Malai Sandwich" />
                    </div>
                    <div class="product-info">
                      <h3>Kaju Nnakhatai</h3>
                      <p>
                        Kaju Nanakhatai is a rich, buttery Indian shortbread cookie
                        made with cashew nuts, ghee, and flour, offering a delightful
                        melt-in-your-mouth texture. .
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/140 aSassorted cupcakes-6.jpg" alt="Paan Laddu" />
                    </div>
                    <div class="product-info">
                      <h3>assorted cupcake</h3>
                      <p>
                        Cupcakes are individual, miniature cakes often topped with
                        frosting and sprinkles, offering a sweet, customizable treat
                        perfect for any occasion.
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/147 kheer kadam-4.jpg" alt="Kesar Angoori" />
                    </div>
                    <div class="product-info">
                      <h3>Kher kadam</h3>
                      <p>
                        Kheer Kadam is a popular Bengali sweet made of milk-based
                        khoya (mawa) filled with rasgulla, offering a delightful
                        combination of creamy and spongy textures..
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/92 pineapple patrani-5.jpg" alt="Malai Ghevar" />
                    </div>
                    <div class="product-info">
                      <h3>pineapple patrani</h3>
                      <p>
                        It is a flavorful dish where pineapple slices are marinated
                        with a mix of spices and herbs, then wrapped in banana leaves
                        and steamed to create a fragrant, tangy, and tropical treat. .
                      </p>
                    </div>
                  </div>
                </div>
                <div class="product-box">
                  <div class="product-card">
                    <div class="product-image">
                      <img src="img/77 rajwadi peda-3.jpg" alt="Malai Ghevar" />
                    </div>
                    <div class="product-info">
                      <h3>rajwadi peda</h3>
                      <p>
                        Rajwadi Peda is a rich, indulgent Indian sweet made from
                        condensed milk, sugar, and ghee, often garnished with nuts and
                        flavored with cardamom, offering a royal, melt-in-your-mouth
                        experience. .
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
    </section>

    <div class="footer-bottom" style="background-color:linear-gradient(45deg, #ffe259, #ffa751); padding: 20px; text-align: center;">
      <p>&copy; 2024 Sudhamrit. Crafted with ❤️. All Rights Reserved.</p>
  </div>

    <script>
        // Load products from localStorage and display them
        function loadProducts() {
            const products = JSON.parse(localStorage.getItem("products")) || [];
            const productsContainer = document.getElementById("productsContainer");

            if (products.length === 0) {
                productsContainer.innerHTML += "<p>....</p>";
                return;
            }

            // Loop through each product and create a card
            products.forEach(product => {
                const productCard = `
                    <div class="product-box">
                        <div class="product-card">
                            <div class="product-image">
                                <img src="${product.image}" alt="${product.name}" onerror="this.src='https://via.placeholder.com/150';">
                            </div>
                            <div class="product-info">
                                <h3>${product.name}</h3>
                                <p>${product.description}</p>
                            </div>
                        </div>
                    </div>
                `;
                productsContainer.insertAdjacentHTML("beforeend", productCard);
            });
        }

        // Load products on page load
        window.onload = loadProducts;

        // Toggle mobile menu
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            menuToggle.classList.toggle('active');
        });
    </script>
</body>
</html>