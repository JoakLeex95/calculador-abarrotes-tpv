# Calculadora de Precios TPV para iPhone

Esta es una aplicación web progresiva (PWA). Se publica gratis con GitHub Pages y se puede agregar a la pantalla de inicio del iPhone para abrirla como una app.

## Publicar con GitHub Pages
1. Entra a https://github.com e inicia sesión.
2. Crea un repositorio nuevo, por ejemplo: `calculadora-precios-tpv`.
3. Sube **todos** los archivos de esta carpeta a la raíz del repositorio (`index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`).
4. En el repositorio abre **Settings → Pages**.
5. En **Build and deployment**, elige **Deploy from a branch**.
6. Selecciona la rama **main** y la carpeta **/(root)**; pulsa **Save**.
7. GitHub te dará una dirección similar a `https://TU-USUARIO.github.io/calculadora-precios-tpv/`.

## Instalar en iPhone
1. Abre esa dirección en **Safari** (no desde el navegador interno de otra app).
2. Pulsa **Compartir**.
3. Elige **Agregar a pantalla de inicio**.
4. Confirma con **Agregar**. Aparecerá el icono y podrás abrirla en pantalla completa.

## Fórmula implementada
Precio = Costo / (1 - ganancia deseada) / (1 - comisión TPV * (1 + IVA comisión)).

Ejemplo: costo 100, ganancia 15%, TPV 3.5%, IVA de comisión 16%:
100 / 0.85 / 0.9594 = 122.610381...

La ganancia objetivo es porcentaje sobre costo antes de TPV. La app también calcula la ganancia neta después de la comisión. No redondea el precio matemático.

## Privacidad
No hay servidor ni base de datos: los cálculos se realizan en el dispositivo. Los últimos valores ingresados se guardan localmente en el navegador.
