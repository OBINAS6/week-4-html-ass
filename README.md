# week-4-html-ass


http://127.0.0.1:3000/week%204%20css%20assigment.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Flexbox/Grid Page</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
    }

    /* Navigation */
    nav {
      background-color: #333;
      color: white;
      padding: 1rem;
    }

    nav ul {
      display: flex;
      justify-content: space-around;
      list-style: none;
    }

    nav ul li {
      cursor: pointer;
    }

    /* Main layout using Grid */
    .container {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
      gap: 1rem;
      padding: 1rem;
    }

    .box {
      background-color: #f2f2f2;
      padding: 1rem;
      border-radius: 8px;
    }

    /* Media Queries */
    @media (max-width: 768px) {
      .container {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 480px) {
      nav ul {
        flex-direction: column;
        align-items: center;
      }

      .container {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <nav>
    <ul>
      <li>Home</li>
      <li>About</li>
      <li>Services</li>
      <li>Contact</li>
    </ul>
  </nav>

  <div class="container">
    <div class="box">Sidebar</div>
    <div class="box">Main Content</div>
    <div class="box">Extra Info</div>
  </div>
</body>
</html>
