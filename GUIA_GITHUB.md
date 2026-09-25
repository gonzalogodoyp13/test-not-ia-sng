# Publicar la distribución en GitHub

Usa un repositorio **privado separado**, por ejemplo `notifica-windows`.
El repositorio existente `NOTIFICA-IA` contiene la aplicación: no subas toda esa
carpeta para distribuir el agente.

## Primera publicación desde el navegador

1. En GitHub, pulsa **New repository**. Escribe `notifica-windows`, selecciona
   **Private** y crea un README inicial. No elijas una licencia de código abierto
   para tu software sin haber decidido otorgarla.
2. En el repositorio nuevo, usa **Add file → Upload files**.
3. Sube **el contenido de la carpeta `repository` preparada**, no su carpeta padre.
   Incluye README, guías, ejemplo y herramientas. Comprueba también `.gitignore`.
   Guarda el commit en `main`. No subas configuraciones reales de usuarios.
4. Abre **Releases → Draft a new release**.
5. Crea el tag `v0.12.0-managed.1`, dirigido a `main`. Título sugerido:
   `NOTIFICA Windows 0.12.0 - instalación administrada`.
6. Copia el contenido de `release-assets/RELEASE-NOTES.md` en la descripción.
7. Adjunta `NOTIFICA-Windows-0.12.0-managed.zip` y `SHA256SUMS.txt` desde
   `release-assets`. Los binarios van aquí, **no como archivos normales del repositorio**.
8. Marca **pre-release** mientras no se haya aceptado la instalación real en los
   equipos destino. Puedes guardarla primero como borrador y comprobar archivos y hashes.
9. Publica cuando estés listo para descargarla desde tus sesiones de control remoto.

Al ser privado, accede con tu cuenta desde la sesión de instalación y cierra esa
sesión de GitHub al terminar en un PC ajeno. No incrustes un token personal de
GitHub en scripts, URLs, JSON ni accesos directos. No necesitas dar a todos los
usuarios acceso al repositorio si tú haces las instalaciones.

## Versiones siguientes

Crea un tag y Release nuevos; no sustituyas silenciosamente el ZIP de una versión
ya usada. Guarda sus huellas y conserva paquetes anteriores para investigar
instalaciones. Este primer instalador es para altas nuevas, no actualiza instalaciones
existentes. Antes de distribuir una actualización, prepara y prueba su migración
con preservación de claves, configuración y documentos.

## Qué nunca subir

`.env`, contraseñas, PIN, códigos de inscripción activos, PFX/P12/PEM con claves,
credenciales de GitHub, bases de datos, documentos de clientes, diarios de firma,
archivos de identidad ni la carpeta `C:\ProgramData\NotificaIA`.
La distribución preparada se obtiene mediante una lista explícita de archivos;
no es una copia completa de tu escritorio ni del proyecto.

## Por qué usar Releases

GitHub Releases está diseñado para distribuir archivos binarios. Cada archivo
adjunto debe medir menos de 2 GiB. El ZIP de este agente incluye runtimes y motor
PDF; por eso es mucho más grande que las guías del repositorio.

Fuentes: [Crear un repositorio](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository),
[Administrar Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository),
[Acerca de Releases y límites](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases).
