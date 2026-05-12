# Repaso DAM como app

La versión de app está en `index.html`. `preview.html` queda como copia previa.

## Lo recomendado

Lo normal para una app web instalable es publicarla como PWA en una URL HTTPS. Así:

- se instala en móvil/tablet desde Chrome, Edge o Safari;
- aparece con icono en la pantalla de inicio;
- abre en modo app, no como archivo HTML descargado;
- guarda el progreso en el almacenamiento de esa app;
- funciona offline después de la primera carga.

## Publicar con GitHub Pages

Esta carpeta ya incluye `.github/workflows/pages.yml`, así que está preparada para GitHub Pages.

Pasos:

1. Crea un repositorio en GitHub.
2. Sube todo el contenido de esta carpeta.
3. En GitHub, ve a `Settings` > `Pages`.
4. En `Build and deployment`, selecciona `GitHub Actions`.
5. Haz un push a `main` o ejecuta manualmente el workflow `Publicar PWA`.
6. GitHub te dará una URL parecida a:

```text
https://TU_USUARIO.github.io/NOMBRE_DEL_REPO/
```

Abre esa URL en el móvil o tablet.

## Instalar en móvil/tablet

Android con Chrome o Edge:

1. Abre la URL HTTPS de GitHub Pages.
2. Menú del navegador.
3. `Instalar app` o `Añadir a pantalla de inicio`.
4. Abre desde el icono `Repaso DAM`.

iPad/iPhone con Safari:

1. Abre la URL HTTPS.
2. Botón compartir.
3. `Añadir a pantalla de inicio`.

## Prueba local rápida

En Windows puedes hacer doble clic en:

```text
start_app.bat
```

En Linux/WSL/macOS:

```bash
./start_app.sh
```

Después abre en el ordenador:

```text
http://localhost:8765/index.html
```

También puedes abrirlo desde móvil/tablet en la misma Wi-Fi usando la IP local del ordenador:

```text
http://TU_IP_LOCAL:8765/index.html
```

La prueba local sirve para revisar la app, pero la instalación real como PWA debe hacerse desde HTTPS.

## Si quieres APK sin Kotlin

La alternativa habitual es envolver esta misma app web con Capacitor. No habría que reescribir la interfaz en Kotlin; el código seguiría siendo HTML/CSS/JavaScript y Capacitor generaría el proyecto Android.
