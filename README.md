<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Financial App</title>

  <!-- Font Awesome -->
  <link rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family: Arial, Helvetica, sans-serif;
    }

    body{
      background:#f3f5f9;
    }

    .container{
      display:flex;
      min-height:100vh;
    }

    /* SIDEBAR */
    .sidebar{
      width:250px;
      background:#1f4c8f;
      color:white;
      padding:20px;
    }

    .logo{
      display:flex;
      align-items:center;
      gap:10px;
      font-size:24px;
      font-weight:bold;
      margin-bottom:40px;
    }

    .menu{
      list-style:none;
    }

    .menu li{
      margin-bottom:15px;
    }

    .menu a{
      text-decoration:none;
      color:white;
      display:flex;
      align-items:center;
      gap:12px;
      padding:12px 15px;
      border-radius:10px;
      transition:0.3s;
    }

    .menu a:hover,
    .menu .active{
      background:#3db27f;
    }

    /* MAIN */
    .main{
      flex:1;
      padding:25px;
    }

    /* TOPBAR */
    .topbar{
      display:flex;
      justify-content:space-between;
      align-items:center;
      margin-bottom:25px;
    }

    .topbar h1{
      font-size:32px;
      color:#222;
    }

    .profile{
      display:flex;
      align-items:center;
      gap:15px;
    }

    .profile img{
      width:40px;
      height:40px;
      border-radius:50%;
    }

    /* ACTION BAR */
    .action-bar{
      display:flex;
      justify-content:space-between;
      align-items:center;
      margin-bottom:20px;
    }

    .btn{
      background:#3db27f;
      color:white;
      border:none;
      padding:12px 20px;
      border-radius:10px;
      cursor:pointer;
      font-size:16px;
    }

    .dropdown{
      padding:10px 15px;
      border-radius:10px;
      border:1px solid #ccc;
      background:white;
    }

    /* CARD */
    .card{
      background:white;
      border-radius:15px;
      padding:20px;
      margin-bottom:20px;
      box-shadow:0 2px 10px rgba(0,0,0,0.05);
    }

    .card h2{
      margin-bottom:20px;
      color:#333;
    }

    .grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:20px;
    }

    .item{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:15px;
      border:1px solid #eee;
      border-radius:10px;
    }

    .item-left{
      display:flex;
      align-items:center;
      gap:15px;
    }

    .icon{
      width:40px;
      height:40px;
      border-radius:10px;
      display:flex;
      justify-content:center;
      align-items:center;
      color:white;
      font-size:18px;
    }

    .brown{ background:#8b5e3c; }
    .yellow{ background:#f5c542; }
    .blue{ background:#3498db; }
    .red{ background:#e57373; }
    .orange{ background:#ff9800; }

    .price{
      font-weight:bold;
      color:#333;
    }

    @media(max-width:768px){
      .container{
        flex-direction:column;
      }

      .sidebar{
        width:100%;
      }

      .grid{
        grid-template-columns:1fr;
      }
    }

  </style>
</head>
<body>

<div class="container">

  <!-- SIDEBAR -->
  <div class="sidebar">
    <div class="logo">
      <i class="fa-solid fa-wallet"></i>
      Financial App
    </div>

    <ul class="menu">
      <li>
        <a href="#" class="active">
          <i class="fa-solid fa-house"></i>
          Dashboard
        </a>
      </li>

      <li>
        <a href="#">
          <i class="fa-solid fa-money-bill-transfer"></i>
          Transactions
        </a>
      </li>

      <li>
        <a href="#">
          <i class="fa-solid fa-chart-column"></i>
          Analisis
        </a>
      </li>

      <li>
        <a href="#">
          <i class="fa-solid fa-layer-group"></i>
          Kategori
        </a>
      </li>

      <li>
        <a href="#">
          <i class="fa-solid fa-bullseye"></i>
          Goals
        </a>
      </li>
    </ul>
  </div>

  <!-- MAIN -->
  <div class="main">

    <!-- TOPBAR -->
    <div class="topbar">
      <h1>Kategori</h1>

      <div class="profile">
        <i class="fa-regular fa-bell"></i>
        <img src="https://i.pravatar.cc/100" alt="">
        <span>Budi Sutanto</span>
      </div>
    </div>

    <!-- ACTION -->
    <div class="action-bar">
      <button class="btn">
        + Add Category
      </button>

      <select class="dropdown">
        <option>Top e-Inibulr</option>
      </select>
    </div>

    <!-- INCOME -->
    <div class="card">
      <h2>Income</h2>

      <div class="grid">

        <div class="item">
          <div class="item-left">
            <div class="icon brown">
              <i class="fa-solid fa-wallet"></i>
            </div>
            <span>Gaji</span>
          </div>

          <div class="price">Rp 5.000.000</div>
        </div>

        <div class="item">
          <div class="item-left">
            <div class="icon yellow">
              <i class="fa-solid fa-gift"></i>
            </div>
            <span>Bonus</span>
          </div>

          <div class="price">Rp 1.200.000</div>
        </div>

      </div>
    </div>

    <!-- EXPENSE -->
    <div class="card">
      <h2>Expense</h2>

      <div class="grid">

        <div class="item">
          <div class="item-left">
            <div class="icon orange">
              <i class="fa-solid fa-burger"></i>
            </div>
            <span>Makanan</span>
          </div>

          <div class="price">Rp 840.000</div>
        </div>

        <div class="item">
          <div class="item-left">
            <div class="icon red">
              <i class="fa-solid fa-bag-shopping"></i>
            </div>
            <span>Belanja</span>
          </div>

          <div class="price">Rp 2.000.000</div>
        </div>

      </div>
    </div>

  </div>

</div>

</body>
</html>
