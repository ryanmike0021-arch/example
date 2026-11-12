
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>ELYZ</title>

<style>
* {box-sizing:border-box}
body {
    margin:0;
    font-family:Arial;
    background:#f1f7fa;
}
header {
    background:#087db5;
    color:white;
    padding:20px;
    text-align:center;
}
.container {padding:20px}
.dashboard {
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
    gap:15px;
}
.card,.section {
    background:white;
    padding:18px;
    border-radius:10px;
    margin-bottom:15px;
    box-shadow:0 2px 5px #ccc;
}
.card {text-align:center}
.card h2 {color:#087db5}
input,select {
    width:100%;
    padding:11px;
    margin:6px 0;
    border:1px solid #ccc;
    border-radius:5px;
}
button {
    background:#087db5;
    color:white;
    border:0;
    padding:10px 15px;
    border-radius:5px;
    cursor:pointer;
}
.paid {color:green;font-weight:bold}
.unpaid {color:red;font-weight:bold}
table {
    width:100%;
    border-collapse:collapse;
    min-width:650px;
    margin-top:12px;
}
th,td {
    padding:10px;
    border:1px solid #ddd;
    text-align:left;
}
th {background:#087db5;color:white}
.table-container {overflow-x:auto}
.small-btn {background:#198754;padding:7px}
</style>
</head>

<body>

<header>
<h1>ELYZ WATER</h1>
<p>kay peppa</p>
</header>

<div class="container">

<h2>Dashboard</h2>

<div class="dashboard">

<div class="card">
<h3>Kinita</h3>
<h2 id="sales">₱0.00</h2>
</div>

<div class="card">
<h3>Slim Gallon</h3>
<h2 id="slim">0</h2>
</div>

<div class="card">
<h3>Round Gallon</h3>
<h2 id="round">0</h2>
</div>

<div class="card">
<h3>350ml Bottle</h3>
<h2 id="b350">0</h2>
</div>

<div class="card">
<h3>500ml Bottle</h3>
<h2 id="b500">0</h2>
</div>

<div class="card">
<h3>Unpaid Balance</h3>
<h2 id="unpaid">₱0.00</h2>
</div>

<div class="card">
<h3>Total Customers</h3>
<h2 id="customerCount">0</h2>
</div>

</div>

<!-- INVENTORY -->

<div class="section">
<h2> Inventory</h2>

<label>Slim Gallon Stock</label>
<input type="number" id="addSlim" min="0" placeholder="Add slim gallons">

<label>Round Gallon Stock</label>
<input type="number" id="addRound" min="0" placeholder="Add round gallons">

<label>350ml Bottle Stock</label>
<input type="number" id="add350" min="0" placeholder="Add 350ml bottles">

<label>500ml Bottle Stock</label>
<input type="number" id="add500" min="0" placeholder="Add 500ml bottles">

<button onclick="updateInventory()">Add Inventory</button>
</div>

<!-- SALES -->

<div class="section">
<h2> Bagong Customer</h2>

<label>Customer Name</label>
<input id="customer" placeholder="Customer Name">

<label>Contact Number</label>
<input id="contact" placeholder="Contact Number">

<label>Product</label>
<select id="product">
<option value="slim">Slim Gallon</option>
<option value="round">Round Gallon</option>
<option value="b350">350ml Bottle</option>
<option value="b500">500ml Bottle</option>
</select>

<label>Quantity</label>
<input type="number" id="quantity" min="1" placeholder="Quantity">

<label>Price per Item</label>
<input type="number" id="price" min="0.01" step="0.01" placeholder="Price">

<label>Payment Status</label>
<select id="payment">
<option value="Unpaid">Unpaid</option>
<option value="Paid">Paid</option>
</select>

<button onclick="addSale()">Save Sale</button>
</div>

<!-- CUSTOMER LIST -->

<div class="section">
<h2> List</h2>

<input id="customerSearch"
placeholder="Search Customer..."
oninput="displayCustomers()">

<div class="table-container">
<table>
<thead>
<tr>
<th>Customer</th>
<th>Contact</th>
<th>Transactions</th>
<th>Total Purchases</th>
<th>Unpaid</th>
</tr>
</thead>
<tbody id="customerRecords"></tbody>
</table>
</div>
</div>

<!-- SALES RECORDS -->

<div class="section">
<h2> Benta</h2>

<input id="salesSearch"
placeholder="Search Customer or Product..."
oninput="displayRecords()">

<div class="table-container">
<table>
<thead>
<tr>
<th>Date</th>
<th>Customer</th>
<th>Product</th>
<th>Qty</th>
<th>Total</th>
<th>Payment</th>
<th>Action</th>
</tr>
</thead>
<tbody id="records"></tbody>
</table>
</div>
</div>

</div>

<script>

// INVENTORY DATA

let inventory = JSON.parse(
localStorage.getItem("waterInventory")
) || {
    slim:0,
    round:0,
    b350:0,
    b500:0
};

let salesRecords = JSON.parse(
localStorage.getItem("waterSales")
) || [];

// PRODUCT NAMES

const productNames = {
    slim:"Slim Gallon",
    round:"Round Gallon",
    b350:"350ml Bottle",
    b500:"500ml Bottle"
};

// SAVE DATA

function saveData() {
    localStorage.setItem(
        "waterInventory",
        JSON.stringify(inventory)
    );

    localStorage.setItem(
        "waterSales",
        JSON.stringify(salesRecords)
    );

    displayData();
}

// ADD INVENTORY

function updateInventory() {

    let fields = ["slim","round","b350","b500"];
    let inputs = ["addSlim","addRound","add350","add500"];

    let values = inputs.map(id => {
        let value = document.getElementById(id).value;
        return value === "" ? 0 : Number(value);
    });

    if (values.some(v => !Number.isInteger(v) || v < 0)) {
        alert("Enter valid whole-number quantities.");
        return;
    }

    if (values.every(v => v === 0)) {
        alert("Enter at least one inventory quantity.");
        return;
    }

    fields.forEach((field,index) => {
        inventory[field] += values[index];
        document.getElementById(inputs[index]).value = "";
    });

    saveData();
    alert("Inventory successfully updated!");
}

// ADD SALE

function addSale() {

    let customer = document.getElementById("customer").value.trim();
    let contact = document.getElementById("contact").value.trim();
    let product = document.getElementById("product").value;
    let quantity = Number(document.getElementById("quantity").value);
    let price = Number(document.getElementById("price").value);
    let payment = document.getElementById("payment").value;

    if (!customer || !Number.isInteger(quantity) ||
        quantity <= 0 || !Number.isFinite(price) || price <= 0) {
        alert("Complete all required information.");
        return;
    }

    if (inventory[product] < quantity) {
        alert("Not enough stock for " + productNames[product] + "!");
        return;
    }

    inventory[product] -= quantity;

    let total = quantity * price;

    salesRecords.push({
        id: Date.now() + Math.random(),
        date: new Date().toLocaleDateString(),
        customer,
        contact,
        product: productNames[product],
        quantity,
        total,
        payment
    });

    saveData();

    document.getElementById("customer").value = "";
    document.getElementById("contact").value = "";
    document.getElementById("quantity").value = "";
    document.getElementById("price").value = "";

    alert("Sale successfully saved!");
}

// MARK AS PAID

function markPaid(index) {
    if (confirm("Mark this transaction as PAID?")) {
        salesRecords[index].payment = "Paid";
        saveData();
    }
}

// CUSTOMER LIST

function displayCustomers() {

    let search = document.getElementById("customerSearch")
        .value.toLowerCase();

    let customers = {};

    salesRecords.forEach(sale => {

        let name = sale.customer;

        if (!customers[name]) {
            customers[name] = {
                contact:sale.contact || "",
                transactions:0,
                purchases:0,
                unpaid:0
            };
        }

        customers[name].transactions++;
        customers[name].purchases += sale.total;

        if (sale.payment === "Unpaid") {
            customers[name].unpaid += sale.total;
        }

        if (!customers[name].contact && sale.contact) {
            customers[name].contact = sale.contact;
        }
    });

    let output = "";

    Object.keys(customers).forEach(name => {

        if (!name.toLowerCase().includes(search)) return;

        let c = customers[name];

        output += `
        <tr>
        <td>${escapeHTML(name)}</td>
        <td>${escapeHTML(c.contact)}</td>
        <td>${c.transactions}</td>
        <td>₱${c.purchases.toFixed(2)}</td>
        <td class="${c.unpaid > 0 ? 'unpaid':'paid'}">
        ₱${c.unpaid.toFixed(2)}
        </td>
        </tr>`;
    });

    document.getElementById("customerRecords").innerHTML =
        output || "<tr><td colspan='5'>No customers found.</td></tr>";
}

// SALES RECORDS

function displayRecords() {

    let search = document.getElementById("salesSearch")
        .value.toLowerCase();

    let output = "";

    salesRecords.forEach((sale,index) => {

        let text = (sale.customer + " " + sale.product).toLowerCase();

        if (!text.includes(search)) return;

        output += `
        <tr>
        <td>${escapeHTML(sale.date)}</td>
        <td>${escapeHTML(sale.customer)}</td>
        <td>${escapeHTML(sale.product)}</td>
        <td>${sale.quantity}</td>
        <td>₱${sale.total.toFixed(2)}</td>
        <td class="${sale.payment === 'Paid'?'paid':'unpaid'}">
        ${sale.payment}
        </td>
        <td>
        ${sale.payment === "Unpaid"
        ? `<button class="small-btn" onclick="markPaid(${index})">Mark Paid</button>`
        : "✓ Paid"}
        </td>
        </tr>`;
    });

    document.getElementById("records").innerHTML =
        output || "<tr><td colspan='7'>No records found.</td></tr>";
}

// ESCAPE TEXT

function escapeHTML(value) {
    return String(value).replace(/[&<>"']/g, c => ({
        "&":"&amp;","<":"&lt;",">":"&gt;",
        '"':"&quot;","'":"&#39;"
    })[c]);
}

// DASHBOARD

function displayData() {

    let totalSales = 0;
    let unpaid = 0;

    salesRecords.forEach(sale => {
        totalSales += sale.total;
        if (sale.payment === "Unpaid") {
            unpaid += sale.total;
        }
    });

    document.getElementById("sales").innerText =
        "₱" + totalSales.toFixed(2);

    document.getElementById("slim").innerText = inventory.slim;
    document.getElementById("round").innerText = inventory.round;
    document.getElementById("b350").innerText = inventory.b350;
    document.getElementById("b500").innerText = inventory.b500;

    document.getElementById("unpaid").innerText =
        "₱" + unpaid.toFixed(2);

    document.getElementById("customerCount").innerText =
        new Set(salesRecords.map(s => s.customer)).size;

    displayCustomers();
    displayRecords();
}

displayData();

</script>

</body>
</html>
