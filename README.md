<h1 align="center">Workshop de ink! - toolkit</h1>
<img src="https://media0.giphy.com/media/hvXcXEyDpdV1uZJ0nJ/200w.webp?cid=ecf05e470gqc03fx9wa4nt2zjp9lvodxtmmq3oe1a0jx211w&ep=v1_gifs_search&rid=200w.webp&ct=g" align="right" width="300">
<p>
  Aquí encontrarás las herramientas y características que deberás tener instaladas para llevar a cabo con éxito el workshop #2 de ink! y Astar Network en Medellín, Universidad EAFIT.
</p>
<h3 align="center">
  Pre-requisitos
</h3>
<p>
  1. Deberás tener instalado un sistema operativo linux, Unix o en caso de poseer Windows, con tener WSL podrás trabajar. <br>
  2. Instala en tu Visual Studio Code, la extensión de <a href="https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer">Rust-Analizer</a>. <br>
  
  Con esto estarás lista o listo para seguir el tutorial.
</p> <br>
<h3 align="center">
  Compilador compatible con C
</h3>
<p>
  Lo primero que debes hacer es incluir un enlazador o un compilador compatible con <a href="https://www.google.com/search?q=c+programming+language&oq=c+programming+language&aqs=chrome.0.0i355i512i543j46i340i512j0i512l5j69i60.8316j0j7&sourceid=chrome&ie=UTF-8">C</a> como <code>clang</code> que es un entorno de desarrollo integrado (IDE). Ejecuta estos dos comandos: <br>
  <div align="center">
  <code>sudo apt install build-essential</code> & <code>sudo apt install clang curl git make</code>
  </div>
</p>
<h3 align="center">
  Instalar un paquete de criptografía
</h3>
<p>
  Debido a que la cadena de bloques requiere criptografía estándar para admitir la generación de pares de claves pública/privada y la validación de firmas de transacciones, también debes tener un paquete que proporcione criptografía. Ejecuta el siguiente comando:
  <div align="center"> <code>sudo apt install libssl-dev</code> </div> <br>
  Además, debes instalar un paquete con todas las características necesarias para trabajar con <code>libssl-dev</code>. Ejecuta este comando: 
  <div align="center"> <code>sudo apt install pkg-config</code> </div> <br>
  Existe un comando que te descargará todo lo necesario antes de poder instalar Rust: <br><br>
  <div align="center"> <code>sudo apt install --assume-yes git clang curl libssl-dev protobuf-compiler</code> </div>
</p>
<h3 align="center">
  Instalar Rust 🦀
</h3>
<p>
  ¡Ahora sí, a instalar Rust 🦀! Ejecuta el siguiente comando en tu terminal: <br>
<div align="center"> <code>curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh</code> </div> <br>

Este comando descargará las herramientas y las características del lenguaje necesarias para desarrollar con el. Luego necesitarás incluir a <code>cargo</code> a tu shell, ejecuta alguno de los siguientes comandos: <br>
<div align="center"> <code>source $HOME/.cargo/env</code> o <code>source ~/.cargo/env</code> </div> <br>

Verifica que se haya instalado de forma correcta: <br>
<div align="center"> <code>cargo --version</code> o <code>rustc --version</code> </div> <br>

<i>Si ya tenías instalado Rust, lo más recomendable es que cada cierto tiempo lo actualices a la versión más reciente. Ejecuta estos comandos en tu terminal para actualizarlo: </i> <br>
<div align="center"> <code>rustup default stable</code> & <code>rustup update</code> </div>
</p>
<h3 align="center">
  Instalar herramientas de Web Assembly
</h3>
<p>
  Necesitas instalar unas herramientas específicas para trabajar con Web Assembly. Ejecuta estos 4 comandos: <br>
  <div align="center"> <code>rustup component add rust-src</code> & <code>rustup update nightly</code> & <code>rustup component add rust-src --toolchain nightly</code> & <code>rustup target add wasm32-unknown-unknown --toolchain nightly</code> </div> <br>
  Verifica que haya quedado instalado de forma correcta con estos comandos: <br><br>
  <div align="center"> <code>rustup show</code> & <code>rustup +nightly show</code> </div> <br>
  Es posible que debas instalar el  paquete binaryen, que se utiliza para optimizar el código de bytes de un contrato de Web Assembly. Ejecuta estos comandos: <br><br>
  <div align="center"> <code>sudo apt update</code> & <code>sudo apt -y install binaryen</code> </div>
</p>
<h3 align="center">
  Dependencias para el uso de las APIs
</h3>
<p>
  Se deben instalar otras dos dependencias para vincular a Ink!, por ejemplo, para advertir a los usuarios sobre el uso de las API de una manera que podría generar problemas de seguridad. Ejecuta este comando: <br>
  <div align="center"> <code>cargo install cargo-dylint dylint-link</code> </div>
</p>
<h3 align="center">
  ¡Instalemos <code>cargo-contract</code>!
</h3>
<p>
  <code>cargo contract</code> es la herramienta de CLI para crear, actualizar, compilar nuestros contratos y que trae muchas opciones más por cierto. Ejecuta el siguiente comando en tu terminal: <br>
  <div align="center"> <code>cargo install cargo-contract --force --locked</code> </div> <br>
  Verifica que se haya instalado con éxito haciendo uso del siguiente comando: <br><br>
  <div align="center"> <code>cargo contract --version</code> </div>
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
  
  También podrás usar la <a href="https://portal.astar.network/shibuya-testnet/assets">Astar Portal</a>.
</p>
<h3 align="center">¡Felicitaciones!</h3>
<p>
  ¡Felicidades! Con esto tendrás un entorno de desarrollo listo y preparado para llevar a cabo el <a href="https://twitter.com/dotlabs__/status/1651325286342963200?s=20">Workshop de Astar Network</a> por parte del equipo de <a href="https://dotlabs.academy/">dotlabs()</a>.
</p>
