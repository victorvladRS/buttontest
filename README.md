# buttontest
<!DOCTYPE html>
<html lang="en">
<head>
    <title></title>
    <meta charset="utf-8">
 
    <style>
 
    #button {
        width:200px;
        height:100px;
        position:absolute;
        top:100px;
        left:100px;
        background: linear-gradient(-90deg, blue, green);
        color: red;
        border: solid 2px black;
    }
 
 
    #button:hover {
        background: linear-gradient(-90deg, green, blue);
    }
    
    </style>
</head>
<body>
 
   <button id="button" onclick="myFunction()">Click Me!</button>
 
 
<script>

function myFunction() {
    alert("Wow you actually got me..Good job!");
}

</script>



<script>
    var button = document.getElementById("button");
    var browserWidth = window.innerWidth || document.documentElement.clientWidth;
    var browserHeight = window.innerHeight || document.documentElement.clientHeight;
    var buttonWidth = button.offsetWidth;
    var buttonHeight = button.offsetHeight;
 
    function move() {
        button.style.left = Math.floor(Math.random()*(browserWidth-buttonWidth)) + "px";
        button.style.top = Math.floor(Math.random()*(browserHeight-buttonHeight)) + "px";
    }
 
    if(typeof addEventListener !== "undefined") {
        button.addEventListener("mouseover", move, false);
    } else if (typeof attachEvent !== "undefined") {
        button.attachEvent("onmouseover", move);
    } else {
        button.onmousover = move;
    }
 
</script>
</body>
</html>
