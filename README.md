<div align="center">

# 🏥 Visor DICOM - ASTRAI EAFIT

### *Visualización médica de siguiente generación*

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://www.javascript.com/)
[![DICOM](https://img.shields.io/badge/DICOM-Standard-blue.svg)](https://www.dicomstandard.org/)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

<img src="https://via.placeholder.com/800x400/1a1a2e/16c79a?text=Visor+DICOM+ASTRAI+EAFIT" alt="Banner" width="100%"/>

*Un visor DICOM moderno, intuitivo y potente para la visualización y análisis de imágenes médicas*

[🚀 Demo](#-demo) • [📦 Instalación](#-instalación) • [📖 Documentación](#-uso) • [🤝 Contribuir](#-contribución)

</div>

---

## ✨ Características Principales

<table>
<tr>
<td width="50%">

### 🖼️ Visualización Avanzada
- ✅ Carga rápida de archivos DICOM
- ✅ Zoom fluido con interpolación
- ✅ Paneo suave y responsivo
- ✅ Rotación en tiempo real
- ✅ Inversión de colores

</td>
<td width="50%">

### 🔧 Herramientas Profesionales
- ✅ Medición de distancias (mm)
- ✅ Medición de ángulos (°)
- ✅ Anotaciones personalizables
- ✅ Windowing dinámico
- ✅ Presets por modalidad

</td>
</tr>
<tr>
<td width="50%">

### 📊 Análisis Inteligente
- ✅ Metadatos DICOM completos
- ✅ Información del paciente
- ✅ Historial de mediciones
- ✅ Estadísticas de imagen
- ✅ Exportación de datos

</td>
<td width="50%">

### 💻 Experiencia de Usuario
- ✅ Interfaz moderna y limpia
- ✅ Atajos de teclado
- ✅ Drag & Drop
- ✅ Responsive design
- ✅ Sin instalación requerida

</td>
</tr>
</table>

---

## 🎯 Demo

```bash
# Prueba rápida sin instalación
npx http-server
# Navega a http://localhost:8080
```

<div align="center">
<img src="https://via.placeholder.com/600x350/0f3460/16c79a?text=Vista+Principal" alt="Screenshot"/>
</div>

---

## 📦 Instalación

### 🚀 Inicio Rápido (Recomendado)

```bash
# 1. Clona el repositorio
git clone https://github.com/ASTRAI-EAFIT/visor-dicom.git

# 2. Navega al directorio
cd visor-dicom

# 3. Inicia el servidor
python -m http.server 8000
# O con Node.js
npx http-server -p 8000

# 4. Abre tu navegador
# → http://localhost:8000
```

### 🐳 Con Docker

```bash
docker build -t visor-dicom .
docker run -p 8080:80 visor-dicom
```

### 📥 Descarga Directa

Descarga la última versión desde [Releases](https://github.com/ASTRAI-EAFIT/visor-dicom/releases)

---

## 🎨 Uso

### 1️⃣ Carga de Imágenes

<table>
<tr>
<td width="33%">

**🖱️ Drag & Drop**
```
Arrastra tu archivo
.dcm a la ventana
```

</td>
<td width="33%">

**📁 Selector de Archivos**
```
Click en "Cargar DICOM"
Selecciona tu archivo
```

</td>
<td width="33%">

**⌨️ Atajo**
```
Ctrl + O
(Cmd + O en Mac)
```

</td>
</tr>
</table>

### 2️⃣ Herramientas Interactivas

#### 🪟 Ajuste de Ventana (Windowing)

| Acción | Control |
|--------|---------|
| Ajustar Brillo | 🖱️ Arrastrar verticalmente |
| Ajustar Contraste | 🖱️ Arrastrar horizontalmente |
| Presets Rápidos | 🔘 Panel lateral |

**Presets Disponibles:**
- 🫀 **Abdomen**: W:400, L:50
- 🧠 **Cerebro**: W:80, L:40  
- 🫁 **Pulmón**: W:1500, L:-600
- 🦴 **Hueso**: W:2000, L:300

#### 🔍 Zoom y Navegación

```
🖱️ Scroll           → Zoom In/Out
🖱️ Click Derecho    → Paneo (arrastrar)
🖱️ Doble Click      → Ajustar al visor
⌨️  +/-              → Zoom incremental
⌨️  0                → Reset
```

#### 📏 Mediciones

<table>
<tr>
<th>Herramienta</th>
<th>Uso</th>
<th>Resultado</th>
</tr>
<tr>
<td>📐 Distancia</td>
<td>Click en 2 puntos</td>
<td>Medida en mm</td>
</tr>
<tr>
<td>📊 Ángulo</td>
<td>Click en 3 puntos</td>
<td>Ángulo en grados</td>
</tr>
<tr>
<td>✏️ Anotación</td>
<td>Click y escribe</td>
<td>Texto sobre imagen</td>
</tr>
</table>

#### ⚙️ Transformaciones

```javascript
// Atajos de teclado
R  →  Rotar 90° (horario)
I  →  Invertir colores
H  →  Voltear horizontal
V  →  Voltear vertical
Esc → Cancelar herramienta actual
```

---

## 🏗️ Arquitectura del Proyecto

```
📦 visor-dicom-astrai-eafit/
┣ 📂 src/
┃ ┣ 📂 js/
┃ ┃ ┣ 📜 dicomParser.js      # Parser DICOM optimizado
┃ ┃ ┣ 📜 imageRenderer.js    # Motor de renderizado
┃ ┃ ┣ 📜 tools.js             # Herramientas de medición
┃ ┃ ┣ 📜 windowLevel.js       # Control de ventana
┃ ┃ ┗ 📜 utils.js             # Utilidades y helpers
┃ ┣ 📂 css/
┃ ┃ ┣ 📜 main.css             # Estilos principales
┃ ┃ ┗ 📜 components.css       # Componentes UI
┃ ┗ 📂 assets/
┃   ┣ 🎨 icons/               # Iconos SVG
┃   ┗ 🖼️ images/             # Recursos gráficos
┣ 📂 libs/
┃ ┣ 📚 cornerstone/           # Cornerstone.js v2.6
┃ ┗ 📚 dicomParser/           # dicomParser v1.8
┣ 📜 index.html               # Punto de entrada
┣ 📜 app.js                   # Aplicación principal
┣ 📜 package.json             # Dependencias npm
┣ 📜 README.md                # Esta documentación
┗ 📜 LICENSE                  # Licencia MIT
```

---

## 🔬 Stack Tecnológico

<div align="center">

| Categoría | Tecnología |
|-----------|-----------|
| **Frontend** | ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat&logo=css3) ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black) |
| **Visualización** | ![Cornerstone](https://img.shields.io/badge/-Cornerstone.js-4A90E2?style=flat) ![Canvas](https://img.shields.io/badge/-Canvas_API-FF6B6B?style=flat) |
| **DICOM** | ![dicomParser](https://img.shields.io/badge/-dicomParser-00B4D8?style=flat) |
| **Build Tools** | ![Webpack](https://img.shields.io/badge/-Webpack-8DD6F9?style=flat&logo=webpack) (opcional) |

</div>

---

## 💡 Casos de Uso

<table>
<tr>
<td width="33%" align="center">

### 🎓 Educación
Ideal para estudiantes de medicina y radiología

</td>
<td width="33%" align="center">

### 🔬 Investigación
Análisis de imágenes para papers y estudios

</td>
<td width="33%" align="center">

### 🏥 Clínica
Revisión rápida de estudios (no diagnóstico)

</td>
</tr>
</table>

---

## 📊 Compatibilidad

### ✅ Navegadores Soportados

| Navegador | Versión Mínima | Status |
|-----------|----------------|--------|
| Chrome | 90+ | ✅ Soportado |
| Firefox | 88+ | ✅ Soportado |
| Safari | 14+ | ✅ Soportado |
| Edge | 90+ | ✅ Soportado |
| Opera | 76+ | ⚠️ Parcial |

### 📁 Formatos DICOM

- ✅ Implicit VR Little Endian
- ✅ Explicit VR Little Endian
- ✅ Profundidad: 8, 12, 16 bits
- ✅ Modalidades: CT, MR, CR, DX, US, XA
- ⚠️ DICOM comprimido (en desarrollo)

---

## 🚀 Roadmap

### 🎯 Versión 1.0 (Actual)
- [x] Visualización básica DICOM
- [x] Herramientas de medición
- [x] Windowing manual y presets
- [x] Interfaz responsive

### 🔮 Versión 2.0 (En desarrollo)
- [ ] Soporte multi-series
- [ ] Visualización MPR (3D)
- [ ] Herramientas de segmentación
- [ ] Exportación PNG/JPEG
- [ ] Anotaciones persistentes

### 🌟 Versión 3.0 (Futuro)
- [ ] Integración con PACS
- [ ] DICOM Web (WADO, QIDO, STOW)
- [ ] Colaboración en tiempo real
- [ ] IA para detección automática
- [ ] Aplicación móvil nativa

---

## 🤝 Contribución

¡Las contribuciones son bienvenidas! Sigue estos pasos:

### 1. Fork el proyecto
```bash
# Click en "Fork" en GitHub
```

### 2. Crea tu rama
```bash
git checkout -b feature/MiNuevaCaracteristica
```

### 3. Realiza cambios
```bash
git add .
git commit -m "✨ Agrega nueva característica increíble"
```

### 4. Push a tu fork
```bash
git push origin feature/MiNuevaCaracteristica
```

### 5. Abre un Pull Request
Describe claramente tus cambios y el problema que resuelven

---

## 📝 Guía de Estilos

```javascript
// ✅ Bueno
function cargarImagenDICOM(archivo) {
  if (!archivo) return null;
  return parseadorDICOM.parsear(archivo);
}

// ❌ Evitar
function load(f) {
  return parser.parse(f);
}
