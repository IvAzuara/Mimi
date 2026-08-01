# Mimi 🌼 Una Gerbera Blanca Interactiva

Este proyecto es una experiencia web interactiva, minimalista y elegante que presenta una **gerbera blanca** (flor) sobre un fondo oscuro y ambiental. Al hacer clic sobre la flor, se dispara un efecto visual de chispas flotantes y se revela un mensaje especial.

## 🚀 Tecnologías y Decisiones de Diseño

### ¿Por qué Astro?
Para una página de aterrizaje interactiva y estática como esta, **Astro** es la mejor opción frente a React o Vue por los siguientes motivos:
1. **Rendimiento**: Astro compila la página en HTML estático y CSS puro, reduciendo a cero la carga de JavaScript inicial para el navegador.
2. **Generación en Build-Time**: Los cientos de pétalos individuales que componen la gerbera blanca se calculan y generan de forma aleatoria durante la compilación en el servidor/construcción. El cliente recibe el SVG completamente dibujado sin tener que ejecutar JS pesado para posicionar cada pétalo.
3. **Mantenibilidad**: Permite estructurar y modularizar componentes fácilmente, además de añadir integraciones de React o Tailwind en el futuro con un solo comando (`pnpm astro add`).

### Diseño de la Flor (SVG + Filtros)
- **Procedural**: Pétalos generados con ligeras variaciones de escala, opacidad y rotación para una apariencia orgánica.
- **Fidelidad**: Filtro de turbulencia SVG para recrear la textura afelpada/polen del disco central de la gerbera.
- **Micro-interacciones**: Animación de respiración suave, efectos de inclinación y escala en hover, y una explosión de partículas de chispas en el punto de clic.

---

## ✍️ Cómo cambiar el mensaje

El mensaje que se revela al hacer clic en la flor ("Te amo") está definido en la cabecera de la página. Para cambiarlo:

1. Abre el archivo [`src/pages/index.astro`](file:///src/pages/index.astro).
2. Localiza la línea **8**:
   ```javascript
   // Mensaje secreto (fácil de editar más adelante)
   const message = "Te amo";
   ```
3. Reemplaza `"Te amo"` por el texto que prefieras (por ejemplo, `"Eres especial"`, `"Feliz día"`, etc.).
4. Guarda el archivo y compila el proyecto.

---

## 🧞 Comandos y Desarrollo

Ejecuta los siguientes comandos desde la carpeta raíz del proyecto:

| Comando | Acción |
| :--- | :--- |
| `pnpm dev` | Inicia el servidor de desarrollo local en `http://localhost:4321` |
| `pnpm build` | Compila la página de producción optimizada dentro de `./dist/` |
| `pnpm preview` | Previsualiza el build de producción localmente |
| `pnpm astro ...` | Ejecuta comandos de la CLI de Astro (ej. `pnpm astro add react`) |
