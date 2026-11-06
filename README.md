# Andes Aventura - Aplicación Móvil de Turismo y Reservas

Aplicación móvil nativa para Android, desarrollada en **Kotlin**, que permite a los usuarios explorar paquetes turísticos de la Cordillera Blanca, realizar reservas con cálculo automático de costos, gestionar sus cuentas y localizar puntos de encuentro y destinos turísticos mediante mapas interactivos integrados con **Google Maps**.

---

## 1. Requisitos del entorno

Antes de ejecutar el proyecto, asegúrate de contar con las siguientes herramientas:

- **Android Studio:** Iguana o superior (se recomienda Koala o Ladybug).
- **Android SDK:** API 24 (Android 7.0 Nougat) como versión mínima y API 34 o superior como versión de destino.
- **JDK:** Java 8 u 11, según la configuración de Gradle del proyecto.
- **Dispositivo:** Emulador Android con Google Play Services o dispositivo físico Android.

---

## 2. Instalación y configuración

### 2.1. Clonar el repositorio

Clona el repositorio desde GitHub:

```bash
git clone https://github.com/Jeysson0102/andes-aventura-app.git
```


### 2.2. Abrir el proyecto

1. Inicia Android Studio.
2. Selecciona la opción **Open**.
3. Busca y selecciona la carpeta del proyecto clonado.
4. Espera a que Gradle sincronice las dependencias y bibliotecas necesarias, incluidas Material Design y Google Maps.

### 2.3. Configurar Google Maps

Para utilizar correctamente los mapas, debes configurar una API Key válida de **Google Maps SDK for Android**.

Abre el archivo `AndroidManifest.xml` y verifica que contenga la siguiente configuración dentro de la etiqueta `<application>`:

```xml
<meta-data
    android:name="com.google.android.geo.API_KEY"
    android:value="TU_API_KEY_AQUI" />
```

Reemplaza `TU_API_KEY_AQUI` por tu clave de API de Google Maps.

---

## 3. Ejecución de la aplicación

1. Abre el proyecto en Android Studio.
2. Selecciona un dispositivo virtual (por ejemplo, un emulador Pixel) o conecta un dispositivo Android físico con la opción **Depuración USB** habilitada.
3. Haz clic en el botón verde **Run 'app'** o presiona `Shift + F10`.
4. Espera a que el proyecto se compile e instale.
5. La aplicación se iniciará mostrando la pantalla de bienvenida.

---

## 4. Flujo de prueba y funcionalidades

### 4.1. Bienvenida, registro e inicio de sesión

Al iniciar la aplicación, el usuario puede:

- Seleccionar **Registrarse** para crear una nueva cuenta de viajero.
- Iniciar sesión con una cuenta existente.
- Utilizar las credenciales predeterminadas, si están configuradas en el proyecto.

Las cuentas nuevas comienzan con cero reservas registradas.

### 4.2. Catálogo de paquetes turísticos

En la pantalla principal (**Home**) se puede:

- Visualizar un saludo personalizado.
- Consultar el resumen de las reservas activas.
- Explorar el catálogo dinámico de paquetes turísticos mediante un `RecyclerView`.

### 4.3. Detalle del destino turístico

Al seleccionar un paquete turístico, se muestra su información detallada, que incluye:

- Altitud.
- Nivel de dificultad.
- Precio.
- Horarios.
- Información y guía del destino.

Desde esta pantalla, el usuario puede seleccionar **Reservar esta aventura** para iniciar el proceso de reserva.

### 4.4. Formulario de reservas

El formulario permite registrar los datos del viaje y seleccionar una fecha mediante un calendario desplegable.

Además, incorpora un cálculo automático del costo total de la reserva.

### 4.5. Gestión de reservas y filtros

En la sección **Mis Reservas**, el usuario puede consultar y gestionar sus reservas, actualizar su estado de asistencia y aplicar filtros mediante chips interactivos:

- **Pendientes**
- **Confirmadas**
- **Finalizadas**

### 4.6. Google Maps e indicaciones

La aplicación integra Google Maps para visualizar información geográfica relacionada con las reservas.

Desde el mapa, el usuario puede:

- Visualizar su ubicación actual.
- Identificar el punto de encuentro mediante un marcador naranja.
- Identificar el destino turístico mediante un marcador verde.
- Visualizar la ruta entre ambos puntos mediante una línea `Polyline`.
- Utilizar el botón **Cómo llegar** para obtener indicaciones hacia el destino.

---

## 5. Tecnologías y herramientas

- **Lenguaje de programación:** Kotlin.
- **Plataforma:** Android.
- **Entorno de desarrollo:** Android Studio.
- **Interfaz de usuario:** Material Design.
- **Listados dinámicos:** RecyclerView.
- **Mapas y geolocalización:** Google Maps SDK for Android.
- **Construcción del proyecto:** Gradle.

---

## 6. Consideraciones

- Es necesario configurar una API Key válida de Google Maps para utilizar las funcionalidades de mapas.
- El emulador debe contar con Google Play Services para garantizar la compatibilidad con Google Maps.
- Algunas funcionalidades pueden requerir permisos de ubicación en el dispositivo.
- La configuración de compilación debe respetar las versiones de SDK y JDK establecidas en el proyecto.
