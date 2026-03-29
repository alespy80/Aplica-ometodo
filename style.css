const TOTAL = 6;
let etapaAtual = 0;

function avancar(n) {
  // Ocultar atual
  const atual = document.getElementById(`etapa-${etapaAtual}`);
  if (atual) { atual.classList.remove("ativa"); atual.classList.add("oculta"); }

  // Mostrar nova
  etapaAtual = n;
  const nova = document.getElementById(`etapa-${etapaAtual}`);
  if (nova) { nova.classList.remove("oculta"); nova.classList.add("ativa"); }

  // Atualizar barra
  const pct = (etapaAtual / TOTAL) * 100;
  document.getElementById("progress-bar").style.width = pct + "%";

  // Atualizar dots
  atualizarDots();

  // Scroll para o topo
  window.scrollTo({ top: 0, behavior: "smooth" });
}

function atualizarDots() {
  const wrap = document.getElementById("steps-indicator");
  wrap.innerHTML = "";
  for (let i = 0; i <= TOTAL; i++) {
    const d = document.createElement("div");
    d.className = "si-dot";
    if (i < etapaAtual)  d.classList.add("concluida");
    if (i === etapaAtual) d.classList.add("ativa");
    d.onclick = () => { if (i <= etapaAtual) avancar(i); };
    d.title = `Etapa ${i}`;
    wrap.appendChild(d);
  }
}

function reiniciar() {
  avancar(0);
}

// Init
atualizarDots();
