<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Christian Sinchi - Shakers CDJR</title>
    <style>
        body {
            background-color: #1a1a1a;
            color: #ffffff;
            font-family: 'Helvetica', Arial, sans-serif;
            margin: 0;
            padding: 10px; /* Reduced padding for smaller screens */
            line-height: 1.5;
        }

        .container {
            max-width: 100%; /* Changed from 700px to fit smaller screens */
            width: 100%; /* Ensures full width on mobile */
            margin: 0 auto;
            border: 2px solid;
            border-image: linear-gradient(45deg, #c0c0c0, #ffffff, #c0c0c0) 1;
            padding: 15px; /* Reduced padding for mobile */
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.1);
            animation: shimmer 4s infinite;
            border-radius: 10px;
            background: #222222;
            box-sizing: border-box; /* Ensures padding doesn’t overflow */
        }

        @keyframes shimmer {
            0% { border-image: linear-gradient(45deg, #c0c0c0, #ffffff, #c0c0c0) 1; }
            50% { border-image: linear-gradient(45deg, #ffffff, #c0c0c0, #ffffff) 1; }
            100% { border-image: linear-gradient(45deg, #c0c0c0, #ffffff, #c0c0c0) 1; }
        }

        .header {
            text-align: center;
            margin-bottom: 20px; /* Reduced for mobile */
        }

        .dealership-name {
            font-size: clamp(1.8em, 6vw, 2.5em); /* Scales font size dynamically */
            margin-bottom: 5px;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.5), 0 0 20px rgba(255, 255, 255, 0.3);
            animation: sparkle 2s infinite;
        }

        .sparkle-name {
            font-size: clamp(1.5em, 5vw, 2em); /* Scales font size dynamically */
            margin: 10px 0;
            text-shadow: 0 0 8px rgba(255, 255, 255, 0.5), 0 0 15px rgba(255, 255, 255, 0.3);
            animation: sparkle 2s infinite;
        }

        @keyframes sparkle {
            0% { text-shadow: 0 0 8px rgba(255, 255, 255, 0.5), 0 0 15px rgba(255, 255, 255, 0.3); }
            50% { text-shadow: 0 0 12px rgba(255, 255, 255, 0.7), 0 0 20px rgba(255, 255, 255, 0.5); }
            100% { text-shadow: 0 0 8px rgba(255, 255, 255, 0.5), 0 0 15px rgba(255, 255, 255, 0.3); }
        }

        .header p {
            margin: 5px 0;
            font-size: clamp(0.8em, 3.5vw, 1em); /* Scales text for readability */
            color: #e0e0e0;
        }

        .button {
            background: linear-gradient(to bottom, #ffffff, #d0d0d0);
            border: none;
            padding: 8px 15px; /* Slightly reduced padding */
            margin: 5px;
            border-radius: 20px;
            cursor: pointer;
            color: #333;
            font-weight: 600;
            box-shadow: 0 2px 10px rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
            font-size: clamp(0.8em, 3vw, 0.9em); /* Scales button text */
        }

        .button:hover {
            background: linear-gradient(to bottom, #e0e0e0, #ffffff);
            box-shadow: 0 4px 15px rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }

        .button.selected {
            background: linear-gradient(to bottom, #1E90FF, #1C86EE);
            color: white;
            box-shadow: 0 4px 15px rgba(30, 144, 255, 0.4);
        }

        .section {
            margin-bottom: 20px; /* Reduced for mobile */
        }

        select, input {
            width: 100%;
            padding: 8px 10px; /* Slightly reduced padding */
            margin: 6px 0; /* Reduced margin */
            background: #333;
            color: #fff;
            border: 1px solid #555;
            border-radius: 6px;
            box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.2);
            font-size: clamp(0.8em, 3vw, 0.9em); /* Scales input text */
            box-sizing: border-box;
        }

        h2 {
            font-size: clamp(1.2em, 4vw, 1.5em); /* Scales heading */
            text-shadow: 0 0 6px rgba(255, 255, 255, 0.2);
            margin-bottom: 10px; /* Reduced for mobile */
        }

        #contact-form {
            display: none;
        }

        .info-text {
            color: #bbbbbb;
            font-style: italic;
            margin: 10px 0;
            text-align: center;
            font-size: clamp(0.7em, 3vw, 0.9em); /* Scales text */
        }

        /* Media query for smaller screens (e.g., iPhone) */
        @media (max-width: 450px) {
            .button {
                display: block; /* Stack buttons vertically */
                width: 100%; /* Full width for easier tapping */
                margin: 5px 0; /* Adjust spacing */
            }
            .header p {
                line-height: 1.2; /* Tighter line spacing */
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 class="dealership-name">Shakers CDJR</h1>
            <p>1230 Main St, Watertown, CT 06795</p>
            <h1 class="sparkle-name">Christian Sinchi</h1>
            <p>Dealership Phone: (860) 266-2921 - Ask for Christian</p>
            <p>Christian's Cell: (347) 702-2499</p>
            <p>Email: csinchi@shakerscdjr.com</p>
            <p><strong>Fluent in English & Spanish | Habla Español</strong></p>
        </div>

        <div class="section" id="questions">
            <h2>Find Your Perfect Vehicle</h2>
            
            <div>
                <p>Buying or Leasing?</p>
                <button class="button" onclick="selectButton(this, 'transaction', 'Buying')">Buying</button>
                <button class="button" onclick="selectButton(this, 'transaction', 'Leasing')">Leasing</button>
            </div>

            <div>
                <p>Price Range?</p>
                <select id="price-range" onchange="saveAnswer('price', this.value)">
                    <option value="">Select Price Range</option>
                    <option value="Under $20,000">Under $20,000</option>
                    <option value="$20,000 - $30,000">$20,000 - $30,000</option>
                    <option value="$30,000 - $40,000">$30,000 - $40,000</option>
                    <option value="$40,000+">$40,000+</option>
                </select>
            </div>

            <div>
                <p>Favorite Color?</p>
                <select id="color" onchange="saveAnswer('color', this.value)">
                    <option value="">Select Color</option>
                    <option value="Black">Black</option>
                    <option value="White">White</option>
                    <option value="Red">Red</option>
                    <option value="Blue">Blue</option>
                    <option value="Silver">Silver</option>
                    <option value="Other">Other</option>
                </select>
            </div>

            <div>
                <p>Preferred Model?</p>
                <select id="model" onchange="saveAnswer('model', this.value)">
                    <option value="">Select Model</option>
                    <option value="Wrangler">Wrangler</option>
                    <option value="Grand Cherokee">Grand Cherokee</option>
                    <option value="Cherokee">Cherokee</option>
                    <option value="Compass">Compass</option>
                    <option value="Other Jeep">Other Jeep</option>
                    <option value="Different Vehicle">Different Vehicle (e.g., saw on website/in person)</option>
                </select>
            </div>

            <div>
                <p>New or Used?</p>
                <button class="button" onclick="selectButton(this, 'condition', 'New')">New</button>
                <button class="button" onclick="selectButton(this, 'condition', 'Used')">Used</button>
                <button class="button" onclick="selectButton(this, 'condition', 'Other')">Other</button>
            </div>

            <div>
                <p>Transmission?</p>
                <button class="button" onclick="selectButton(this, 'transaction', 'Automatic')">Automatic</button>
                <button class="button" onclick="selectButton(this, 'transmission', 'Manual')">Manual</button>
            </div>

            <button class="button" onclick="showContactForm()">Submit to Christian</button>
        </div>

        <div class="section" id="contact-form">
            <h2>Contact Christian</h2>
            <p class="info-text">This information will only be sent to Christian Sinchi via email. He will personally contact you after receiving your submission.</p>
            <input type="text" id="name" placeholder="Your Full Name" required>
            <input type="tel" id="phone" placeholder="Your Phone Number" required>
            <input type="email" id="email" placeholder="Your Email Address" required>
            <input type="text" id="address" placeholder="Your Address (Optional)">
            <button class="button" onclick="sendEmail()">Send to Christian</button>
        </div>
    </div>

    <script>
        let customerData = {};

        function saveAnswer(key, value) {
            customerData[key] = value;
        }

        function selectButton(button, key, value) {
            const buttons = button.parentElement.querySelectorAll('.button');
            buttons.forEach(btn => btn.classList.remove('selected'));
            button.classList.add('selected');
            saveAnswer(key, value);
        }

        function showContactForm() {
            document.getElementById('questions').style.display = 'none';
            document.getElementById('contact-form').style.display = 'block';
        }

        function sendEmail() {
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const email = document.getElementById('email').value;
            const address = document.getElementById('address').value;

            if (!name || !phone || !email) {
                alert('Please fill in all required fields (Name, Phone, Email)');
                return;
            }

            const subject = `Vehicle Inquiry from ${name}`;
            const body = `Dear Christian Sinchi,

You have a new customer inquiry from Shakers CDJR:

Customer Information:
Name: ${name}
Phone: ${phone}
Email: ${email}
Address: ${address || 'Not provided'}

Vehicle Preferences:
Transaction Type: ${customerData.transaction || 'Not specified'}
Price Range: ${customerData.price || 'Not specified'}
Preferred Color: ${customerData.color || 'Not specified'}
Preferred Model: ${customerData.model || 'Not specified'}
Condition: ${customerData.condition || 'Not specified'}
Transmission: ${customerData.transmission || 'Not specified'}

Please contact this customer at your earliest convenience to assist them with their vehicle purchase.

Thank you,
${name}
${phone}
${email}`;

            window.location.href = `mailto:csinchi@shakerscdjr.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
        }
    </script>
</body>
</html>
