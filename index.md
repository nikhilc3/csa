---
layout: default
title: Student Blog
---

<html>
    <head>
        <style>
            body {
                font-family: Arial, sans-serif;
                background-color: #2c3e50;
                color: #ecf0f1;
            }
            .Title {
                position: absolute;
                left: 50%;
                top: 90px;
                transform: translate(-50%, -50%);
                transition: color 0.5s; 
            }
            .Title:hover {
                cursor: pointer; 
            }
            .codeText {
                position: absolute;
                left: 50%;
                top: 50%;
                transform: translate(-50%, -50%);
                font-size: 3em;
                animation: colorChange 5s infinite alternate, moveUpDown 2s infinite alternate;
                cursor: pointer;
            }
            @keyframes colorChange {
                0% { color: #e74c3c; }
                25% { color: #3498db; }
                50% { color: #2ecc71; }
                75% { color: #f39c12; }
                100% { color: #e74c3c; }
            }
            @keyframes moveUpDown {
                0% { transform: translateY(-10px) translateX(-50%); }
                100% { transform: translateY(10px) translateX(-50%); }
            }
        </style>
    </head>
    <body>
        <h1 class="Title" onmouseover="changeColor(this)" onmouseout="resetColor(this)">Nikhil's Github Pages</h1>
        <div class="codeText">code/code/code</div>
        <script>
            function changeColor(element) {
                element.style.color = "#e67e22";
            }
            function resetColor(element) {
                element.style.color = "#ecf0f1";
            }
        </script>
    </body>
</html>
