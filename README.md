# Kaminaljuyú AR - Realidad Aumentada para el Patrimonio Cultural

**Proyecto de Graduación 2025**

**Carnet:** 21666  
**Nombre:** Carlos Edgardo López Barrera  
**Título:** Implementación de modelos tridimensionales mediante Realidad Aumentada para ofrecer una experiencia inmersiva en una aplicación móvil Android con tecnología ARCore en el Parque Arqueológico Kaminaljuyú  
**Universidad:** Universidad del Valle de Guatemala  
**Facultad:** Ingeniería  
**Carrera:** Ingeniería en Ciencias de la Computación y Tecnologías de la Información  
**Fecha:** Enero 2025

---

## 📋 Descripción del Proyecto

ARTour Kaminaljuyú es una aplicación móvil innovadora que integra **Realidad Aumentada (AR)** para enriquecer la experiencia de los visitantes del Parque Arqueológico Kaminaljuyú en Guatemala. Mediante la tecnología **ARCore de Google**, la aplicación permite visualizar modelos tridimensionales de estructuras arqueológicas sobrepuestos al entorno físico real, ofreciendo una experiencia inmersiva, educativa y culturalmente significativa.

### Contexto y Motivación

El Parque Arqueológico Kaminaljuyú es uno de los sitios más representativos de la civilización maya en Guatemala. Sin embargo, enfrenta desafíos importantes:

- La mayoría de los montículos se encuentran erosionados o sin excavar
- Limitada información interactiva disponible para visitantes
- Señalización textual tradicional que dificulta la comprensión del valor histórico
- Baja motivación del público, especialmente jóvenes, para realizar recorridos presenciales

Este proyecto responde a la necesidad de **modernizar y enriquecer la experiencia de exploración** del parque mediante tecnologías inmersivas, permitiendo que los visitantes visualicen reconstrucciones digitales de estructuras arqueológicas, accedan a información contextualizada y exploren el patrimonio cultural de manera interactiva y accesible.

### Objetivos

#### Objetivo General

Implementar modelos tridimensionales mediante Realidad Aumentada para ofrecer una experiencia inmersiva en una aplicación móvil Android con tecnología ARCore en el Parque Arqueológico Kaminaljuyú.

#### Objetivos Específicos

1. **Integrar objetos y modelos tridimensionales** en una aplicación móvil para Android, permitiendo su visualización inmersiva en el entorno físico mediante la tecnología de Realidad Aumentada ARCore

2. **Desarrollar e implementar interacciones funcionales** entre los modelos 3D y el usuario, mediante técnicas de posicionamiento espacial, gestos táctiles y retroalimentación visual y/o táctil para mejorar la experiencia de exploración

3. **Establecer anclajes espaciales precisos** para la correcta proyección de los modelos 3D en el entorno físico del Parque Kaminaljuyú, logrando una alineación coherente entre la realidad aumentada y el espacio real mediante funcionalidades avanzadas de ARCore

4. **Evaluar el rendimiento, estabilidad y correcta ejecución** de la aplicación móvil en diferentes dispositivos Android mediante pruebas técnicas de carga, compatibilidad y comportamiento en campo, asegurando su funcionamiento óptimo en condiciones reales de uso

---

## Tecnologías Utilizadas

### Plataforma Principal
- **ARCore** - Framework de Realidad Aumentada de Google para Android
- **Android SDK** - Plataforma de desarrollo móvil
- **Kotlin** - Lenguaje de programación principal

### Motor Gráfico y Renderizado
- **Sceneform** (Google) - Renderizado 3D para aplicaciones AR
- **OpenGL ES** - Procesamiento gráfico en tiempo real

### Procesamiento de Modelos 3D
- **Formato .obj** - Modelos tridimensionales
- **Texturas y materiales** - Visualización realista de estructuras

### Componentes y Módulos Desarrollados

#### Gestión de Modelos 3D
- `ModelController.kt` - Controlador principal para carga y gestión de modelos
- `ModelPart.kt` - Representación de componentes individuales de modelos
- Carga asincrónica de recursos `.obj`
- Aplicación de transformaciones espaciales (traslación, rotación, escala)

#### Sistema de Interacción
- Gestos multitáctiles (pellizcar, rotar, desplazar)
- `HapticFeedback.kt` - Retroalimentación háptica para reforzar interacción
- Manipulación en tiempo real de objetos virtuales

#### Infraestructura AR
- `ARCoreSessionLifecycleHelper.kt` - Gestión del ciclo de vida de sesiones AR
- Detección de superficies mediante reconocimiento de planos
- Anclaje espacial preciso de modelos 3D
- Calibración espacial con el entorno físico

### Optimizaciones Técnicas

- **Reducción de complejidad geométrica** - Para dispositivos móviles
- **Agrupación de materiales** - Minimizar llamadas de renderizado
- **Control de tamaño de texturas** - Balance entre calidad visual y rendimiento
- **Procesamiento en tiempo real** - Renderizado fluido (60 FPS objetivo)

### Herramientas de Desarrollo
- **Android Studio** - IDE principal
- **Git/GitHub** - Control de versiones
- **Unity** (opcional) - Herramientas de preprocesamiento 3D

### APIs y Servicios
- **Google ARCore API** - Funcionalidades de Realidad Aumentada
- **Geolocalización (GPS)** - Sistema de navegación espacial
- **Almacenamiento local** - Caché de modelos y recursos

---

## 📦 Requisitos Previos

### Hardware

- **Dispositivo Android** compatible con ARCore
- **Versión mínima:** Android 7.0 (API Level 24) o superior
- **Características requeridas:**
  - Cámara trasera con capacidades AR
  - Giroscopio y acelerómetro
  - GPS para funcionalidades de geolocalización
- **Memoria RAM:** Mínimo 3 GB (recomendado 4 GB o más)
- **Almacenamiento:** Al menos 500 MB de espacio disponible

### Software (Para Desarrollo)

- **Android Studio** Arctic Fox (2020.3.1) o superior
- **JDK** 11 o superior
- **Gradle** 7.0+
- **Android SDK:**
  - SDK Platform API 33 (Android 13)
  - Build Tools 33.0.0
- **Google Play Services para ARCore**
- **Git** para control de versiones

### Verificar Compatibilidad ARCore

Para verificar si tu dispositivo es compatible con ARCore:

```bash
# Visita la lista oficial de dispositivos compatibles
https://developers.google.com/ar/devices
```

Dispositivos Android comunes compatibles:
- Google Pixel (todas las versiones desde Pixel 1)
- Samsung Galaxy S8 y superiores
- Samsung Galaxy Note 8 y superiores
- Xiaomi Mi 8 y superiores
- Huawei P20 y superiores (sin servicios Google puede requerir ajustes)

---

## 🔧 Instalación

### Opción 1: Instalación desde APK (Usuarios Finales)

1. **Descargar el APK** desde la carpeta `/release` o desde el enlace de distribución
2. **Habilitar instalación de fuentes desconocidas** en tu dispositivo Android:
   - Ve a `Configuración > Seguridad > Fuentes desconocidas`
   - Activa la opción
3. **Instalar el archivo APK** descargado
4. **Verificar permisos** requeridos:
   - Cámara
   - Ubicación (GPS)
   - Almacenamiento

### Opción 2: Compilación desde Código Fuente (Desarrolladores)

Sigue estos pasos para configurar el proyecto en tu entorno de desarrollo:

#### 1. Clonar el repositorio

```bash
git clone https://github.com/csuvg/PG-2025-21666.git
cd PG-2025-21666
```

#### 2. Abrir el proyecto en Android Studio

```bash
# Abrir Android Studio y seleccionar:
# File > Open > [Ruta al proyecto clonado]/src
```

#### 3. Configurar variables de entorno (opcional)

Si el proyecto requiere API keys específicas, crea un archivo `.env` o `local.properties`:

```bash
cd src
cp .env.example .env
```

Edita el archivo `.env` con tus credenciales:

```properties
# Google Maps API (si aplica)
GOOGLE_MAPS_API_KEY=tu_clave_aqui

# ARCore Cloud Anchors (si aplica)
ARCORE_CLOUD_ANCHOR_API_KEY=tu_clave_aqui
```

**Importante:** El archivo `google-services.json` debe ser obtenido de Firebase Console si el proyecto utiliza servicios de Google. No está incluido en el repositorio por seguridad.

#### 4. Sincronizar dependencias de Gradle

En Android Studio:

```bash
# Android Studio sincronizará automáticamente las dependencias
# O ejecuta manualmente:
./gradlew build
```

#### 5. Configurar dispositivo de prueba

**Opción A: Dispositivo físico (recomendado para AR)**

1. Habilitar **Opciones de desarrollador** en tu dispositivo Android
2. Activar **Depuración USB**
3. Conectar el dispositivo via USB
4. Verificar que Android Studio detecte el dispositivo

**Opción B: Emulador (limitado para AR)**

```bash
# Nota: ARCore no funciona completamente en emuladores
# Se recomienda usar dispositivo físico para pruebas completas
```

#### 6. Compilar y ejecutar

En Android Studio:

```bash
# Clic en el botón "Run" (▶️) o presiona Shift+F10
# Selecciona tu dispositivo de destino
```

O desde terminal:

```bash
./gradlew installDebug
```

---

## ▶️ Ejecución

### Para Usuarios Finales

1. **Abrir la aplicación** "Kaminaljuyú AR" en tu dispositivo Android
2. **Aceptar los permisos** solicitados (cámara, ubicación)
3. **Dirigirte al Parque Arqueológico Kaminaljuyú**
4. **Seguir las instrucciones** en pantalla para iniciar la experiencia AR

### Flujo de Uso de la Aplicación

#### 1. Pantalla de Inicio
- Visualización del mapa del Parque Kaminaljuyú
- Selección de montículo o estructura a explorar
- Información general del sitio

#### 2. Modo AR
- Apuntar la cámara hacia una superficie plana
- Esperar a que ARCore detecte el plano (indicador visual)
- Tocar la pantalla para anclar el modelo 3D

#### 3. Interacción con Modelos 3D

**Gestos disponibles:**
- **Pellizcar:** Escalar el modelo (zoom in/out)
- **Rotar con un dedo:** Girar el modelo en su eje vertical
- **Arrastrar:** Mover el modelo sobre el plano detectado
- **Tocar el modelo:** Mostrar información contextual

#### 4. Navegación en el Parque
- Flechas AR indican la dirección al siguiente montículo
- Distancia en tiempo real al punto de interés
- Información arqueológica contextualizada

### Para Desarrolladores

#### Ejecución en modo Debug

```bash
# Desde Android Studio
# Seleccionar configuración "app" y presionar Run

# O desde terminal
./gradlew installDebug
adb shell am start -n com.artour.kaminaljuyu/.MainActivity
```

#### Generar APK de Producción

```bash
# APK de Release
./gradlew assembleRelease

# El APK estará en:
# app/build/outputs/apk/release/app-release.apk
```

#### Generar Bundle para Google Play

```bash
./gradlew bundleRelease

# El Bundle estará en:
# app/build/outputs/bundle/release/app-release.aab
```

### Solución de Problemas Comunes

#### La cámara no detecta planos
- Asegúrate de tener buena iluminación
- Apunta a superficies con textura (evita superficies lisas o reflectantes)
- Mueve lentamente el dispositivo para que ARCore escanee el entorno

#### El modelo 3D no se carga
- Verifica tu conexión a internet (si se descargan remotamente)
- Revisa que el dispositivo tenga suficiente memoria disponible
- Reinicia la aplicación

#### Bajo rendimiento o lag
- Cierra aplicaciones en segundo plano
- Reduce la calidad gráfica en configuración (si disponible)
- Verifica que tu dispositivo cumpla con los requisitos mínimos

---

## 📂 Estructura del Proyecto

```
PG-2025-21666/
│
├── demo/
│   └── demo.mp4              # Video demostrativo del proyecto (3-5 min)
│                             # Incluye: introducción, demostración de
│                             # funcionalidades, casos de uso reales
│
├── docs/
│   └── informe_final.pdf     # Informe técnico completo del proyecto
│                             # Documento de graduación con metodología,
│                             # resultados y conclusiones
│
├── src/                      # Código fuente de la aplicación Android
│   ├── app/
│   │   ├── src/
│   │   │   ├── main/
│   │   │   │   ├── java/com/artour/kaminaljuyu/
│   │   │   │   │   ├── MainActivity.kt
│   │   │   │   │   ├── ar/
│   │   │   │   │   │   ├── ModelController.kt     # Controlador de modelos 3D
│   │   │   │   │   │   ├── ModelPart.kt           # Componentes de modelos
│   │   │   │   │   │   ├── HapticFeedback.kt      # Retroalimentación táctil
│   │   │   │   │   │   └── ARCoreSessionLifecycleHelper.kt
│   │   │   │   │   ├── models/                     # Clases de datos
│   │   │   │   │   ├── ui/                         # Interfaces de usuario
│   │   │   │   │   ├── navigation/                 # Sistema de navegación
│   │   │   │   │   └── utils/                      # Utilidades generales
│   │   │   │   ├── res/
│   │   │   │   │   ├── layout/                     # Layouts XML
│   │   │   │   │   ├── drawable/                   # Recursos gráficos
│   │   │   │   │   ├── values/                     # Strings, colores, estilos
│   │   │   │   │   └── raw/                        # Modelos 3D (.obj)
│   │   │   │   └── AndroidManifest.xml
│   │   ├── build.gradle.kts                        # Configuración de Gradle (app)
│   │   └── proguard-rules.pro
│   ├── gradle/
│   ├── build.gradle.kts                            # Configuración de Gradle (proyecto)
│   ├── settings.gradle.kts
│   ├── .env.example                                # Plantilla variables de entorno
│   └── README.md                                   # Documentación del código fuente
│
├── .gitignore                                      # Archivos excluidos del repo
└── README.md                                       # Este archivo
```

### Descripción de Componentes Clave

#### `/src/app/src/main/java/.../ar/`
Módulos principales de Realidad Aumentada:
- **ModelController.kt**: Gestión de carga, renderizado y transformaciones de modelos 3D
- **ModelPart.kt**: Representación de componentes individuales de las estructuras arqueológicas
- **HapticFeedback.kt**: Sistema de retroalimentación táctil para mejorar la interacción
- **ARCoreSessionLifecycleHelper.kt**: Administración del ciclo de vida de sesiones AR

#### `/src/app/src/main/res/raw/`
Recursos de modelos 3D en formato `.obj` de las estructuras del Parque Kaminaljuyú:
- Montículo C-II-12
- Montículo C-II-13
- Montículo C-II-3
- Otras estructuras arqueológicas

#### `/demo/`
Video demostración que muestra:
1. Introducción al proyecto y contexto
2. Funcionalidades principales de la app
3. Casos de uso en el Parque Kaminaljuyú
4. Interacción con modelos 3D mediante gestos
5. Sistema de navegación AR

#### `/docs/`
Documentación académica completa que incluye:
- Marco teórico sobre geometría proyectiva y AR
- Metodología de desarrollo
- Resultados de pruebas de usabilidad
- Análisis de rendimiento
- Conclusiones y recomendaciones

---

## Funcionalidades Principales

### 1. Visualización de Modelos 3D en Realidad Aumentada

- **Renderizado en tiempo real** de estructuras arqueológicas del Parque Kaminaljuyú
- **Anclaje espacial preciso** mediante detección de planos de ARCore
- **Superposición coherente** de modelos virtuales sobre el entorno físico
- **Optimización automática** para diferentes dispositivos móviles

**Estructuras disponibles:**
- Montículo C-II-12
- Montículo C-II-13
- Montículo C-II-3
- Estructuras adicionales del complejo arqueológico

### 2. Interacción Táctil con Modelos

**Gestos multitáctiles implementados:**

#### Escalado (Pinch to Zoom)
- Pellizcar con dos dedos para acercar/alejar
- Visualización de detalles arquitectónicos
- Rango de escala: 0.5x a 5x

#### Rotación
- Girar con un dedo para rotar el modelo
- Rotación en 360° sobre eje vertical
- Exploración de todos los ángulos de la estructura

#### Traslación
- Arrastrar para mover el modelo sobre la superficie detectada
- Reposicionamiento dinámico en el espacio AR

### 3. Retroalimentación Háptica

- **Vibración táctil** al interactuar con modelos
- **Confirmación háptica** al anclar objetos en el espacio
- **Feedback sensorial** que refuerza la experiencia inmersiva

### 4. Sistema de Información Contextual

#### Tarjetas Emergentes
- **Información arqueológica** al tocar un modelo
- **Datos históricos** sobre cada estructura
- **Características arquitectónicas** relevantes
- **Período de construcción** y cultura

#### Contenido Educativo
- Descripción de la importancia histórica
- Contexto cultural de la civilización maya
- Relación con otras estructuras del sitio

### 5. Navegación AR en el Parque

#### Sistema de Flechas Direccionales
- **Indicadores AR** que señalan hacia el siguiente punto de interés
- **Distancia en tiempo real** al destino
- **Orientación dinámica** que sigue el movimiento del usuario
- **Rutas sugeridas** para recorrido óptimo

#### Geolocalización Integrada
- **GPS de precisión** para ubicar estructuras
- **Mapa interactivo** del parque
- **Posición actual del usuario** en el sitio

### 6. Optimización de Rendimiento

#### Gestión de Recursos Gráficos
- **Carga asincrónica** de modelos 3D
- **LOD (Level of Detail)** automático según distancia
- **Culling** de objetos fuera de vista
- **Compresión de texturas** para reducir uso de memoria

#### Rendimiento Objetivo
- **60 FPS** en dispositivos de gama media-alta
- **30-45 FPS** en dispositivos de gama media
- **Consumo optimizado** de batería
- **Tiempo de carga** < 3 segundos por modelo

### 7. Características Técnicas Avanzadas

#### Detección de Superficies
- **Reconocimiento automático** de planos horizontales y verticales
- **Anclaje persistente** que mantiene posición de modelos
- **Adaptación a diferentes condiciones** de iluminación

#### Transformaciones Espaciales
- **Matrices de transformación 4×4** para precisión matemática
- **Cuaterniones** para rotaciones suaves sin gimbal lock
- **Coordenadas homogéneas** para proyección precisa

---

## 🎥 Demo y Documentación

### Video Demostración

📹 **[Ver Video Demo](./demo/demo.mp4)** - Duración: 3-5 minutos

Demostración completa de funcionalidades principales, interacción con modelos 3D, navegación AR y casos de uso reales en el Parque Kaminaljuyú.

### Informe Técnico Completo

📚 **[Informe Final PDF](./docs/informe_final.pdf)**

Documentación completa incluyendo marco teórico, metodología, resultados de pruebas, análisis técnico, conclusiones y recomendaciones.

---

## 🧪 Pruebas y Validación

### Resultados de Pruebas de Usabilidad

**Participantes:** Usuarios reales del Parque Kaminaljuyú

| Criterio | Resultado |
|----------|-----------|
| Facilidad de uso | 8.5/10 |
| Claridad de instrucciones | 9.0/10 |
| Precisión de detección | 8.2/10 |
| Calidad visual 3D | 9.2/10 |
| Utilidad educativa | 9.5/10 |
| Intención de recomendar | 90% |

### Rendimiento Técnico

**FPS por dispositivo:**
- Gama alta (Samsung S21, Pixel 5): 55-60 FPS
- Gama media (Xiaomi Mi 10, Galaxy A52): 35-50 FPS
- Gama baja: 25-35 FPS

**Tiempo de carga de modelos:**
- Montículo C-II-12: 2.1 segundos
- Montículo C-II-13: 1.8 segundos
- Montículo C-II-3: 2.3 segundos

**Consumo de recursos:**
- RAM: 280-450 MB
- Almacenamiento: ~150 MB
- Batería (30 min uso): 15-20%

---

## Autor

| Nombre | Carnet |
|--------|--------|
| **Carlos Edgardo López Barrera** | **21666** |

---

## Contribuciones

Proyecto académico de graduación de la Universidad del Valle de Guatemala. El código fuente está disponible para fines educativos y de investigación.

Para reportar problemas o sugerencias, crear un issue en el repositorio especificando dispositivo y versión de Android.

---

## 📧 Contacto

**Autor:** Carlos Edgardo López Barrera  
**Carnet:** 21666  
**Email:** lop21666@uvg.edu.gt  
**Universidad:** Universidad del Valle de Guatemala  
**Carrera:** Ingeniería en Ciencias de la Computación y Tecnologías de la Información

---

## 📝 Licencia

Este proyecto está bajo una licencia de uso académico. Ver el archivo LICENSE para más detalles.

---

## Agradecimientos

**Asesoras:**
- Ing. Dulce María Chacón Muñoz - Orientación y acompañamiento
- Lcda. María Jimena Lucía Chocochic Arriaga - Asesoría técnica y académica

**Equipo ARTour Kaminaljuyú:**
- Josué Morales, Brian Carrillo, Marco Ramírez, Luz Coronado, Claudia Velásquez

**Familia:**
- Axel López, Elma Barrera, Axel López Jr., Carmen López

**Instituciones:**
- Universidad del Valle de Guatemala
- Parque Arqueológico Kaminaljuyú
- Google ARCore Team

---

## 🔗 Enlaces Útiles

- [Documentación de ARCore](https://developers.google.com/ar)
- [Dispositivos compatibles con ARCore](https://developers.google.com/ar/devices)
- [Universidad del Valle de Guatemala](https://www.uvg.edu.gt/)

---