<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Animação de Lápis Escrevendo</title>
<style>
  /* Estilo do lápis */
  .pencil {
    position: absolute;
    width: 20px;
    height: 20px;
    background: #f4a261;
    border-radius: 50% 0 0 50%;
    transform: rotate(45deg);
    animation: pencilMove 3s ease-in-out forwards;
  }
  .pencil:before {
    content: "";
    position: absolute;
    width: 10px;
    height: 10px;
    background: #000;
    border-radius: 50%;
    top: 5px;
    left: 10px;
  }

  /* Animação do texto sendo "escrito" */
  .writing-text {
    font-family: 'Patrick Hand', cursive;
    font-size: 24px;
    color: #333;
    overflow: hidden;
    border-right: .15em solid orange;
    white-space: nowrap;
    margin: 0 auto;
    animation: typing 3s steps(30, end), blink-caret .5s step-end infinite;
  }

  /* Animações */
  @keyframes typing {
    from { width: 0 }
    to { width: 100% }
  }

  @keyframes blink-caret {
    from, to { border-color: transparent }
    50% { border-color: orange; }
  }

  @keyframes pencilMove {
    0% { top: 0; left: 0; }
    100% { top: 30px; left: 320px; }
  }
</style>
</head>
<body>

<div style="position: relative; display: flex; align-items: center;">
  <div class="pencil"></div>
  <div class="writing-text">OLÁ! SEJA BEM-VINDO AO MEU GITHUB!</div>
</div>

</body>
</html>
