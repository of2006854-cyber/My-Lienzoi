# Lienzo infinito → APK con GitHub (sin Android Studio)

Este repositorio compila solo el APK en la nube de GitHub cada vez que subes cambios.

## Pasos (una sola vez)
1. Entra a https://github.com y crea una cuenta (o inicia sesión).
2. Arriba a la derecha: **+ → New repository**. Nombre: `lienzo-infinito`. Déjalo en **Public**. Pulsa **Create repository**.
3. En la página del repositorio pulsa **uploading an existing file**.
4. Arrastra **todo el contenido** de esta carpeta (las carpetas `.github`, `keystore`, `resources`, `scripts`, `www` y los archivos `.gitignore`, `README.md`, `capacitor.config.json`, `package.json`). Abajo pulsa **Commit changes**.
   - Si la carpeta `.github` no se sube: pulsa **Add file → Create new file**, escribe el nombre `.github/workflows/build-apk.yml`, pega ahí el contenido de ese archivo y pulsa **Commit changes**.
5. Ve a la pestaña **Actions**. Si pide permiso, pulsa **I understand my workflows, go ahead and enable them**. Verás **Construir APK** ejecutándose (círculo amarillo). Tarda de 5 a 10 minutos. Cuando salga el check verde ✓, ya está.
6. Descarga el APK: en la página principal del repositorio, a la derecha, entra a **Releases → Lienzo infinito (APK más reciente) → Assets → Lienzo-infinito.apk**.
7. Pásalo al celular (o ábrelo desde el navegador del celular), ábrelo y acepta **instalar de fuentes desconocidas**.

## Para actualizar la app
- Entra a `www/index.html` en GitHub, pulsa el lápiz ✏ (o sube el archivo nuevo), y pulsa **Commit changes**. Se genera un APK nuevo solo, en la misma página de Releases.
- También puedes forzar una compilación en **Actions → Construir APK → Run workflow**.

## Importante
- Si ya instalaste un APK hecho en tu PC con Android Studio, desinstálalo una vez antes de instalar este (la firma es distinta). Haz antes «Copia de todo» para no perder notas.
- Los APK de GitHub siempre usan la misma firma, así que las siguientes versiones se instalan encima sin perder tus notas.
- Si el repositorio es **Private**, para descargar el APK tendrás que iniciar sesión en GitHub desde el celular.
