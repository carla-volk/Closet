# Percha — armario y combinador de outfits

App de una sola página (HTML+CSS+JS, sin backend) para catalogar tu ropa con fotos
y evaluar si un outfit combina, usando reglas de color y estilo (base de conocimiento
"Amelia" — sin IA, 100% reglas fijas).

## Cómo usarla online (recomendado)

1. En este repo, asegúrate de que el archivo principal se llame exactamente
   **`index.html`** (todo minúsculas). GitHub Pages solo sirve ese nombre en la raíz.
2. Ve a **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main** /
   carpeta **/(root)** → **Save**.
3. Espera 1-2 minutos. Tu app queda en:
   `https://<tu-usuario>.github.io/<nombre-del-repo>/`
4. Ábrela desde el navegador del celular y agrégala a la pantalla de inicio
   (Compartir → "Añadir a pantalla de inicio" en iPhone, o menú ⋮ → "Añadir a
   pantalla principal" en Android).

## Cómo usarla localmente

También puedes abrir el archivo `.html` directamente desde tu explorador de
archivos → "Abrir con" → Chrome. Funciona, pero el almacenamiento local del
navegador no siempre es confiable en ese modo — para uso diario, mejor
GitHub Pages.

## Tus datos: dónde viven y cómo respaldarlos

Todo (fotos y prendas) se guarda **solo en el navegador de ese dispositivo**
(IndexedDB), nunca en un servidor. Eso significa:

- No se comparte entre celular y computadora automáticamente.
- Si borras datos del navegador, o cambias de navegador/dispositivo, tu armario
  desaparece de ahí — a menos que tengas un respaldo.

Por eso la app tiene un botón de respaldo:

- **⬇ Exportar respaldo (JSON)** — descarga un archivo `percha-respaldo-FECHA.json`
  con todas tus prendas y fotos.
- **⬆ Restaurar respaldo** — vuelve a cargar ese JSON, en el mismo dispositivo
  o en otro. Puedes elegir si lo agrega a lo que ya tienes o si reemplaza todo.

Recomendación: exporta un respaldo cada vez que agregues varias prendas nuevas,
y guarda ese JSON en Google Drive, iCloud o donde prefieras.

## Estructura del repo

- `index.html` — la app completa (todo en un solo archivo).
