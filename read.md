<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sudhamrit</title>
    <!-- Google Font for modern typography -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
    <link href="/img/111.png" rel="icon">

    
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: #f0f2f5;
        }
        .header {
            background: linear-gradient(135deg, #1a237e, #0d47a1);
            padding: 25px;
            color: white;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }
        .header h2 {
            margin: 0;
            font-size: 32px;
            font-weight: 600;
            letter-spacing: 0.5px;
        }
        .header button {
            background: rgba(255, 255, 255, 0.1);
            color: white;
            padding: 12px 24px;
            font-size: 16px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 15px;
        }
        .header button:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }
        .container {
            display: flex;
            flex-direction: column;
            padding: 30px;
            gap: 25px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .button-container {
            width: 100%;
            display: flex;
            gap: 20px;
            justify-content: flex-start;
            align-items: center;
        }
        .button {
            padding: 12px 24px;
            width: 220px;
            height: 45px;
            background: linear-gradient(135deg, #6366f1, #4f46e5);
            color: white;
            border: none;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(99, 102, 241, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        .button:before {
            content: '+';
            font-size: 20px;
            font-weight: 400;
        }
        .button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(99, 102, 241, 0.4);
            background: linear-gradient(135deg, #4f46e5, #4338ca);
        }
        .button:active {
            transform: translateY(-1px);
            box-shadow: 0 4px 15px rgba(99, 102, 241, 0.2);
        }
        .product-card {
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: auto;
            max-width: 100%;
            text-align: center;
            transition: all 0.3s ease;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.15);
        }
        .product-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .product-card h4 {
            font-size: 18px;
            color: #1a237e;
            margin: 10px 0;
            font-weight: 600;
        }
        .product-card p {
            font-size: 14px;
            color: #546e7a;
            line-height: 1.6;
            margin: 0 0 15px 0;
            flex-grow: 1;
        }
        .product-card button {
            background: linear-gradient(135deg, #d32f2f, #f44336);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            width: 100%;
            margin-top: auto;
        }
        .product-card button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(244, 67, 54, 0.3);
        }
        .modal {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 35px;
            border-radius: 16px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            width: 450px;
            z-index: 999;
        }
        .modal::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            z-index: -1;
        }
        .modal h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: #1a237e;
            font-weight: 600;
        }
        .modal input {
            width: 100%;
            padding: 12px;
            margin: 8px 0 20px;
            font-size: 16px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            transition: border-color 0.3s ease;
        }
        .modal input:focus {
            border-color: #1a237e;
            outline: none;
        }
        .modal button {
            width: 100%;
            padding: 12px;
            margin: 8px 0;
            font-size: 16px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        .modal button[type="submit"] {
            background: linear-gradient(135deg, #1a237e, #0d47a1);
            color: white;
            border: none;
        }
        .modal button[type="submit"]:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(26, 35, 126, 0.3);
        }
        .modal button[type="button"] {
            background: #f5f5f5;
            color: #333;
            border: 1px solid #ddd;
        }
        .modal button[type="button"]:hover {
            background: #eeeeee;
        }
        #productList {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
            padding: 20px 0;
            width: 100%;
        }
        .home-button {
            padding: 12px 24px;
            width: 140px;
            height: 45px;
            background: linear-gradient(135deg, #2dd4bf, #0d9488);
            color: white;
            border: none;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(45, 212, 191, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            text-decoration: none;
        }
        .home-button:before {
            content: '🏠';
            font-size: 18px;
        }
        .home-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(45, 212, 191, 0.4);
            background: linear-gradient(135deg, #0d9488, #0f766e);
        }
        #addOfferBtn:before {
            content: '🏷️';
            font-size: 18px;
        }
        
        #addOfferBtn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(245, 158, 11, 0.4);
            background: linear-gradient(135deg, #d97706, #b45309);
        }
        
        .modal input[type="number"],
        .modal input[type="date"] {
            width: 100%;
            padding: 12px;
            margin: 8px 0 20px;
            font-size: 16px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            transition: border-color 0.3s ease;
        }
        
        .modal input[type="number"]:focus,
        .modal input[type="date"]:focus {
            border-color: #1a237e;
            outline: none;
        }
        .section-title {
            margin-top: 40px;
            color: #1a237e;
            font-size: 24px;
            font-weight: 600;
        }
        
        .offers-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .offer-card {
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .offer-card h4 {
            color: #1a237e;
            margin: 0;
            font-size: 18px;
        }
        
        .offer-discount {
            font-size: 24px;
            color: #f59e0b;
            font-weight: bold;
        }
        
        .offer-expiry {
            color: #64748b;
            font-size: 14px;
            display: flex;
            flex-direction: column;
            gap: 4px;
        }
        
        .offer-expiry-date, .offer-expiry-time {
            display: inline-block;
        }
        
        .offer-card button {
            background: linear-gradient(135deg, #ef4444, #dc2626);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .offer-card button:hover {
            background: linear-gradient(135deg, #dc2626, #b91c1c);
        }

        .offer-actions {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }

        .edit-btn {
            background: linear-gradient(135deg, #3b82f6, #2563eb) !important;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
        }

        .delete-btn {
            background: linear-gradient(135deg, #ef4444, #dc2626) !important;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
        }

        .edit-btn:hover {
            background: linear-gradient(135deg, #2563eb, #1d4ed8) !important;
            transform: translateY(-2px);
        }

        .delete-btn:hover {
            background: linear-gradient(135deg, #dc2626, #b91c1c) !important;
            transform: translateY(-2px);
        }

        .offer-card {
            position: relative;
            padding-bottom: 60px;
        }

        .offer-actions {
            position: absolute;
            bottom: 20px;
            left: 20px;
            right: 20px;
        }

        /* Add styles for time input */
        .modal input[type="time"] {
            width: 100%;
            padding: 12px;
            margin: 8px 0 20px;
            font-size: 16px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            transition: border-color 0.3s ease;
        }
        
        .modal input[type="time"]:focus {
            border-color: #1a237e;
            outline: none;
        }
        
        .offer-expiry {
            color: #64748b;
            font-size: 14px;
            display: flex;
            flex-direction: column;
            gap: 4px;
        }
        
        .offer-expiry-date, .offer-expiry-time {
            display: inline-block;
        }

        /* Add styles for expired offers */
        .offer-card.expired {
            opacity: 0.7;
            background: #f8f8f8;
        }
        
        .expired-tag {
            background: #ef4444;
            color: white;
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 12px;
            margin-top: 4px;
            display: inline-block;
        }

        /* Add these new styles */
        .success-message {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #10b981;
            color: white;
            padding: 15px 25px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            animation: slideIn 0.3s ease-out, fadeOut 0.3s ease-in 2.7s;
        }

        @keyframes slideIn {
            from {
                transform: translateX(100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        @keyframes fadeOut {
            from {
                opacity: 1;
            }
            to {
                opacity: 0;
            }
        }

        .offer-card .offer-actions {
            opacity: 0.7;
            transition: opacity 0.3s ease;
        }

        .offer-card:hover .offer-actions {
            opacity: 1;
        }

        .modal h3 {
            position: relative;
            padding-bottom: 10px;
            margin-bottom: 20px;
        }

        .modal h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background: #1a237e;
            border-radius: 3px;
        }
    </style>
</head>
<body>
    <div class="header">
        <h2>Admin Dashboard - Manage Products</h2>
        <button onclick="logout()">Logout</button>
    </div>

    <div class="container">
        <div class="button-container">
            <button class="button" id="addProductBtn">Add New Product</button>
            <button class="button" id="addOfferBtn" style="background: linear-gradient(135deg, #f59e0b, #d97706);">Add Offer</button>
        </div>
        <div id="productList"></div>
        
        <h3 class="section-title">Current Offers</h3>
        <div id="offersList" class="offers-grid"></div>
    </div>

    <!-- Modal for adding new product -->
    <div id="productModal" class="modal">
        <h3>Add Product</h3>
        <form id="productForm">
            <label for="productName">Name:</label>
            <input type="text" id="productName" required><br>
            
            <label for="productDescription">Description:</label>
            <input type="text" id="productDescription" required><br>
            
            <label for="productImageFile">Upload Image:</label>
            <input type="file" id="productImageFile" accept="image/*" required><br>
            
            <button type="submit">Add Product</button>
            <button type="button" onclick="closeModal()">Close</button>
        </form>
    </div>

    <!-- New Modal for adding offers -->
    <div id="offerModal" class="modal">
        <h3>Add Special Offer</h3>
        <form id="offerForm">
            <label for="offerTitle">Offer Title:</label>
            <input type="text" id="offerTitle" required><br>
            
            <label for="offerDiscount">Discount Percentage:</label>
            <input type="number" id="offerDiscount" min="1" max="99" required><br>
            
            <label for="offerExpiry">Expiry Date:</label>
            <input type="date" id="offerExpiry" required><br>
            
            <label for="offerExpiryTime">Expiry Time:</label>
            <input type="time" id="offerExpiryTime" required><br>
            
            <button type="submit">Add Offer</button>
            <button type="button" onclick="closeOfferModal()">Close</button>
        </form>
    </div>

    <script>
        // Check if the user is logged in as an admin
        function checkAdminLogin() {
            const isAdminLoggedIn = localStorage.getItem("isAdminLoggedIn");
            if (!isAdminLoggedIn || isAdminLoggedIn !== "true") {
                // Redirect to the login page if not logged in
                window.location.href = "index.html";
            }
        }

        // Open the modal for adding a product
        document.getElementById("addProductBtn").onclick = function () {
            document.getElementById("productModal").style.display = "block";
        };

        // Close the modal
        function closeModal() {
            document.getElementById("productModal").style.display = "none";
        }

        // Add a new product
        document.getElementById("productForm").onsubmit = function (e) {
            e.preventDefault();

            const name = document.getElementById("productName").value;
            const description = document.getElementById("productDescription").value;
            const imageFile = document.getElementById("productImageFile").files[0];

            if (!imageFile) {
                alert("Please upload an image.");
                return;
            }

            // Convert the image file to a Base64 string
            const reader = new FileReader();
            reader.onload = function (event) {
                const imageBase64 = event.target.result; // Base64 string

                // Fetch the existing products from localStorage
                const products = JSON.parse(localStorage.getItem("products")) || [];

                // Add the new product to the array
                products.push({ name, description, image: imageBase64 });

                // Save the updated product list to localStorage
                localStorage.setItem("products", JSON.stringify(products));

                // Reload the product list
                loadProducts();

                // Close the modal and reset the form
                closeModal();
                document.getElementById("productForm").reset();
            };
            reader.readAsDataURL(imageFile); // Start reading the file
        };

        // Load products from localStorage and display them
        function loadProducts() {
            const products = JSON.parse(localStorage.getItem("products")) || [];
            const productList = document.getElementById("productList");
            productList.innerHTML = ""; // Clear the existing products

            // Loop through each product and create a card
            products.forEach((product, index) => {
                const productCard = `
                    <div class="product-card" data-index="${index}">
                        <img src="${product.image}" alt="${product.name}">
                        <h4>${product.name}</h4>
                        <p>${product.description}</p>
                        <button onclick="deleteProduct(${index})">Delete</button>
                    </div>
                `;
                productList.insertAdjacentHTML("beforeend", productCard);
            });
        }

        // Delete a product by index
        function deleteProduct(index) {
            const products = JSON.parse(localStorage.getItem("products")) || [];
            products.splice(index, 1); // Remove the product at the given index
            localStorage.setItem("products", JSON.stringify(products)); // Save the updated product list
            loadProducts(); // Reload the product list
        }

        // Logout function to clear admin login status
        function logout() {
            localStorage.removeItem("isAdminLoggedIn"); // Remove the admin login flag
            window.location.href = "index.html"; // Redirect to the login page
        }

        // Check admin login status on page load
        checkAdminLogin();

        // Load products on page load
        window.onload = function() {
            loadProducts();
            loadOffers();
        };

        // Open the offer modal
        document.getElementById("addOfferBtn").onclick = function () {
            document.getElementById("offerModal").style.display = "block";
        };

        // Close the offer modal
        function closeOfferModal() {
            document.getElementById("offerModal").style.display = "none";
        }

        // Add a new offer
        document.getElementById("offerForm").onsubmit = function (e) {
            e.preventDefault();

            const title = document.getElementById("offerTitle").value;
            const discount = document.getElementById("offerDiscount").value;
            const expiryDate = document.getElementById("offerExpiry").value;
            const expiryTime = document.getElementById("offerExpiryTime").value;

            // Combine date and time
            const expiry = new Date(`${expiryDate}T${expiryTime}`);

            // Check if the expiry date/time is in the future
            if (expiry <= new Date()) {
                alert("Please select a future date and time for the offer expiry.");
                return;
            }

            const offers = JSON.parse(localStorage.getItem("offers")) || [];
            offers.push({ 
                title, 
                discount, 
                expiry: expiry.toISOString(),
                expiryTime: expiryTime
            });
            localStorage.setItem("offers", JSON.stringify(offers));

            alert("Offer added successfully!");
            closeOfferModal();
            document.getElementById("offerForm").reset();
            loadOffers();
        };

        // Function to load and display offers
        function loadOffers() {
            const offers = JSON.parse(localStorage.getItem("offers")) || [];
            const offersList = document.getElementById("offersList");
            offersList.innerHTML = "";

            offers.forEach((offer, index) => {
                const expiryDate = new Date(offer.expiry);
                const now = new Date();
                const isExpired = expiryDate <= now;
                
                const formattedDate = expiryDate.toLocaleDateString();
                const formattedTime = expiryDate.toLocaleTimeString();
                
                const offerCard = `
                    <div class="offer-card ${isExpired ? 'expired' : ''}">
                        <h4>${offer.title}</h4>
                        <div class="offer-discount">${offer.discount}% OFF</div>
                        <div class="offer-expiry">
                            <span class="offer-expiry-date">Expires on: ${formattedDate}</span>
                            <span class="offer-expiry-time">at ${formattedTime}</span>
                            ${isExpired ? '<span class="expired-tag">EXPIRED</span>' : ''}
                        </div>
                        <div class="offer-actions">
                            ${!isExpired ? `<button onclick="editOffer(${index})" class="edit-btn">Edit</button>` : ''}
                            <button onclick="deleteOffer(${index})" class="delete-btn">Delete</button>
                        </div>
                    </div>
                `;
                offersList.insertAdjacentHTML("beforeend", offerCard);
            });
        }

        // Function to delete an offer with confirmation
        function deleteOffer(index) {
            const offers = JSON.parse(localStorage.getItem("offers")) || [];
            const offer = offers[index];
            
            // Show confirmation dialog
            if (confirm(`Are you sure you want to delete the offer "${offer.title}"?`)) {
                offers.splice(index, 1);
                localStorage.setItem("offers", JSON.stringify(offers));
                
                // Show success message
                const successMsg = document.createElement('div');
                successMsg.className = 'success-message';
                successMsg.textContent = 'Offer deleted successfully!';
                document.body.appendChild(successMsg);
                
                // Remove success message after 3 seconds
                setTimeout(() => {
                    successMsg.remove();
                }, 3000);
                
                loadOffers();
            }
        }

        // Function to edit an offer
        function editOffer(index) {
            const offers = JSON.parse(localStorage.getItem("offers")) || [];
            const offer = offers[index];
            
            // Update modal title to show we're editing
            const modalTitle = document.querySelector('#offerModal h3');
            modalTitle.textContent = 'Edit Offer';
            
            // Populate the modal with offer data
            document.getElementById("offerTitle").value = offer.title;
            document.getElementById("offerDiscount").value = offer.discount;
            
            // Split the datetime into date and time
            const expiryDate = new Date(offer.expiry);
            document.getElementById("offerExpiry").value = expiryDate.toISOString().split('T')[0];
            document.getElementById("offerExpiryTime").value = offer.expiryTime || 
                expiryDate.toLocaleTimeString('en-US', { hour12: false }).slice(0, 5);
            
            // Show the modal
            const modal = document.getElementById("offerModal");
            modal.style.display = "block";
            
            // Update submit button text
            const submitBtn = document.querySelector('#offerForm button[type="submit"]');
            submitBtn.textContent = 'Update Offer';
            
            // Update the form submission handler for editing
            const form = document.getElementById("offerForm");
            form.onsubmit = function(e) {
                e.preventDefault();
                
                const newExpiryDate = document.getElementById("offerExpiry").value;
                const newExpiryTime = document.getElementById("offerExpiryTime").value;
                const newExpiry = new Date(`${newExpiryDate}T${newExpiryTime}`);

                // Check if the new expiry date/time is in the future
                if (newExpiry <= new Date()) {
                    alert("Please select a future date and time for the offer expiry.");
                    return;
                }
                
                // Update the offer
                offers[index] = {
                    title: document.getElementById("offerTitle").value,
                    discount: document.getElementById("offerDiscount").value,
                    expiry: newExpiry.toISOString(),
                    expiryTime: newExpiryTime
                };
                
                localStorage.setItem("offers", JSON.stringify(offers));
                
                // Show success message
                const successMsg = document.createElement('div');
                successMsg.className = 'success-message';
                successMsg.textContent = 'Offer updated successfully!';
                document.body.appendChild(successMsg);
                
                // Remove success message after 3 seconds
                setTimeout(() => {
                    successMsg.remove();
                }, 3000);
                
                closeOfferModal();
                form.reset();
                resetOfferForm();
                loadOffers();
            };
        }

        // Function to reset offer form to add mode
        function resetOfferForm() {
            const modalTitle = document.querySelector('#offerModal h3');
            modalTitle.textContent = 'Add Special Offer';
            
            const submitBtn = document.querySelector('#offerForm button[type="submit"]');
            submitBtn.textContent = 'Add Offer';
            
            setupNewOfferHandler();
        }

        // Function to setup handler for adding new offers
        function setupNewOfferHandler() {
            document.getElementById("offerForm").onsubmit = function(e) {
                e.preventDefault();

                const title = document.getElementById("offerTitle").value;
                const discount = document.getElementById("offerDiscount").value;
                const expiryDate = document.getElementById("offerExpiry").value;
                const expiryTime = document.getElementById("offerExpiryTime").value;

                // Combine date and time
                const expiry = new Date(`${expiryDate}T${expiryTime}`);

                // Check if the expiry date/time is in the future
                if (expiry <= new Date()) {
                    alert("Please select a future date and time for the offer expiry.");
                    return;
                }

                const offers = JSON.parse(localStorage.getItem("offers")) || [];
                offers.push({ 
                    title, 
                    discount, 
                    expiry: expiry.toISOString(),
                    expiryTime: expiryTime
                });
                localStorage.setItem("offers", JSON.stringify(offers));

                alert("Offer added successfully!");
                closeOfferModal();
                this.reset();
                loadOffers();
            };
        }

        // Initialize the new offer handler
        setupNewOfferHandler();
    </script>
</body>
</html>