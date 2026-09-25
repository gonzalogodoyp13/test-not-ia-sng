# NOTIFICA IA · Distribución Windows

Agente 0.12.0 para firma con token y recepción automática de PDF.
Distribución **sin certificado de firma de código**, instalada personalmente por
el responsable mediante control remoto. Repositorio previsto: privado.

## Descargar

Abre **Releases** y descarga el ZIP `NOTIFICA-Windows-0.12.0-managed.zip` junto con
sus huellas. El ZIP automático **Source code** no contiene los runtimes del agente.

- [Instalación, inscripción y sesión remota](INSTALACION.md).
- [Cómo cargar esta carpeta y publicar una versión en GitHub](GUIA_GITHUB.md).
- [Plantilla de datos del PC](examples/install-request.example.json).

El instalador admite altas nuevas y reanudación de su propia instalación
interrumpida. No reemplaza agentes existentes. La instalación real en los PCs
destino sigue pendiente de aceptación; la primera publicación debe ser pre-release.

No se requiere firma de editor para este procedimiento. El certificado FEA del
token, HTTPS, validación de los PDF y controles de cuenta/oficina siguen vigentes.
El paquete no modifica las protecciones globales de Windows. Algunos equipos
pueden bloquear aplicaciones sin firma según su política.

## Contenido del repositorio

Esta carpeta contiene guías, herramientas y un ejemplo sin datos reales.
Los binarios se distribuyen como adjuntos de Releases. Los avisos y licencias
de las dependencias se incluyen en el paquete; no se concede una licencia
adicional de código abierto sobre NOTIFICA por publicar esta carpeta.
