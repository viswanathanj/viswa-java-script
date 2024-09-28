<!DOCTYPE html>
<html>
<head>
  <title>Background Color Changer</title>
</head>
<body>
  <h1>COLOUR CHANGE</h1>
  <button id="prev-button">previous </button>
  <button id="next-button">next</button>

  <script>
const colors = ['orange', 'red', 'blue','green','purple'];
let currentIndex = 0;

document.getElementById('prev-button').addEventListener('click', () => {
  currentIndex = (currentIndex - 1 + colors.length) % colors.length;
  changeColor();
});

document.getElementById('next-button').addEventListener('click', () => {
  currentIndex = (currentIndex + 1) % colors.length;
  changeColor();
});

function changeColor() {
  document.body.style.background = colors[currentIndex];
}
  </script>
</body>
</html>
