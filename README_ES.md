# Norvik RPG Android 1.0

Prototipo jugable de RPG 2D de mundo abierto para Android, un jugador y sin conexión.

## Incluye
- Mundo 2D con bosque, caminos, aldeas y lugares por explorar.
- Controles táctiles y teclado.
- Cuatro personajes con diálogo.
- Misión de mercancías perdidas con recompensa.
- Combate básico contra lobos y bandidos.
- Salud, oro, experiencia, inventario, pociones y curación.
- Día y hora simulados.
- Guardado local en el dispositivo.
- APK compilable desde Android Studio.

## Requisitos para compilar
- Android Studio actualizado.
- JDK incluido en Android Studio.
- Android SDK Platform 35 y Build Tools instalados desde SDK Manager.
- Conexión a Internet la primera vez para descargar Gradle y el plugin de Android.

## Compilar APK en Windows
1. Descomprime `NorvikAndroid.zip`.
2. Abre Android Studio → **Open** → selecciona la carpeta `NorvikAndroid` (la que contiene `settings.gradle`).
3. Espera a que termine **Gradle Sync**. Si solicita instalar SDK Platform 35 o Build Tools, acepta.
4. Selecciona **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. Al terminar, pulsa **locate** en la notificación. El APK de depuración suele quedar en:
   `app/build/outputs/apk/debug/app-debug.apk`

Alternativa desde una terminal de Android Studio, dentro de la carpeta del proyecto:
- Windows: `gradlew.bat assembleDebug`
- Linux/macOS: `./gradlew assembleDebug`

Si el proyecto no tiene `gradlew.bat`, abre el proyecto con Android Studio y deja que configure Gradle; también puedes usar la terminal integrada si el wrapper está disponible.

## Instalar en el teléfono
1. Copia `app-debug.apk` al teléfono (USB, Drive o mensajería).
2. Abre el archivo en Android.
3. Si Android lo solicita, autoriza **Instalar apps desconocidas** para la aplicación que abrió el archivo.
4. Confirma la instalación y abre **Norvik RPG**.

También puedes conectar el teléfono con depuración USB activada y usar:
`adb install -r app/build/outputs/apk/debug/app-debug.apk`

## Controles
- Flechas táctiles para caminar.
- **Hablar / usar** cerca de un personaje para dialogar; cerca de un enemigo, para atacar; lejos de ambos, usa una poción si tienes.
- **Mochila**, **Misiones**, **Mapa** y **Guardar** para abrir los paneles.
- Cerca de Aldric (Norvik), acepta la misión; luego viaja al este por el camino hasta Puerto Gris y habla con Viktor para cobrar la recompensa.
- Puedes descansar con Mara por 15 de oro para recuperar toda la salud.
- El guardado se almacena en el almacenamiento web local de la aplicación y persiste normalmente entre sesiones.

## Limitaciones de esta primera versión
- Es un prototipo inicial: gráficos dibujados por código, mundo generado al iniciar y sistema de combate sencillo.
- No contiene todavía música, animaciones avanzadas, sistema de equipo profundo, tienda general, diálogos ramificados ni publicación en Google Play.
- El proyecto fuente está incluido. El APK no se puede afirmar compilado o probado aquí: debe generarse en Android Studio siguiendo los pasos anteriores.
