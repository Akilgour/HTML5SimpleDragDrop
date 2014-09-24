HTML5SimpleDragDrop
===================


This will be the base sample code for this 

<!DOCTYPE HTML>
<html>
<head>
<style>
#div1, #div2,#div3, #div4
{float:left; width:100px; height:35px; margin:10px;padding:10px;border:1px solid #aaaaaa;}
</style>
<script>
function allowDrop(ev) {
    ev.preventDefault();
}

function drag(ev) {
    ev.dataTransfer.setData("text/html", ev.target.id);
}

function drop(ev) {
    ev.preventDefault();
    var data = ev.dataTransfer.getData("text/html");
    ev.target.appendChild(document.getElementById(data));
	alert(document.getElementById(data))
	alert(ev.target.id)
		alert(data)
}
</script>
</head>
<body>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)">
  <img src="img_w3slogo.gif" draggable="true" ondragstart="drag(event)" id="drag1" width="88" height="31">
</div>

<div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<div id="div3" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<div id="div4" ondrop="drop(event)" ondragover="allowDrop(event)">
  <img src="img_w3slogo.gif" draggable="true" ondragstart="drag(event)" id="drag2" width="88" height="31">
</div>
</body>
</html>
