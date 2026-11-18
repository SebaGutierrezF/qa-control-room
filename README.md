# QA Control Room — QA Automation Starter Kit Pro v1.0.0

Sitio estático para revisar y mejorar el producto **QA Automation Starter Kit — Pro v1.0.0**. El repositorio de este dashboard debe permanecer separado del repositorio privado y del ZIP comercial.

## Publicar con GitHub Pages

1. Crear un repositorio **público** llamado `qa-control-room` en GitHub (sin archivos generados por defecto, si usarás los comandos de Git).
2. Subir `index.html`, `README.md` y opcionalmente `.nojekyll` a la raíz de la rama `main`.
3. Abrir **Settings → Pages → Build and deployment**.
4. Elegir **Deploy from a branch**, seleccionar **main** y **/(root)**, y presionar **Save**.
5. Abrir `https://<usuario>.github.io/qa-control-room/` cuando GitHub indique que la publicación está lista.

**No es necesario un proceso de compilación, npm, React ni un workflow personalizado.** El archivo `index.html` contiene el CSS y JS necesarios.

### Subir desde PowerShell y Git

Ejecutar en la carpeta descomprimida de este paquete (si el repositorio remoto se creó vacío):

```powershell
git init
git branch -M main
git add index.html README.md .nojekyll .gitignore
git commit -m "feat: publish QA Control Room initial site"
git remote add origin https://github.com/<usuario>/qa-control-room.git
git push -u origin main
```

Reemplazar `<usuario>` por el nombre de usuario de GitHub. Si se sube desde el navegador de GitHub, `index.html` en la raíz es suficiente para mostrar el Site. `.nojekyll` es opcional para este archivo HTML independiente.

## Datos y privacidad

- **El sitio es público, pero no contiene backend.** Los datos editados se guardan en `localStorage` del navegador, separados por navegador, perfil, dispositivo y origen (URL).
- **GitHub Pages no sincroniza registros, testers ni resultados.** Para cambiar de equipo o recopilar resultados, exportar e importar respaldos JSON manualmente.
- **No subir al repositorio** capturas privadas, JUnit con identificadores, respaldos exportados, nombres de testers, credenciales, rutas locales personales, ZIP comercial o fuentes privadas.
- Los ejemplos de prueba y resultados iniciales son **evidencia histórica reportada por el autor**, no ejecución en vivo ni resultados de clientes.
- Las regresiones sintéticas y el test contra la página pública de Selenium **no prueban ROI, defectos reales de clientes ni compatibilidad universal**.
- El sitio **no inicia automáticamente pytest** ni ejecuta Selenium; registra/importa resultados y ayuda a diagnosticarlos.
- `noindex` en `index.html` pide a buscadores que no indexen este panel, pero **no lo hace privado**.

## Evolución

Los casos, ejecuciones, evidencias, feedback, brechas y decisiones se administran sin reconstruir el producto. Para actualizar el sitio, editar `index.html`, subir un commit al mismo repositorio y conservar una copia de seguridad JSON antes de cambios estructurales.

## Estado inicial

- 5 casos de API
- 8 casos Selenium UI
- 3 casos de framework
- 2 casos de Helpdesk
- Resultados históricos agregados 18/18 y dos repeticiones 17/18 con `test_ui_005_search` en error.
- **No** contiene información verificable de clientes, ROI ni ventas reales.

