# ¿El software es lo tuyo?

Test vocacional con estética arcade para el stand de la **Tecnicatura Superior en Desarrollo de Software** del ISFDyT N° 125 en la Noche de los Institutos.

Los estudiantes de sexto año responden 12 situaciones cotidianas y reciben:

- su **clase de jugador** (tipo de interés dominante) y su código de 3 letras,
- su **compatibilidad con Desarrollo de Software** y el rol que podrían ocupar en un equipo,
- un **pase al salón** (o pase de invitado, si la compatibilidad es baja),
- su compatibilidad con las otras carreras que tienen stand: Educación Inicial, Educación Primaria, Educación Especial, Enfermería y Seguridad e Higiene, con la marca **✔ ABRE** en las confirmadas para el año que viene,
- con el pase desbloqueado (o desde el link `#carrera`), la **ficha de la carrera**: las 22 materias por año con su carga horaria, qué se aprende a hacer, dónde se trabaja y cómo se ingresa (datos de la Res. 5847/19 DGCyE),
- su resultado para llevarse: botón para **descargarlo como imagen** y, en la PC del stand, un **QR** que abre el mismo resultado en el celular.

## Cómo funciona

El test se basa en el modelo de intereses de John Holland (RIASEC: Realista, Investigador, Artístico, Social, Emprendedor, Convencional), el mismo que usa el O*NET Interest Profiler.

- Cada opción de cada situación suma a un tipo de interés, sin mostrarlo en pantalla. El orden de las opciones se mezcla en cada partida.
- El puntaje de cada tipo es la proporción de veces que se eligió sobre las veces que apareció, relativo al tipo más fuerte.
- La compatibilidad con cada carrera es la **correlación** entre el perfil del jugador (sus 6 tipos) y el perfil de la carrera, armado con el código de interés de O*NET de la ocupación asociada (primera letra peso 3, segunda 2, tercera 1, el resto 0). Compara la forma del perfil: si alguien se destaca justo en lo que la carrera no pide, la compatibilidad da baja. La correlación (de −1 a 1) se lleva a una escala de 0 a 100%:

| Carrera | Ocupación O*NET | Código |
|---|---|---|
| Desarrollo de Software | Software Developers (15-1252.00) | IC |
| Educación Inicial | Kindergarten Teachers (25-2012.00) | SA |
| Educación Primaria | Elementary School Teachers (25-2021.00) | S |
| Educación Especial | Special Education Teachers (25-2057.00) | SAI |
| Enfermería | Registered Nurses (29-1141.00) | SCI |
| Seguridad e Higiene | Occupational Health and Safety Specialists (19-5011.00) | ICR |

Las carreras confirmadas para el año que viene (dato de preceptoría) tienen `abre:true` en `CARRERAS`: por ahora Software, Enfermería y Primaria. Si se confirma otra, se cambia ahí.

Con 50% o más de compatibilidad con Software se muestra el pase al salón desbloqueado y el botón para ver la carrera.

Es un juego orientativo, no un test vocacional profesional.

## Uso en el stand

- Abrir la versión publicada en GitHub Pages en la PC del stand. El inicio muestra un **QR** para jugar desde el celular (varios a la vez) y el botón para jugar en esa misma pantalla.
- Desde el celular (link `#jugar`) no hay vuelta automática al inicio ni contador de jugadores.
- El link `#carrera` abre directo la ficha de la carrera, sin jugar el test y sin importar la compatibilidad. Es el que va en el QR impreso de "Info de la carrera"; al final tiene un botón para hacer el test.
- Al subir un `index.html` nuevo, aumentar `VERSION` al principio del `<script>`: va en los links de los QR y evita que un celular muestre una versión vieja guardada.
- Se puede responder tocando o con las teclas `1`–`4` / `A`–`D`.
- La pantalla de resultado vuelve sola al inicio después de 90 segundos sin uso.
- El contador de "jugadores esta noche" se guarda en el navegador de ese dispositivo.
- Se necesita internet para los QR y las tipografías. Sin conexión se puede jugar en la PC con fuentes de respaldo y el QR muestra la dirección en texto.

## Personalizar

Las situaciones, las carreras y los textos de resultado están al principio del `<script>` en `index.html`, en las constantes `SITUACIONES`, `CARRERAS`, `TIPOS`, `ROL_SOFT` y `PLAN` (materias de la ficha de la carrera). El umbral del pase está en `UMBRAL`.
