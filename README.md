<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Demon Slayer Coin (DSC) – Presale</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #0b0b0b;
      color: #fff;
      text-align: center;
    }

    header {
      background: #1a0000;
      padding: 30px 0;
      box-shadow: 0 0 10px red;
    }

    h1 {
      font-size: 2.5rem;
      margin: 0;
      color: #ff2a2a;
    }

    .logo {
      width: 160px;
      margin-bottom: 15px;
      border-radius: 50%;
      box-shadow: 0 0 20px red;
    }

    .content {
      padding: 40px 20px;
    }

    p {
      font-size: 1.2rem;
      line-height: 1.6;
      max-width: 700px;
      margin: auto;
    }

    .buy-button {
      margin-top: 30px;
      background: red;
      color: white;
      padding: 15px 30px;
      border: none;
      border-radius: 8px;
      font-size: 1.2rem;
      cursor: pointer;
      transition: 0.3s;
    }

    .buy-button:hover {
      background: #cc0000;
    }

    footer {
      background: #111;
      padding: 20px 0;
      color: #aaa;
      margin-top: 50px;
    }
  </style>
</head>
<body>

  <header>
    <img src="https://i.imgur.com/lHeTZVw.png" alt="DSC Logo" class="logo">
    <h1>Demon Slayer Coin (DSC)</h1>
  </header>

  <div class="content">
    <p>Join the exclusive presale of <strong>DSC</strong> – the anime-inspired token on BNB Chain. 🔥</p>

    <p><strong>Price:</strong> 0.000016 BNB per DSC<br>
    <strong>Total Supply:</strong> 1,000,000,000<br>
    <strong>Presale Supply:</strong> 500,000,000</p>

    <button class="buy-button" onclick="buyDSC()">Buy Now with MetaMask</button>
  </div>

  <footer>
    &copy; 2025 Demon Slayer Coin. All rights reserved.
  </footer>

  <script>
    async function buyDSC() {
      if (typeof window.ethereum === 'undefined') {
        alert('Please install MetaMask!');
        return;
      }

      const accounts = await ethereum.request({ method: 'eth_requestAccounts' });
      const user = accounts[0];
      const recipient = "0xE94De7162C73Cb6a774079c5398A80A5C0254cd6"; // Your Wallet
      const amountInBNB = "0.01";

      const tx = {
        from: user,
        to: recipient,
        value: (parseFloat(amountInBNB) * 1e18).toString(16),
      };

      try {
        await ethereum.request({
          method: 'eth_sendTransaction',
          params: [tx],
        });
        alert("Transaction sent successfully!");
      } catch (err) {
        console.error(err);
        alert("Transaction failed!");
      }
    }
  </script>

</body>
</html>
