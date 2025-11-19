<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>777 Level Up | BGMI & Free Fire Top-Up</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      min-height: 100vh;
      background: radial-gradient(circle at top, #111827 0, #020617 45%, #000 100%);
      color: #f9fafb;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      font-size: 16px;
    }

    .container {
      width: 100%;
      max-width: 520px;
      background: rgba(15, 23, 42, 0.96);
      border-radius: 18px;
      padding: 20px 20px 24px;
      box-shadow: 0 18px 45px rgba(0, 0, 0, 0.75);
      border: 1px solid rgba(148, 163, 184, 0.25);
      backdrop-filter: blur(10px);
    }

    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 14px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-logo {
      width: 34px;
      height: 34px;
      border-radius: 12px;
      background: radial-gradient(circle at top, #22c55e, #15803d);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #020617;
      font-weight: 800;
      font-size: 16px;
    }

    .brand-title {
      font-size: 20px;
      font-weight: 700;
    }

    .brand-sub {
      font-size: 11px;
      color: #9ca3af;
    }

    .badge {
      font-size: 11px;
      padding: 4px 9px;
      border-radius: 999px;
      background: rgba(34, 197, 94, 0.16);
      color: #22c55e;
      border: 1px solid rgba(34, 197, 94, 0.5);
    }

    .tagline {
      font-size: 15px;
      color: #9ca3af;
      margin-bottom: 12px;
    }

    #gameLogoBox {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 10px;
    }

    #gameLogo {
      width: 26px;
      height: 26px;
      border-radius: 6px;
      object-fit: cover;
    }

    #gameLogoText {
      font-size: 12px;
      color: #9ca3af;
    }

    label {
      font-size: 15px;
      margin-bottom: 6px;
      display: block;
    }

    input,
    select {
      width: 100%;
      padding: 13px 15px;
      border-radius: 10px;
      border: 1px solid #1f2937;
      background: #020617;
      color: #e5e7eb;
      margin-bottom: 14px;
      outline: none;
      font-size: 15px;
    }

    input:focus,
    select:focus {
      border-color: #3b82f6;
      box-shadow: 0 0 0 1px rgba(59, 130, 246, 0.4);
    }

    .warning {
      font-size: 12px;
      color: #f97316;
      margin-bottom: 4px;
    }

    .pill-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 12px;
      margin-bottom: 8px;
    }

    .pill {
      padding: 12px 12px 10px;
      border-radius: 14px;
      border: 1px solid #111827;
      background: #020617;
      cursor: pointer;
      transition: transform 0.18s ease, box-shadow 0.18s ease,
                  border-color 0.18s ease, background 0.18s ease;
      font-size: 12px;
      position: relative;
      overflow: hidden;
    }

    .pill-title {
      font-weight: 600;
      margin-bottom: 2px;
      font-size: 14px;
    }

    .pill-meta {
      font-size: 13px;
      color: #9ca3af;
    }

    .pill-price {
      font-size: 14px;
      margin-top: 4px;
      color: #22c55e;
      font-weight: 600;
    }

    .pill.active {
      border-color: #22c55e;
      background: radial-gradient(circle at top left, rgba(34,197,94,0.18), #020617);
    }

    .pill:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px rgba(15, 23, 42, 0.7);
    }

    .pill.demo-offer {
      border-color: #facc15;
      box-shadow: 0 0 15px rgba(250, 204, 21, 0.35);
      animation: pulseGlow 1.8s infinite alternate;
    }

    .pill.demo-offer::before {
      content: "OFFER";
      position: absolute;
      top: -6px;
      left: -6px;
      font-size: 9px;
      background: #facc15;
      color: #1f2937;
      padding: 2px 6px;
      border-radius: 999px;
      font-weight: 700;
    }

    @keyframes pulseGlow {
      from {
        transform: translateY(0);
        box-shadow: 0 0 10px rgba(250, 204, 21, 0.25);
      }
      to {
        transform: translateY(-2px);
        box-shadow: 0 0 18px rgba(250, 204, 21, 0.55);
      }
    }

    .summary {
      margin-top: 8px;
      padding: 10px 12px;
      border-radius: 10px;
      background: #020617;
      border: 1px dashed rgba(148, 163, 184, 0.5);
      font-size: 13px;
      color: #e5e7eb;
      transition: background 0.2s ease, border-color 0.2s ease;
    }

    .summary.flash {
      border-color: #22c55e;
    }

    .summary strong {
      color: #22c55e;
    }

    .total-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 10px;
      font-size: 14px;
    }

    .total-label {
      color: #9ca3af;
    }

    .total-amount {
      font-size: 16px;
      font-weight: 700;
    }

    .info {
      margin-top: 8px;
      font-size: 13px;
      color: #9ca3af;
      line-height: 1.4;
    }

    .btn-primary {
      width: 100%;
      margin-top: 14px;
      padding: 11px 14px;
      border-radius: 999px;
      border: none;
      background: linear-gradient(135deg, #22c55e, #16a34a);
      color: #020617;
      font-weight: 700;
      font-size: 14px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      transition: 0.15s;
    }

    .btn-primary:hover {
      filter: brightness(1.06);
      transform: translateY(-1px);
      box-shadow: 0 10px 25px rgba(34, 197, 94, 0.35);
    }

    .btn-subtext {
      font-size: 11px;
      color: rgba(15,23,42,0.9);
    }

    .disclaimer {
      margin-top: 10px;
      font-size: 11px;
      color: #6b7280;
      line-height: 1.4;
    }

    #playerError {
      font-size: 11px;
      margin-top: -8px;
      margin-bottom: 8px;
      display: none;
    }

    #formError {
      margin-top: 8px;
      font-size: 11px;
      color: #f97316;
      display: none;
    }

    .input-error {
      border-color: #ef4444 !important;
      box-shadow: 0 0 0 1px rgba(239, 68, 68, 0.4);
    }

    .input-success {
      border-color: #22c55e !important;
      box-shadow: 0 0 0 1px rgba(34, 197, 94, 0.4);
    }

    @media (max-width: 480px) {
      .container {
        padding: 16px 14px 20px;
      }
      .brand-title {
        font-size: 18px;
      }
      .pill-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="header">
      <div class="brand">
        <div class="brand-logo">77</div>
        <div>
          <div class="brand-title">777 Level Up</div>
          <div class="brand-sub">BGMI & Free Fire UC / Diamonds</div>
        </div>
      </div>
      <div class="badge">Direct Top-Up</div>
    </div>

    <div id="gameLogoBox">
      <img id="gameLogo" src="bgmi-logo.jpg" alt="Game Logo">
      <span id="gameLogoText">BGMI UC</span>
    </div>

    <p class="tagline">
      Step 1: Game & Player ID fill karein · Step 2: Pack choose karein · Step 3: Payment & UTR Google Form pe complete karein.
    </p>

    <label for="game">Select Game</label>
    <select id="game">
      <option value="BGMI">BGMI</option>
      <option value="Free Fire">Free Fire</option>
    </select>

    <p class="warning">
      Please enter correct Player ID and check again – galat ID par top-up wapas nahi hoga.
    </p>

    <label for="playerId">Player ID / UID</label>
    <input type="text" id="playerId" placeholder="Enter your in-game Player ID / UID">
    <p id="playerError"></p>

    <label>Choose Pack (Demo + Regular)</label>

    <div class="pill-grid" id="packsGrid"></div>

    <div class="summary" id="summaryBox">
      Selected — <strong>None</strong><br>
      Total: ₹0
    </div>

    <div class="total-row">
      <span class="total-label">Total Payable</span>
      <span class="total-amount" id="totalAmount">₹0</span>
    </div>

    <p class="info">
      Player ID/UID dhyaan se check karein. Hum kabhi bhi password ya OTP nahi maangte.
    </p>

    <button class="btn-primary" type="button" id="continueBtn">
      Proceed to Payment Form
      <span class="btn-subtext">(Google Form)</span>
    </button>

    <div id="formError"></div>

    <p class="disclaimer">
      This website is not affiliated with or endorsed by BGMI, Garena or any other game publishers. Delivery time may vary during peak events or server issues.
    </p>
  </div>

  <script>
    const packsBase = [
      { id: 1,  name: "Demo Pack", amount: 29,
        uc: "🎯 60 UC",
        diamonds: "💎 100 Diamonds",
        note: "Try service – cheap test pack" },

      { id: 2,  name: "Demo Plus", amount: 99,
        uc: "🎯 240 UC",
        diamonds: "💎 200 Diamonds",
        note: "Starter value pack" },

      { id: 3,  name: "Basic Pack", amount: 600,
        uc: "🎯 2100 UC",
        diamonds: "💎 2100 Diamonds",
        note: "Perfect for regular top-up" },

      { id: 4,  name: "Pro Pack", amount: 900,
        uc: "🎯 4100 UC",
        diamonds: "💎 4100 Diamonds",
        note: "For heavy players" },

      { id: 5,  name: "Elite Pack", amount: 1400,
        uc: "🎯 5900 UC",
        diamonds: "💎 5900 Diamonds",
        note: "Events & crates" },

      { id: 6,  name: "Mega Pack", amount: 2000,
        uc: "🎯 8800 UC",
        diamonds: "💎 8800 Diamonds",
        note: "Big push pack" },

      { id: 7,  name: "Legend Pack", amount: 2400,
        uc: "🎯 10000 UC",
        diamonds: "💎 10000 Diamonds",
        note: "Max value combo" }
    ];

    const packsGrid      = document.getElementById('packsGrid');
    const summaryBox     = document.getElementById('summaryBox');
    const totalAmountEl  = document.getElementById('totalAmount');
    const continueBtn    = document.getElementById('continueBtn');
    const playerIdInput  = document.getElementById('playerId');
    const gameSelect     = document.getElementById('game');
    const gameLogo       = document.getElementById('gameLogo');
    const gameLogoText   = document.getElementById('gameLogoText');
    const playerErrorEl  = document.getElementById('playerError');
    const formErrorEl    = document.getElementById('formError');

    let selectedPack = null;

    function isValidBgmiId(id) {
      const onlyDigits = /^[0-9]+$/.test(id);
      return onlyDigits && id.length === 11;
    }

    function showError(msg) {
      formErrorEl.textContent = msg;
      formErrorEl.style.display = msg ? 'block' : 'none';
    }

    function clearError() {
      showError('');
    }

    function showPlayerError(msg, success = false) {
      playerErrorEl.textContent = msg;
      playerErrorEl.style.display = msg ? 'block' : 'none';
      playerErrorEl.style.color = success ? '#22c55e' : '#f97316';
    }

    function getDisplayAmount(pack) {
      const game = gameSelect.value;
      return game === "Free Fire" ? pack.diamonds : pack.uc;
    }

    function renderPacks() {
      packsGrid.innerHTML = "";
      packsBase.forEach(pack => {
        const div = document.createElement('div');

        if (pack.id === 1 || pack.id === 2) {
          div.className = 'pill demo-offer';
        } else {
          div.className = 'pill';
        }

        const displayAmount = getDisplayAmount(pack);

        div.innerHTML = `
          <div class="pill-title">${pack.name}</div>
          <div class="pill-meta">${displayAmount}</div>
          <div class="pill-price">₹${pack.amount}</div>
        `;

        div.addEventListener('click', () => {
          document.querySelectorAll('.pill').forEach(p => p.classList.remove('active'));
          div.classList.add('active');

          selectedPack = { ...pack };

          summaryBox.classList.remove('flash');
          void summaryBox.offsetWidth;
          summaryBox.classList.add('flash');

          summaryBox.innerHTML = `
            Selected — <strong>${selectedPack.name} (${getDisplayAmount(selectedPack)})</strong><br>
            Note: ${selectedPack.note}<br>
            Total: ₹${selectedPack.amount}
          `;

          totalAmountEl.textContent = '₹' + selectedPack.amount;
        });

        packsGrid.appendChild(div);
      });
    }

    renderPacks();

    // Live UID validation (BGMI only)
    playerIdInput.addEventListener('input', () => {
      const val = playerIdInput.value.trim();

      playerIdInput.classList.remove('input-error', 'input-success');
      showPlayerError('');

      if (gameSelect.value !== "BGMI") return;
      if (!val) return;

      if (!/^[0-9]*$/.test(val)) {
        playerIdInput.classList.add('input-error');
        showPlayerError('Sirf numbers allow hain (0–9).');
        return;
      }

      if (val.length < 11) {
        playerIdInput.classList.add('input-error');
        showPlayerError('BGMI UID exactly 11 ank ka hota hai. Abhi ' + val.length + ' hain.');
        return;
      }

      if (val.length > 11) {
        playerIdInput.classList.add('input-error');
        showPlayerError('11 se zyada digits nahi hone chahiye.');
        return;
      }

      playerIdInput.classList.add('input-success');
      showPlayerError('UID sahi lag rahi hai.', true);
    });

    gameSelect.addEventListener('change', () => {
      renderPacks();
      selectedPack = null;
      summaryBox.innerHTML = `
        Selected — <strong>None</strong><br>
        Total: ₹0
      `;
      totalAmountEl.textContent = '₹0';

      playerIdInput.classList.remove('input-error', 'input-success');
      showPlayerError('');
      clearError();

      if (gameSelect.value === "BGMI") {
        gameLogo.src  = "bgmi-logo.jpg";
        gameLogoText.textContent = "BGMI UC";
      } else {
        gameLogo.src  = "freefire-logo.png";
        gameLogoText.textContent = "Free Fire Diamonds";
      }
    });

    // CONTINUE BUTTON -> direct Google Form (pre-filled)
    continueBtn.addEventListener('click', () => {
      clearError();
      showPlayerError('');

      const playerId = playerIdInput.value.trim();
      const game     = gameSelect.value;

      if (!playerId) {
        showPlayerError('Please enter your Player ID / UID.');
        playerIdInput.classList.add('input-error');
        return;
      }

      if (game === "BGMI" && !isValidBgmiId(playerId)) {
        showPlayerError('BGMI UID sirf 11 ank ka number hota hai.');
        playerIdInput.classList.add('input-error');
        return;
      }

      if (!selectedPack) {
        showError('Please select a pack first.');
        return;
      }

      const baseUrl = "https://docs.google.com/forms/d/e/1FAIpQLScahD73ISvPY0GNSIR83jy15wgr1_arNXvjkNEk2HOer1TkZA/viewform?usp=pp_url";

      const gameVal      = encodeURIComponent(game);
      const playerVal    = encodeURIComponent(playerId);
      const packVal      = encodeURIComponent(selectedPack.name);
      const amountStrVal = encodeURIComponent(getDisplayAmount(selectedPack));
      const amountRsVal  = encodeURIComponent(selectedPack.amount.toString());
      const timeVal      = encodeURIComponent(new Date().toLocaleString());

      const url =
        baseUrl +
        "&entry.96667261="  + gameVal +
        "&entry.101739645=" + playerVal +
        "&entry.989959081=" + packVal +
        "&entry.446374616=" + amountStrVal +
        "&entry.675822869=" + amountRsVal +
        "&entry.2032042513="+ timeVal;

      window.location.href = url;
    });
  </script>

</body>
</html>
