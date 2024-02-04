<h1 align="center">Ink! toolkit for MacOS 🍏</h1>
<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdTc5NjVwdjJhNjdkNXE0MzZpaXdmemRrbDByMGI1NTlxdXg4aTl1aSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bfrlODgSLqXxS/giphy.gif" align="right" width="210">
<p>
  Repositorio donde encontrarás los módulos y dependencias necesarias que deberás tener instaladas en tu máquina local para trabajar con el Rust🦀 eDSL llamado ink!🦑 y Swanky en MacOS 🍏.
</p>
<h3 align="center">
  Pre-requisitos
</h3>
<p>
  1. Deberás tener instalado un sistema operativo MacOS 🍏.<br>
  2. Instala un manejador de paquetes, te recomiendo <a href="https://brew.sh/">Homebrew</a>.<br>
  3. Instala en tu máquina las herramientas de <a href="https://mac.install.guide/commandlinetools/3">Xcode</a>.<br>
  4. Contar con experiencia usando la terminal, para instalar paquetes.<br>
  5. (Opcional) Instala la extensión de <a href="https://www.subwallet.app/">SubWallet</a> en tu navegador.
  
  ¡Con esto estarás lista o listo para seguir el tutorial!
</p>
<hr>
<h3 align="center">
  Compilador GCC
</h3>
<p>
  Lo primero que debes hacer es instalar el compilador portable <a href="https://osxdaily.com/2023/05/02/how-install-gcc-mac/">GCC</a> que se ejecuta en la mayoría de las plataformas disponibles. Ejecuta este comando en tu terminal: </p>
  <ul>
    <li><code>brew install gcc</code></li>
  </ul>
  <hr>
  <h3 align="center">
  Herramienta protobuf
</h3>
<p>
  <a href="https://protobuf.dev/">Protobuf</a> es un formato de serialización de datos que se utiliza para estructurar datos de manera eficiente e intercambiar información entre diferentes lenguajes de programación. Ejecuta este comando en tu terminal: </p>
  <ul>
    <li><code>brew install protobuf</code></li>
  </ul>
  <hr>
<h3 align="center">
  Paquete criptográfico
</h3>
<p>
  Debido a que la cadena de bloques requiere criptografía estándar para admitir la generación de pares de claves pública/privada y la validación de firmas de transacciones, también debes tener un paquete que proporcione criptografía. Ejecuta éstos comandos: </p>
<ul>
  <li><code>brew install openssl</code></li> 
</ul>
 <p>
  Por último, ejecuta este comando para verificar y/o descargar algunas herramientas esenciales antes de instalar Rust 🦀: </p>
  <ul>
    <li><code> brew install --only-dependencies git curl gcc protobuf openssl</code></li>
  </ul>
<hr>
<h3 align="center">
  Instalación de Rust 🦀
</h3>
<p>
  ¡Ahora sí, a instalar Rust! 🦀 Ejecuta el siguiente comando en tu terminal: </p>
  <ul>
    <li><code>curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh</code></li>
  </ul>
<p>
Este comando descargará un script con el instalador de rust, <a href="https://rustup.rs/">Rustup</a>, quién se encargará de alojarlo en tu máquina local y mantener las versiones. Ejecuta el siguiente comando: </p>
<ul>
  <li><code>source "$HOME/.cargo/env"</code></li>
</ul>
<p>Verifica que se haya instalado de forma correcta:</p>
<ul>
  <li><code>cargo --version</code></li>
  <li><code>rustc --version</code></li>
</ul>

<p>Si ya tenías instalado Rust, lo más recomendable es que cada cierto tiempo (min 3 meses) lo actualices a la versión más reciente. Ejecuta estos comandos en tu terminal para actualizarlo: </p>
<ul>
  <li><code>rustup default stable</code></li>
  <li><code>rustup update</code></li>
</ul>
<hr>
<h3 align="center">
  Instalar herramientas de Web Assembly
</h3>
<p>
  Necesitas instalar unas herramientas específicas para trabajar con Web Assembly. Ejecuta estos cinco comandos: </p>
  <ul>
    <li><code>rustup update nightly</code></li>
    <li><code>rustup component add rust-src</code></li>
    <li><code>rustup target add wasm32-unknown-unknown</code></li>
    <li><code>rustup component add rust-src --toolchain nightly</code></li>
    <li><code>rustup target add wasm32-unknown-unknown --toolchain nightly</code></li>
  </ul>
  <p>
    Verifica que hayan quedado instalados de forma correcta con estos comandos: </p>
    <ul>
      <li><code>rustup show</code></li>
      <li><code>rustup +nightly show</code></li>
    </ul>
    <p>El output en tu terminal debería verse así:</p>
    <img src="/MacOS/commands.png"/>
    <p>
  Es posible que debas instalar el  paquete <code>binaryen</code> que se utiliza para optimizar el código de bytes de un contrato de Web Assembly. Ejecuta este comando en tu terminal: </p>
  <ul>
    <li><code>brew install binaryen</code> </li>
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
  ¡Instalemos las famosas herramientas de Swanky suite 😎!
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
<hr>
<h3 align="center">¡Felicitaciones!</h3>
<p>
  ¡Felicidades! Con esto tendrás tu entorno de desarrollo local listo para trabajar con ink!🦑 y crear aplicaciones robustas con Swanky.
</p>
