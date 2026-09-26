# JDot 🚀

**JDot** es un motor de animación 3D enfocado en educación, simulaciones físicas y desarrollo de videojuegos, diseñado con una interfaz unificada e implementado sobre la plataforma de alto rendimiento **GraalVM** utilizando el framework Truffle.

El proyecto simplifica la creación de experiencias interactivas y simulación gráfica mediante una API limpia e intuitiva, mientras aprovecha el compilador JIT de GraalVM para ejecutar cálculos cinemáticos, físicas de partículas y algoritmos de animación a velocidades cercanas al código nativo, manteniendo compatibilidad total con clientes web modernos vía WebGL y WebGPU.

---

## 🌟 Características Principales

* **Interfaz Unificada para Animación y Juegos:** API simplificada orientada a objetos que abstrae la complejidad de la física, la cinemática inversa y la jerarquía de transformaciones 3D.
* **Cálculo Físico y Matemático Acelerado por JIT:** Optimización dinámica de bucles de simulación, detección de colisiones e interpolación de fotogramas (*keyframing*) sobre el AST de Truffle.
* **Interoperabilidad Políglota de Cero Copia:** Capacidad para integrar lógica de simulación o IA escrita en Python, Java, JavaScript, Ruby o C/C++ en el mismo bucle de renderizado sin sobrecostes de transporte.
* **Pipeline Web Scalable & Headless:** Generación directa de buffers de geometría para WebGL/WebGPU y soporte de ejecución *headless* en servidor para renderizado de animaciones en la nube o pruebas automatizadas.

---

## 🏗️ Arquitectura de la Plataforma

* **JDot Animation Core Engine:** Motor de tiempo de ejecución implementado con nodos Truffle especializado en árboles de comportamiento, esqueletos de animación y grafos de escena 3D.
* **Physics & Math Runtime:** Módulo de álgebra lineal y simulación de cuerpos rígidos optimizado para instrucciones vectoriales (SIMD/AVX) por el compilador JIT de GraalVM.
* **Web Native Exporter / Bridge:** Capa de comunicación binaria y serialización que envía la información del grafo de escena hacia clientes web HTML5 en tiempo real.

---

## 🚦 Inicio Rápido

### Prerrequisitos

* **GraalVM JDK** (versión 21 o superior) con componentes Truffle habilitados.
* Variable de entorno `JAVA_HOME` apuntando a la instalación de GraalVM.

### Instalación

```bash
# Clonar el repositorio
git clone [https://github.com/tu-usuario/jdot.git](https://github.com/tu-usuario/jdot.git)
cd jdot

# Construir el motor y las herramientas CLI con Gradle
./gradlew build
