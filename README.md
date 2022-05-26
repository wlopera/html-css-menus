# html-css-menus
Html CSS Crear menus base y con Dropdown

## Menu Horizontal Base
```
<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      margin: 0;
    }

    ul {
      list-style-type: none;
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: #333;
      position: fixed;
      top: 0;
      width: 100%;
    }

    li {
      float: left;
      border-right: 1px solid #bbb;
    }

    li a {
      display: block;
      text-decoration: none;
      color: white;
      padding: 14px 16px;
    }

    li a:hover {
      background-color: #04AA6D;
      color: #FFF
    }

    .divClass {
      padding: 20px;
      margin-top: 30px;
      background-color: #1abc9c;
      height: 1500px;
      overflow-y: scroll
    }
  </style>
</head>
<body>
  <ul>
    <li><a href="#android">Android</a></li>
    <li><a href="#apple">Apple</a></li>
    <li><a href="#motorola">Motorola</a></li>
    <li><a href="#huawei">Huawei</a></li>
    <li><a href="#lg">LG</a></li>
    <li style="float:right"><a href="#about">A cerca de...</a></li>
  </ul>
  <div class="divClass">
    <h1>Menú Horizontal</h1>
    <hr>
    <h1>Barra de navegación superior fija</h1>
    <h2>Desplácese por esta página para ver el efecto</h2>
    <h2>La barra de navegación permanecerá en la parte superior de la página mientras se desplaza</h2>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
  </div>
</body>
</html>
```
![Captura](https://user-images.githubusercontent.com/7141537/170302046-e3090de6-37d0-4cbe-bc66-13406e27633b.PNG)

## Menu Vertical Base
```
<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      margin: 0;
    }

    ul {
      list-style-type: none;
      padding: 0;
      margin: 0;
      background-color: #dddddd;
      width: 20%;
      position: fixed;
      height: 100%;
      overflow: auto;
      top: 0
    }

    li {
      border-bottom: 1px solid #555;
    }

    li a {
      display: block;
      text-decoration: none;
      padding: 8px 16px;
      color: #000
    }

    li a:hover {
      background-color: #04AA6D;
      color: #FFF
    }

    .divClass {
      margin-left: 20%;
      padding: 1px 16px;
      height: 1000px;
      background-color: #1abc9c;
      overflow-y: scroll
    }
  </style>
</head>
<body>
  <ul>
    <li><a href="#android">Android</a></li>
    <li><a href="#apple">Apple</a></li>
    <li><a href="#motorola">Motorola</a></li>
    <li><a href="#huawei">Huawei</a></li>
    <li><a href="#lg">LG</a></li>
    <li><a href="#about">A cerca de...</a></li>
  </ul>
  <div class="divClass">
    <h1>Menú Vertical</h1>
    <hr>
    <h1>Barra de navegación superior fija</h1>
    <h2>Desplácese por esta página para ver el efecto</h2>
    <h2>La barra de navegación permanecerá en la parte superior de la página mientras se desplaza</h2>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
  </div>
</body>
</html>
```
![Captura1](https://user-images.githubusercontent.com/7141537/170302039-f5bb43dc-995b-4c87-9700-679f92db8937.PNG)

## Menu Horizontal Base con Dropdown
```
<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      margin: 0;
    }

    ul {
      list-style-type: none;
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: #333;
    }

    li {
      float: left;
      border-right: 1px solid #bbb;
    }

    li a, .dropbtn {
      display: inline-block;
      text-decoration: none;
      color: white;
      padding: 14px 16px;
    }


    li a:hover, .dropdown:hover .dropbtn {
      background-color: #1abc9c;
      color: #FFF
    }
    
      li.dropdown {
        display: inline-block;
      }

	
    .dropdown-content {
      display: none;
      position: absolute;
      background-color: #f9f9f9;
      min-width: 160px;
      box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
      z-index: 1;
    }

    .dropdown-content a {
      color: black;
      padding: 12px 16px;
      text-decoration: none;
      display: block;
      text-align: left;
    }

    .dropdown-content a:hover {background-color: #f1f1f1;}

    .dropdown:hover .dropdown-content {
      display: block;
	}

    .divClass {
      padding: 20px;
      margin-top: 30px;
      background-color: #1abc9c;
      height: 1500px;
      overflow-y: scroll
    }
  </style>
</head>
<body>
  <div style="position: fixed;top: 0;width: 100%;">
    <ul>
      <li><a href="#android">Android</a></li>
      <li><a href="#apple">Apple</a></li>
      <li><a href="#motorola">Motorola</a></li>
      <li><a href="#huawei">Huawei</a></li>
      <li><a href="#lg">LG</a></li>
      <li class="dropdown"><a href="javascript:void(0)" class="dropbtn">Otros</a>
        <div class="dropdown-content">
          <a href="#">Celular 1</a>
          <a href="#">Celuar 2</a>
          <a href="#">Celular 3</a>
        </div>
      </li>
      <li style="float:right"><a href="#about">A cerca de...</a></li>
    </ul>
  </div>
  <div class="divClass">
    <h1>Menú Horizontal</h1>
    <hr>
    <h1>Barra de navegación superior fija</h1>
    <h2>Desplácese por esta página para ver el efecto</h2>
    <h2>La barra de navegación permanecerá en la parte superior de la página mientras se desplaza</h2>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
    <p>Algún texto algún texto algún texto algún texto...</p>
  </div>
</body>
</html>
```
![Captura2](https://user-images.githubusercontent.com/7141537/170302043-2a62ef83-d70f-45db-8e6f-bcb7d9a1f935.PNG)

## Menu Form Base
```
<!DOCTYPE html>
<html>
<style>
    * {
        box-sizing: border-box;
    }

    .main {
        margin-top: 20px
    }

    .container {
        background-color: #dddddd;
        margin: auto;
        padding: 20px;
        border: 1px sold #000;
        border-radius: 5px;
        width: 60%;
    }

    .col-25 {
        float: left;
        width: 25%;
        margin-top: 6px;
    }

    .col-75 {
        float: left;
        width: 75%;
        margin-top: 6px;
    }

    /* Clear floats after the columns */
    .row::after {
        content: "";
        display: table;
        clear: both;
    }

    label {
        padding: 12px 12px 12px 8px;
        display: inline-block;
    }

    .header {
        background-color: #04AA6D;
        width: 100%;
        text-align: center;
        font-size: 20px;
        font-weight: bold;
        border-radius: 5px;
        margin-bottom: 10px;
    }

    input[type=text],
    select,
    textarea {
        width: 100%;
        padding: 12px;
        border: 1px solid #ccc;
        border-radius: 4px;
        resize: vertical;
    }

    input[type=submit] {
        background-color: #04AA6D;
        color: white;
        padding: 12px 20px;
        margin-top: 12px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        float: right;
    }

    input[type=submit]:hover {
        background-color: #6dea73;
    }

    /* Diseño receptivo: cuando la pantalla tiene menos de 600 px de ancho, las dos columnas se apilan una encima de la otra en lugar de una al lado de la otra */
    @media screen and (max-width: 600px) {

        .col-25,
        .col-75,
        input[type=submit] {
            width: 100%;
            margin-top: 0;
        }
    }
</style>
<head>
</head>
<body>
    <div class="main">
        <div class="container">
            <form action="https://disneyparks.disney.go.com/es/">
                <div>
                    <div class="row">
                        <label for="fname" class="header">Datos del Cliente</label>
                    </div>
                    <div class="row">
                        <div class="col-25">
                            <label for="fname">Nombre</label>
                        </div>
                        <div class="col-75">
                            <input type="text" id="fname" name="fname" placeholder="Ingrese su nombre...">
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-25">
                            <label for="lname">Apellido</label>
                        </div>
                        <div class="col-75">
                            <input type="text" id="lname" name="lname" placeholder="Ingrese su apellido...">
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-25">
                            <label for="country">País</label>
                        </div>
                        <div class="col-75">
                            <select name="country" id="country">
                                <option value="0">Seleccione...</option>
                                <option value="1">Argentina</option>
                                <option value="2">Brasil</option>
                                <option value="3">Colombia</option>
                                <option value="4">Panamá</option>
                                <option value="5">Venezuela</option>
                            </select>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-25">
                            <label for="subject">Asunto</label>
                        </div>
                        <div class="col-75">
                            <textarea name="subject" id="subject" cols="30" rows="10"
                                placeholder="Agregar mensaje..."></textarea>
                        </div>
                    </div>
                    <div class="row">
                        <input type="submit" value="Enviar">
                    </div>
                </div>
            </form>
        </div>
    </div>
</body>
</html>
```
![Captura](https://user-images.githubusercontent.com/7141537/170526233-2de9e1e2-2ab8-41af-8a6c-cb7e0ca0f616.PNG)
![Captura1](https://user-images.githubusercontent.com/7141537/170526236-3e309183-ca13-4fe6-806f-99d77b445ad2.PNG)
