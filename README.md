# 🧅 Laravel Flow 3D

**Visualización 3D interactiva del ciclo de vida de una petición HTTP en Laravel** — HTML puro, un solo archivo, sin servidor, sin internet (three.js embebido).

Abre `index.html` y verás cómo una petición viaja en 3D por el "restaurante Laravel": el maître (Router), el portero (Middleware), el chef (Controller) y la despensa (Modelos/BD).

## Dos versiones

| Archivo | Versión | Cómo se ve |
|---|---|---|
| [`index.html`](https://marusan94.github.io/laravel-flow-3d/) | 🧅 **Realista** | Esferas concéntricas (una "cebollla"): la petición entra en espiral hacia el núcleo (Modelos) y sale de vuelta. Incluye **desvíos reales**: ruta 404, redirección a login sin sesión, y validación que devuelve errores |
| [`didactica.html`](https://marusan94.github.io/laravel-flow-3d/didactica.html) | 📏 **Didáctica** | Línea recta: estaciones en orden (Kernel → Router → Middleware → Controller → Modelos) con ida y vuelta sobre un solo camino |

Ambas tienen:
- 🎮 Modo **guiado** (historias con preguntas por nodo) y modo **libre** (explora cada estación a tu ritmo)
- 💻 Tarjetas de **código PHP real** con máquina de escribir
- 🍽️ Metáfora del **restaurante** en cada nodo: el maître (Router), el portero (Middleware), el chef (Controller), la despensa (BD)
- 🎥 Cámara libre: rotar (arrastrar), zoom (rueda/pellizco), pan (clic derecho), WASD
- 🎬 Modo cine, panel ocultable, controles táctiles para móvil

## Historias disponible (versión realista)

1. **Camino feliz** — `GET /usuarios/1` resolviendo el perfil completo
2. **404** — URL que no existe: el maître no la encuentra
3. **Sin sesión** — el portero frena un `GET /panel` y te manda a `/login` (302)
4. **Formulario inválido** — `POST /usuarios` sin email: la validación devuelve errores en sesión

## Por qué no es un "proyecto real"

Es una demo didáctica: quería *ver* el flujo de una petición Laravel de forma bonita e intuitiva, no construir un framework. Todo el lío experimental está en un HTML autónomo de ~640 KB (three.js r128 embebido, MIT).

## Licencia

MIT — haz lo que quieras con él.
