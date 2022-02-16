<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Glowing Buttons</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <a href="#">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      Neon Button
    </a>

    <a href="#">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      Neon Button
    </a>

    <a href="#">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      Neon Button
    </a>
  </body>
</html>

<style>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@400;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #050801;
  font-family: 'Raleway', sans-serif;
  font-weight: bold;
}

a {
  display: inline-block;
  position: relative;
  color: #03e9f4;
  padding: 30px 25px;
  margin: 25px 30px 25px 0;
  letter-spacing: 4px;
  text-transform: uppercase;
}

a:hover {
  color: black;
  background-color: #03e9f4;
  transition: 0.5s;
  -webkit-box-shadow: 2px 3px 76px 30px rgba(22,227,217,1);
  -moz-box-shadow: 2px 3px 76px 30px rgba(22,227,217,1);
  box-shadow: 2px 3px 76px 30px rgba(22,227,217,1);
}


</style>