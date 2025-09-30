# all17<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>JKS Group of Business</title>
<style>
  body { font-family: Arial, sans-serif; margin:0; background: #22232c; color: #fff; }
  header { font-size: 2.2rem; font-weight: bold; color: #3aaaff; text-align: center; padding: 36px 10px 10px; user-select: none; }
  #dashboard { max-width: 960px; margin: 20px auto; display: grid; grid-template-columns: repeat(4,1fr); gap: 20px; }
  .service-button { border: 2.5px solid #ffe066; border-radius: 12px; padding: 20px; text-align: center; cursor: pointer; font-weight: 600; color: #ffe066; background-color: #232335; box-shadow: 0 0 18px #ffe066aa; transition: all 0.3s ease; user-select: none; }
  .service-button:hover { color: #fffbd0; background-color: #232342; box-shadow: 0 0 38px #ffe066ff; transform: scale(1.05); }
  .section { max-width: 960px; margin: 20px auto; padding: 20px; background: #f9f9f9; color: #222; border-radius: 12px; display: none; }
  .section.active { display: block; }
  h2 { color: #205081; border-bottom: 3px solid #85bbeb; padding-bottom: 6px; }
  button.back-button, form button.submit-btn { margin-top: 20px; padding: 10px 15px; font-weight: 600; cursor: pointer; border: none; border-radius: 6px; background-color: #3498db; color: white; }
  input, textarea, select { width: 100%; padding: 8px; margin-top: 4px; border-radius: 6px; border: 1px solid #ccc; box-sizing: border-box; }
  label { font-weight: 600; margin-top: 12px; display: block; }
  nav.small-nav { display: flex; justify-content: center; gap: 12px; margin-bottom: 18px; flex-wrap: wrap; }
  nav.small-nav button { padding: 10px 14px; font-weight: 600; border-radius: 8px; border: none; cursor: pointer; background: #eef2ff; color: #3366cc; transition: background 0.3s, color 0.3s; }
  nav.small-nav button.selected { background: #3366cc; color: white; }
  nav.small-nav button:hover:not(.selected) { background: #d3d9f6; }
  iframe#mapIframe { width: 100%; height: 300px; border: none; border-radius: 12px; margin: 20px 0; }
  video { display: block; margin: 20px auto; border-radius: 12px; max-width: 100%; height: auto; }
  .gallery { display: flex; gap: 12px; flex-wrap: wrap; margin-bottom: 20px; }
  .img-card { border: 1px solid #ccc; border-radius: 8px; overflow: hidden; width: 160px; text-align: center; background: white; cursor: pointer; box-shadow: 0 0 5px #aaa; }
  .img-card img { width: 100%; height: 90px; object-fit: cover; }
  .img-card p { margin: 8px 0; font-weight: 600; color: #205081; }
</style>
</head>
<body>
<header>JKS Group of Business</header>

<div id="dashboard">
  <div class="service-button" onclick="showSection('ecommerce')">My E-commerce</div>
  <div class="service-button" onclick="showSection('events')">Events & Catering</div>
  <div class="service-button" onclick="showSection('courier')">Courier & Ride Booking</div>
  <div class="service-button" onclick="showSection('job')">Job Consultancy & Services</div>
  <div class="service-button" onclick="showSection('tours')">Tours & Travels</div>
  <div class="service-button" onclick="showSection('realestate')">Real Estate & Construction</div>
  <div class="service-button" onclick="showSection('investment')">Investment & Business</div>
  <div class="service-button" onclick="showSection('loans')">Loans & Insurance</div>
  <div class="service-button" onclick="showSection('homeservices')">Home Services</div>
</div>

<!-- E-commerce -->
<div id="ecommerce" class="section">
  <h2>My E-commerce</h2>
  <nav class="small-nav">
    <button class="selected" onclick="switchEcommTab('groceries', this)">Groceries</button>
    <button onclick="switchEcommTab('food', this)">Food</button>
    <button onclick="switchEcommTab('pharmacy', this)">Pharmacy</button>
    <button onclick="switchEcommTab('camera', this)">Camera</button>
    <button onclick="switchEcommTab('maps', this)">Location Map</button>
  </nav>

  <div id="groceriesTab" class="ecomm-tab active">
    <h3>Groceries Categories</h3>
    <div class="gallery">
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?milk" alt="Milk"/><p>Milk</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?meat" alt="Meat"/><p>Meat</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?fruits" alt="Fruits"/><p>Fruits</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?vegetables" alt="Vegetables"/><p>Vegetables</p></div>
    </div>
    <form id="ecommerceGroceriesForm">
      <label for="nameEcomGro">Name</label>
      <input type="text" id="nameEcomGro" name="nameEcomGro" required />
      <label for="mobileEcomGro">Mobile Number</label>
      <input type="tel" id="mobileEcomGro" name="mobileEcomGro" />
      <label for="orderEcomGro">Order Details</label>
      <textarea id="orderEcomGro" name="orderEcomGro" rows="3" required></textarea>
      <label for="addressEcomGro">Delivery Address</label>
      <textarea id="addressEcomGro" name="addressEcomGro" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>

  <div id="foodTab" class="ecomm-tab" style="display:none;">
    <h3>Food Categories</h3>
    <div class="gallery">
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?biriyani" alt="Biriyani"/><p>Biriyani</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?tiffins" alt="Tiffins"/><p>Tiffins</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?icecream" alt="Ice Cream"/><p>Ice Cream</p></div>
    </div>
    <form id="ecommerceFoodForm">
      <label for="nameEcomFood">Name</label>
      <input type="text" id="nameEcomFood" name="nameEcomFood" required />
      <label for="mobileEcomFood">Mobile Number</label>
      <input type="tel" id="mobileEcomFood" name="mobileEcomFood"/>
      <label for="orderEcomFood">Order Details</label>
      <textarea id="orderEcomFood" name="orderEcomFood" rows="3" required></textarea>
      <label for="addressEcomFood">Delivery Address</label>
      <textarea id="addressEcomFood" name="addressEcomFood" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>

  <div id="pharmacyTab" class="ecomm-tab" style="display:none;">
    <h3>Pharmacy</h3>
    <div class="gallery">
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?medicine" alt="Medicines"/><p>Medicines</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?health" alt="Health Products"/><p>Health Products</p></div>
    </div>
    <form id="ecommercePharmacyForm">
      <label for="nameEcomPhar">Name</label>
      <input type="text" id="nameEcomPhar" name="nameEcomPhar" required />
      <label for="mobileEcomPhar">Mobile Number</label>
      <input type="tel" id="mobileEcomPhar" name="mobileEcomPhar"/>
      <label for="orderEcomPhar">Order Details</label>
      <textarea id="orderEcomPhar" name="orderEcomPhar" rows="3" required></textarea>
      <label for="addressEcomPhar">Delivery Address</label>
      <textarea id="addressEcomPhar" name="addressEcomPhar" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>

  <div id="cameraTab" class="ecomm-tab" style="display:none;">
    <h3>Camera Access</h3>
    <button onclick="openCamera()">Start Camera</button>
    <video id="video" autoplay></video>
  </div>

  <div id="mapsTab" class="ecomm-tab" style="display:none;">
    <h3>Location Map</h3>
    <iframe id="mapIframe"
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3806.473283539352!2d78.4743343148517!3d17.38977028803544!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bcb91908b1d9a77%3A0x2c896c17b60a465f!2sHyderabad!5e0!3m2!1sen!2sin!4v1696063039954!5m2!1sen!2sin"
      allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
  </div>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Events & Catering (updated with budgets in customized) -->
<div id="events" class="section">
  <h2>Events & Catering</h2>
  <nav class="small-nav">
    <button class="selected" onclick="switchEventTab('package', this)">Package</button>
    <button onclick="switchEventTab('customized', this)">Customized</button>
    <button onclick="switchEventTab('premium', this)">Premium</button>
  </nav>

  <div id="packageTab" class="tab-content">
    <p>Choose your package and services.</p>
    <ul>
      <li>Silver: 50,000 - 1,00,000</li>
      <li>Gold: 1,00,000 - 3,00,000</li>
      <li>Diamond: 3,00,000 - 5,00,000</li>
      <li>Platinum: 5,00,000 - 8,00,000</li>
    </ul>
    <form id="eventsPackageForm">
      <label>Name</label>
      <input type="text" id="namePackage" name="namePackage" required />
      <label>Mobile Number</label>
      <input type="tel" id="mobilePackage" name="mobilePackage" required />
      <label>Email</label>
      <input type="email" id="emailPackage" name="emailPackage" required />
      <label>Message</label>
      <textarea id="messagePackage" name="messagePackage" rows="3" required></textarea>
      <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
    </form>
  </div>

  <div id="customizedTab" class="tab-content" style="display:none;">
    <p>Select customized services and enter budget for each:</p>
    <form id="customizedBudgetForm">
      <ul>
        <li><input type="checkbox" id="decoration" name="decoration" /> <label for="decoration">Decoration Items</label> <input type="number" name="budget_decoration" placeholder="Budget" min="0" /></li>
        <li><input type="checkbox" id="dj" name="dj" /> <label for="dj">DJ, Dance & Singing</label> <input type="number" name="budget_dj" placeholder="Budget" min="0" /></li>
        <!-- similarly for all other categories -->
      </ul>
      <label>Name</label>
      <input type="text" id="nameCustom" name="nameCustom" required />
      <label>Mobile Number</label>
      <input type="tel" id="mobileCustom" name="mobileCustom" required />
      <label>Email</label>
      <input type="email" id="emailCustom" name="emailCustom" required />
      <label>Additional Message</label>
      <textarea id="messageCustom" name="messageCustom" rows="3" required></textarea>
      <button type="submit" class="submit-btn">Send Customized Inquiry</button>
    </form>
  </div>

  <div id="premiumTab" class="tab-content" style="display:none;">
    <p>Premium services include:</p>
    <ul>
      <li>Exclusive Venue Booking</li>
      <li>International Catering Options</li>
      <li>DJ Services</li>
      <li>Special Lighting & Effects</li>
      <li>Other premium services</li>
    </ul>
    <form id="eventsPremiumForm">
      <label>Name</label>
      <input type="text" id="namePremium" name="namePremium" required />
      <label>Mobile Number</label>
      <input type="tel" id="mobilePremium" name="mobilePremium" required />
      <label>Email</label>
      <input type="email" id="emailPremium" name="emailPremium" required />
      <label>Message</label>
      <textarea id="messagePremium" name="messagePremium" rows="3" required></textarea>
      <button type="submit" class="submit-btn">Send Premium Inquiry</button>
    </form>
  </div>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Continue similar blocks for Courier, Job, Loans, Tours, Investment, Home Services -->

<script>
function showSection(id) {
  document.getElementById('dashboard').style.display = "none";
  document.querySelectorAll(".section").forEach(s => s.classList.remove("active"));
  document.getElementById(id).classList.add("active");
}
function backToDashboard() {
  document.getElementById('dashboard').style.display = "grid";
  document.querySelectorAll(".section").forEach(s => s.classList.remove("active"));
}
function switchEcommTab(tabId, btn) {
  [...btn.parentNode.children].forEach(b => b.classList.remove("selected"));
  btn.classList.add("selected");
  document.querySelectorAll(".ecomm-tab").forEach(tab => tab.style.display = "none");
  document.getElementById(tabId + "Tab").style.display = "block";
}
function switchEventTab(tabId, btn) {
  [...btn.parentNode.children].forEach(b => b.classList.remove("selected"));
  btn.classList.add("selected");
  ["packageTab", "customizedTab", "premiumTab"].forEach(id => {
    document.getElementById(id).style.display = (id === tabId + "Tab") ? "block" : "none";
  });
}

// Form handlers for WhatsApp message open calls go here
// Apply handlers for all forms as shown in previous code snippets

</script>
</body>
</html>
