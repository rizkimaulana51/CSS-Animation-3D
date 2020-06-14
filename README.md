# CSS-Animation-3D

<!DOCTYPE html>

<html>
    <head>
        <meta http-equiv="CONTENT-TYPE" content="text/html; charset=UTF-8">
        <link rel="stylesheet" href="styles/style.css"/>
        <title>animation calc()</title>
<style>
    
* {
margin:0;
padding:0;
box-sizing:border-box;
}

body {
min-height:100vh;
background:dodgerblue;
display:flex;
alig-items:center;
justify-content:center;
}

.container {
position:relative;
width:150px;
height:150px;
display:flex;
justify-content:center;
align-items:center;
transform:perspective(500px) rotateX(135deg);
transform-style:preserve-3d;
margin: 50% auto;
}

.container span {
position:absolute;
display:block;
transform:perspective(500px) rotateX(135deg);
transform-style:preserve-3d;
border:15px solid white;
border-radius:50%;
animation: animasi 6s ease-in-out infinite;
box-shadow: 0 10px 0 #efebed,
            inset 0 10px 0 #ececec;
animation-delay:calc(1s * var(--i));

}

@keyframes animasi {
 0% {
  transform:translateZ(-100px);
  width:100%;
  height:100%;
 }

 25% {
  transform:translateZ(100px);
  width:100%;
  height:100%;
 }

 50% {
  transform:translateZ(100px);
  width:15%;
  height:15%;
 }

 75% {
  transform:translateZ(-100px);
  width:15%;
  height:15%;
 }

 100% {
  transform:translateZ(-100px);
  width:100%;
  height:100%;
 }
} 

</style>
    </head>
    <body>
        <div class="container">
            <span style="--i:1;"></span>
            <span style="--i:2;"></span>
            <span style="--i:3;"></span>
            <span style="--i:4;"></span>
            <span style="--i:5;"></span>
            <span style="--i:6;"></span>
        </div>
        
    
    </body>
</html>
