# sa-et-ça
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercices - Sa vs Ça</title>
    <style>
        .correct { color: green; }
        .incorrect { color: red; }
        .feedback { margin-top: 5px; }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["ça", "sa", "sa", "ça", "sa", "ça", "sa", "ça", "sa", "ça", "ça", "sa", "ça", "sa", "ça", "ça", "sa", "ça", "sa", "ça"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✔️ Correct";
                    feedback.className = "correct feedback";
                    score++;
                } else {
                    feedback.innerText = `❌ Incorrect. La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "ça" est un pronom démonstratif (cela), tandis que "sa" est un déterminant possessif.`;
                    feedback.className = "incorrect feedback";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>
<body>
    <h2>Exercices - Complétez avec "sa" ou "ça"</h2>

    <p><strong>Règle :</strong> "Ça" est un pronom démonstratif qui peut être remplacé par "cela". "Sa" est un déterminant possessif utilisé pour indiquer que quelque chose appartient à quelqu'un (équivalent de "son" mais au féminin).</p>

    <form>
        <ol>
            <li>___ va être difficile. <input type="text" id="reponse1"> <span id="feedback1"></span></li>
            <li>Elle a oublié ___ valise. <input type="text" id="reponse2"> <span id="feedback2"></span></li>
            <li>Je ne trouve plus ___ clé. <input type="text" id="reponse3"> <span id="feedback3"></span></li>
            <li>___ ne m'intéresse pas. <input type="text" id="reponse4"> <span id="feedback4"></span></li>
            <li>Il est fier de ___ performance. <input type="text" id="reponse5"> <span id="feedback5"></span></li>
            <li>___ ne se fait pas tout seul. <input type="text" id="reponse6"> <span id="feedback6"></span></li>
            <li>Elle a pris ___ voiture pour aller au travail. <input type="text" id="reponse7"> <span id="feedback7"></span></li>
            <li>___ me paraît impossible. <input type="text" id="reponse8"> <span id="feedback8"></span></li>
            <li>Elle a perdu ___ montre hier. <input type="text" id="reponse9"> <span id="feedback9"></span></li>
            <li>___ va aller mieux avec le temps. <input type="text" id="reponse10"> <span id="feedback10"></span></li>
            <li>Je pense que ___ va fonctionner. <input type="text" id="reponse11"> <span id="feedback11"></span></li>
            <li>Il a terminé ___ journée fatigué. <input type="text" id="reponse12"> <span id="feedback12"></span></li>
            <li>___ m'étonne vraiment. <input type="text" id="reponse13"> <span id="feedback13"></span></li>
            <li>Elle aime ___ nouvelle robe. <input type="text" id="reponse14"> <span id="feedback14"></span></li>
            <li>___ va être intéressant à regarder. <input type="text" id="reponse15"> <span id="feedback15"></span></li>
            <li>___ n'est pas normal. <input type="text" id="reponse16"> <span id="feedback16"></span></li>
            <li>Il a oublié de prendre ___ casquette. <input type="text" id="reponse17"> <span id="feedback17"></span></li>
            <li>___ m'embête beaucoup. <input type="text" id="reponse18"> <span id="feedback18"></span></li>
            <li>Elle n'a pas retrouvé ___ chaussure. <input type="text" id="reponse19"> <span id="feedback19"></span></li>
            <li>___ va prendre du temps. <input type="text" id="reponse20"> <span id="feedback20"></span></li>
        </ol>

        <button type="button" onclick="verifier()">Vérifier</button>
    </form>

    <p id="score"></p>
</body>
</html>
