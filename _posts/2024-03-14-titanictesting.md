---
toc: true
comments: false
layout: post
title: Titanic Testing
description: 
type: plans
courses: { compsci: {week: 19} }
image: images/erfef.webp
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titanic Survival Prediction</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
        }
        h1 {
            text-align: center;
            margin-bottom: 20px;
        }
        form {
            max-width: 500px;
            margin: 0 auto;
        }
        label {
            display: block;
            margin-bottom: 10px;
        }
        input[type="text"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 20px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #45a049;
        }
        .result {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Titanic Survival Prediction</h1>
    <form id="predictionForm">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required> <!-- Add this input field for the name -->
        <label for="pclass">Pclass (1, 2, or 3):</label>
        <input type="text" id="pclass" name="pclass" required>
        <label for="sex">Sex (male or female):</label>
        <input type="text" id="sex" name="sex" required>
        <label for="age">Age:</label>
        <input type="text" id="age" name="age" required>
        <label for="sibsp">Sibsp (number of siblings/spouses):</label>
        <input type="text" id="sibsp" name="sibsp" required>
        <label for="parch">Parch (number of parents/children):</label>
        <input type="text" id="parch" name="parch" required>
        <label for="fare">Fare:</label>
        <input type="text" id="fare" name="fare" required>
        <label for="embarked">Embarked (C, Q, or S):</label>
        <input type="text" id="embarked" name="embarked" required>
        <label for="alone">Alone (true or false):</label>
        <input type="text" id="alone" name="alone" required>
        <button type="submit">Predict</button>
    </form>
    <div id="result" class="result"></div>
    <script>
        document.getElementById("predictionForm").addEventListener("submit", function(event) {
            event.preventDefault();
            let formData = new FormData(this);
            fetch("http://127.0.0.1:8086/api/predict", {
                method: "POST",
                body: JSON.stringify(Object.fromEntries(formData)),
                mode: 'cors',
                headers: {
                    "Content-Type": "application/json"
                }
            })
            .then(response => response.json())
            .then(data => {
                let resultDiv = document.getElementById("result");
                resultDiv.textContent = "Survival prediction: " + (data[0] === 1 ? "Survived" : "Did not survive");
            })
            .catch(error => {
                console.error("Error:", error);
            });
        });
    </script>
</body>
</html>
