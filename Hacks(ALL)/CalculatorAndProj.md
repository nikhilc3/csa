---
layout: default
title: Calculator Project
type: hacks
courses: { 'csa': {'week':0} }
---



<html>
    <head>
        <style>
            .title1{
                position:absolute;
                left:30%;
                bottom:25%;
                transform:translate(-50%,-50%);
            }
            .game {
                width: 300px;
                margin: 20px auto;
                padding: 9px;
                border: 1px solid #ddd;
                border-radius: 5px;
                background-color: #f5f5f5;
                text-align: center;
            }
            .btnGuess {
                margin: 10px;
                padding: 10px 20px;
                cursor: pointer;
            }
            .gameResult {
                margin-top: 20px;
                font-size: 18px;
            }
            .title{
                position:absolute;
                left:30%;
                top:30%;
                transform:translate(-50%,-50%);
            }
            .calculator {
                width: 250px;
                margin: 20px auto;
                border: 1px solid #ddd;
                border-radius: 5px;
                overflow: hidden;
            }
            .screen {
                width: 100%;
                height: 50px;
                background-color: #f5f5f5;
                padding: 10px;
                font-size: 18px;
                text-align: right;
                border: none;
            }
            .buttons {
                display: grid;
                grid-template-columns: repeat(4, 1fr);
            }
            button {
                padding: 20px;
                border: none;
                border-top: 1px solid #ddd;
                font-size: 18px;
                cursor: pointer;
                transition: background-color 0.3s;
            }
            button:hover {
                background-color: #f5f5f5;
            }
            .equals {
                grid-column: 1 / span 3;
                background-color: #0074d9;
                color: white;
            }
            .clear {
                background-color: #f44336; /* Red color for clarity */
                color: white; /* White text color */
            }
            .clear:hover {
                background-color: #f5f5f5; /* Darker red when hovered */
            }
        </style>
    </head>
    <body>
    <h1 class = "title">Calculator</h1>
        <div class="calculator">
            <input type="text" class="screen" disabled>
            <div class="buttons">
                <button class="num" value="1">1</button>
                <button class="num" value="2">2</button>
                <button class="num" value="3">3</button>
                <button class="op" value="-">-</button>
                <button class="num" value="4">4</button>
                <button class="num" value="5">5</button>
                <button class="num" value="6">6</button>
                <button class="op" value="*">*</button>
                <button class="num" value="7">7</button>
                <button class="num" value="8">8</button>
                <button class="num" value="9">9</button>
                <button class="op" value="/">/</button>
                <button class="num" value="0">0</button>
                <button value="." class="num">.</button>
                <button>   </button>
                <button class="op" value="+">+</button>
                <button value="=" class="equals">=</button>
                <button class="clear">Clear</button>
            </div>
        </div>
        <h1 class = "title1"> Coin Flip Game</h1>
        <div class="game">
            <p>Guess whether the coin will be heads or tails:</p>
            <button class="btnGuess" data-guess="heads">Heads</button>
            <button class="btnGuess" data-guess="tails">Tails</button>
            <p class="gameResult"></p>
        </div>
    </body>
    <script>
        let screen = document.querySelector('.screen');
        let nums = document.querySelectorAll('.num');
        let ops = document.querySelectorAll('.op');
        let equals = document.querySelector('.equals');
        let currentOp = '';
        let currentValue = '';
        let prevValue = '';
        nums.forEach(num => {
            num.addEventListener('click', function() {
                screen.value += this.value;
            });
        });
        ops.forEach(op => {
            op.addEventListener('click', function() {
                prevValue = screen.value;
                screen.value = '';
                currentOp = this.value;
            });
        });
        equals.addEventListener('click', function() {
            currentValue = screen.value;
            if (currentOp && currentValue) {
                screen.value = eval(prevValue + currentOp + currentValue);
                currentOp = '';
                currentValue = '';
                prevValue = '';
            }
        });
        let buttons = document.querySelectorAll('.btnGuess');
        let gameResult = document.querySelector('.gameResult');
        buttons.forEach(button => {
            button.addEventListener('click', function() {
                let userGuess = this.getAttribute('data-guess');
                let coinFlipResult = Math.random() < 0.5 ? 'heads' : 'tails';
                if (userGuess === coinFlipResult) {
                    gameResult.textContent = `You're right! It was ${coinFlipResult}!`;
                } else {
                    gameResult.textContent = `Sorry, it was ${coinFlipResult}. Try again!`;
                }
            });
        });
        let clear = document.querySelector('.clear');
        clear.addEventListener('click', function() {
            screen.value = ''; 
            currentOp = ''; 
            currentValue = ''; 
            prevValue = ''; 
        });
    </script>
</html>
