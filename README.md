
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <div class="loader" style="width: 10em; height: 10em; font-size: 30px; border-radius: 50%; border-top: 0.3em solid hotpink; position: relative; box-sizing: border-box; animation: rotating 2s ease-in-out infinite;">
    <span style="color: white; width: inherit; height: inherit; position: absolute; text-align: center; line-height: 10em; font-family: sans-serif; animation: rotating 2s linear infinite; --direction: -1;">Welcome</span>
  </div>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: black;
    }
   .loader::before,
   .loader::after {
      content: '';
      position: absolute;
      width: inherit;
      height: inherit;
      border-radius: 50%;
      box-sizing: border-box;
      top: -0.2em;
      --direction: 1;
    }
   .loader::before {
      border-top: 0.3em solid dodgerblue;
      transform: rotate(120deg);
    }
   .loader::after {
      border-top: 0.3em solid gold;
      transform: rotate(240deg);
    }
    @keyframes rotating {
      50% {
        transform: rotate(180deg * var(--direction)); 
      }
      100% {
        transform: rotate(360deg * var(--direction)); /* 去掉 calc 函数，提高兼容性 */
      }
    }
  </style>
</body>
</html>
