# Fosa de Atacama · 8.000 metros bajo el Pacífico

**Proyecto Final Unidad 3 — Taller de Diseño de Interfaces**
Postulación al concurso **Chile Re-Descubre** (Congreso Futuro · ACHIPEC · CRTIC)

- 🔗 **Experiencia en línea:** https://portafolio.insta3d.cl/fosa-atacama/
- 🎬 **Cápsula audiovisual (1 min):** `<enlace al video>`

---

## Tema elegido

**Descubrimiento de la Fosa de Atacama** (caso del libro *Hecho en Chile. 50 ideas, descubrimientos e innovaciones*, de Macarena Rojas Ábalos y Natalia Salazar Muñoz).

Frente a las costas de Chile se extiende uno de los ambientes más extremos y desconocidos del planeta: la Fosa de Atacama, con profundidades cercanas a los 8.000 metros. Expediciones científicas chilenas han explorado su biodiversidad para entender cómo puede existir vida bajo una presión enorme, en oscuridad permanente y con escasez de alimento.

## Descripción conceptual

> **Un lugar al que ningún ser humano puede ir, vivido en primera persona.**

La realidad virtual es la única forma de "estar" a 8.000 metros de profundidad. La persona viaja dentro de un **lander**, el vehículo sin tripulación que usan los científicos para llegar al fondo de la fosa, y **lo opera con sus propias manos**, como los investigadores que lo controlan desde el barco.

Las tres condiciones extremas que nombra el caso se traducen en sensaciones:

| Condición | Cómo se vive en la experiencia |
|---|---|
| **Oscuridad permanente** | La luz del sol desaparece a los 200 m. Desde ahí, solo se ve lo que ilumina la linterna en la mano y, en el fondo, los focos del lander |
| **Presión enorme** | El medidor sube hasta unas 800 atmósferas, la estructura del lander cruje y los controles vibran cada vez más fuerte |
| **Escasez de alimento** | La nieve marina cae lentamente, y basta soltar un poco de carnada para que la vida aparezca desde la oscuridad |

**Recorrido (unos 3 minutos):**
1. **Superficie.** Al amanecer, en la cubierta de un barco de investigación frente a Antofagasta. La persona **baja la palanca** para soltar el lander al mar.
2. **Descenso (unos 100 segundos), narrado hito por hito:**
   - **0 m:** la superficie se ve desde abajo y se aleja; burbujas y un cardumen.
   - **200 m:** se acaba la luz del sol.
   - **1.000 m:** zona de medianoche, con medusas y destellos de bioluminiscencia.
   - **4.000 m:** zona abisal, a unos 2 °C y más de 400 atmósferas.
   - **5.400 m:** aparece el sumergible **Limiting Factor**, en el que Osvaldo Ulloa y Victor Vescovo bajaron a 8.069 m el 21 de enero de 2022. Se muestra una ficha con una fotografía real del sumergible.
   - **6.000 m:** zona hadal; las paredes de la fosa se cierran alrededor.
   - **7.000 m:** una línea de sensores como las del observatorio **IDOOS**, instalado por Chile desde 2023.
   - **7.700 m:** llegando al fondo.
3. **El fondo.** Golpe al tocar fondo y oscuridad total. La persona **baja la palanca** para encender los focos y aparece el lecho de la fosa.
4. **La carnada.** La persona **baja el brazo con la carnada** frente a la cámara. Llega un enjambre de anfípodos y, desde la oscuridad, tres peces caracol.
5. **Especies nuevas.** *Paraliparis selti* («selti» significa azul en kunza) y *Dulcibella camanchaca*, un crustáceo cazador hallado a 7.902 m y nombrado como la niebla del desierto.
6. **Expediciones chilenas desde 2018.** El cierre: en 2018, la expedición Atacamex llevó el lander Audacia a 8.081 m, la primera vez que la ciencia chilena tocó el punto más profundo de la fosa.

## Cómo usarla

### En Meta Quest (experiencia principal)
1. Abre la URL en el **navegador del Meta Quest**.
2. Presiona **Entrar en realidad virtual**.
3. Frente a ti hay una consola con una **palanca**. Se puede accionar de cuatro maneras:
   - **Empujarla con la mano hacia ti**, sin apretar ningún botón.
   - **Agarrarla** con el gatillo o el botón lateral del control y tirar. El control vibra.
   - **Apuntarle** con el control y apretar el gatillo.
   - Apretar **A** o **X**, o **juntar el índice y el pulgar** si usas las manos sin controles.
4. **Linterna:** va en la mano izquierda si usas controles; si usas solo las manos, va en la cabeza.
5. **Continuar:** aprieta el gatillo o junta los dedos.

Se recomienda jugarla **de pie** y despejar un círculo de un metro a tu alrededor. La persona nunca se desplaza: el lander es un marco fijo, lo que evita el mareo durante el descenso.

### En pantalla (computador o celular)
Presiona **Ver en pantalla**, arrastra para mirar y usa el botón de acción o **Enter** para operar el lander.

| Tecla | Acción |
|---|---|
| `Enter` / `Espacio` | Bajar la palanca o continuar |
| `H` | Ocultar los controles, para grabar |
| `Shift + N` | Saltar a la etapa siguiente, para ensayar |

**Parámetros de URL:** `?demo` opera el lander solo, útil para grabar · `?fase=3` empieza en una etapa (1 a 6) · `?silencio` desactiva el sonido.

## Tecnologías empleadas

| Tecnología | Uso |
|---|---|
| **A-Frame 1.6 (WebXR)** | Escena VR para Meta Quest con controles (`hand-controls`) y con manos sin controles (`hand-tracking-controls`), vibración y panel de textos dentro de la escena |
| **Three.js** con shaders propios (GLSL) | Océano con oleaje y reflejo del cielo, agua que cambia de color con la profundidad, superficie vista desde abajo, rayos de sol, nieve marina que solo se ve donde la ilumina un haz, haces de luz volumétricos, nubes de sedimento, medusas y bioluminiscencia |
| **Materiales PBR** | Texturas fotográficas de barro, acero y roca, con mapa de entorno tomado de una foto real de un amanecer, y tono cinematográfico (ACES) |
| **Modelado por código** | Barco de investigación, lander con sus instrumentos, peces caracol de cuerpo translúcido que ondula, enjambre de anfípodos con `InstancedMesh`, cardumen y pepinos de mar |
| **Web Audio API** | Música y sonido generados en tiempo real, sin archivos de audio: un colchón de acordes con reverberación que cambia con cada momento del relato, campanas sueltas, olas y viento, sonar con eco, crujidos de presión, paso del sumergible, golpe y sedimento al tocar fondo |

## Estructura del repositorio

```
fosa-atacama/
├── index.html            Escena A-Frame e interfaz en pantalla
├── css/estilos.css       Estilos de la interfaz en pantalla
├── assets/               Fotografía del cielo y texturas PBR (Poly Haven, CC0)
├── js/
│   ├── base.js           Estado, luz compartida entre shaders, texturas y utilidades de modelado
│   ├── superficie.js     Cielo, océano, costa, barco y chapuzón
│   ├── lander.js         Lander con focos, cámara, instrumentos y brazo de carnada
│   ├── agua.js           Columna de agua, nieve marina, burbujas, medusas, cardumen y fondo
│   ├── fauna.js          Anfípodos y peces caracol
│   ├── descenso.js       Sumergible Limiting Factor, línea de sensores IDOOS, pared de la fosa y ficha con foto
│   ├── interaccion.js    Palanca, linterna, panel VR y manejo de controles y manos
│   ├── principal.js      Relato, descenso, ambiente según profundidad, modo VR y modo pantalla
│   ├── narrativa.js      Textos de cada etapa, zonas de profundidad y puntos de vista
│   └── sonido.js         Música y efectos con Web Audio
└── GUION.md              Guion de la cápsula audiovisual de 1 minuto
```

## Ejecutar en local

```bash
python3 -m http.server 8000
```

Luego abre `http://localhost:8000`. Para probar en el Quest usa la versión publicada, porque WebXR exige HTTPS.

## Publicación

La experiencia se publica en **https://portafolio.insta3d.cl/fosa-atacama/**, dentro del portafolio del taller (repositorio `portafolio`, desplegado en Cloudflare). Para actualizarla, copia los archivos de este repositorio a la carpeta `fosa-atacama/` del portafolio y súbelos.

## Fuentes

- Bases del concurso Chile Re-Descubre (noviembre de 2026), caso *Descubrimiento de la Fosa de Atacama*.
- Emol (2019): [Atacamex: el viaje de los científicos chilenos que estudiaron la Fosa de Atacama a 8 mil metros de profundidad](https://www.emol.com/noticias/Tecnologia/2019/06/18/951775/Atacamex-El-viaje-de-los-cientificos-chilenos-que-estudiaron-la-Fosa-de-Atacama-a-8-mil-metros-de-profundidad.html).
- Newcastle University (2018): [Three new species of snailfish discovered in the Atacama Trench](https://www.ncl.ac.uk/press/articles/latest/2018/09/threenewspecies) y (2022) [New snailfish species](https://www.ncl.ac.uk/press/articles/latest/2022/10/newsnailfishspecies/). *Marine Biodiversity* (2022): [descripción de *Paraliparis selti*](https://link.springer.com/article/10.1007/s12526-022-01294-0).
- Marine Technology News (2018): [A Record-setting Journey to the Atacama Trench](https://www.marinetechnologynews.com/news/record-setting-journey-atacama-560175), sobre el lander Audacia.
- Caladan Oceanic: [Atacama Trench](https://caladanoceanic.com/?p=5914), e Instituto Milenio de Oceanografía: [Atacama Hadal](https://imo.udec.cl/en/?p=1214), sobre la inmersión tripulada de 2022.
- Instituto Milenio de Oceanografía: [IDOOS](https://imo.udec.cl/en/expediciones-y-observatorio/idoos/), y POGO: [Chile completes the installation of its first Integrated Deep-Ocean Observing System](https://pogo-ocean.org/?p=120137).
- Woods Hole Oceanographic Institution (2024): [*Dulcibella camanchaca*](https://www.whoi.edu/press-room/news-release/dulcibella-camanchaca). 24 Horas: [nueva especie de crustáceo depredador en la Fosa de Atacama](https://www.24horas.cl/tendencias/tecnologia-y-ciencias/hallan-nueva-especie-crustaceo-depredador-fosa-atacama).

**Notas de rigor:**
- La presión aumenta cerca de 1 atmósfera cada 10 metros, así que a 8.000 m es unas 800 veces la de la superficie.
- *Paraliparis selti* fue descrito formalmente en 2022 y se ha observado aproximadamente entre 6.000 y 7.600 m. El pez de la experiencia es una representación estilizada.
- *Dulcibella camanchaca* fue recolectado a 7.902 m en una expedición de 2023 y descrito en 2024, con participación del Instituto Milenio de Oceanografía.
- La inmersión tripulada de 2022 llegó a 8.069 m (± 8 m) según Caladan Oceanic. En la experiencia, el sumergible aparece a media bajada como recurso narrativo.
- IDOOS incluye líneas de sensores de corrientes, temperatura, salinidad, presión y oxígeno, y sensores de presión en el fondo. La línea que se ve es una representación, no una réplica de sus equipos.
- Las medusas, el cardumen, los destellos del descenso y los pepinos de mar del fondo son fauna representativa, no especies identificadas de la fosa.

## Créditos

Diseño, programación y modelado 3D: Luis Felipe Benítez.

**Fotografía del sumergible:** [Limiting Factor floating on the water surface](https://commons.wikimedia.org/wiki/File:Limiting_Factor_floating_on_the_water_surface.jpg), de Richard Varcoe para Caladan Oceanic, licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Se usa reducida de tamaño. Es una foto del sumergible en pruebas, no de la inmersión en la Fosa de Atacama.

**Texturas y cielo**, de [Poly Haven](https://polyhaven.com) con licencia **CC0** (dominio público):
- Cielo: panorámica *Umhlanga Sunrise*.
- Texturas: *Brown Mud 03* (sedimento), *Metal Plate* (cubierta), *Green Metal Rust* (casco y lastre) y *Boulder 01* (rocas).

Los modelos 3D (barco, lander, sumergible y fauna) están hechos por código; el sumergible se modeló mirando fotografías publicadas. El pez caracol y los anfípodos son representaciones a partir de las descripciones e imágenes publicadas, no modelos anatómicos exactos.
