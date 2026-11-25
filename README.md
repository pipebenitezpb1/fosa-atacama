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
1. **Superficie.** De noche, en la cubierta de un barco frente a Antofagasta. La persona **baja la palanca** para soltar el lander al mar.
2. **Descenso.** Unos 50 segundos de caída libre. El agua pasa de azul a negro, la nieve marina sube alrededor y aparecen medusas y destellos de bioluminiscencia. Se cruzan los 200 m (fin de la luz del sol), los 1.000 m, la zona abisal, la zona hadal y los 7.000 m, profundidad donde cabría el Aconcagua completo.
3. **El fondo.** Golpe al tocar fondo y oscuridad total. La persona **baja la palanca** para encender los focos y aparece el lecho de la fosa.
4. **La carnada.** La persona **suelta la carnada**. Llega un enjambre de anfípodos y, desde la oscuridad, un pez caracol.
5. **Especies nuevas.** *Paraliparis selti* («selti» significa azul en kunza) y *Dulcibella camanchaca*, un crustáceo cazador hallado a 7.902 m y nombrado como la niebla del desierto.
6. **Atacamex 2018.** El cierre con el hito chileno: científicos del Instituto Milenio de Oceanografía llevaron por primera vez un lander a la parte más profunda de la fosa, a 8.081 m.

## Cómo usarla

### En Meta Quest (experiencia principal)
1. Abre la URL en el **navegador del Meta Quest**.
2. Presiona **Entrar en realidad virtual**.
3. Usa los **dos controles**:
   - **Agarrar la palanca:** acerca la mano a la manija, mantén el **gatillo** (o el botón lateral) y **tira hacia ti**. El control vibra al moverla.
   - **Linterna:** va en la mano izquierda. Apunta para iluminar.
   - **Continuar:** aprieta el gatillo lejos de la palanca.

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
| **A-Frame 1.6 (WebXR)** | Escena VR para Meta Quest: controles con `hand-controls`, vibración de los controles y panel de textos dentro de la escena |
| **Three.js** (dentro de A-Frame) | Componentes propios: océano con oleaje, barco, lander, nieve marina y bioluminiscencia con partículas, medusas, fondo marino procedural, enjambre de anfípodos con `InstancedMesh`, pez caracol articulado, focos y linterna con `SpotLight`, palanca que se agarra con la mano |
| **Web Audio API** | Sonido generado en tiempo real: olas, rumor del océano, sonar con eco, crujidos de presión, golpe al tocar fondo. No usa archivos de audio con derechos |
| **Canvas 2D** | Textos dentro de la escena (con tildes y ñ) para el panel VR y la etiqueta de la palanca |

Todos los modelos 3D se generan por código, sin modelos de terceros.

## Estructura del repositorio

```
fosa-atacama/
├── index.html            Escena A-Frame e interfaz en pantalla
├── css/estilos.css       Estilos de la interfaz en pantalla
├── js/
│   ├── componentes.js    Componentes A-Frame (océano, lander, nieve marina, fauna, palanca, panel VR…)
│   ├── principal.js      Relato, descenso, ambiente según profundidad, modo VR y modo pantalla
│   ├── narrativa.js      Textos de cada etapa, zonas de profundidad y puntos de vista
│   └── sonido.js         Paisaje sonoro con Web Audio
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
- Woods Hole Oceanographic Institution (2024): [*Dulcibella camanchaca*](https://www.whoi.edu/press-room/news-release/dulcibella-camanchaca). 24 Horas: [nueva especie de crustáceo depredador en la Fosa de Atacama](https://www.24horas.cl/tendencias/tecnologia-y-ciencias/hallan-nueva-especie-crustaceo-depredador-fosa-atacama).

**Notas de rigor:**
- La presión aumenta cerca de 1 atmósfera cada 10 metros, así que a 8.000 m es unas 800 veces la de la superficie.
- *Paraliparis selti* fue descrito formalmente en 2022 y se ha observado aproximadamente entre 6.000 y 7.600 m. El pez de la experiencia es una representación estilizada.
- *Dulcibella camanchaca* fue recolectado a 7.902 m en una expedición de 2023 y descrito en 2024, con participación del Instituto Milenio de Oceanografía.
- Las medusas y destellos del descenso representan la bioluminiscencia en general, no especies identificadas de la fosa.

## Créditos

Diseño, programación y modelado 3D: Luis Felipe Benítez.
