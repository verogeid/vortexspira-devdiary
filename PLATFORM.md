# ⚙️ Ingeniería de la Experiencia y Arquitectura Detallada

***

<a id="indice"></a>
<div align="center">

[Zero Fricción](#friccion) • [TTS Local](#tts) • [Portabilidad](#portabilidad) • [Diseño](#diseno) • [Ecosistema UX](#ecosistema) • [Certificación](#certificacion)

</div>

***

[**⬅️ Volver al Resumen Principal**](./README.md)

---

<a id="friccion"></a>
## 1. 🧠 Zero Fricción y Guía Contextual (Detalles)

* **Sincronización Total (Highlight & Voz):** La plataforma ofrece una sincronización perfecta entre el resaltado visual de la frase y la voz del mentor.
* **Selección de Voces por Rol:** Configura y personaliza la voz y el **tono** para cada rol (Narrador, Lector de Código, Consejos), mejorando la diferenciación auditiva.
* **Dictado Amigable (Visual vs. Audio):** El núcleo del formato `.vsl` es la capacidad de **desacoplar el texto que se muestra del texto que se lee**. Esto permite que el "Lector de Código" narre el código de forma natural (ej: "creamos la constante equis") mientras el usuario ve el código literal (ej: `const x = 1;`), eliminando la principal fuente de fricción del audio-aprendizaje técnico.
* **Navegación *Hands-Free*:** Controla la reproducción (Reproducir/Parar, Siguiente/Anterior Frase, Reiniciar capítulo) desde el **teclado multimedia** con la **ventana minimizada**.
* **Guía Visual Contextual (Modo Desktop - En Desarrollo):** Un modal de visualizaciones mostrará una **captura de pantalla sincronizada** con el *highlight* para guiar al alumno en las implicaciones del código en el navegador o en la localización de menús de herramientas.
* **Parseo Dinámico Condicional (Single Source of Truth):** VortexSpira® no duplica el contenido para distintos niveles. Nuestro motor lee un único archivo fuente (markdown enriquecido) y construye el DOM en tiempo real dependiendo del modo de reproducción seleccionado por el usuario:
    * Al ejecutar el **Modo Mentor**, el parser compila únicamente los nodos de conocimiento avanzado, ignorando a los personajes secundarios.
    * Al ejecutar el **Modo Teatralización**, el motor inyecta en el DOM los nodos correspondientes a los `storyChar` (personajes de apoyo) y transmuta las líneas del mentor para interactuar con ellos. Todo el proceso es transparente y garantiza que **un usuario sordociego reciba exactamente la misma riqueza semántica, contexto y carga de información** que un usuario vidente, manteniendo la integridad del árbol de accesibilidad (A11Y).

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="tts"></a>
## 2. 🗣️ Voces Inteligentes y Adaptables (Arquitectura de Cero Lag)

VortexSpira® utiliza las voces Text-to-Speech (TTS) **disponibles en tu navegador y sistema operativo**. Prioriza las de mayor calidad (online como Google) y conmuta a las locales (offline) si pierdes la conexión, garantizando un aprendizaje ininterrumpido.

La variedad y calidad dependen de tu navegador (Chrome/Edge son los mejores) y de los **paquetes de idioma instalados en tu sistema operativo**. Para más opciones, simplemente instala los paquetes de voz completos desde la configuración de idioma de tu Windows, macOS o Linux.
<sub><em>Nota: La API de Edge tiene un bug conocido que hace que no respete el tono configurado para las voces.</em></sub>

Esta arquitectura local se ha elegido deliberadamente sobre el uso de voces "online premium" por razones de coste, rendimiento y arquitectura:
1.  **Coste:** Las voces premium por API elevan los costes de licencia, lo que afectaría al precio y duración de la licencia del usuario final.
2.  **Rendimiento:** Introducen un "lag" (latencia) inaceptable al generar el audio, rompiendo la fluidez y el *highlight* instantáneo.
3.  **Fragmentación:** El modelo de VortexSpira se basa en la generación de audio *en tiempo real*. Un modelo de "cache" (generar y descargar cientos de archivos de audio fragmentados por cada módulo) no es escalable y haría imposible el cambio de voz o de módulo de forma instantánea.

**Evolución Futura (El Motor TTS Local):**
Para ampliar el número de voces no robóticas del **navegador**, sin caer en los problemas de coste y latencia, se está estudiando la incorporación de un **motor TTS neuronal que se ejecute 100% offline dentro de la PWA (vía WebAssembly)**. Esta arquitectura permitirá incluir voces "VS" premium por defecto en el freemium sin lag.

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="portabilidad"></a>
## 3. 🔗 Continuidad y Portabilidad (Multidispositivo)

* **Diseño 100% Responsive:** La interfaz está diseñada para adaptarse perfectamente a cualquier tamaño de pantalla, desde móviles y tabletas hasta ordenadores de escritorio.
* **Aprendizaje Offline Híbrido:** Inicia sesión y carga tu módulo una vez, y luego consume **todo el contenido del módulo sin conexión** a internet. Perfecto para viajar o zonas de baja cobertura. La conexión solo es necesaria para validar tu licencia, cambiar de módulo o sincronizar tu progreso.
* **Sincronización Automática (En Desarrollo):** Podrás pausar una lección en un dispositivo y continuar **exactamente en la misma frase** en otro, garantizando la continuidad de la sesión.
* **Compatibilidad Total:** La interfaz es completamente accesible y navegable con el **teclado** y compatible con **lectores de pantallas** (ARIA).
* **Control de Playback:** Haz clic en **cualquier frase de la pantalla** para saltar instantáneamente a ese punto y reanudar la narración.

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="diseno"></a>
### 🎨 **Diseño Coherente y Control de la Interfaz (UI)**

* **Temas Inteligentes:** Soporte completo para el **Modo Oscuro** en todos los elementos (contenido y *modales*).
* **Personalización:** Ajusta y guarda la **familia** y el **tamaño de la fuente** a tu gusto.
* **Modales Estables:** Los menús de configuración y activación tienen un **tamaño máximo fijo** que previene "saltos" en el diseño (`CLS`).
* **Botones Visibles y Profesionales:** Controles clave como Guardar (💾) y Activar (🔓) utilizan un diseño minimalista ("Ghost Button") que se **ilumina en el borde** al interactuar.
  
<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="ecosistema"></a>
## 4. 🌌 El Ecosistema: Diseño Anti-Fatiga del Universo VortexSpira

Mi transición a Ingeniero de Calidad Integral ha definido la arquitectura de la plataforma.

<div align="center">
  <img src="./images/vortexspira-universe-demo.gif" alt="Demostración de la navegación del Universo VortexSpira con foco guiado y efecto blur" width="700" target="_top" style="border-radius: 10px;"/>
</div>

### 👁️ Foco Guiado y Reducción de Carga Cognitiva (Detalles)

El diseño simula una **habitación cilíndrica tridimensional** donde las secciones y cursos se encuentran en las "paredes". Esto permite una navegación intuitiva que, de nuevo, minimiza la fricción mental.

El núcleo de la reducción de la fatiga se centra en el **Foco Guiado** mediante una técnica innovadora:

* **Aplicación del *Bug de las Cataratas***: He implementado una solución inspirada en la forma en que el cerebro procesa la información periférica con ciertos problemas visuales. Se aplica una **máscara *blur* degradada** a las columnas o secciones en las que no está el foco.
* **Resultado:** Esto reduce drásticamente la cantidad de información que el cerebro tiene que procesar en la visión periférica, permitiendo que **toda la atención se centre en el elemento activo**.

### 🖱️ Controles de Interacción (A11Y Avanzados)

La interfaz se construyó con la accesibilidad como requisito no funcional primario, garantizando que el diseño sea utilizable para **todos** los perfiles de usuario.

#### **Interacción con Ratón (Inmersión 3D):**

* **Rotación por Drag and Drop:** El usuario puede **clicar y arrastrar** el ratón sobre el lienzo para girar la habitación cilíndrica y explorar las diferentes secciones de cursos, ofreciendo una experiencia inmersiva e intuitiva.
* **Rotación por Rueda del Ratón (`Mouse Wheel`):** Al usar la **rueda de *scroll***, el usuario también puede girar la habitación de forma incremental, facilitando la navegación precisa sin necesidad de *drag*.
* **Selección:** Clicar en cualquier botón lo selecciona directamente.

#### **Interacción con Teclado (Manos Libres):**

* **Navegación Total sin Ratón:** La navegación es completamente funcional y eficiente usando únicamente el teclado.
* **Controles de Navegación Jerárquica:**
    * La tecla **`Tab`** permite **cambiar entre las secciones** principales de la página (e.g., de la matriz de cursos a la ayuda rápida).
    * Los **`Cursores`** (`↑`, `↓`, `←`, `→`) permiten **navegar entre las opciones** o cursos dentro de la sección que tiene el foco.
* **Controles de Acción:**
    * La **Barra Espaciadora** (`Space`) y la tecla **`Enter`** (Intro) se usan para **seleccionar** la opción o curso que tiene el foco.
    * La tecla **`Esc`** (Escape) se usa para la acción de **"Volver"** o para cerrar el modal actual.
* **Guía Visual:** El **efecto *ghost* en el botón** con foco proporciona un *highlight* de alta visibilidad.
* **Compatibilidad con Lectores de Pantalla:** Toda la estructura de navegación está debidamente etiquetada con atributos ARIA.

### 📱 Diseño *Responsive* (Adaptación)

La experiencia de navegación es coherente y **sin fisuras** en cualquier factor de forma, manteniendo el mismo enfoque de reducción de carga cognitiva:

* **Vista Desktop (Foco en Columnas):** Mantiene la simulación 3D y aplica el *blur* a las columnas periféricas.
* **Vista Tablet (Foco en Fila Central):** Adapta la disposición, pero mantiene el *highlight* en el elemento central.
* **Vista Móvil (Foco en Botón):** Se transforma en una lista vertical, donde el *blur* se sustituye por una jerarquía de enfoque clara en el botón activo.

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="certificacion"></a>
## 5. 🛠️ Flujo de Licencias, Certificación y Catálogo (Detalles)

* **Gestión Centralizada:** El modal de activación te permite **actualizar tu clave global** en cualquier momento.
* **🛒 Catálogo Inteligente:** Muestra un **catálogo de productos adquiridos** y **módulos disponibles para la compra**, con altura limitada y scroll.
* **🎓 Exámenes de Nivel Profesional:** Los exámenes son tipo test (formato ISTQB), donde cada pregunta puede tener múltiples respuestas correctas y debes marcarlas todas para acertar.
  - 50 preguntas si es un curso completo, 30 si es un módulo.
  - 70% acertado para superar el examen.
  - Intentos limitados. Se podrá adquirir una ampliación de intentos, a un precio reducido, para la misma certificación, pero el examen será otro.
  - QR de verificación impreso en la certificación. 
* **🔒 Acceso Visual:** Los capítulos se desbloquean en tiempo real en el selector, reemplazando el candado (visible si no se ha adquirido el módulo).

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="licencia"></a>
## Licencia y Derechos de Uso

La plataforma **VortexSpira®** es un software comercial propietario.

* **Copyright © 2025 Diego González Fernández.** Todos los derechos reservados.
* El uso de la plataforma VortexSpira® requiere la adquisición de una **licencia válida** a través de los canales de venta autorizados (Hotmart).
* La distribución, modificación o ingeniería inversa del software están estrictamente prohibidas sin acuerdo previo por escrito con el autor.
* La marca VortexSpira® está registrada o en proceso de registro.
* La creación intelectual de la plataforma está registrada en **Safe Creative** ([**🛡️ Registro de Derechos**](https://www.safecreative.org)).

El **contenido de los cursos** que se ejecutan en esta plataforma se licencia por separado bajo sus propios términos al adquirir cada producto.

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

© 2025 Diego González Fernández
[LinkedIn](https://www.linkedin.com/in/diego-gonzalez-fernandez)
