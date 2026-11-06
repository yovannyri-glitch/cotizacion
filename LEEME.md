# Cotizador EASYCAR – APK

Este proyecto empaqueta el cotizador (carpeta `www/index.html`) como app de Android con Capacitor.

## Opción A: compilar en GitHub (sin instalar nada)

1. Crea un repositorio en github.com (puede ser privado).
2. Sube TODO el contenido de esta carpeta (incluida `.github`; si la web no deja subir carpetas ocultas, usa GitHub Desktop o `git push`).
3. Ve a la pestaña **Actions** > **Compilar APK**. Si no arrancó solo, pulsa **Run workflow**.
4. Cuando termine (unos 5 a 10 min), abre la ejecución y descarga **Cotizador-EASYCAR-apk** (viene en .zip; dentro está `app-debug.apk`).
5. Pasa el APK al celular y ábrelo. Android pedirá permitir "instalar apps de origen desconocido".

## Opción B: Android Studio

```
npm install
npx cap add android
npx cap sync android
npx cap open android
```
Luego en Android Studio: Build > Build APK(s).

## Notas

- El APK es de depuración (firmado con clave de debug): sirve para instalar y usar internamente. Para publicarlo en Play Store hay que generar uno firmado (release).
- Para cambiar el cotizador, edita `www/index.html` y vuelve a compilar.
- Las fuentes se cargan de Google Fonts; sin internet se usan las del sistema. Todo lo demás funciona sin conexión.
- El botón de WhatsApp abre la app de WhatsApp del celular.
