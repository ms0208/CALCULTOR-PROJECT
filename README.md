# CALCULTOR-PROJECT
# calculator .html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Manav Calculator</title>
    <link rel="stylesheet" href="calculator.css">
    <link rel="stylesheet" href="utils.css">
</head>
<body>
      <h1 class="centre"> Welcome to Calculate me </h1>
      <div class="container bg-red mx-auto">
        <div class="row">
            <input class="input" type="text">
        </div>
        <div class="row">
            <button class="button">7</button>
            <button class="button">8</button>
            <button class="button">9</button>
            <button class="button">*</button>
        </div>
        <div class="row">
            <button class="button">6</button>
            <button class="button">5</button>
            <button class="button">4</button>
            <button class="button">/</button>
        </div>
        <div class="row">
            <button class="button">3</button>
            <button class="button">2</button>
            <button class="button">1</button>
            <button class="button">+</button>
        </div>
        <div class="row">
            <button class="button">0</button>
            <button class="button">=</button>
            <button class="button">C</button>
            <button class="button">-</button>
        </div>
      </div>
      <script src="calculator.js"></script>
</body>
</html>
# caculator.js
let string = "";
let buttons = document.querySelectorAll('.button');
Array.from(buttons).forEach((button)=>{
    button.addEventListener('click', (e)=>{
        if(e.target.innerHTML == '='){
            string = eval(string);
            document.querySelector('input').value = string;
        }
        else if(e.target.innerHTML == 'C'){
            string = "";
            document.querySelector('input').value = string;
        }
        else{
        console.log(e.target)
        string = string + e.target.innerHTML;
        document.querySelector('input').value = string;
        }
    })

})
        
 # utils.css
 *{
    margin:0;
    padding:0;
   
}
body{
    background-color: black;
}
.centre{
    text-align: center;
    font-size: 70px;
    font-weight: bold;
    color:white;
    margin-top: 20px;
    margin-bottom: 30px;
}

.mx-auto{
    margin: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.button{
    padding: 10px 40px;
    margin: 0 3px;
    border: 2px solid aqua;
    border-radius: 20px;
    cursor:pointer;
    font-size: 40px;
}
.button:hover{
    color:red;
}
.row{
    margin: 12px 0;
}
.input{
    font-size: 40px;
    padding: 10px;
    color:blue;
    border: 2px solid orangered;
    border-radius: 20px;
}


 
 
       
