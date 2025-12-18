# konsultasiJadwalolahraga
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <title>Jualan Baju murah</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: #222;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .card {
      background: #ffffff;
      padding: 30px;
      border-radius: 15px;
      width: 400px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.25);
    }
    h1 {
      text-align: center;
      margin-bottom: 20px;
      color: #e83e8c;
    }
    input, button {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      border-radius: 5px;
      border: none;
    }
    input {
      background: #2b2b2b;
      color: #fff;
    }
    button {
      cursor: pointer;
      font-weight: bold;
    }
    .btn-primary { background: #0d6efd; color: #fff; }
    .btn-green { background: #198754; color: #fff; }
    .btn-yellow { background: #ffc107; color: #000; }
    .hidden { display: none; }
    .product {
      border: 2px solid #dee2e6;
      padding: 15px;
      border-radius: 12px;
      margin-bottom: 15px;
      background: linear-gradient(135deg, #fdfbfb, #ebedee);
    }
    .price {
      color: #198754;
      font-weight: bold;
      font-size: 16px;
    }
  </style>
</head>
<body>

<div class="card" id="loginPage">
  <h1>Jualan Baju murah</h1>
  <input type="text" id="username" placeholder="Username" />
  <input type="password" id="password" placeholder="Password" />
  <button class="btn-primary" onclick="submitLogin()">Submit</button>
</div>

<div class="card" id="etalasePage" style="display:none;">
  <h1>Etalase Produk</h1>

  <div class="product">
    <h3>Produk 1</h3>
    <img src="https://via.placeholder.com/300x300/ff6f91/ffffff?text=Baju+Produk+1" alt="Produk 1" style="width:100%;border-radius:10px;margin-bottom:10px;" />
    <p class="price">Harga: Rp 25.000</p>
    <button class="btn-green" onclick="buyProduct(1)">Buy Product 1</button>
  </div>

  <div class="product">
    <h3>Produk 2</h3>
    <img src="https://via.placeholder.com/300x300/6f42c1/ffffff?text=Baju+Produk+2" alt="Produk 2" style="width:100%;border-radius:10px;margin-bottom:10px;" />
    <p class="price">Harga: Rp 15.000</p>
    <button class="btn-yellow" onclick="buyProduct(2)">Buy Product 2</button>
  </div>
</div>

<script>
  function submitLogin() {
    const username = document.getElementById('username').value.trim();
    const password = document.getElementById('password').value.trim();

    if (!username || !password) {
      alert('All data is required');
      return;
    }

    console.log('Collect Data to database:', { username, password });
    alert('Data has been submitted');

    document.getElementById('loginPage').style.display = 'none';
    document.getElementById('etalasePage').style.display = 'block';
  }

  function buyProduct(productId) {
    const confirmBuy = confirm('Please click buy for transaction');

    if (confirmBuy) {
      let message = '';
      if (productId === 1) {
        message = 'Halo Admin, saya ingin konsultasi Produk 1 (Rp 25.000)';
      } else {
        message = 'Halo Admin, saya ingin konsultasi Produk 2 (Rp 15.000)';
      }

      const phone = '6285785218016';
      const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
      window.location.href = url;
    } else {
      alert('Canceled confirmation');
    }
  }
</script>

</body>
</html>
