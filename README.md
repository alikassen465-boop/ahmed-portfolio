<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<title>Kurdistan Flag Animation</title>

<style>
body {
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #111;
}

.flag {
  width: 600px;
  height: 400px;
  position: relative;
  box-shadow: 0 0 20px black;
  overflow: hidden;
}


.stripe {
  height: 33.33%;
  width: 100%;
  opacity: 0;
}


.red {
  background: #d40000;
  animation: show 1s forwards;
}

.white {
  background: #ffffff;
  animation: show 1s forwards;
  animation-delay: 1s;
}

.green {
  background: #009933;
  animation: show 1s forwards;
  animation-delay: 2s;
}


.sun {
  position: absolute;
  width: 120px;
  height: 120px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) scale(0);
  animation: sunShow 1s forwards;
  animation-delay: 3s;
}

.sun::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background:
    repeating-conic-gradient(
      gold 0deg 8.57deg,
      transparent 8.57deg 17.14deg
    );
  border-radius: 50%;
}

.sun::after {
  content: "";
  position: absolute;
  width: 70px;
  height: 70px;
  background: gold;
  border-radius: 50%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}


@keyframes show {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes sunShow {
  from {
    transform: translate(-50%, -50%) scale(0);
  }
  to {
    transform: translate(-50%, -50%) scale(1);
  }
}
</style>
</head>

<body>

<div class="flag">
  <div class="stripe red"></div>
  <div class="stripe white"></div>
  <div class="stripe green"></div>
  <div class="sun"></div>
</div>

</body>
</html>
