# 🕒 AppFichaje - Sistema de Control de Asistencia

Proyecto final de aplicación móvil para la gestión de horarios de empleados, desarrollado con **Android Studio** y las últimas tecnologías de Google.

---

## 🚀 Características Principales

* **Autenticación segura:** Acceso restringido mediante ID de usuario y PIN numérico.
* **Lógica de Fichaje Inteligente:** El sistema detecta automáticamente el estado del usuario (Entrada/Salida) para evitar registros duplicados o erróneos.
* **Gestión de Roles:**
    * **Empleado:** Registro de jornada y consulta de historial personal.
    * **Administrador:** Panel de gestión de usuarios (Alta/Baja) y visualización del historial completo de la plantilla.
* **Persistencia de Datos:** Implementación de base de datos local con **Room** para asegurar que los datos no se pierdan al cerrar la app.

---

## 🛠️ Stack Tecnológico



* **Lenguaje:** Kotlin 1.9+
* **Interfaz:** Jetpack Compose (Material Design 3).
* **Base de Datos:** Room Persistence Library (SQLite).
* **Arquitectura:** MVVM (Model-View-ViewModel).
* **Navegación:** Compose Navigation con Scaffold y BottomBar.

---

## 📥 Guía de Instalación y Uso

### 1. Requisitos previos
* Android Studio (Ladybug o superior).
* JDK 17.
* Dispositivo o Emulador con **Android 7.0 (API 24)** o superior.

### 2. Configuración
1.  Descarga y descomprime el archivo `.zip`.
2.  En Android Studio, ve a **File > Open** y selecciona la carpeta del proyecto.
3.  Deja que **Gradle** sincronice las dependencias (necesitarás conexión a internet).

### 3. Credenciales Maestras (Acceso Inicial)
Como la base de datos se inicializa vacía, utiliza estos datos para entrar por primera vez:

| Usuario | PIN | Rol |
| :--- | :--- | :--- |
| **admin** | **1234** | **ADMIN** |

---

## 📂 Estructura del Proyecto

* `MainActivity.kt`: Contiene toda la lógica de la interfaz de usuario dividida en componentes `@Composable`.
* `AppViewModel.kt`: Gestiona el estado de la aplicación, el login y la comunicación con la base de datos.
* `UserEntity.kt / AppDatabase.kt`: Definición del esquema de datos y las consultas (DAO).

---

## 📝 Notas del Desarrollador
* Se ha corregido un error crítico de `ClassCastException` en la pantalla de Login mediante el uso de parámetros nombrados en los layouts de Compose.
* El diseño utiliza colores corporativos (`PrimaryBlue`, `SuccessGreen`, `ErrorRed`) definidos en constantes para mantener la coherencia visual.
* La navegación es dinámica y adapta los iconos de la barra inferior según el rol del usuario logueado.
