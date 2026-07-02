# Inventario de fotos diario — Produce Solutions

Esta página muestra el inventario fresco del día. El link que manda el bot por WhatsApp cada mañana apunta aquí.

## Cómo actualizarla cada mañana (sin tocar código)

1. **Sube las fotos nuevas** a la carpeta `images/` (arrastra y suelta directo en GitHub, botón "Add file → Upload files").
   - Usa nombres simples sin espacios ni acentos, ej: `mango-ataulfo.jpg`, `pina-5ct.jpg`.
2. **Edita el archivo `hoy.json`** (haz clic en el archivo → ícono de lápiz para editar):
   - Cambia `"fecha"` a la fecha de hoy, formato `AAAA-MM-DD` (ej: `2026-07-03`).
   - En `"productos"`, agrega o quita bloques según lo que tengas hoy en piso:
     ```json
     {
       "nombre": "Nombre del producto",
       "imagen": "images/nombre-del-archivo.jpg",
       "nota": "Texto corto opcional, ej: Recién llegado"
     }
     ```
   - Puedes dejar `"nota": ""` si no quieres poner nada ahí.
3. Dale clic a **"Commit changes"** (guardar cambios) — la página se actualiza sola en 1-2 minutos.

## El link que va en la plantilla de WhatsApp

Una vez activado GitHub Pages en este repositorio (Settings → Pages → Branch: main), el link es:

```
https://producesolutionsonline-ai.github.io/inventario-produce-2/
```

Ese es el link fijo que se usa en la plantilla `fotos_inventario_diario` — nunca cambia, solo cambia el contenido que muestra.
