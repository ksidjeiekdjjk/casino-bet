<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Casino 365X</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="logo-nav">
      <div class="logo">🎰 Casino 365X</div>
      <nav>
        <button class="menu-btn" id="menuOpen">☰</button>
        <ul id="menuNav">
          <li><a href="#" class="active" data-section="presentacion">Inicio</a></li>
          <li><a href="#" data-section="juegos">Juegos</a></li>
          <li><a href="#" data-section="cuenta">Mi Cuenta</a></li>
        </ul>
      </nav>
    </div>
    <div id="saldo-container">
      Saldo: <span id="saldo">1000</span> créditos
      <button id="recargarBtn">Recargar</button>
    </div>
  </header>
  <main>
    <section id="presentacion">
      <h2>¡Bienvenido a Casino 365X!</h2>
      <p>Disfruta de los mejores juegos, gana créditos y vive la experiencia más divertida en línea.</p>
      <button id="irJuegosBtn">Ir a Juegos</button>
    </section>
    <section id="juegos" class="oculto">
      <h2>Juegos disponibles</h2>
      <div class="juego-card" id="slotCard">
        <h3>Tragaperras Deluxe</h3>
        <div id="slot-machine">
          <div id="slots">
            <span id="slot1">🍒</span>
            <span id="slot2">🍋</span>
            <span id="slot3">🍉</span>
          </div>
          <label>
            Apuesta:
            <input type="number" id="apuesta" min="1" max="100" value="10">
          </label>
          <button id="spinBtn">Girar</button>
          <p id="result"></p>
        </div>
      </div>
    </section>
    <section id="cuenta" class="oculto">
      <h2>Mi Cuenta</h2>
      <p>Usuario: <strong>invitado</strong></p>
      <p>Saldo actual: <span id="saldoCuenta">1000</span> créditos</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2025 Casino 365X. Juego responsable y diversión garantizada.</p>
  </footer>
  <script src="casino.js"></script>
</body>
</html>
:root {
  --color-principal: #2b56a3;
  --color-secundario: #f7c948;
  --color-fondo: #181f2a;
  --color-texto: #fff;
  --color-boton: #f7c948;
  --color-boton-hover: #d4a326;
  --color-card: #223356;
}

body {
  background: var(--color-fondo);
  color: var(--color-texto);
  font-family: 'Segoe UI', Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  background: var(--color-principal);
  color: var(--color-texto);
  padding: 1em 0.5em;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo-nav {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5em;
  font-weight: bold;
  letter-spacing: 1px;
}

nav {
  position: relative;
}

.menu-btn {
  display: none;
  background: none;
  border: none;
  color: var(--color-secundario);
  font-size: 1.7em;
  cursor: pointer;
  margin-right: 1em;
}

nav ul {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

nav ul li {
  margin-left: 1em;
}

nav a {
  color: var(--color-secundario);
  text-decoration: none;
  font-weight: bold;
  padding: 0.5em 0.8em;
  border-radius: 4px;
  transition: background 0.2s, color 0.2s;
}

nav a.active, nav a:hover {
  color: var(--color-texto);
  background: var(--color-boton-hover);
}

#saldo-container {
  background: #1b355c;
  padding: 0.5em 1em;
  border-radius: 8px;
  margin-top: 0.7em;
  display: flex;
  align-items: center;
  gap: 1em;
}

main {
  max-width: 700px;
  margin: 2em auto;
  padding: 1em;
}

section {
  margin-bottom: 2em;
}

h2 {
  color: var(--color-secundario);
}

.juego-card {
  background: var(--color-card);
  border-radius: 12px;
  padding: 1em;
  margin-top: 1em;
  box-shadow: 0 2px 8px #0002;
}

#slot-machine {
  margin-top: 1em;
}

#slots {
  font-size: 2.5em;
  margin-bottom: 0.7em;
  letter-spacing: 0.5em;
}

label {
  font-weight: bold;
  margin-right: 0.5em;
}

input[type="number"] {
  width: 60px;
  padding: 0.3em;
  font-size: 1em;
  border-radius: 4px;
  border: none;
  margin-right: 0.5em;
}

button {
  background: var(--color-boton);
  color: #222;
  border: none;
  border-radius: 6px;
  padding: 0.5em 1.2em;
  font-size: 1em;
  cursor: pointer;
  font-weight: bold;
  margin-top: 0.3em;
}

button:hover {
  background: var(--color-boton-hover);
}

#result {
  margin-top: 1em;
  font-size: 1.1em;
  min-height: 1.5em;
}

footer {
  background: var(--color-principal);
  color: #fff;
  text-align: center;
  padding: 1em 0;
  margin-top: 2em;
}

/* Ocultar secciones */
.oculto {
  display: none;
}

/* Responsive */
@media (max-width: 800px) {
  main {
    padding: 0.3em;
  }
  #saldo-container {
    flex-direction: column;
    gap: 0.3em;
  }
  .logo-nav {
    flex-direction: column;
    align-items: flex-start;
  }
}

@media (max-width: 600px) {
  nav ul {
    flex-direction: column;
    background: var(--color-principal);
    position: absolute;
    right: 0;
    top: 2.5em;
    min-width: 150px;
    border-radius: 8px;
    box-shadow: 0 4px 10px #0005;
    display: none;
  }
  nav ul.show {
    display: block;
  }
  .menu-btn {
    display: inline;
  }
}
// Navegación entre secciones con menú responsive
const navLinks = document.querySelectorAll('nav a');
const sections = {
  presentacion: document.getElementById('presentacion'),
  juegos: document.getElementById('juegos'),
  cuenta: document.getElementById('cuenta'),
};
navLinks.forEach(link => {
  link.addEventListener('click', (e) => {
    e.preventDefault();
    navLinks.forEach(l => l.classList.remove('active'));
    link.classList.add('active');
    Object.values(sections).forEach(sec => sec.classList.add('oculto'));
    const id = link.dataset.section || 'presentacion';
    if (sections[id]) sections[id].classList.remove('oculto');
    if (id === 'cuenta') actualizaSaldoCuenta();
    cerrarMenu();
  });
});

// Botón "Ir a Juegos"
document.getElementById('irJuegosBtn').onclick = () => {
  navLinks[1].click();
};

// Menú Responsive
const menuBtn = document.getElementById('menuOpen');
const menuNav = document.getElementById('menuNav');
menuBtn.onclick = function() {
  menuNav.classList.toggle('show');
};
function cerrarMenu() {
  if (window.innerWidth <= 600) {
    menuNav.classList.remove('show');
  }
}
window.addEventListener('resize', cerrarMenu);

// Saldo ficticio
let saldo = 1000;
const saldoSpan = document.getElementById('saldo');
const saldoCuentaSpan = document.getElementById('saldoCuenta');
const recargarBtn = document.getElementById('recargarBtn');
recargarBtn.onclick = () => {
  saldo = 1000;
  actualizaSaldo();
  actualizaSaldoCuenta();
};

function actualizaSaldo() {
  saldoSpan.textContent = saldo;
}
function actualizaSaldoCuenta() {
  saldoCuentaSpan.textContent = saldo;
}
actualizaSaldo();

// Tragaperras
const emojis = ["🍒", "🍋", "🍉", "🍇", "🍀", "🍊"];
const slots = [
  document.getElementById("slot1"),
  document.getElementById("slot2"),
  document.getElementById("slot3"),
];
const spinBtn = document.getElementById("spinBtn");
const apuestaInput = document.getElementById("apuesta");
const result = document.getElementById("result");

spinBtn.onclick = function () {
  const apuesta = parseInt(apuestaInput.value, 10);
  if (isNaN(apuesta) || apuesta < 1 || apuesta > saldo) {
    result.textContent = "Apuesta inválida.";
    return;
  }
  saldo -= apuesta;
  actualizaSaldo();
  actualizaSaldoCuenta();

  // Girar los slots
  for (let i = 0; i < slots.length; i++) {
    const rand = Math.floor(Math.random() * emojis.length);
    slots[i].textContent = emojis[rand];
  }

  // Lógica de premios
  if (
    slots[0].textContent === slots[1].textContent &&
    slots[1].textContent === slots[2].textContent
  ) {
    const premio = apuesta * 10;
    saldo += premio;
    actualizaSaldo();
    actualizaSaldoCuenta();
    result.textContent = `¡Felicidades! Ganaste ${premio} créditos 🎉`;
  } else if (
    slots[0].textContent === slots[1].textContent ||
    slots[1].textContent === slots[2].textContent ||
    slots[0].textContent === slots[2].textContent
  ) {
    const premio = apuesta * 2;
    saldo += premio;
    actualizaSaldo();
    actualizaSaldoCuenta();
    result.textContent = `¡Casi! Te llevas ${premio} créditos.`;
  } else {
    result.textContent = "Sin premio. ¡Intenta de nuevo!";
  }
};
