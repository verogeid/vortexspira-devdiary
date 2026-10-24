# 👤 El Arquitecto, Visión y Modelo de Negocio

***

<a id="indice"></a>
<div align="center">

[Arquitecto](#arquitecto) • [Escultor](#escultor) • [Seguridad](#seguridad) • [Educadores](#educadores) • [Freemium y Accesibilidad Económica](#freemium) • [Filosofía Social](#filosofia-social)

</div>

***

[**⬅️ Volver al Resumen Principal**](./README.md)

---

<a id="arquitecto"></a>
## 1. 👤 Del Arquitecto: Una Plataforma Nacida de la Experiencia

<img src="./images/Diego.jpeg" alt="Diego González Fernández" width="150" align="right" style="border-radius: 10px;"/>

VortexSpira® es una plataforma creada y diseñada por **Diego González Fernández, Ingeniero de Calidad Integral**. Nació de una necesidad personal: buscaba crear un **audiolibro multilenguaje** para aprender idiomas de forma inmersiva, pero también una herramienta que se adaptara a mi "hardware" mental (pensamiento no lineal y memoria asociativa) y a mi "software" (pensamiento lateral).

Esta arquitectura personal es la que condiciona mi forma de explicar y enseñar, buscando siempre el "porqué" y el "sistema" debajo de la "palabrería".

Mi filosofía de 'QA Holístico' se aplica a cada detalle, desde la arquitectura 'inexpugnable' de la plataforma hasta el contenido que enseña el 'porqué' antes que el 'cómo'. Mi objetivo no es enseñarte a escribir código, es enseñarte a pensar como un arquitecto.

> *Me suele comentar un amigo y colaborador que descanse de vez en cuando. Esto tiene un inconveniente: equivale a retirar las manos del manillar que gobierna mi pensamiento lateral. Puedo estar haciendo cualquier otra cosa y tener una epifanía.*

> *En pocos días he solicitado una auditoría radiométrica y colorimétrica de los materiales expuestos en las PDI para el Departamento de Educación del gobierno local (ya admitida a trámite como plausible); seguido una solicitud formal de estudio de colorimetría como estresor parásito que pudiera estar consumiendo ATP en patologías como la Esclerosis Múltiple (EM) para el Departamento de Salud; y nuevamente, una ampliación sobrevenida para el primero relacionando la auditoría propuesta con el estudio solicitado, como causa principal de la caída de la comprensión lectora en los informes PISA.*

> *Ahora entenderéis por qué mis cursos se salen de la norma. Todo es **neurociencia, neuroergonomía y psicología atencional**; ergo, todo es **accesibilidad, rendimiento y ciberseguridad** en el plano digital.*

> *Un agradecimiento especial a **Josu** por hacerme descansar, y tener estás epifanías involuntarias, y a mí hermano **Gorka** por hacerme mirar la pantalla desde otra perspectiva.*

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="escultor"></a>
## 2. 🏗️ Arquitecto y Escultor: Un Proceso de Refinamiento Holístico

Mi rol en la creación de **VortexSpira®** es el de un **arquitecto y escultor de software**. Defino la visión y la arquitectura, y luego me apalanco en la IA como un asistente de ejecución de alta velocidad que me entrega la "materia prima" funcional. 

Pero la verdadera ingeniería empieza ahí. **El trabajo no es pedir, es refinar.**

### 🗿 Quitar el "mármol sobrante"
Un ejemplo perfecto es la implementación del *dark mode*. La IA generó un primer borrador funcional, pero con una deuda técnica masiva: duplicaba todas las variables y reglas CSS para ambos modos, creando una redundancia insostenible. Mi trabajo como escultor fue aplicar la **calidad holística**:

1. **Refactorización total:** Centralicé las reglas para que existieran una sola vez.
2. **Variables Dinámicas:** Definí colores base para *light mode* y usé un único bloque `@media` para sobrescribir exclusivamente las variables necesarias.
3. **Mantenibilidad:** Renombré elementos del DOM para mejorar la legibilidad y facilitar escalabilidad futura.

### 🔍 Depuración Senior y "Deep QA"
Donde la IA suele fallar es en el diagnóstico de problemas complejos de estado o eventos. Para evitar que la herramienta entre en un bucle infinito de "parches sobre parches", intervengo con una **metodología de depuración de bajo nivel**:

* **Hacks de QA:** Implemento rastreadores para identificar qué *listener* específico está recibiendo el foco o en qué fase exacta (captura o burbujeo) se está perdiendo un evento.
* **Diagnóstico de Causa Raíz:** No permito que la IA intente "arreglar" un fallo sin antes averiguar qué está pasando realmente en el ciclo de vida del DOM.
* **Intervención Manual:** Esta supervisión evita la acumulación de lógica redundante y garantiza que la solución sea técnica, no solo visual.

### 🚀 Visión a Largo Plazo
Desarrollo la plataforma **por capas**, siguiendo una hoja de ruta arquitectónica que la IA no puede prever. Mi labor es preparar el código desde el "minuto cero" para la escalabilidad, dejando instalados los "conductos en la pared" para funcionalidades futuras ya contempladas en el mapa estratégico.

> Este ciclo de **visión estratégica, ejecución asistida y refactorización senior** es la única forma de garantizar que la plataforma no solo funcione, sino que posea una arquitectura inexpugnable y preparada para el futuro.

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="seguridad"></a>
## 3. 🛡️ Arquitectura de Seguridad (Detalles)

* **Seguridad Criptográfica:** Las licencias de usuario se emiten como **JWS Asimétricos** (firmados digitalmente) por un servicio **serverless** dedicado. Este, a su vez, se comunica con la aplicación principal usando un **JWE Rotativo con IV**, garantizando que la información del usuario no solo viaja firmada, sino también cifrada y con claves que cambian constantemente.
* **Protección de Contenido:** El usuario debe estar online para iniciar sesión o cambiar de módulo porque **cada módulo del curso está cifrado de manera independiente**.
* **Defensa Proactiva:** Basamos nuestra robustez en una **sanitización agresiva por lista blanca** y una política estricta de **minimización de datos**. Solo almacenamos la información mínima indispensable, eliminando cualquier riesgo asociado al manejo de datos sensibles innecesarios.

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="educadores"></a>
## 4. 🚀 Más Allá de los Cursos: Una Herramienta para Creadores Educativos

VortexSpira® no es solo una plataforma para consumir cursos; es también una **herramienta de autor** diseñada para empoderar a los educadores y eliminar la barrera tecnológica.

Bajo una licencia institucional especial (gratuita para administraciones públicas y asociaciones), los profesores de educación especial reciben un manual mínimo. Con él, pueden usar un simple **editor de textos en su propio móvil** para crear lecciones didácticas totalmente compatibles con nuestra plataforma.

El proceso es de una simplicidad radical:
1.  El profesor **crea** el contenido en un archivo de texto.
2.  Lo **comparte** directamente con el alumno (por email, WhatsApp, etc.).
3.  El alumno **importa** ese archivo en su PWA de VortexSpira®.

El resultado es un material de estudio personalizado y altamente accesible que el alumno puede **consumir de forma inmediata**, con todas las ventajas de control, personalización y "Ansiedad Cero" de la plataforma.

Es nuestra filosofía aplicada a la creación: damos a los expertos en pedagogía el poder de "ingeniar" su propio contenido, sin fricción.

> *Especial agradecimiento a **Naiara** y a **Allen** por hacerme sensible a tantos neurodivergentes olvidados por las editoriales. Ver de cerca vuestra lucha frente a las barreras del sistema educativo fue la chispa que me inspiró a enfocar el desarrollo de esta herramienta hacia quienes más lo necesitan. Sin vosotros, esta aplicación nunca hubiera sido lo que es.*

<div align="center">
  <img src="./images/import-modal-desktop.png" alt="Importación de contenidos externos" width="550" target="_top" style="border-radius: 10px;"/>
</div>

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="freemium"></a>
## 5. 🎁 Freemium y Accesibilidad Económica

VortexSpira® no es un producto que compras a ciegas. Cuando esté disponible, la plataforma se instalará como una PWA (Aplicación Web Progresiva) en tu sistema. Por defecto, tendrás acceso **gratuito y permanente** a los **dos primeros capítulos de cada módulo, de cada curso.**

Podrás explorar la interfaz, probar la metodología y aprender los fundamentos sin coste alguno. Cuando estés listo para convertirte en un Arquitecto, podrás adquirir la licencia para desbloquear todo el contenido (marcado con 🔒) directamente desde la plataforma.

Además, aplicamos principios de **Equidad Económica Global**. Creemos que el talento está distribuido uniformemente, pero las oportunidades no. Por eso, nuestros precios se ajustan dinámicamente según la **Paridad de Poder Adquisitivo (PPP)** de cada región, asegurando que el esfuerzo para acceder al conocimiento de élite sea equivalente, vivas donde vivas.

<div align="right">

[Volver al índice ▲](#indice)

</div>

---

<a id="filosofia-social"></a>
## 6. ⚖️ Filosofía Social: Techo Salarial, Sin Dividendos y Alquiler Social

VortexSpira® nace como un proyecto de profundo impacto social, y su modelo económico está blindado desde la raíz para garantizar que el conocimiento y los recursos no se conviertan en herramientas de especulación.

* **Sin ánimo de lucro y sin dividendos:** La plataforma no contempla el reparto de dividendos entre socios ni inversores. Todo el excedente económico tiene un destino predeterminado por diseño arquitectónico y estatutario.
* **Techo salarial estricto:** La retribución máxima para cualquier puesto equivalente dentro de la estructura estará rigurosamente **techada al 150% del salario del sector** tecnológico para su categoría. Nadie hará fortuna a costa de la educación o la neurodivergencia.
* **El capital humano es el recurso más importante:** Cualquier persona contratada por VortexSpira®, o por sus entidades derivadas, contará exactamente con los mismos beneficios y condiciones de bienestar. No solo debemos estar orgullosos de nuestro trabajo, sino también debidamente remunerados.
* **Destino de los excedentes:** Los beneficios generados más allá del mantenimiento operativo se canalizarán en un orden de prioridades muy claro:
  1. **Asociaciones:** Financiación y dotación de herramientas gratuitas para colectivos neurodivergentes y neurodegenerativas.
  2. **Educación y Sanidad:** Apoyo directo a iniciativas públicas y comunitarias.
  3. **Ladrillo Social:** El remanente disponible se destinará a la adquisición de locales y viviendas para destinarlas a **alquiler social**, con una condición innegociable: las rentas estarán **atadas al Salario Mínimo Interprofesional (SMI) y nunca al IPC**, protegiendo a los inquilinos de la especulación inmobiliaria.

> *No queremos levantar muros por diferencias económicas. El excedente vuelve a la sociedad que lo hace posible.*

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
