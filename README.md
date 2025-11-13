/<!DOCTYPE html>
/<html>
/  <head>
/    <title>Your Name</title>
/  </head>
/  <body>
/    <h1>Hello, world!</h1>
/    <p>Welcome to my personal site.</p>
/  </body>
/</html>

<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Meu Site Pessoal</title>
<style>
  /* Estilos básicos para as abas */
  body {
    font-family: Arial, sans-serif;
    margin: 20px;
  }
  .tab {
    overflow: hidden;
    border-bottom: 2px solid #ccc;
  }
  .tab button {
    background-color: #f1f1f1;
    float: left;
    border: none;
    outline: none;
    cursor: pointer;
    padding: 14px 20px;
    font-size: 16px;
    transition: background-color 0.3s;
  }
  .tab button:hover {
    background-color: #ddd;
  }
  .tab button.active {
    background-color: #ccc;
    font-weight: bold;
  }
</style>
</head>
<body>

<h1>Meu Site Pessoal</h1>

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'about')">About Me</button>
  <button class="tablinks" onclick="openTab(event, 'publications')">Publications</button>
  <button class="tablinks" onclick="openTab(event, 'education')">Education</button>
</div>

<!-- Conteúdo das abas será adicionado depois -->

<script>
function openTab(evt, tabName) {
  // Esta função será detalhada em passos futuros
}
</script>

</body>
</html>
