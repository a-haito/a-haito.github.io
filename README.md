
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz sur les énergies solaires</title>
</head>
<body>
    <h1>Quiz sur les énergies solaires programmé par Wafa</h1>
    <form action="#" onsubmit="event.preventDefault(); calculateScore();">

        <h3>Question 1:</h3>
        <p>Quelle est la source d'énergie principale pour la production d'énergie solaire ?</p>
        <input type="radio" name="q1" value="a"> a) Vent<br>
        <input type="radio" name="q1" value="b"> b) Combustibles fossiles<br>
        <input type="radio" name="q1" value="c"> c) Rayonnement solaire<br>
        <input type="radio" name="q1" value="d"> d) Eau<br>

        <h3>Question 2:</h3>
        <p>Quelle technologie est utilisée pour convertir la lumière du soleil en électricité ?</p>
        <input type="radio" name="q2" value="a"> a) Photosynthèse<br>
        <input type="radio" name="q2" value="b"> b) Thermique solaire<br>
        <input type="radio" name="q2" value="c"> c) Photovoltaïque solaire<br>
        <input type="radio" name="q2" value="d"> d) Géothermique<br>

        <h3>Question 3:</h3>
        <p>Quelle est la durée de vie moyenne des panneaux solaires ?</p>
        <input type="radio" name="q3" value="a"> a) 5-10 ans<br>
        <input type="radio" name="q3" value="b"> b) 15-20 ans<br>
        <input type="radio" name="q3" value="c"> c) 25-30 ans<br>
        <input type="radio" name="q3" value="d"> d) 40-50 ans<br>

        <h3>Question 4:</h3>
        <p>Quel matériau est couramment utilisé dans la fabrication des cellules solaires ?</p>
        <input type="radio" name="q4" value="a"> a) Silicium<br>
        <input type="radio" name="q4" value="b"> b) Aluminium<br>
        <input type="radio" name="q4" value="c"> c) Cuivre<br>
        <input type="radio" name="q4" value="d"> d) Fer<br>

        <h3>Question 5:</h3>
        <p>Quelle est la plage d'efficacité des panneaux solaires commerciaux typiques ?</p>
        <input type="radio" name="q5" value="a"> a) 10-15%<br>
        <input type="radio" name="q5" value="b"> b) 20-25%<br>
        <input type="radio" name="q5" value="c"> c) 30-35%<br>
        <input type="radio" name="q5" value="d"> d) 40-45%<br>

        <input type="submit" value="Soumettre">
    </form>

    <div id="result"></div>

    <script>
        function calculateScore() {
            var score = 0;
            var totalQuestions = 5;

            var q1 = document.querySelector('input[name="q1"]:checked');
            var q2 = document.querySelector('input[name="q2"]:checked');
            var q3 = document.querySelector('input[name="q3"]:checked');
            var q4 = document.querySelector('input[name="q4"]:checked');
            var q5 = document.querySelector('input[name="q5"]:checked');

            if (q1 && q1.value === "c") score++;
            if (q2 && q2.value === "c") score++;
            if (q3 && q3.value === "c") score++;
            if (q4 && q4.value === "a") score++;
            if (q5 && q5.value === "a") score++;

            var resultDiv = document.getElementById('result');
            resultDiv.innerHTML = "Votre score est de " + score + "/" + totalQuestions;
        }
    </script>
</body>
</html>
