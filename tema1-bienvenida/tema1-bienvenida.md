---
marp: true
theme: ual
lang: es
size: 16:9
paginate: true
title: 'Bienvenida'
description: 'Taller de Informática'
header: 'Taller de Informática'
footer: 'Taller de Informática · Universidad de Mayores · UAL'
---

<style>
/* Docente (diapositiva normal, fondo blanco) */
section.docente { justify-content: center; }
section.docente > p:first-of-type {
  align-self: flex-start; margin: 0 0 18px;
  padding: 6px 16px; border: 2px solid var(--ual-claro); border-radius: 999px;
  font-size: 18px; font-weight: 800; letter-spacing: .18em; text-transform: uppercase; color: var(--ual);
}
section.docente h1 { font-size: 64px; font-weight: 900; color: var(--ual-tinta); margin-bottom: 0.15em; }
section.docente h1::after { margin-top: 16px; }
.datos { display: flex; gap: 16px; flex-wrap: wrap; margin: 6px 0 30px; }
.datos span {
  display: inline-flex; align-items: center; gap: 10px;
  background: var(--ual-velo); border: 2px solid var(--ual-claro);
  border-radius: 999px; padding: 8px 24px; font-size: 26px; font-weight: 700; color: var(--ual-oscuro);
}
.rotulo { font-size: 18px !important; font-weight: 800; letter-spacing: .18em; text-transform: uppercase; color: var(--texto-suave) !important; margin: 0 0 12px !important; }
.asignaturas { display: grid; grid-template-columns: 1fr 1fr; gap: 28px; max-width: 1000px; }
.asignatura {
  position: relative; overflow: hidden;
  background: #fff; color: var(--texto); border-radius: 22px;
  padding: 26px 30px 26px 132px; min-height: 150px;
  display: flex; flex-direction: column; justify-content: center;
  border: 2px solid var(--ual-claro); border-bottom: 8px solid var(--sol);
  box-shadow: 0 10px 28px rgba(35, 54, 70, .12);
}
.asignatura .ico {
  position: absolute; left: 26px; top: 50%; transform: translateY(-50%);
  width: 84px; height: 84px; border-radius: 20px; display: grid; place-items: center;
  font-size: 46px; background: var(--ual-velo);
}
.asignatura b { display: block; font-size: 33px; font-weight: 900; line-height: 1.1; color: var(--ual-tinta); }
.asignatura small { display: block; margin-top: 8px; font-size: 22px; line-height: 1.3; color: var(--texto-suave); }
.asignatura.redes { border-bottom-color: var(--ual); }

/* Los nueve temas */
.temas { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-top: 6px; }
.temas > div {
  display: flex; align-items: center; gap: 14px;
  background: #fff; border-radius: 16px; border-left: 7px solid var(--ual);
  box-shadow: 0 6px 18px rgba(35, 54, 70, .10);
  padding: 14px 18px; font-size: 25px; font-weight: 800; line-height: 1.15; color: var(--ual-tinta);
}
.temas > div span { font-size: 40px; line-height: 1; }
.temas > div.alerta { border-left-color: var(--alerta); }

/* DigComp: áreas y niveles */
.areas { display: grid; grid-template-columns: repeat(5, 1fr); gap: 16px; margin-top: 4px; }
.areas > div {
  background: #fff; border-radius: 18px; border-top: 7px solid var(--ual);
  box-shadow: 0 8px 22px rgba(35, 54, 70, .11); padding: 20px 18px 24px;
  font-size: 24px; line-height: 1.25; color: var(--texto-suave);
}
.areas > div:nth-child(2) { border-top-color: var(--sol); }
.areas > div:nth-child(3) { border-top-color: var(--ual-tinta); }
.areas > div:nth-child(4) { border-top-color: var(--alerta); }
.areas > div:nth-child(5) { border-top-color: var(--ual-oscuro); }
.areas .ico { display: block; font-size: 50px; line-height: 1; margin-bottom: 10px; }
.areas b { display: block; font-size: 28px; line-height: 1.1; color: var(--ual-tinta); margin-bottom: 6px; }
.areas i { display: block; font-style: normal; font-size: 16px; font-weight: 800; letter-spacing: .14em; color: var(--ual); margin-bottom: 4px; }
.competencias .tarjeta { font-size: 26px; padding: 20px 24px 22px; }
.competencias .tarjeta b { font-size: 29px; }
.competencias ol { margin: 8px 0 0; font-size: 26px; color: var(--texto); }
.competencias ol > li { padding-left: 1.9em; margin: 0.3em 0; color: var(--texto); }
.competencias ol > li::before { content: attr(data-n); width: auto; height: auto; padding: 0 7px; border-radius: 6px; font-size: 16px; line-height: 1.6; top: 0.12em; }
.niveles { display: flex; align-items: flex-end; gap: 18px; margin-top: 8px; }
.niveles > div {
  flex: 1; border-radius: 16px 16px 0 0; padding: 16px 18px; color: var(--ual-tinta);
  background: var(--ual-velo); border-bottom: 6px solid var(--ual-claro); font-size: 24px; line-height: 1.25;
}
.niveles b { display: block; font-size: 31px; margin-bottom: 4px; }
.niveles > div:nth-child(1) { height: 200px; }
.niveles > div.meta { background: var(--sol); border-bottom-color: var(--ual-tinta); }
.niveles.ejemplo > div { font-size: 22px; }
.niveles.ejemplo b { font-size: 27px; }
.niveles > div:nth-child(2) { height: 240px; }
.niveles > div:nth-child(3) { height: 280px; }
.niveles > div:nth-child(4) { height: 320px; }
.niveles + .nota { margin-top: 22px; font-size: 24px; }
.niveles small { display: inline-block; margin-top: 8px; padding: 2px 12px; border-radius: 999px; background: var(--ual-tinta); color: #fff; font-size: 16px; font-weight: 800; letter-spacing: .08em; text-transform: uppercase; }

/* Cada tema: escena de la vida real + lo que aprenderás */
.tema { grid-template-columns: 5fr 6fr; gap: 52px; }
.escena { background: var(--ual-velo); border-radius: 22px; padding: 26px 32px 18px; border-left: 10px solid var(--sol); }
.escena small, .tema .rotulo {
  display: block; margin: 0 0 12px; font-size: 18px; font-weight: 800;
  letter-spacing: .16em; text-transform: uppercase; color: var(--texto-suave);
}
.escena p { font-size: 31px; font-weight: 700; line-height: 1.25; color: var(--ual-tinta); margin: 0 0 .55em; }
.tema ul { font-size: 29px; margin: 0; }
.tema ul > li { margin: 0.32em 0; }
.tema .chat { font-size: 26px; }
section.riesgo .escena { background: var(--alerta-velo); border-left-color: var(--alerta); }

/* Tarjetas grandes con el icono encima */
.grande .tarjeta .ico { float: none; display: block; margin: 0 0 12px; font-size: 1.5em; }

/* Cuenta de la UAL */
.cuenta { font-weight: 900; color: var(--ual); font-size: 40px; line-height: 1.1; display: block; margin: 6px 0; }
.cuenta.larga { font-size: 32px; }

/* Tabla Android / iPhone */
table.donde { font-size: 25px; }
table.donde td:first-child { font-weight: 800; color: var(--ual-tinta); white-space: nowrap; }
.ruta { color: var(--ual); font-weight: 900; padding: 0 .15em; }
/* Esquema de la pantalla de Gemini */
.gemini { position: relative; background: #fff; border: 3px solid var(--ual-claro); border-radius: 26px; padding: 20px 24px; height: 340px; display: flex; flex-direction: column; box-shadow: 0 10px 28px rgba(35, 54, 70, .12); font-size: 26px; }
.g-barra { display: flex; align-items: center; gap: 14px; color: var(--ual-tinta); position: relative; font-size: 30px; }
.g-barra b { flex: 1; }
.g-foto { position: relative; width: 44px; height: 44px; border-radius: 50%; background: var(--ual); color: #fff; display: grid; place-items: center; font-weight: 800; font-size: 22px; }
.g-hola { flex: 1; display: grid; place-items: center; font-size: 30px; font-weight: 800; color: var(--ual); text-align: center; }
.g-caja { display: flex; align-items: center; gap: 16px; font-size: 27px; border: 2px solid var(--ual-claro); border-radius: 999px; padding: 10px 18px; color: var(--texto-suave); }
.g-caja > span, .g-caja i { position: relative; }
.g-caja i { margin-right: auto; font-style: normal; }
.g-num { position: absolute; top: -18px; right: -16px; width: 30px; height: 30px; border-radius: 50%; background: var(--sol); color: var(--ual-tinta); font: 900 18px/30px var(--fuente); text-align: center; }
.g-barra > .g-num { position: static; margin-right: -6px; }
.g-leyenda { font-size: 27px; }
.g-leyenda > li { margin: 0.35em 0; color: var(--texto); }
.g-leyenda > li::before { background: var(--sol); color: var(--ual-tinta); }
table.cuentas { font-size: 26px; }
table.cuentas th:not(:first-child) { width: 38%; }
table.cuentas td.si { color: var(--ual-oscuro); font-weight: 800; }
table.cuentas td.no { color: var(--alerta); font-weight: 900; }
</style>

<!-- _class: portada -->
<!-- _header: '' -->
<!-- _footer: '' -->
<!-- _paginate: false -->

Universidad de Mayores · Universidad de Almería

# Bienvenida

## Taller de Informática

---

<!-- header: 'Bienvenida' -->

<!-- _class: docente -->

Departamento de Informática · Universidad de Almería

# Juan José Moreno Riado

<div class="datos"><span>✉️ juanjomoreno@ual.es</span><span>🔬 Grupo Supercomputación-Algoritmos</span></div>

<p class="rotulo">Asignaturas que imparto</p>

<div class="asignaturas">
<div class="asignatura"><span class="ico">🖥️</span><b>Arquitectura de Computadores</b><small>Cómo funciona un ordenador por dentro</small></div>
<div class="asignatura redes"><span class="ico">🌐</span><b>Fundamentos de Redes</b><small>Cómo se comunican los ordenadores</small></div>
</div>

---

<!-- _class: portada -->
<!-- header: 'Nuestra guía: DigComp 3.0' -->
<!-- _header: '' -->
<!-- _footer: '' -->

Parte 1

# Nuestra guía: DigComp 3.0

## ¿Qué necesita saber hoy una persona para manejarse en el mundo digital?

---

# DigComp 3.0, el mapa europeo

> El **Marco Europeo de Competencia Digital** describe lo que una persona necesita *saber*, *saber hacer* y con qué *actitud* usar la tecnología en su vida diaria, en el trabajo y para participar en la sociedad.

<div class="rejilla-4 compacta">
<div class="tarjeta"><span class="ico">🇪🇺</span><b>Quién</b>La Comisión Europea</div>
<div class="tarjeta sol"><span class="ico">📅</span><b>Cuándo</b>2025, quinta edición. La primera es de 2013</div>
<div class="tarjeta tinta"><span class="ico">👵</span><b>Para quién</b>Para todas las edades</div>
<div class="tarjeta"><span class="ico">📱</span><b>Con qué</b>Con cualquier aparato y marca</div>
</div>

---

# Saber, saber hacer y actitud

Cada competencia junta tres cosas. Por ejemplo, ante un bulo:

<div class="rejilla-3 grande">
<div class="tarjeta"><span class="ico">🧠</span><b>Saber</b>Qué es un bulo y por qué corre tanto</div>
<div class="tarjeta sol"><span class="ico">🖐️</span><b>Saber hacer</b>Buscar la fuente original antes de reenviarlo</div>
<div class="tarjeta tinta"><span class="ico">💛</span><b>Actitud</b>Desconfiar con calma, sin miedo a la tecnología</div>
</div>

---

# ¿Por qué hace falta?

<div class="dos">
<div class="tarjeta"><span class="dato">56 %</span><p>de los adultos de la Unión Europea tenía en 2023 al menos competencias digitales <strong>básicas</strong></p></div>
<div class="tarjeta sol"><span class="dato">80 %</span><p>es el objetivo europeo para <strong>2030</strong>: que casi todo el mundo pueda manejarse en el mundo digital</p></div>
</div>

<div class="aviso">💡 El marco lo dice claro: la competencia digital se aprende <strong>a lo largo de toda la vida</strong>. Justo lo que hacemos aquí.</div>

---

# Cinco áreas

<div class="areas">
<div><span class="ico">🔎</span><i>ÁREA 1</i><b>Información</b>Buscar, saber si es fiable y guardarla</div>
<div><span class="ico">💬</span><i>ÁREA 2</i><b>Comunicación</b>Hablar, compartir y colaborar con respeto</div>
<div><span class="ico">🎨</span><i>ÁREA 3</i><b>Creación</b>Hacer textos, fotos y vídeos propios</div>
<div><span class="ico">🛡️</span><i>ÁREA 4</i><b>Seguridad y bienestar</b>Proteger aparatos, datos y salud</div>
<div><span class="ico">🔧</span><i>ÁREA 5</i><b>Resolver problemas</b>Arreglar, adaptar y seguir aprendiendo</div>
</div>

<div class="etiquetas"><span>5 áreas</span><span>21 competencias</span><span>4 niveles</span></div>

---

# Las 21 competencias, en sencillo (1 de 2)

<div class="rejilla-2 competencias">
<div class="tarjeta"><b>🔎 Área 1 · Información</b>
<ol>
<li data-n="1.1">Buscar en internet y afinar la búsqueda</li>
<li data-n="1.2">Saber si algo es fiable o es un bulo</li>
<li data-n="1.3">Guardar y ordenar archivos y contactos</li>
</ol>
</div>
<div class="tarjeta sol"><b>💬 Área 2 · Comunicación</b>
<ol>
<li data-n="2.1">Mensajes, llamadas y asistentes</li>
<li data-n="2.2">Compartir con cabeza</li>
<li data-n="2.3">Usar servicios públicos y conocer tus derechos</li>
<li data-n="2.4">Colaborar en grupo</li>
<li data-n="2.5">Convivir en la red con buenas formas</li>
<li data-n="2.6">Cuidar tu identidad y tu huella</li>
</ol>
</div>
</div>

---

# Las 21 competencias, en sencillo (2 de 2)

<div class="rejilla-3 competencias">
<div class="tarjeta tinta"><b>🎨 Área 3 · Creación</b>
<ol>
<li data-n="3.1">Crear textos, fotos y vídeos</li>
<li data-n="3.2">Retocar y combinar</li>
<li data-n="3.3">Respetar los derechos de autor</li>
<li data-n="3.4">Entender qué es un programa y la IA</li>
</ol>
</div>
<div class="tarjeta alerta"><b>🛡️ Área 4 · Seguridad</b>
<ol>
<li data-n="4.1">Proteger tus aparatos</li>
<li data-n="4.2">Proteger tus datos</li>
<li data-n="4.3">Cuidar tu bienestar</li>
<li data-n="4.4">Cuidar el medio ambiente</li>
</ol>
</div>
<div class="tarjeta"><b>🔧 Área 5 · Problemas</b>
<ol>
<li data-n="5.1">Resolver fallos técnicos</li>
<li data-n="5.2">Adaptar la tecnología a tus necesidades</li>
<li data-n="5.3">Usarla con creatividad</li>
<li data-n="5.4">Saber en qué mejorar y seguir aprendiendo</li>
</ol>
</div>
</div>

---

# Lo nuevo de esta edición

<div class="areas">
<div><span class="ico">🤖</span><b>Inteligencia artificial</b>Está dentro de las 21 competencias</div>
<div><span class="ico">🔐</span><b>Ciberseguridad</b>Protegernos de engaños y ataques</div>
<div><span class="ico">⚖️</span><b>Derechos digitales</b>Libertad para elegir y responsabilidad</div>
<div><span class="ico">🧘</span><b>Bienestar</b>Una relación sana con las pantallas</div>
<div><span class="ico">📰</span><b>Bulos</b>No dejarnos engañar por la desinformación</div>
</div>

<div class="aviso">💡 Las cinco prioridades tienen su sitio en nuestro taller.</div>

---

# La IA aparece en todo el marco

<div class="rejilla-3 compacta">
<div class="tarjeta"><b>1.1 · Buscar</b>No es lo mismo preguntar a un buscador que a una IA</div>
<div class="tarjeta sol"><b>1.2 · Evaluar</b>Cada vez cuesta más saber si un texto lo ha escrito una persona o una IA</div>
<div class="tarjeta tinta"><b>2.1 · Comunicarse</b>Un chatbot no es una persona, aunque lo parezca</div>
<div class="tarjeta"><b>3.1 · Crear</b>La IA genera, pero una persona tiene que revisarlo</div>
<div class="tarjeta sol"><b>3.3 · Derechos</b>Lo que está hecho con IA hay que decirlo</div>
<div class="tarjeta alerta"><b>4.3 · Bienestar</b>Los asistentes de IA tienen límites: no son un amigo ni un médico</div>
</div>

---

# Cuatro niveles

<div class="niveles">
<div><b>Básico</b>Tareas sencillas, con ayuda si hace falta</div>
<div class="meta"><b>Intermedio</b>Tareas concretas, por tu cuenta<br><small>⭐ Nuestra meta</small></div>
<div class="meta"><b>Avanzado</b>Tareas complejas, y ayudar a otros<br><small>⭐ Nuestra meta</small></div>
<div><b>Muy avanzado</b>Crear soluciones nuevas y liderar</div>
</div>

<p class="nota">Queremos que hagáis las cosas por vuestra cuenta y que podáis ayudar a vuestra familia y a vuestros amigos.</p>

---

# Una competencia, cuatro niveles

<p class="nota">4.2 · Proteger tus datos, ante un SMS falso del banco:</p>

<div class="niveles ejemplo">
<div><b>Básico</b>Con ayuda, me doy cuenta de que el SMS es falso</div>
<div class="meta"><b>Intermedio</b>Lo reconozco yo solo, no toco el enlace y bloqueo el número</div>
<div class="meta"><b>Avanzado</b>Ayudo a mi familia a reconocer estos engaños y a proteger sus cuentas</div>
<div><b>Muy avanzado</b>Organizo una charla en mi barrio para prevenir estafas</div>
</div>

---

<!-- _class: pasos -->

# Nos vamos a basar en DigComp 3.0

1. **Los temas del taller** cubren las cinco áreas
2. **El cuestionario de hoy** nos dice desde dónde partimos
3. **Cada sesión** trabaja competencias concretas
4. **El último día** veréis todo lo que habéis aprendido

---

<!-- _class: portada -->
<!-- header: 'Qué vamos a aprender' -->
<!-- _header: '' -->
<!-- _footer: '' -->

Parte 2

# ¿Qué vamos a aprender?

## Lo que usáis cada día, con calma y en vuestro propio móvil

---

# Nueve temas para el día a día

<div class="temas">
<div><span>🤖</span>Inteligencia artificial</div>
<div><span>📱</span>Manejo del móvil y el ordenador</div>
<div><span>🔎</span>Internet fiable y contrastar información</div>
<div><span>💬</span>WhatsApp y otras redes sociales</div>
<div class="alerta"><span>🛡️</span>Ciberseguridad</div>
<div><span>☁️</span>La nube y vuestros archivos</div>
<div><span>🪪</span>Certificados digitales</div>
<div><span>🏛️</span>Trámites con la administración</div>
<div><span>🏥</span>Salud</div>
</div>

<div class="aviso">🤖 Empezamos por la IA porque, según DigComp, forma parte de <strong>todas</strong> las competencias.</div>

---

# 🤖 Inteligencia artificial

<div class="dos tema">
<div class="chat">
<div class="burbuja yo"><small>Tú</small>Explícame con palabras sencillas esta carta del banco</div>
<div class="burbuja ia"><small>Asistente</small>Claro. Te avisan de que a partir de marzo cambia la comisión de tu cuenta…</div>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Pedirle que explique, redacte o traduzca</li>
<li>Preguntar bien: quién, qué, contexto y formato</li>
<li>Pillarla cuando se inventa las cosas</li>
<li>Sospechar de fotos, vídeos y voces falsas</li>
</ul>
</div>
</div>

---

# 📱 Manejo del móvil y el ordenador

<div class="dos tema">
<div class="escena">
<small>¿Te suena?</small>
<p>«No veo bien las letras del WhatsApp»</p>
<p>«Con el ratón no atino»</p>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Agrandar la letra y ajustar brillo y volumen</li>
<li>Escribir y dar órdenes con la voz</li>
<li>Manejar el ratón y el teclado del ordenador</li>
<li>Hacer capturas de pantalla y leer códigos QR</li>
</ul>
</div>
</div>

---

# 🔎 Internet fiable y contrastar información

<div class="dos tema">
<div class="escena">
<small>¿Te suena?</small>
<p>«Me han reenviado que el ajo en ayunas cura la tensión»</p>
<p>¿Verdad o bulo?</p>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Buscar bien, también con la voz o la cámara</li>
<li>Saber si una web es oficial y de fiar</li>
<li>Comprobar un bulo antes de reenviarlo</li>
<li>Usar Google Maps para llegar a cualquier sitio</li>
</ul>
</div>
</div>

---

# 💬 WhatsApp y otras redes sociales

<div class="dos tema">
<div class="chat">
<div class="burbuja ia"><small>Lucía (nieta)</small>¡Abuela, que no te veo! Pon la cámara 📷</div>
<div class="burbuja yo"><small>Tú</small>¿Y eso dónde se toca? 😅</div>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Notas de voz, fotos, documentos y ubicación</li>
<li>Videollamadas con toda la familia a la vez</li>
<li>Grupos: silenciarlos o salir de ellos</li>
<li>Facebook, Instagram y YouTube: qué compartir y con quién</li>
</ul>
</div>
</div>

---

<!-- _class: riesgo -->

# 🛡️ Ciberseguridad

<div class="dos tema">
<div class="chat">
<div class="burbuja ia mal"><small>Número desconocido</small>Hola mamá, se me ha roto el móvil y este es mi número nuevo. ¿Me haces un Bizum? Es urgente 🙏</div>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Ver las señales: prisa, un enlace o que te pidan claves</li>
<li>Proteger tus cuentas con buenas contraseñas</li>
<li>Pagar y comprar por internet sin sustos</li>
<li>Qué hacer si pierdes el móvil o ya has picado</li>
</ul>
</div>
</div>

---

# ☁️ La nube y vuestros archivos

<div class="dos tema">
<div class="escena">
<small>¿Te suena?</small>
<p>«Tengo miles de fotos y no encuentro la de la boda»</p>
<p>«Si pierdo el móvil, ¿pierdo las fotos?»</p>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Ordenar fotos y documentos en el PC y el móvil</li>
<li>Enviarlos por correo o por WhatsApp</li>
<li>Guardar copia de todo en la nube</li>
<li>Escanear papeles y rellenar un PDF</li>
<li>Cambiar de móvil sin perder nada</li>
</ul>
</div>
</div>

---

# 🪪 Certificados digitales

<div class="dos tema">
<div class="escena">
<small>¿Te suena?</small>
<p>«Para continuar, identifíquese con Cl@ve o certificado digital»</p>
<p>…y no sabes por dónde empezar</p>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Saber qué son Cl@ve y el certificado digital</li>
<li>Elegir el que más te conviene</li>
<li>Darte de alta, paso a paso</li>
<li>Usarlos con seguridad, nunca en un PC compartido</li>
</ul>
</div>
</div>

---

# 🏛️ Trámites con la administración

<div class="dos tema">
<div class="escena">
<small>¿Te suena?</small>
<p>«Para eso tiene que pedir cita previa por internet»</p>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Pedir cita: Seguridad Social, DGT, ayuntamiento…</li>
<li>Ver tus notificaciones en Mi Carpeta Ciudadana</li>
<li>Descargar justificantes y certificados</li>
<li>Evitar las webs falsas que cobran por trámites gratis</li>
</ul>
</div>
</div>

---

# 🏥 Salud

<div class="dos tema">
<div class="escena">
<small>¿Te suena?</small>
<p>«Llevo media hora llamando al centro de salud para pedir cita»</p>
</div>
<div>
<p class="rotulo">Aprenderás a</p>
<ul>
<li>Pedir y anular cita con Salud Andalucía</li>
<li>Consultar tu receta y tu medicación</li>
<li>Llevar la tarjeta sanitaria en el móvil</li>
<li>Poner recordatorios para no olvidar una pastilla</li>
</ul>
</div>
</div>

---

# Y en todas las clases…

<div class="rejilla-2">
<div class="tarjeta alerta"><span class="ico">🛡️</span><b>Píldora antiestafa</b>Diez minutos cada jueves con un caso real y reciente</div>
<div class="tarjeta"><span class="ico">📱</span><b>Android e iPhone</b>Fichas con los pasos de los dos cuando cambien</div>
<div class="tarjeta sol"><span class="ico">💡</span><b>Truco de la semana</b>Algo pequeño del móvil que te cambia el día a día</div>
<div class="tarjeta tinta"><span class="ico">🏠</span><b>Un reto para casa</b>Para practicar lo del día durante la semana</div>
</div>

---

# Cuatro ideas para todo el curso

<div class="rejilla-2">
<div class="tarjeta"><span class="ico">🔧</span><b>Aquí no se rompe nada</b>Casi todo se arregla con el botón de volver atrás</div>
<div class="tarjeta sol"><span class="ico">🙋</span><b>No hay preguntas tontas</b>Si tú tienes la duda, seguro que otros también</div>
<div class="tarjeta tinta"><span class="ico">🐢</span><b>Cada uno a su ritmo</b>Nadie se queda atrás</div>
<div class="tarjeta alerta"><span class="ico">🤝</span><b>Nos ayudamos entre todos</b>Si a ti ya te sale, echa una mano al de al lado: explicándolo, sin hacerlo por él</div>
</div>

---

<!-- _class: portada -->
<!-- header: 'Cuestionario inicial' -->
<!-- _header: '' -->
<!-- _footer: '' -->

Parte 3

# Cuestionario inicial

## Quiero conoceros para preparar el taller a vuestra medida

---

# Antes de empezar

<div class="rejilla-3 grande">
<div class="tarjeta"><span class="ico">📝</span><b>No es un examen</b>No hay respuestas buenas ni malas</div>
<div class="tarjeta sol"><span class="ico">✖️</span><b>Marca con una X</b>Una casilla, salvo si pone «varios»</div>
<div class="tarjeta tinta"><span class="ico">✋</span><b>¿Alguna duda?</b>Levanta la mano y la vemos juntos</div>
</div>

<div class="aviso">💡 Con vuestras respuestas sabré en qué ir más despacio y en qué podemos ir más rápido.</div>

---

<!-- _class: pasos -->

# Cuatro partes

1. **Tus aparatos y tus cuentas**<br>Qué móvil tienes, si tienes wifi, correo, Cl@ve…
2. **¿Qué sabes hacer?**<br>Una tabla con tareas del día a día
3. **Cómo te gusta aprender**<br>Los temas que más te interesan
4. **Cuéntanos**<br>Con tus palabras: qué usas, qué quieres aprender y qué te preocupa

---

<!-- _class: portada -->
<!-- header: 'Puesta a punto' -->
<!-- _header: '' -->
<!-- _footer: '' -->

Parte 4

# Puesta a punto

## Dejamos listos el ordenador del aula y vuestro móvil

---

# Dos aparatos, dos cuentas

<div class="rejilla-2">
<div class="tarjeta"><span class="ico">🖥️</span><b>El PC del aula</b>Con tu <strong>cuenta de la UAL</strong>: una cuenta nueva y vacía, para practicar sin miedo. También la pondremos en el móvil.</div>
<div class="tarjeta alerta"><span class="ico">📱</span><b>Tu móvil</b>Con tu <strong>cuenta personal</strong> de Google o Apple: para lo confidencial, como los trámites, la salud o el banco.</div>
</div>

<div class="aviso">🔐 <strong>La regla de oro:</strong> en el PC del aula, solo la cuenta de la UAL. Lo personal, siempre en tu móvil.</div>

---

# Tu cuenta de la UAL

Al matricularte en la Universidad de Mayores ya tienes una cuenta, aunque no la hayas usado nunca.

<div class="cadena">
<div class="tarjeta"><span class="ico">👤</span><b>Tu usuario</b><span class="cuenta">abc123</span>3 letras y 3 números</div>
<div class="flecha">→</div>
<div class="tarjeta sol"><span class="ico">✉️</span><b>Tu correo de la UAL</b><span class="cuenta larga">abc123@inlumine.ual.es</span>Una cuenta de Google</div>
</div>

<div class="aviso">🔑 Con ese usuario y su contraseña entras en el campus virtual, en Google y en Microsoft.</div>

---

# Ventajas de una cuenta educativa

<div class="rejilla-3 compacta">
<div class="tarjeta"><span class="ico">☁️</span><b>Más espacio</b>Drive y OneDrive con el espacio que da la UAL, aparte del de tu cuenta personal</div>
<div class="tarjeta sol"><span class="ico">🤖</span><b>Gemini y NotebookLM</b>La IA de Google para educación: tus conversaciones no se usan para entrenarla</div>
<div class="tarjeta tinta"><span class="ico">📝</span><b>Office</b>Word, Excel y PowerPoint con tu cuenta de Microsoft de la UAL</div>
<div class="tarjeta"><span class="ico">🚫</span><b>Sin anuncios</b>Gmail y Drive educativos no usan tus datos para publicidad</div>
<div class="tarjeta sol"><span class="ico">🎥</span><b>Videollamadas</b>Google Meet sin el límite de tiempo de las cuentas gratuitas</div>
<div class="tarjeta alerta"><span class="ico">🧪</span><b>Para practicar</b>Está vacía: aquí te puedes equivocar sin perder nada</div>
</div>

<p class="nota">Depende de lo que active la UAL. Y es tuya para siempre si te das de alta en Antiguos Alumnos de la UAL.</p>

---

<!-- _class: pasos -->

# Paso a paso (1 de 2): activar la cuenta

<style scoped>section.pasos ol > li { font-size: 0.84em; }</style>

1. **Entra en campus.ual.es**<br>Con tu usuario: 3 letras y 3 números
2. **¿No sabes la contraseña?**<br>«¿Olvidó su contraseña?»: llega un enlace al correo de tu matrícula
3. **Activa Google**<br>«Servicio UAL Cloud» <span class="ruta">›</span> alta en «Servicio Cloud Alumnos»
4. **Activa Microsoft**<br>«Servicios UAL-Microsoft» <span class="ruta">›</span> alta, para usar Office

---

<!-- _class: pasos -->

# Paso a paso (2 de 2): conectarla

<ol style="counter-reset: paso 4">
<li><strong>En el PC del aula</strong><br>Abre el navegador y entra en Google con tu correo de la UAL</li>
<li><strong>En un Android</strong><br>Ajustes <span class="ruta">›</span> Cuentas <span class="ruta">›</span> Añadir cuenta <span class="ruta">›</span> Google</li>
<li><strong>En un iPhone</strong><br>Instala Gmail y Google Drive, y entra con tu correo de la UAL</li>
<li><strong>Comprueba que funciona</strong><br>Abre Gmail: para cambiar de cuenta, toca tu foto arriba a la derecha</li>
</ol>

---

# Lo que vamos a dejar listo

<div class="rejilla-3 compacta">
<div class="tarjeta sol"><span class="ico">🎓</span><b>La cuenta de la UAL</b>En el PC del aula y en el móvil, con Google y con Microsoft</div>
<div class="tarjeta"><span class="ico">🔀</span><b>Dos cuentas, un móvil</b>Saber cambiar de una a otra en Gmail, Drive y Chrome</div>
<div class="tarjeta tinta"><span class="ico">🤖</span><b>Tu asistente de IA</b>Gemini con la cuenta de la UAL, para preguntarle lo que quieras</div>
<div class="tarjeta alerta"><span class="ico">🛡️</span><b>Tu cuenta, blindada</b>La revisión de seguridad y la verificación en dos pasos</div>
<div class="tarjeta"><span class="ico">🆘</span><b>Recuperación al día</b>Un teléfono y un correo para recuperar la contraseña si la olvidas</div>
<div class="tarjeta sol"><span class="ico">☁️</span><b>Copia de seguridad</b>Comprobar que tus fotos y contactos están a salvo en la nube</div>
</div>

<div class="aviso">💡 <strong>Atajo:</strong> si no encuentras una opción, pregúntale a la IA. Y comprueba que es verdad.</div>

---

# ¿Qué cuenta uso para cada cosa?

<table class="donde cuentas">
<tr><th></th><th>🎓 Cuenta de la UAL</th><th>🔑 Cuenta personal</th></tr>
<tr><td>Ejercicios del taller</td><td class="si">Sí, en el PC y en el móvil</td><td>No hace falta</td></tr>
<tr><td>Probar la IA</td><td class="si">Sí, con más protección</td><td>Con cuidado: nada personal</td></tr>
<tr><td>Fotos y contactos</td><td>No</td><td class="si">Sí, con copia en la nube</td></tr>
<tr><td>Papeles importantes</td><td>No</td><td class="si">Sí, en tu móvil</td></tr>
<tr><td>Trámites, salud y banco</td><td class="no">Nunca</td><td class="si">Sí, solo en tu móvil</td></tr>
</table>

<div class="aviso">🔀 Para cambiar de cuenta, toca tu foto arriba a la derecha. En el PC del aula, cierra sesión al terminar.</div>

---

# Revisión de seguridad de tu cuenta

<style scoped>.dos ol { font-size: 27px; margin: 0; } .dos ol > li { margin: 0.25em 0; }</style>

<div class="dos">
<div>
<p class="rotulo">Cuatro preguntas</p>
<ol>
<li>¿Reconoces todos los aparatos conectados a tu cuenta?</li>
<li>¿Están al día tu teléfono y tu correo de recuperación?</li>
<li>¿Tienes activada la verificación en dos pasos?</li>
<li>¿Qué aplicaciones pueden entrar en tu cuenta?</li>
</ol>
</div>
<div class="rejilla-2 compacta">
<div class="tarjeta"><b>Google</b>Ajustes <span class="ruta">›</span> Google <span class="ruta">›</span> Gestionar tu cuenta <span class="ruta">›</span> Seguridad</div>
<div class="tarjeta tinta"><b>iPhone</b>Ajustes <span class="ruta">›</span> tu nombre <span class="ruta">›</span> Inicio de sesión y seguridad</div>
</div>
</div>

<div class="aviso">🆘 Hoy lo habéis visto: sin correo de recuperación, no se recupera una contraseña.</div>

---

# Os presento a Gemini

La inteligencia artificial de Google, con vuestra cuenta de la UAL.

<div class="rejilla-3">
<div class="tarjeta"><span class="ico">🖥️</span><b>En el PC</b>Abre el navegador y entra en <strong>gemini.google.com</strong></div>
<div class="tarjeta sol"><span class="ico">🤖</span><b>En Android</b>La app <strong>Gemini</strong>. Si no la tienes, en Play Store</div>
<div class="tarjeta tinta"><span class="ico">🍎</span><b>En iPhone</b>La app <strong>Google Gemini</strong>, en la App Store</div>
</div>

<div class="aviso">🎓 Entra siempre con tu <strong>cuenta de la UAL</strong>. Para comprobarlo, mira la foto de arriba a la derecha.</div>

---

# Así es por dentro

<div class="dos">
<div class="gemini">
<div class="g-barra"><span class="g-num">1</span>☰ <b>Gemini</b><span class="g-foto">A<span class="g-num">2</span></span></div>
<div class="g-hola">Hola, ¿en qué puedo ayudarte?</div>
<div class="g-caja"><span>＋<span class="g-num">4</span></span><i>Pregunta a Gemini<span class="g-num">3</span></i><span>🎙️<span class="g-num">5</span></span></div>
</div>
<div>
<ol class="g-leyenda">
<li><strong>El menú:</strong> tus conversaciones y «Nueva conversación»</li>
<li><strong>Tu foto:</strong> con qué cuenta has entrado</li>
<li><strong>La caja:</strong> escribe lo que quieras</li>
<li><strong>El «+»:</strong> añade una foto o un documento</li>
<li><strong>El micrófono:</strong> díselo hablando</li>
</ol>
</div>
</div>

<p class="nota">La pantalla cambia a menudo. Lo importante es reconocer estas cinco piezas.</p>

---

# Encargo 1 · Una excursión de un día

<div class="dos tema">
<div class="chat">
<div class="burbuja yo"><small>Tú</small>Quiero pasar un día en el Cabo de Gata con mi pareja, sin caminatas largas. ¿Qué me recomiendas?</div>
<div class="burbuja yo"><small>Tú, después</small>¿Y dónde podemos comer pescado?</div>
<div class="burbuja yo"><small>Y al final</small>Hazme el plan en una lista corta, con horarios</div>
</div>
<div>
<p class="rotulo">Fíjate</p>
<ul>
<li>No hace falta acertar a la primera: <strong>se conversa</strong></li>
<li>Cada mensaje afina el anterior</li>
<li>Comprueba los sitios en Google Maps: ¿existen? ¿están abiertos?</li>
</ul>
</div>
</div>

---

# Encargo 2 · ¿Qué cocino hoy?

<div class="dos tema">
<div class="chat">
<div class="burbuja yo"><small>Tú, con una foto de tu nevera</small>¿Qué puedo cocinar para dos con esto?</div>
<div class="burbuja yo"><small>Tú, después</small>Que sea sin horno y en media hora</div>
<div class="burbuja yo"><small>Y al final</small>Hazme la lista de lo que me falta para comprar</div>
</div>
<div>
<p class="rotulo">Fíjate</p>
<ul>
<li>La IA también <strong>ve fotos</strong>: usa el «+»</li>
<li>Pídele cambios hasta que te guste</li>
<li>La lista se puede copiar y mandar por WhatsApp</li>
</ul>
</div>
</div>

---

# Encargo 3 · Aprende y ponte a prueba

<div class="dos tema">
<div class="chat">
<div class="burbuja yo"><small>Tú</small>Cuéntame la historia de la Alcazaba de Almería en cinco frases, como si fuera un cuento</div>
<div class="burbuja yo"><small>Tú, después</small>¿Quién mandó construirla?</div>
<div class="burbuja yo"><small>Y al final</small>Hazme tres preguntas tipo test para ver si me he enterado</div>
</div>
<div>
<p class="rotulo">Fíjate</p>
<ul>
<li>Pídele que se ponga <strong>a tu nivel</strong></li>
<li>Que te examine: así se aprende mejor</li>
<li>Comprueba un dato en una web oficial: a veces se inventa cosas</li>
</ul>
</div>
</div>

---

<!-- _class: resumen -->

# Reto para casa

- 🛡️ Haz con calma la revisión de seguridad de tu cuenta personal
- 🆘 Comprueba que tu teléfono y tu correo de recuperación están al día
- 🤖 Haz a Gemini un encargo sobre algo que te guste, y cuéntanos el jueves qué tal
- 🪪 Busca en la web oficial cómo darte de alta en Cl@ve, si aún no la tienes

<p class="nota">Y cada jueves: el móvil cargado, el cargador, las gafas de cerca y una libreta.</p>

---

<!-- _class: cierre -->
<!-- _header: '' -->
<!-- _footer: '' -->
<!-- _paginate: false -->

Taller de Informática

# ¡Manos a la obra!
