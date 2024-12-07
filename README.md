<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            background-color: #2b2b2b;
  margin: 0;
}

    
        .header{
            background: linear-gradient(120deg, #1a1d23, #3a3f4b);
    padding: 20px;
    text-align: center;
    color: aliceblue;
    font-family: 'Times New Roman', Times, serif;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    box-sizing: border-box;
        }
        .topnav{
            border: #555555;
            overflow:hidden;
            background-color:#333333;
            color: aliceblue;
            font-family: Georgia, 'Times New Roman', Times, serif;

        }
        .topnav a{
            float: left;
            display: block;
            color: antiquewhite;
            text-align: center;
            padding: 15px 20px;
            text-decoration: double;
            font-family: Georgia, 'Times New Roman', Times, serif;
        }
        .topnav :hover{
            
            color: #555555;
        }
        .body{
            flex-grow:1;
            padding:10px;
            background-color:#2b2b2b;
            overflow: hidden;
            
        }
        #outerbox{
            width:250px;
            overflow: hidden;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border-radius: 10px;
            background-position:center;width: 450;
            margin:10px auto;
            box-shadow:10px 15px 20px;
            
           
           
        
        }
        #slidebox{
            
            position: relative;
            display: flex;
            width:1000px;
            height: 4500;
            animation:slider 30s infinite;
            

           
            
        }
        

        @keyframes slider {

            0% {
                left: 0px;
            }

            11% {
                left: -250px;
            }

            22% {
                left: -500px;
            }

            33% {
                left: -750px;
            }

            44% {
                left: -1000px;
            }

            55% {
                left: -1250px;
            }

            66% {
                left: -1500px;
            }

            77% {
                left: -1750px;
            }

            88% {
                left: -2000px;
            }

            100% {
                left: -2250px;
            }
        }

        #slidebox img {
            width: 1000px;
            height: 250px;
            align-items: center;
            justify-content: center;
            
        }
    .open-modal
    {
    padding: 10px 15px;
    background-color:none;
    color: white;
    text-align: center;
    border: none;
    cursor: pointer;
    border-radius: 5px;
    float: right;
    text-decoration: none;
}
.open-modal:hover{
    background-color: none;
}


.modal{
    display: none;
    position: fixed;
    z-index: 1;
    left: 0%;
    top: 0%;
    width: 100%;
    height:100vh;
    overflow: none;
    backdrop-filter: blur(5px);
    background-color: transparent;
}
.modal-toggle{
    display: none;
}
.modal-toggle:checked + .modal{
    display: block;
}
.modal-content{
    background-color: rgb(218, 208, 253);
    margin-top: 15%;
    margin: 10% auto;
    padding: 15px;
    border: 1px solid #888;
    width:300px;
    border-radius: 5px;
    position: relative;
    height: 350px;
}
.close{
color: #aaa;
float: right;
font-size: 28px;
font-weight: bold;
color: pointer;
}
.close:hover{
    color:black;
}
.form{
    display: flex;
    flex-direction: column;
}
.form:hover{
    background-color: transparent;
}
.label{
    margin: 10px 0 5px;
}
input[type="text"],
input[type="password"]{
padding: 10px;
margin-bottom: 15px;
border: 1px solid #ccc;
border-radius: 4px;
}
button[type="log-in"]{
    background-color: lawngreen;
    border: none;
    padding: 10px;
    color: white;
    border-radius: 5px;
    cursor: pointer;
}
button[type="Register"]{
    background-color: lawngreen;
    border: none;
    padding: 10px;
    color: white;
    border-radius: 5px;
    cursor: pointer;
}
button[type="submit"]:hover{
background-color: #888;
}
.bottom{
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: #232526;
    padding-top: 5px;
    padding-bottom: 5px;
    color: white;
}
.header {
            background: linear-gradient(120deg, #1a1d23, #3a3f4b);
            padding: 20px 50px;
            text-align: center;
            color: aliceblue;
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            box-sizing: border-box;
        }

        .header img {
            height: 80px;
            width: 80px;
            border-radius: 50%;
            margin-right: 20px;
        }

        .header h1 {
            font-size: 32px;
            color: white;
            display: inline;
        }

        .search-container {
            display: flex;
            align-items:right;
            justify-content: flex-end;
            flex-grow: 1;
        }

        .search-container input[type="search"] {
            padding: 10px;
            font-size: 16px;
            border-radius: 4px;
            border: none;
            margin-right: 5px;
            width: 300px;
        }

        .search-container button {
            padding: 10px;
            background-color: lawngreen;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .search-container button:hover {
            background-color: #777777;
        }
        .gallery {
  display: flex;
  justify-content: center;
  align-items: center;
  perspective: 1200px;
  width: 100vw;
  height: 40vh; /* Ensure the gallery takes full viewport height */
}

.gallery-container {
    width: 200px;  /* Make the container relative to the viewport */
    height: 200px; /* Make the container relative to the viewport */
  position: relative;
  transform-style: preserve-3d;
  animation: rotate 15s infinite linear;
  transform-origin: center center; /* Ensures rotation is centered */
}

.gallery-image {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 10px; /* Rounded corners for images */
}

.gallery-image img {
  width: 100%;
  height: 100%;
  object-fit: contain; /* Ensures images fit within the container */
  border-radius: 10px;
}

.gallery-image:nth-child(1) { transform: rotateY(0deg); }
.gallery-image:nth-child(2) { transform: rotateY(90deg); }
.gallery-image:nth-child(3) { transform: rotateY(180deg); }
.gallery-image:nth-child(4) { transform: rotateY(-90deg); }

@keyframes rotate {
  0% { transform: rotateY(0deg); }
  100% { transform: rotateY(360deg); }
}

/* Thumbnail Gallery */
.thumbnail-gallery {

  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  justify-content: center;
  margin-top: 20px;
}

/* Responsive Styles */
@media (max-width: 768px) {
  .gallery-container {
    width: 70vw;
    height: 70vh;
  }
}
.thumbnail {
      position: relative;
      overflow: hidden;
      width: 100px;
      height: 100px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }

    .thumbnail img {
      width: 100%;
      height: 100;
      display: block;
    }

    .thumbnail:hover {
      transform: scale(1.1);
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
    }
    .description {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      background: rgba(0, 0, 0, 0.6);
      color: white;
      text-align: center;
      font-style: initial;
      font-size: 15px;
      padding: 5px;
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .thumbnail:hover .description {
      opacity: 1;
    }
     .thumbnail {
        width: 150px;
        height: 100%;
      }

    .description {
        font-size: 9px;
}
footer {
            background: black;
            color: white;
            text-align: center;
            padding: 5px;
            position: relative;
            bottom: 0;
            width: 100%;
        }
        body::-webkit-scrollbar{
  display: none;
}
    </style>
    
 </head>
 <body>
    <div class="header">
        <img src="360_F_169375330_ec1Xv9kLUPs9JxVwq9Fiq0QGpQQVZY24.jpg" alt="Logo" >
        <h1><span style="color: blue;">Tecno</span> <span style="color: #555555;">Zone</span></h1>
        <div class="search-container">
            <input type="search" id="search" placeholder="search..." size="30px">
            <button type="submit">Search</button>
        </div>
    </div></div>
    <div class="topnav">
        <a href="#" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; font-size: large; background-color: #888;" >HOME</a>
        <a href="lab7.html" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; font-size: large;">PRODUCTS</a>
        <a href="about.html" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; font-size: large;">ABOUT</a>
        <a href="#" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; font-size: large;">SHOP NOW!</a>
        <label for="modal-toggle" class="open-modal" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;  font-size: large; margin-top: 5px;">LOG-IN</label>
        <input type="checkbox" id="modal-toggle" class="modal-toggle">
   
<div class="modal">
<div class="modal-content">
<label for="modal-toggle" class="close">&times;</label>

<form style="color: #555555;">
    <center style="font-family: Arial, Helvetica, sans-serif;">
        <h2>LOG-IN</h2>
    <br><input type="text" id="username" name="username" required>
    <P style="margin: 0%;"><label for="username">username</label></P>
    
    <br><input type="password" id="password" name="password" required>
    <P style="margin: 0%;"><label for="password">password</label></P>
    <br><button type="log-in">Log-in</button>
</center>
<a href="register.html" style="margin-left: 70%; color: black;">Register</a>
</form>
</div>
</div>
</div>

    <div id="outerbox">
        <div id="slidebox">
            <img src="1.png">
            <img src="2.png">
            <img src="3.png">
            <img src="4.png">
            <img src="5.png">
            <img src="6.png">
            <img src="7.png">
            <img src="8.png">
            <img src="10.png">
            <img src="9.png">

            

        </div>
        
    
    </div>
    <div style="text-align: center; text-transform: uppercase; font-size: large; color: white; padding: 10px;font-family: Georgia, 'Times New Roman', Times, serif; background-color: #1a1d23;">LOOKING FOR AFFORDABLE PHONE OPTIONS?
        <br>HERE ARE SOME TOP PICKS!
    </div>
        <div class="thumbnail-gallery" style="margin-bottom: 20px;">
            <a href="22.html">
                <div class="thumbnail">
                <img src="22.png" alt="Thumbnail Tecno Pova 6 pro 5G">
                <div class="description"> Tecno Pova 6 pro 5G</div>
            </div></a>
            <a href="1.html">
              <div class="thumbnail">
                <img src="1.png" alt="Tecno Pova 3">
              <div class="description">Tecno Pova 3</div>
            
            </div></a>
            <a href="7.html"></a>
        
                <div class="thumbnail">
                  <img src="7.png" alt="Thumbnail Tecno Pova 5 X Free Fire">
                  <div class="description">Tecno Pova 5 X Free Fire</div>
            
            </div></a>
            <a href="11.html">
              <div class="thumbnail">
              <img src="11.png" alt="Thumbnail Tecno Pova neo 3">
              <div class="description">Tecno Pova neo 3</div>
            
            </div></a>
            <a href="29.html">
              <div class="thumbnail">
              <img src="29.png" alt="Thumbnail Tecno Pova 4 pro">
              <div class="description"> Tecno Pova 4 pro</div>
            </div></a></div>
    </div>

 </body>
 </html>
