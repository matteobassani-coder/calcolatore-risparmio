<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calcolatore Risparmio Fumo</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f0f2f5; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .card { background: white; padding: 2rem; border-radius: 20px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); width: 100%; max-width: 400px; text-align: center; }
        h1 { color: #2c3e50; font-size: 1.5rem; }
        .input-group { margin: 20px 0; text-align: left; }
        label { display: block; margin-bottom: 5px; color: #7f8c8d; font-weight: bold; }
        input { width: 100%; padding: 10px; border: 2px solid #ddd; border-radius: 8px; box-sizing: border-box; font-size: 1rem; }
        .result-box { background: #e8f5e9; padding: 20px; border-radius: 12px; margin-top: 20px; border: 1px solid #c8e6c9; }
        .total-amount { display: block; font-size: 2.2rem; color: #2e7d32; font-weight: 800; margin: 10px 0; }
        .message { color: #555; font-style: italic; line-height: 1.4; }
    </style>
</head>
<body>

<div class="card">
    <h1>Quanto potresti risparmiare?</h1>
    
    <div class="input-group">
        <label>Pacchetti al giorno</label>
        <input type="number" id="packs" value="1" step="0.1" oninput="calculate()">
    </div>

    <div class="input-group">
        <label>Prezzo per pacchetto (€)</label>
        <input type="number" id="price" value="6.00" step="0.10" oninput="calculate()">
    </div>

    <div class="result-box">
        <p>In 10 anni avresti accumulato:</p>
        <span id="total" class="total-amount">€ 21.900</span>
        <p id="msg" class="message">Praticamente una Tesla Model 3 nuova di zecca.</p>
    </div>
</div>

<script>
function calculate() {
    const packs = document.getElementById('packs').value;
    const price = document.getElementById('price').value;
    const total = Math.round(packs * price * 365 * 10);
    
    document.getElementById('total').innerText = '€ ' + total.toLocaleString('it-IT');
    
    let msg = "";
    if (total > 40000) msg = "Ti sei perso un piccolo appartamento in provincia o una Tesla.";
    else if (total > 20000) msg = "Praticamente il giro del mondo due volte o un'auto di lusso.";
    else if (total > 10000) msg = "Potevi comprarti una moto nuova o fare 10 vacanze indimenticabili.";
    else msg = "Un bel gruzzolo che avresti potuto investire per il tuo futuro.";
    
    document.getElementById('msg').innerText = msg;
}
</script>

</body>
</html>
