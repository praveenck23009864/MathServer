# Ex.05 Design a Website for Server Side Processing
## Date:

## AIM:
To design a website to find total surface area of a square prism in server side.

## FORMULA:
![image](https://github.com/selvasachein/MathServer/assets/120453887/8ecc8d12-b9a9-43df-be0b-711f299d796d)

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
index.html
```
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>Area of Square Prism</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <style type="text/css">
        body {
            background-color: black;
            margin: 0; /* Add this to remove default body margin */
        }
    
        .edge {
            display: flex;
            height: 100vh;
            width: 100%;
            justify-content: center;
            align-items: center;
        }
    
        .box {
            display: block;
            width: 500px;
            min-height: 300px;
            font-size: 20px;
            background: rgb(0, 255, 60); /* Change the background color to green */
            border-radius: 10px;
            box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
        }
    
        .formelt {
            color: black;
            text-align: center;
            margin-top: 7px;
            margin-bottom: 6px;
        }
    
        h1 {
            color: black;
            text-align: center;
            padding-top: 20px;
        }
    
        input {
            margin: 5px;
            padding: 5px;
            border-radius: 5px;
            border: none;
        }
    </style>
    
</head>

<body>
    <div class="edge">
        <div class="box">
            <h1>Area of a Square Prism</h1>
            <form method="POST">
                {% csrf_token %}
                <div class="formelt">
                    Side : <input type="text" name="length" value="{{l}}"></input>(in m)<br />
                </div>
                <div class="formelt">
                    Height : <input type="text" name="breadth" value="{{b}}"></input>(in m)<br />
                </div>
                <div class="formelt">
                    <input type="submit" value="Calculate"></input><br />
                </div>
                <div class="formelt">
                    Area : <input type="text" name="area" value="{{area}}"></input>m<sup>2</sup><br />
                </div>
            </form>
        </div>
    </div>
</body>
</html>
```
urls.py
```
from django.contrib import admin
from django.urls import path
from mathapp import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path('areaofrectangle/',views.rectarea,name="areaofrectangle"),
    path('',views.rectarea,name="areaofrectangleroot")
]
```


## SERVER SIDE PROCESSING:
![Screenshot 2023-11-15 164010](https://github.com/praveenck23009864/MathServer/assets/141472050/994b339b-c443-4714-9256-b689fc56898b)


## HOMEPAGE:
![Screenshot 2023-11-15 163940](https://github.com/praveenck23009864/MathServer/assets/141472050/503b9a03-6d0e-41cd-a4b4-9854121b4ab1)


## RESULT:
The program for performing server side processing is completed successfully.
