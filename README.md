# drone_ui<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rescue Drone App</title>
  <style>
    body {
      background: #f0f0f0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }

    /* Phone mockup */
    .phone {
      width: 380px;
      height: 760px;
      background: #111;
      border-radius: 40px;
      padding: 20px;
      box-shadow: 0 10px 40px rgba(0,0,0,0.5);
      border: 10px solid #222;
      position: relative;
      overflow: hidden;
    }

    .phone::before {
      content: "";
      width: 120px;
      height: 25px;
      background: #222;
      border-radius: 12px;
      position: absolute;
      top: 10px;
      left: 50%;
      transform: translateX(-50%);
    }

    .app {
      width: 100%;
      height: 100%;
      background: #000;
      border-radius: 25px;
      overflow-y: auto;
      padding: 20px;
      color: #fff;
    }

    h2 {
      text-align: center;
      color: #00ff99;
      margin-bottom: 10px;
    }

    .status {
      background: #111;
      padding: 15px;
      border-radius: 12px;
      margin-bottom: 20px;
    }

    .status p {
      margin: 5px 0;
    }

    .btn {
      display: block;
      padding: 15px;
      border-radius: 12px;
      margin: 10px 0;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
      text-align: center;
    }

    .live { background: #0f5132; }
    .stats { background: #0d6efd; }
    .thermal { background: #6610f2; }
    .ai { background: #fd7e14; }
    .manual { background: #6f42c1; }

    .actions {
      display: flex;
      justify-content: space-between;
      margin-top: 15px;
    }

    .start { background: #198754; flex: 1; margin-right: 5px; }
    .emergency { background: #dc3545; flex: 1; margin-left: 5px; }

    /* Thermal Mode */
    .thermal-mode {
      background: #111;
      border-radius: 12px;
      padding: 15px;
      margin-top: 15px;
      text-align: center;
    }

    .thermal-img {
      width: 100%;
      border-radius: 10px;
      margin-top: 10px;
      background: linear-gradient(135deg, #ff0000, #ffa500, #ffff00, #00ff00, #0000ff, #4b0082, #8a2be2);
      height: 200px;
    }

    @media (max-width: 500px) {
      .phone {
        width: 95%;
        height: 90vh;
      }
    }
  </style>
</head>
<body>
  <div class="phone">
    <div class="app">
      <h2>RESCUE DRONE</h2>
      <div class="status">
        <p>🚁 Drone Connected</p>
        <p>📡 GPS Active</p>
        <p>🤖 AI Detection Ready</p>
      </div>

      <div class="btn live">📷 Live Camera</div>
      <div class="btn stats">📊 Flight Stats</div>
      <div class="btn thermal">🌡️ GPS & Thermal</div>

      <!-- Thermal mode tab -->
      <div class="thermal-mode">
        <h3>Thermal Imaging</h3>
        <p>Navigation & Rescue Heat Map</p>
        <div class="thermal-img"></div>
      </div>

      <div class="btn ai">🛰️ AI Detection</div>
      <div class="btn manual">🎮 Manual Control</div>

      <div class="actions">
        <div class="btn start">Start Mission</div>
        <div class="btn emergency">Emergency</div>
      </div>
    </div>
  </div>
</body>
</html>
