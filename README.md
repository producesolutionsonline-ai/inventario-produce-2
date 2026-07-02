# Inventario de fotos diario — Produce Solutions

Esta página muestra TODAS las fotos que haya en la carpeta `images/`, automáticamente. El link que manda el bot por WhatsApp cada mañana apunta aquí.

## Cómo actualizarla cada mañana (sin tocar código)

1. **Sube las fotos nuevas** a la carpeta `images/` (arrastra y suelta directo en GitHub, botón "Add file → Upload files"). La página las va a mostrar todas automáticamente, no hace falta editar nada más.
2. **Nombra los archivos con el nombre del producto**, sin espacios ni acentos — el nombre del archivo es lo que se muestra en la página:
   - `mango-ataulfo.jpg` → se muestra como "Mango Ataulfo"
   - `pina-5ct.jpg` → se muestra como "Pina 5ct"
   - Evita nombres genéricos tipo `Screenshot 2026-06-27.png` o `Gemini_Generated_Image_xyz.png` — no se van a ver bien en la página.
3. **Para quitar un producto del día**, simplemente borra esa foto de la carpeta `images/` (clic en el archivo → ícono de bote de basura).

## Opcional: agregar una nota corta a una foto (ej. "Recién llegado")

Edita el archivo `hoy.json` y agrega el nombre exacto del archivo dentro de `"notas"`:

```json
{
  "fecha": "2026-07-03",
  "notas": {
    "mango-ataulfo.jpg": "Recién llegado",
    "pina-5ct.jpg": "Buen precio hoy"
  }
}
```

También puedes actualizar `"fecha"` cada mañana (formato `AAAA-MM-DD`) para que el sello circular muestre la fecha correcta.

## El link que va en la plantilla de WhatsApp

```
https://producesolutionsonline-ai.github.io/inventario-produce-2/
```

Ese es el link fijo que se usa en la plantilla `fotos_inventario_diario` — nunca cambia, solo cambia el contenido que muestra.
