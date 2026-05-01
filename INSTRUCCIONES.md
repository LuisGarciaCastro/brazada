# Brazada — instalar como app en iPhone vía GitHub Pages

Guía paso a paso. No hace falta saber programar.

---

## Paso 1 — Crear el repositorio en GitHub

1. Entra en https://github.com y haz login (o crea cuenta gratis si no tienes).
2. Arriba a la derecha, pulsa el **+** → **New repository**.
3. Rellena:
   - **Repository name:** `brazada` (o el nombre que quieras, sin espacios)
   - **Public** ✓ (necesario para que GitHub Pages funcione gratis)
   - NO marques "Add a README" ni nada más
4. Pulsa **Create repository**.

---

## Paso 2 — Subir los archivos

En la pantalla del repo recién creado verás un enlace que dice **"uploading an existing file"**. Pulsa ahí.

Arrastra **TODOS** estos archivos a la zona de subida:

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icon-192.png`
- `icon-512.png`
- `icon-maskable-512.png`
- `apple-touch-icon.png`
- `favicon-32.png`
- `icon.svg` (opcional, por si quieres re-generar iconos en el futuro)

Abajo, en **Commit changes**, pulsa el botón verde **Commit changes**.

---

## Paso 3 — Activar GitHub Pages

1. En el repo, ve a **Settings** (arriba a la derecha del menú del repo).
2. En el menú lateral izquierdo, busca **Pages**.
3. En **Source**, selecciona:
   - Branch: `main`
   - Folder: `/ (root)`
4. Pulsa **Save**.

GitHub te dirá: *"Your site is live at https://TU-USUARIO.github.io/brazada/"*

⏱️ Espera 1-2 minutos a que se despliegue. La primera vez tarda un poquito.

---

## Paso 4 — Instalarla en el iPhone

1. Abre **Safari** en el iPhone (importante: tiene que ser Safari, no Chrome).
2. Ve a tu URL: `https://TU-USUARIO.github.io/brazada/`
3. Cuando cargue la app, pulsa el botón de **Compartir** (cuadrado con flecha hacia arriba) en la parte de abajo.
4. Desliza hacia abajo y pulsa **"Añadir a pantalla de inicio"**.
5. Confirma el nombre (saldrá "Brazada") y pulsa **Añadir**.

🎉 Ya tienes el icono en tu pantalla de inicio. Al pulsarlo se abre como app, sin barras del navegador.

---

## Cómo actualizar la app más adelante

Si algún día modificas algo del HTML:

1. En GitHub, entra en el archivo `index.html`.
2. Pulsa el icono del **lápiz** (arriba derecha del archivo) para editar.
3. Pega el contenido nuevo.
4. Abajo, pulsa **Commit changes**.

En 1-2 minutos los cambios estarán online. La app se actualizará sola la próxima vez que la abras (gracias al service worker).

---

## ¿Y si quiero cambiar el icono?

Edita `icon.svg` o sube tu propio diseño. Genera los PNGs en estos tamaños:
- 180×180 → `apple-touch-icon.png`
- 192×192 → `icon-192.png`
- 512×512 → `icon-512.png` y `icon-maskable-512.png`

Sube los nuevos archivos al repo (sustituyendo los antiguos).

---

## Notas importantes

- **Datos:** se guardan en el almacenamiento del navegador del iPhone. **No se sincronizan entre dispositivos.** Si cambias de iPhone, los datos no se llevan automáticamente (es una limitación de las PWAs).
- **Privacidad:** la URL es pública, pero al ser un nombre que solo tú conoces, es prácticamente privada. Nadie va a buscar `brazada.github.io` por casualidad.
- **Offline:** una vez instalada y abierta una vez, funciona sin internet. Perfecto para el vestuario donde la cobertura suele ser mala.
- **Coste:** 0 €. GitHub Pages es gratis para repos públicos y no tiene límite real de tráfico para este uso.
