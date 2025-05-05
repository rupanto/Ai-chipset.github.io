# Ai-chipset.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Chipset Marketplace</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f0f2f5;
            color: #333;
        }
        .header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background-color: #1a237e;
            color: white;
            border-radius: 8px;
        }
        .features {
            max-width: 800px;
            margin: 0 auto 30px;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .features ol {
            padding-left: 20px;
        }
        .features li {
            margin-bottom: 10px;
        }
        .chips-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            max-width: 1400px;
            margin: 0 auto;
        }
        .chip {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            position: relative;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .chip:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.15);
        }
        .chip-image {
            width: 100%;
            height: 200px;
            border-radius: 8px;
            margin-bottom: 15px;
            object-fit: cover;
            border: 1px solid #eee;
        }
        .serial {
            font-weight: bold;
            font-size: 20px;
            margin-bottom: 10px;
            color: #1a237e;
        }
        .specs {
            margin: 10px 0;
            color: #555;
            font-size: 14px;
        }
        .income {
            margin: 8px 0;
            color: #2e7d32;
            font-weight: 500;
        }
        .price {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: #1a237e;
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 16px;
        }
        .buy-btn {
            display: block;
            width: 100%;
            padding: 12px;
            margin-top: 15px;
            background-color: #00c853;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .buy-btn:hover {
            background-color: #009624;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 100;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
        }
        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 30px;
            border-radius: 10px;
            width: 80%;
            max-width: 500px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            animation: modalopen 0.4s;
        }
        @keyframes modalopen {
            from {opacity: 0; transform: translateY(-50px);}
            to {opacity: 1; transform: translateY(0);}
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover {
            color: #333;
        }
        .payment-option {
            margin: 15px 0;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            background-color: #f9f9f9;
        }
        .payment-option img {
            height: 30px;
            vertical-align: middle;
            margin-right: 10px;
        }
        .user-id {
            background-color: #e3f2fd;
            padding: 10px;
            border-radius: 5px;
            margin: 10px 0;
            font-weight: bold;
            word-break: break-all;
        }
        .submit-btn {
            background-color: #1a237e;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 15px;
            width: 100%;
        }
        .submit-btn:hover {
            background-color: #303f9f;
        }
        .confirmation {
            display: none;
            text-align: center;
            padding: 20px;
            background-color: #e8f5e9;
            border-radius: 5px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>AI Chipset Marketplace</h1>
        <p>High-performance AI chips for your computing needs</p>
    </div>

    <div class="features">
        <h2>Why Choose Our AI Chipsets?</h2>
        <ol>
            <li><strong>Proven Performance:</strong> Each chipset is rigorously tested for maximum efficiency</li>
            <li><strong>Guaranteed Income:</strong> Earn daily with our optimized AI algorithms</li>
            <li><strong>24/7 Support:</strong> Dedicated technical support team available round the clock</li>
            <li><strong>Secure Payments:</strong> Multiple payment options with transaction verification</li>
            <li><strong>Automatic Updates:</strong> Regular firmware updates for peak performance</li>
        </ol>
    </div>

    <div class="chips-container">
        <!-- Chip 1 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1591488320449-011701bb6704?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 1" class="chip-image">
            <div class="serial">AI Chipset #1</div>
            <div class="specs">Specs: 8-core CPU, 16GB RAM, 256GB SSD</div>
            <div class="specs">Performance: 15 TFLOPS</div>
            <div class="income">Hourly Income: 40 Taka</div>
            <div class="income">Daily Income: 1000 Taka</div>
            <div class="price">2000 Taka</div>
            <button class="buy-btn" onclick="openModal(1, 2000)">Buy Now</button>
        </div>

        <!-- Chip 2 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 2" class="chip-image">
            <div class="serial">AI Chipset #2</div>
            <div class="specs">Specs: 12-core CPU, 32GB RAM, 512GB SSD</div>
            <div class="specs">Performance: 30 TFLOPS</div>
            <div class="income">Hourly Income: 80 Taka</div>
            <div class="income">Daily Income: 2000 Taka</div>
            <div class="price">6000 Taka</div>
            <button class="buy-btn" onclick="openModal(2, 6000)">Buy Now</button>
        </div>

        <!-- Chip 3 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1592155931584-901ac15763e3?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 3" class="chip-image">
            <div class="serial">AI Chipset #3</div>
            <div class="specs">Specs: 16-core CPU, 64GB RAM, 1TB SSD</div>
            <div class="specs">Performance: 60 TFLOPS</div>
            <div class="income">Hourly Income: 160 Taka</div>
            <div class="income">Daily Income: 4000 Taka</div>
            <div class="price">18000 Taka</div>
            <button class="buy-btn" onclick="openModal(3, 18000)">Buy Now</button>
        </div>

        <!-- Chip 4 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 4" class="chip-image">
            <div class="serial">AI Chipset #4</div>
            <div class="specs">Specs: 24-core CPU, 128GB RAM, 2TB SSD</div>
            <div class="specs">Performance: 120 TFLOPS</div>
            <div class="income">Hourly Income: 320 Taka</div>
            <div class="income">Daily Income: 8000 Taka</div>
            <div class="price">54000 Taka</div>
            <button class="buy-btn" onclick="openModal(4, 54000)">Buy Now</button>
        </div>

        <!-- Chip 5 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 5" class="chip-image">
            <div class="serial">AI Chipset #5</div>
            <div class="specs">Specs: 32-core CPU, 256GB RAM, 4TB SSD</div>
            <div class="specs">Performance: 240 TFLOPS</div>
            <div class="income">Hourly Income: 640 Taka</div>
            <div class="income">Daily Income: 16000 Taka</div>
            <div class="price">162000 Taka</div>
            <button class="buy-btn" onclick="openModal(5, 162000)">Buy Now</button>
        </div>

        <!-- Chip 6 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1592155931584-901ac15763e3?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 6" class="chip-image">
            <div class="serial">AI Chipset #6</div>
            <div class="specs">Specs: 48-core CPU, 512GB RAM, 8TB SSD</div>
            <div class="specs">Performance: 480 TFLOPS</div>
            <div class="income">Hourly Income: 1280 Taka</div>
            <div class="income">Daily Income: 32000 Taka</div>
            <div class="price">486000 Taka</div>
            <button class="buy-btn" onclick="openModal(6, 486000)">Buy Now</button>
        </div>

        <!-- Chip 7 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 7" class="chip-image">
            <div class="serial">AI Chipset #7</div>
            <div class="specs">Specs: 64-core CPU, 1TB RAM, 16TB SSD</div>
            <div class="specs">Performance: 960 TFLOPS</div>
            <div class="income">Hourly Income: 2560 Taka</div>
            <div class="income">Daily Income: 64000 Taka</div>
            <div class="price">1,458,000 Taka</div>
            <button class="buy-btn" onclick="openModal(7, 1458000)">Buy Now</button>
        </div>

        <!-- Chip 8 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1591488320449-011701bb6704?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 8" class="chip-image">
            <div class="serial">AI Chipset #8</div>
            <div class="specs">Specs: 96-core CPU, 2TB RAM, 32TB SSD</div>
            <div class="specs">Performance: 1920 TFLOPS</div>
            <div class="income">Hourly Income: 5120 Taka</div>
            <div class="income">Daily Income: 128000 Taka</div>
            <div class="price">4,374,000 Taka</div>
            <button class="buy-btn" onclick="openModal(8, 4374000)">Buy Now</button>
        </div>

        <!-- Chip 9 -->
        <div class="chip">
            <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="AI Chipset 9" class="chip-image">
            <div class="serial">AI Chipset #9</div>
            <div class="specs">Specs: 128-core CPU, 4TB RAM, 64TB SSD</div>
            <div class="specs">Performance: 3840 TFLOPS</div>
            <div class="income">Hourly Income: 10240 Taka</div>
            <div class="income">Daily Income: 256000 Taka</div>
            <div class="price">13,122,000 Taka</div>
            <button class="buy-btn" onclick="openModal(9, 13122000)">Buy Now</button>
        </div>
    </div>

    <!-- Payment Modal -->
    <div id="paymentModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2 id="modalTitle">Complete Your Purchase</h2>
            <p id="productInfo">You're purchasing AI Chipset #1 for 2000 Taka</p>
            
            <div class="payment-option">
                <h3>Payment Method</h3>
                <div>
                    <input type="radio" id="bkash" name="payment" value="bkash" checked>
                    <label for="bkash"><img src="https://www.bkash.com/upload/contents/images/logo.svg" alt="bKash"> bKash</label>
                    <div class="user-id">
                        <p><strong>Payment Number:</strong> 01725657887</p>
                        <p><strong>User ID:</strong> AI_CHIP_001</p>
                        <p><strong>Payment Reference:</strong> Your Phone Number</p>
                    </div>
                    <p>After payment, please provide your transaction ID below.</p>
                </div>
                
                <div style="margin-top: 15px;">
                    <input type="radio" id="nagad" name="payment" value="nagad">
                    <label for="nagad"><img src="https://www.nagad.com.bd/wp-content/uploads/2021/11/Nagad-Logo.wine_.png" alt="Nagad" style="height: 25px;"> Nagad</label>
                    <div class="user-id">
                        <p><strong>Payment Number:</strong> 01725657887</p>
                        <p><strong>User ID:</strong> AI_CHIP_001</p>
                        <p><strong>Payment Reference:</strong> Your Phone Number</p>
                    </div>
                    <p>After payment, please provide your transaction ID below.</p>
                </div>
            </div>
            
            <div>
                <label for="trxId">Transaction ID:</label>
                <input type="text" id="trxId" placeholder="Enter your transaction ID" style="width: 100%; padding: 10px; margin-top: 5px; border: 1px solid #ddd; border-radius: 4px;">
            </div>
            
            <div>
                <label for="phone">Your Phone Number:</label>
                <input type="text" id="phone" placeholder="Enter your phone number" style="width: 100%; padding: 10px; margin-top: 5px; border: 1px solid #ddd; border-radius: 4px;">
            </div>
            
            <div>
                <label for="userId">Your User ID (if any):</label>
                <input type="text" id="userId" placeholder="Enter your user ID (optional)" style="width: 100%; padding: 10px; margin-top: 5px; border: 1px solid #ddd; border-radius: 4px;">
            </div>
            
            <button class="submit-btn" onclick="submitPayment()">Submit Payment</button>
            
            <div id="confirmation" class="confirmation">
                <h3>Thank You!</h3>
                <p>Your payment has been submitted successfully.</p>
                <p>We will verify your transaction and activate your AI Chipset within 24 hours.</p>
                <p>You'll receive a confirmation SMS once activated.</p>
                <p><strong>Support Contact:</strong> 01725657887</p>
            </div>
        </div>
    </div>

    <script>
        // Current selected product
        let currentProduct = null;
        let currentPrice = 0;

        // Open payment modal
        function openModal(productId, price) {
            currentProduct = productId;
            currentPrice = price;
            
            document.getElementById('modalTitle').textContent = `Complete Your Purchase`;
            document.getElementById('productInfo').textContent = `You're purchasing AI Chipset #${productId} for ${price.toLocaleString()} Taka`;
            
            // Reset form
            document.getElementById('trxId').value = '';
            document.getElementById('phone').value = '';
            document.getElementById('userId').value = '';
            document.getElementById('confirmation').style.display = 'none';
            
            // Show modal
            document.getElementById('paymentModal').style.display = 'block';
        }

        // Close payment modal
        function closeModal() {
            document.getElementById('paymentModal').style.display = 'none';
        }

        // Submit payment
        function submitPayment() {
            const trxId = document.getElementById('trxId').value;
            const phone = document.getElementById('phone').value;
            const userId = document.getElementById('userId').value;
            const paymentMethod = document.querySelector('input[name="payment"]:checked').value;
            
            if (!trxId || !phone) {
                alert('Please fill in all required fields');
                return;
            }
            
            // In a real application, you would send this data to your server
            const paymentData = {
                productId: currentProduct,
                productName: `AI Chipset #${currentProduct}`,
                price: currentPrice,
                paymentMethod,
                trxId,
                phone,
                userId: userId || 'N/A',
                timestamp: new Date().toISOString()
            };
            
            console.log('Payment submitted:', paymentData);
            
            // Show confirmation
            document.getElementById('confirmation').style.display = 'block';
            
            // Scroll to confirmation
            document.getElementById('confirmation').scrollIntoView({ behavior: 'smooth' });
            
            // In a real app, you would send this data to your server
            // Here we'll just store it in localStorage for demonstration
            const transactions = JSON.parse(localStorage.getItem('chipsetTransactions') || '[]');
            transactions.push(paymentData);
            localStorage.setItem('chipsetTransactions', JSON.stringify(transactions));
        }

        // Close modal when clicking outside
        window.onclick = function(event) {
            const modal = document.getElementById('paymentModal');
            if (event.target == modal) {
                closeModal();
            }
        }
    </script>
</body>
</html>
