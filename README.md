<h1 align="center">Workshop toolkit</h1>
<img src="https://media0.giphy.com/media/hvXcXEyDpdV1uZJ0nJ/200w.webp?cid=ecf05e470gqc03fx9wa4nt2zjp9lvodxtmmq3oe1a0jx211w&ep=v1_gifs_search&rid=200w.webp&ct=g" align="right" width="300">
<p>
  Aquí encontrarás las dependencias y herramientas que deberás tener instaladas para llevar a cabo con éxito el workshop de Astar Network.
</p>
<h3 align="center">
  Pre-requisitos
</h3>
<p>
  1. Deberás tener instalado un sistema operativo linux, en caso de poseer Windows, con tener WSL (Windows Subsystem for Linux) podrás trabajar. <br>
  2. Deberás tener instalado <a href="https://visualstudio.microsoft.com/es/">Visual Studio Code</a>, ya que será el IDE con el cual estaremos trabajando. <br>
  3. Finalmente, instala en tu Visual Studio Code, la extensión de <a href="https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer">Rust-Analizer</a>. <br>
  
  Con esto estarás lista o listo para seguir el tutorial.
</p> <br>
<h3 align="center">
  Compilador compatible con C
</h3>
<p>
  Lo primero que debemos hacer es incluir un enlazador o un compilador compatible con <a href="https://www.google.com/search?q=c+programming+language&oq=c+programming+language&aqs=chrome.0.0i355i512i543j46i340i512j0i512l5j69i60.8316j0j7&sourceid=chrome&ie=UTF-8">C</a> como <code>clang</code> que es un entorno de desarrollo integrado (IDE). Ejecuta estos dos comandos: <br>
  <div align="center">
  <code>sudo apt install build-essential</code> & <code>sudo apt install clang curl git make</code>
  </div>
</p>
<h3 align="center">
  Instalar un paquete de criptografía
</h3>
<p>
  Debido a que la cadena de bloques requiere criptografía estándar para admitir la generación de pares de claves pública/privada y la validación de firmas de transacciones, también debe tener un paquete que proporcione criptografía. Ejecuta el siguiente comando:
  <div align="center"> <code>sudo apt install libssl-dev</code> </div> <br>
  Además, debemos instalar un paquete con todas las características necesarias para trabajar con <code>libssl-dev</code>. Ejecuta este comando: 
  <div align="center"> <code>sudo apt install pkg-config</code> </div>
</p>



















<h3 align="center">
  Reduce trabajo con el <code>Swanky-container</code>
</h3>
<p>
  También podrás reducir todo este trabajo a una sola acción a través del <code>Swanky-container</code>, podrás leer y conocer más de esta alternativa a la configuración manual a través de este <a href="https://github.com/AstarNetwork/swanky-dev-container">repositorio de GitHub</a>.
</p>
<h3 align="center">
  Instala la Polkadot.js y crea una cuenta
</h3>
<p>
  Finalmente, para interactuar con todo el ecosistema, hacer pruebas, obtener tokens y desplegar contratos inteligentes, deberás contar con una Wallet en la Polkadot.js. Para ello te recomiendo seguir este tutorial: <a href="https://www.rspanther.com/wallets/polkadot-js/como-crear-wallet-polkadotjs/">Crea tu billetera en la Polkadot.js</a>. 
</p>
<h3 align="center">¡Felicitaciones!</h3>
<p>
  ¡Felicidades! Con esto tendrás un entorno de desarrollo listo y preparado para llevar a cabo el <a href="https://twitter.com/dotlabs__/status/1651325286342963200?s=20">Workshop de Astar Network</a> por parte del equipo de <a href="https://dotlabs.academy/">dotlabs()</a>.
</p>
