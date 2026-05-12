Proyecto base basic-gym
    Cada vez que se modifique una versión, debe modificarse:
    - src\assets\version.json
    - package.json
    - android\app\build.gradle

    Cada vez que se modifique una sub version, debe modificarse:
    - src\assets\version.json
    - package.json

version.json
    Siempre debe tener la última versión existente (incluye versión menor), por ejemplo: 2.0.1


version.log.json

- Posición 0 (obligatorio): Versión mayor que obliga a descargar nueva apk "installApk": true
- Posición 1 en adelante (opcional): Versión menor (posterior a la mayor) que actualiza el contenido mediante un update.zip "installApk": false

Ejemplo

[
    { "version": "2.0.0", "installApk": true, "changelog": "..." || [] },
    { "version": "2.0.1", "installApk": false, "changelog": "..." || [] }
]
