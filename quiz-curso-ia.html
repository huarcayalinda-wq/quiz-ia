<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Quiz — Curso Avanzado de IA</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body { background: #0d2619; min-height: 100vh; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif; display: flex; align-items: flex-start; justify-content: center; padding: 2rem 1rem; }
  .container { width: 100%; max-width: 640px; }
  .header { text-align: center; margin-bottom: 2rem; }
  .header h1 { color: #a8e6c3; font-size: 22px; font-weight: 600; margin-bottom: 4px; }
  .header p { color: #6abf8a; font-size: 14px; }
  .progress-bg { background: #1a3d2b; border-radius: 8px; height: 8px; margin-bottom: 1.5rem; }
  .progress-fill { background: #3db87a; height: 8px; border-radius: 8px; transition: width 0.4s ease; }
  .card { background: #1a3d2b; border: 1px solid #2a5c3f; border-radius: 14px; padding: 1.5rem; }
  .q-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 1rem; }
  .q-num { font-size: 13px; color: #6abf8a; font-weight: 500; }
  .badge { font-size: 11px; padding: 3px 12px; border-radius: 20px; font-weight: 600; letter-spacing: 0.3px; }
  .b-facil { background: #0d4020; color: #5dd49a; }
  .b-medio { background: #3d3000; color: #f0c040; }
  .b-dificil { background: #4d1010; color: #f08080; }
  .q-text { color: #d4f0e2; font-size: 16px; line-height: 1.6; margin-bottom: 1.25rem; font-weight: 500; }
  .options { display: flex; flex-direction: column; gap: 10px; }
  .opt { background: #0d2619; border: 1px solid #2a5c3f; border-radius: 10px; padding: 12px 16px; color: #a8e6c3; font-size: 14px; cursor: pointer; text-align: left; transition: background 0.15s, border-color 0.15s; line-height: 1.5; }
  .opt:hover:not(:disabled) { background: #1e4030; border-color: #3db87a; }
  .opt.correct { background: #0d4020; border-color: #3db87a; color: #5dd49a; font-weight: 500; }
  .opt.wrong { background: #4d1010; border-color: #c0392b; color: #f08080; }
  .opt.reveal { background: #0d4020; border-color: #3db87a; color: #5dd49a; }
  .opt:disabled { cursor: default; }
  .feedback { margin-top: 14px; font-size: 13px; padding: 10px 14px; border-radius: 10px; display: none; line-height: 1.5; }
  .feedback.show { display: block; }
  .fb-ok { background: #0d4020; color: #5dd49a; border: 1px solid #2a7a45; }
  .fb-fail { background: #4d1010; color: #f08080; border: 1px solid #8b2a2a; }
  .nav { display: flex; justify-content: space-between; align-items: center; margin-top: 1.25rem; }
  .score-txt { font-size: 13px; color: #6abf8a; }
  .next-btn { background: #3db87a; color: #0d2619; border: none; padding: 10px 24px; border-radius: 10px; font-size: 14px; font-weight: 600; cursor: pointer; transition: background 0.15s; }
  .next-btn:hover:not(:disabled) { background: #5dd49a; }
  .next-btn:disabled { background: #2a5c3f; color: #6abf8a; cursor: default; }
  .result { text-align: center; padding: 1rem 0; }
  .result h2 { color: #a8e6c3; font-size: 20px; margin-bottom: 0.5rem; }
  .big { font-size: 56px; font-weight: 700; color: #3db87a; line-height: 1; margin: 0.75rem 0; }
  .result-msg { color: #6abf8a; font-size: 14px; line-height: 1.6; max-width: 340px; margin: 0 auto 1.5rem; }
  .restart { background: #3db87a; color: #0d2619; border: none; padding: 12px 32px; border-radius: 10px; font-size: 15px; font-weight: 600; cursor: pointer; }
  .restart:hover { background: #5dd49a; }
</style>
</head>
<body>
<div class="container">
  <div class="header">
    <h1>Quiz — Curso Avanzado de IA</h1>
    <p>15 preguntas · de fácil a difícil</p>
  </div>
  <div class="progress-bg"><div class="progress-fill" id="prog" style="width:0%"></div></div>
  <div class="card" id="area"></div>
</div>

<script>
const qs = [
  { q:"¿Qué significa API?", opts:["Application Programming Interface","Automated Process Integration","Advanced Protocol Index","Application Process Input"], ans:0, diff:"fácil", fb:"API = Interfaz de Programación de Aplicaciones. Es el contrato que permite que dos sistemas hablen entre sí." },
  { q:"¿Cuál es la función principal de n8n en el stack del curso?", opts:["Base de datos relacional","Orquestador de flujos","Deploy del frontend","Canal de mensajería"], ans:1, diff:"fácil", fb:"n8n conecta y automatiza los flujos entre servicios sin necesidad de código complejo." },
  { q:"¿Qué herramienta se usa para el deploy del frontend en el stack del curso?", opts:["Railway","Supabase","Vercel","GitHub Actions"], ans:2, diff:"fácil", fb:"Vercel es la plataforma optimizada para frontends y sitios estáticos." },
  { q:"¿Cuál es la diferencia clave entre un bot y un agente?", opts:["El bot usa IA y el agente no","El agente decide y actúa, el bot solo responde","El bot trabaja 24/7 y el agente no","No hay diferencia real"], ans:1, diff:"fácil", fb:"El agente puede tomar decisiones propias y escalar; el bot solo responde a comandos predefinidos." },
  { q:"¿Dónde se deben guardar las API keys en producción?", opts:["En el código fuente","En un archivo README","En variables de entorno","En Google Sheets"], ans:2, diff:"fácil", fb:"Las API keys NUNCA deben estar en el código. Siempre en variables de entorno del servidor." },
  { q:"¿Qué ventaja tiene Supabase sobre Google Sheets para la memoria del agente?", opts:["Es más barato","Tiene tablas relacionales e historial real","Funciona sin internet","Es más fácil de usar"], ans:1, diff:"medio", fb:"Supabase soporta relaciones entre tablas, historial completo de conversaciones y escala correctamente." },
  { q:"¿Qué es un webhook en el contexto de WhatsApp Business API?", opts:["Un tipo de mensaje de texto","Un endpoint que recibe notificaciones en tiempo real","Un sistema de pago","Una interfaz visual"], ans:1, diff:"medio", fb:"El webhook es el endpoint de tu servidor que Meta llama automáticamente cuando llega un mensaje." },
  { q:"¿Qué hace el Code Node en n8n?", opts:["Genera código automáticamente","Permite ejecutar JavaScript dentro del flujo","Conecta con GitHub","Despliega el backend"], ans:1, diff:"medio", fb:"El Code Node te da control total con JavaScript personalizado dentro del flujo de automatización." },
  { q:"¿Para qué sirve Railway en el stack del curso?", opts:["Deploy del frontend","Control de versiones","Deploy y hosting del backend","Base de datos principal"], ans:2, diff:"medio", fb:"Railway corre el servidor backend con HTTPS, logs en tiempo real y CI/CD automático." },
  { q:"¿Qué parámetro define el comportamiento base del agente en la Claude API?", opts:["model","max_tokens","system prompt","temperature"], ans:2, diff:"medio", fb:"El system prompt establece las instrucciones base, personalidad y contexto del agente." },
  { q:"En FacturaBot v2, ¿qué capacidad de Claude se usa para leer la foto de la factura?", opts:["Text completion","Vision API","Embeddings API","Batch processing"], ans:1, diff:"difícil", fb:"Vision API permite a Claude procesar imágenes y extraer datos estructurados (JSON) de ellas." },
  { q:"¿Cómo se valida que un webhook realmente viene de Meta y no de un atacante?", opts:["Comparando el IP de origen","Verificando la firma HMAC-SHA256 del payload con tu app secret","Chequeando el user-agent","No se puede validar"], ans:1, diff:"difícil", fb:"Meta firma cada petición con HMAC-SHA256 usando tu app secret. Debes calcular y comparar esa firma." },
  { q:"¿Qué problema resuelve el CI/CD automático al hacer push a GitHub?", opts:["Genera documentación automática","Despliega la nueva versión sin intervención manual","Envía notificaciones al equipo","Actualiza la base de datos"], ans:1, diff:"difícil", fb:"Con CI/CD, cada push a main dispara el pipeline que despliega automáticamente en Railway o Vercel." },
  { q:"¿Cuál es el riesgo principal de no implementar rate limiting en el bot de WhatsApp?", opts:["El bot responde más lento","Un usuario malintencionado puede agotar tus créditos de API generando costos masivos","Los mensajes llegan duplicados","La conexión con Supabase se pierde"], ans:1, diff:"difícil", fb:"Sin rate limiting, cualquier persona puede hacer spam al bot y disparar tu gasto en Claude API y WhatsApp." },
  { q:"Si el historial de conversación crece sin límite en Supabase, ¿qué impacto técnico tiene?", opts:["Ninguno, Supabase escala infinitamente gratis","El context window de Claude se llena y los prompts se vuelven más costosos y lentos","La base de datos se corrompe","n8n deja de funcionar"], ans:1, diff:"difícil", fb:"El context window tiene límite de tokens. Debes implementar truncado o resumen del historial para no excederlo ni inflar costos." }
];

let cur = 0, score = 0, answered = false;

function badge(d) {
  const cls = d==="fácil"?"b-facil":d==="medio"?"b-medio":"b-dificil";
  return `<span class="badge ${cls}">${d}</span>`;
}

function render() {
  const area = document.getElementById("area");
  if (cur >= qs.length) {
    const pct = Math.round((score/qs.length)*100);
    const msg = pct>=80?"¡Excelente dominio del stack! Estás listo para el curso avanzado.":pct>=50?"Buen avance. Repasa los módulos intermedios y vuelve a intentarlo.":"Repasa los fundamentos antes de entrar al curso avanzado.";
    area.innerHTML = `<div class="result">
      <h2>Quiz completado</h2>
      <div class="big">${score}/${qs.length}</div>
      <p class="result-msg">${pct}% correcto · ${msg}</p>
      <button class="restart" onclick="restart()">Intentar de nuevo</button>
    </div>`;
    document.getElementById("prog").style.width = "100%";
    return;
  }
  answered = false;
  const q = qs[cur];
  document.getElementById("prog").style.width = Math.round((cur/qs.length)*100)+"%";
  area.innerHTML = `
    <div class="q-meta">
      <span class="q-num">Pregunta ${cur+1} de ${qs.length}</span>
      ${badge(q.diff)}
    </div>
    <div class="q-text">${q.q}</div>
    <div class="options">
      ${q.opts.map((o,i)=>`<button class="opt" id="o${i}" onclick="pick(${i})">${o}</button>`).join("")}
    </div>
    <div class="feedback" id="fb"></div>
    <div class="nav">
      <span class="score-txt">Puntaje: ${score}/${cur}</span>
      <button class="next-btn" id="nb" onclick="next()" disabled>${cur===qs.length-1?"Ver resultado →":"Siguiente →"}</button>
    </div>`;
}

function pick(i) {
  if (answered) return;
  answered = true;
  const q = qs[cur];
  const fb = document.getElementById("fb");
  for (let j=0;j<q.opts.length;j++) {
    const el = document.getElementById("o"+j);
    el.disabled = true;
    if (j===q.ans) el.classList.add(i===q.ans?"correct":"reveal");
  }
  if (i===q.ans) {
    score++;
    document.getElementById("o"+i).classList.add("correct");
    fb.className="feedback show fb-ok";
    fb.textContent="✓ Correcto. "+q.fb;
  } else {
    document.getElementById("o"+i).classList.add("wrong");
    fb.className="feedback show fb-fail";
    fb.textContent="✗ Incorrecto. "+q.fb;
  }
  document.getElementById("nb").disabled=false;
}

function next() { cur++; render(); }
function restart() { cur=0; score=0; render(); }

render();
</script>
</body>
</html>
