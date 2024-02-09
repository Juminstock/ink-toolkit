<h1 align="center">Ink! toolkit for linux 🐧</h1>
<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaXh0aXUzNHJkcmttdGV4YmhkMWFrbHUxMWhxcGxnbThmNmFlemo0cSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3og0ICG4WxdKSRzE3K/giphy.gif" align="right" width="500">
<p>
  Repositorio donde encontrarás los módulos y dependencias necesarias que deberás tener instaladas en tu máquina local para trabajar con el Rust🦀 eDSL llamado ink!🦑 y Swanky en Linux.
</p>
<h3 align="center">
  Pre-requisitos
</h3>
<p>
  1. Deberás tener instalado un sistema operativo <a href="https://www.stackscale.com/es/blog/distribuciones-linux-populares/">linux</a> o en caso de poseer Windows, con tener <a href="https://learn.microsoft.com/es-es/windows/wsl/install">WSL</a> podrás trabajar. <br>
  2. Deberás contar con experiencia manejando la terminal. <br>
  3. Tendrás que tener los permisos de súper usuario. <br>
  4. Tener experiencia usando manejadores de paquetes, como <a href="https://www.debian.org/doc/manuals/aptitude/pr01s03.es.html">apt</a>. <br>
  5. (Opcional) Instala la extensión de <a href="https://www.subwallet.app/">SubWallet</a> en tu navegador.
  
  Con esto estarás lista o listo para seguir el tutorial.
</p>
<hr>
<h3 align="center">
  Compilador compatible con C
</h3>
<p>
  Lo primero que debes hacer es incluir un enlazador o un compilador compatible con <a href="https://www.google.com/search?q=c+programming+language&oq=c+programming+language&aqs=chrome.0.0i355i512i543j46i340i512j0i512l5j69i60.8316j0j7&sourceid=chrome&ie=UTF-8">C</a>, como <code>clang</code>, que es un entorno de desarrollo integrado (IDE). Ejecuta estos dos comandos en tu terminal: </p>
  <ul>
    <li><code>sudo apt install build-essential</code></li>
    <li><code>sudo apt install clang curl git make</code></li>
  </ul>
  <hr>
<h3 align="center">
  Instalar un paquete de criptografía
</h3>
<p>
  Debido a que la cadena de bloques requiere criptografía estándar para admitir la generación de pares de claves pública/privada y la validación de firmas de             transacciones, también debes tener un paquete que proporcione criptografía. Ejecuta el siguiente comando: </p>
<ul>
  <li><code>sudo apt install libssl-dev</code></li> 
</ul>
<p>
  Además, debes instalar un paquete con todas las características necesarias para trabajar con <code>libssl-dev</code>. Ejecuta este comando: </p>
  <ul>
    <li><code>sudo apt install pkg-config</code></li>
  </ul>
 <p>
  Por último, ejecuta este comando para descargar algunas herramientas esenciales antes de instalar Rust 🦀: </p>
  <ul>
    <li><code>sudo apt install --assume-yes git clang curl libssl-dev protobuf-compiler</code></li>
  </ul>
<hr>
<h3 align="center">
  Instalar Rust 🦀
</h3>
<p>
  ¡Ahora sí, a instalar Rust! 🦀 Ejecuta el siguiente comando en tu terminal: </p>
  <ul>
    <li><code>curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh</code></li>
  </ul>
<p>
Este comando descargará las herramientas y las características necesarias del lenguaje para desarrollar con el. Luego necesitarás incluir a <code>cargo</code> a tu shell, ejecuta alguno de los siguientes comandos: </p>
<ul>
  <li><code>source $HOME/.cargo/env</code></li>
  <li><code>source ~/.cargo/env</code></li>
</ul>
<p>Verifica que se haya instalado de forma correcta:</p>
<ul>
  <li><code>cargo --version</code></li>
  <li><code>rustc --version</code></li>
</ul>

<p>Si ya tenías instalado Rust, lo más recomendable es que cada cierto tiempo lo actualices a la versión más reciente. Ejecuta estos comandos en tu terminal para actualizarlo: </p>
<ul>
  <li><code>rustup default stable</code></li>
  <li><code>rustup update</code></li>
</ul>
<hr>
<h3 align="center">
  Instalar herramientas de Web Assembly
</h3>
<p>
  Necesitas instalar unas herramientas específicas para trabajar con Web Assembly. Ejecuta estos cuatro comandos: </p>
  <ul>
    <li><code>rustup update nightly</code></li>
    <li><code>rustup component add rust-src</code></li>
    <li><code>rustup component add rust-src --toolchain nightly</code></li>
    <li><code>rustup target add wasm32-unknown-unknown --toolchain nightly</code></li>
  </ul>
  <p>
    Verifica que haya quedado instalado de forma correcta con estos comandos: </p>
    <ul>
      <li><code>rustup show</code></li>
      <li><code>rustup +nightly show</code></li>
    </ul>
    <p>El output en tu terminal debería verse así:</p>
    <img src="/Linux/commands.png"/>
    <p>
  Es posible que debas instalar el  paquete <code>binaryen</code> que se utiliza para optimizar el código de bytes de un contrato de Web Assembly. Ejecuta estos comandos en tu terminal: </p>
  <ul>
    <li><code>sudo apt update</code></li>
    <li><code>sudo apt -y install binaryen</code> </li>
  </ul>
<hr>
<h3 align="center">
  Dependencias para el uso de las APIs
</h3>
<p>
  Se deben instalar otras dos dependencias para vincular a Ink!, por ejemplo, para advertir a los usuarios sobre el uso de las API de una manera que podría generar problemas de seguridad. Ejecuta este comando: </p>
  <ul>
    <li><code>cargo install cargo-dylint dylint-link</code></li>
  </ul>
<hr>
<h3 align="center">
  ¡Instalemos <code>cargo-contract</code>!
</h3>
<p>
  <code>cargo contract</code> es la herramienta de CLI para crear, actualizar, interactuar y compilar nuestros contratos y que trae muchas opciones más, por cierto. Ejecuta el siguiente comando en tu terminal: </p>
  <ul>
    <li><code>cargo install cargo-contract --force --locked</code></li>
  </ul>
  <p>
  Verifica que se haya instalado con éxito haciendo uso del siguiente comando: </p>
  <ul>
    <li><code>cargo contract --version</code></li>
  </ul>
<hr>
<h3 align="center">
  ¡Instalemos las famosas herramientas de Swanky suite! 🧑🏻‍💻
</h3>
<p>
  <a href="https://github.com/swankyhub">Swanky suite</a> es un conjunto de herramientas muy especiales para el desarrollo de contratos inteligentes en un entorno local. Es similar a <a href="https://hardhat.org/">HardHat</a> del ecosistema EVM. A swanky lo podemos instalar de diferentes maneras; acá te comparto un recurso que te explicará cinco formas de instalar Swanky: <a href="https://docs.astar.network/docs/build/wasm/swanky-suite/"><code>Instalar swanky</code></a>.
</p>
<h3 align="center">
  Adicional: Reduce trabajo con el <code>Swanky-container</code>
</h3>
<p>
  También podrás reducir todo este trabajo a una sola acción a través del <code>Swanky-container</code>, podrás leer y conocer más de esta alternativa a la configuración manual a través de este <a href="https://github.com/AstarNetwork/swanky-dev-container">repositorio de GitHub</a>.
</p>
<p>Te invito a que visites el repositorio de <a href="https://github.com/inkdevhub">InkDevHub</a> donde encontrarás plantillas y otras herramientas que podrás usar para desarrollar con ink! 🦑.</p>
<hr>
<h3 align="center">¡Felicitaciones!</h3>
<p>
  ¡Felicidades! Con esto tendrás tu entorno de desarrollo local listo para trabajar con ink!🦑 y crear aplicaciones robustas con Swanky.
</p>
