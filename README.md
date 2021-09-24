###  Session Stoarge da web.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Ensinando Session Stoarge</title>
  </head>
  <body>
    <h1>
      Session Stoarge é <span id="textinho">simples</span>
    </h1>

    <script>
      let texto = document.querySelector("#textinho");
      let data = sessionStorage.setItem("text", texto.innerText+" e fácil!"); // Armazenando na session stoarge "simples"
      
      setTimeout(() => {
        texto.innerHtml = sessionStorage.getItem("text"); // Puxando o item "text"
      }, 1000);
      setTimeout(() => {
        sessionStorage.removeItem("text"); // Deletando o item "text"
      }, 2000);
    </script>     
  </body>
</html>
```
