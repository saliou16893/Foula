<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paris sur la Lutte - Sénégal</title>
    <style>
        /* Styles généraux pour la mise en page */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #3498db;
            color: white;
            padding: 15px;
            text-align: center;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .combat {
            display: flex;
            justify-content: space-between;
            background-color: white;
            padding: 10px;
            margin: 10px 0;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
        }

        .combat .details {
            width: 60%;
        }

        .combat .cotes {
            width: 35%;
            text-align: center;
        }

        .combat .cotes button {
            background-color: #3498db;
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
            margin: 5px;
            width: 100px;
        }

        .combat .cotes button:hover {
            background-color: #2980b9;
        }

        footer {
            background-color: #2c3e50;
            color: white;
            padding: 10px;
            text-align: center;
        }

        /* Styles pour les formulaires */
        form input {
            padding: 10px;
            margin: 10px 0;
            width: 100%;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        form button {
            padding: 10px;
            background-color: #3498db;
            color: white;
            border: none;
            width: 100%;
            cursor: pointer;
        }

        form button:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>

<header>
    <h1>Paris sur les Combats de Lutte - Sénégal</h1>
</header>

<div class="container">
    <h2>Combats en Cours</h2>

    <!-- Combat 1 -->
    <div class="combat">
        <div class="details">
            <h3>Bala Gaye 2 vs Tapha Tine</h3>
            <p>Le combat de lutte populaire au Sénégal. Qui sera le champion ?</p>
        </div>
        <div class="cotes">
            <h3>Cotes</h3>
            <button id="bet1">Bala Gaye 2: 1.80</button>
            <button id="bet2">Tapha Tine: 2.10</button>
        </div>
    </div>

    <!-- Combat 2 -->
    <div class="combat">
        <div class="details">
            <h3>Modou Lô vs Eumeu Sène</h3>
            <p>Un combat très attendu entre ces deux géants de la lutte sénégalaise !</p>
        </div>
        <div class="cotes">
            <h3>Cotes</h3>
            <button id="bet3">Modou Lô: 1.95</button>
            <button id="bet4">Eumeu Sène: 2.00</button>
        </div>
    </div>

    <!-- Formulaire de paiement -->
    <h2>Paiement via Wave</h2>
    <form id="paymentForm">
        <input type="number" id="amount" placeholder="Montant (en XOF)" required>
        <input type="text" id="waveNumber" placeholder="Numéro Wave" required>
        <button type="submit">Effectuer le paiement</button>
    </form>
</div>

<footer>
    <p>© 2024 Paris Lutte Sénégal - Tous droits réservés</p>
</footer>

<script>
    let selectedBet = "";

    // Gestion des paris
    function handleBet(bet) {
        selectedBet = bet;
        alert("Vous avez choisi de parier sur: " + bet);
    }

    // Événements de clic pour les paris
    document.getElementById("bet1").addEventListener("click", function() { handleBet("Bala Gaye 2"); });
    document.getElementById("bet2").addEventListener("click", function() { handleBet("Tapha Tine"); });
    document.getElementById("bet3").addEventListener("click", function() { handleBet("Modou Lô"); });
    document.getElementById("bet4").addEventListener("click", function() { handleBet("Eumeu Sène"); });
</script>

</body>
</html>
