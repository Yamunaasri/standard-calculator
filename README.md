# Design of a Standard Calculator

## AIM:

To design a web application for a standard calculator.

## DESIGN STEPS:

### Step 1:
Create a new Django project using  "django-admin startproject",get into the project terminal  and use "python3 manage.py startapp" command.

### Step 2:
Define  urls.py and views.py for the website .Allow host access and add the app name under installed 

### Step 3:
Create a templates folder under the app folder followed by a folder under templates with the app name followed by html file named calculator.html

### Step 4:
Write HTML and CSS code in the file save it and run the app using python manage.py makemigrations and python manage.py migrate commands .Run the Server using "python3 manage.py runserver 0:80" command.

### Step 5:
 Validate the HTML and CSS code.
### Step 6:
Publish the website in the given URL.

## PROGRAM :
### calculator.html
```
<!DOCTYPE html>
<HTML lang="en">
    <head>
        <title>Calculator</title>
        
        <script>
        function calculate(args)
        {
            res = document.getElementById("result");
            expression = res.innerText;
            cmd = args.srcElement.innerText;
            if(cmd == "=")
            {
                expression = "" + eval(expression)
            }
            else if(cmd == "C")
            {
                expression=""
            }
            else if(cmd == "DEL")
            {
                expression = expression.slice(0, -1);

            }
            else if(cmd == "√")
            {
                expression = "" + Math.sqrt(eval(expression));
            }
            else if(cmd == "%")
            {
                expression = expression % 1;
            }
            else if(cmd == "log")
             {
        expression = Math.log10(expression);
           }
       
            else{
                expression = expression + cmd;
            }
            res.innerText = expression;
            

        }
         
        </script>

        <style>
            h1{
                color: white;
            }



            
            .calculator-container {
                width: 400px;
                background-color: white;
                margin: 0 auto; 
                text-align: center;
                
            }

           
            button {
                width: 50px;
                height: 50px;
                margin: 10px; 
                font-size: 20px; 
                
                background-color: white; 
                color: black; 
                border: none;
            }

          
            #result {
                
       background-color:#ABFFBA;
    text-align: right;
    padding-right: 50px;
    font-size: 20px;
    margin-bottom: 20px; 
    border: solid black 0.5px;
    color: black;
    width: 348px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: flex-end;

            }
            h1 {
                padding-top: 5px;
                color: black;
            }
            .redd {
                background-color: brown;
            }
            .bluee {
                
                background-color: cornflowerblue;
            }
            body {
                background-color: black;
            }
        </style>

    </head>
<body>
    <div class="calculator-container">
        <h1>CALCULATOR</h1>
        <div id="result">0</div>
        <button onclick="calculate(event);">7</button>
        <button onclick="calculate(event);">8</button>
        <button onclick="calculate(event);">9</button>
        <button class="bluee"  onclick="calculate(event);">/</button>
        <button class="bluee"  onclick="calculate(event);"> DEL </button><br>
        <button onclick="calculate(event);">4</button>
        <button onclick="calculate(event);">5</button>
        <button onclick="calculate(event);">6</button>
        <button class="bluee"  onclick="calculate(event);">*</button>
        <button class="bluee"  onclick="calculate(event);">√ </button><br>
        <button onclick="calculate(event);">1</button>
        <button onclick="calculate(event);">2</button>
        <button onclick="calculate(event);">3</button>
        <button class="bluee"  onclick="calculate(event);">-</button>
        <button class="bluee"  onclick="calculate(event);">log</button><br>
        <button onclick="calculate(event);">0</button>
        <button onclick="calculate(event);">.</button>
        <button class="redd" onclick="calculate(event);">C</button>
        <button class="bluee"  onclick="calculate(event);">+</button>
        <button class="bluee" onclick="calculate(event);">=</button><br>
    </div>
    </body>
    </HTML>


```

## OUTPUT:
![out1 (2)](https://user-images.githubusercontent.com/118343379/213449745-05c7e4ae-c5f5-41e5-82f9-0f5cdea6bb03.png)
![out2 (2)](https://user-images.githubusercontent.com/118343379/213449773-647c6f3e-9694-4445-906d-f37e5af1e451.png)
![out3](https://user-images.githubusercontent.com/118343379/213449801-f0d83ea3-838f-431b-a510-2bd05be0024e.png)
### HTML VALIDATOR
![Screenshot (98)](https://user-images.githubusercontent.com/118343379/213449861-99c31d0f-0db6-4477-b982-62ff12f192ee.png)


## Result:
Thus we designed a web application for a standard calculator.

