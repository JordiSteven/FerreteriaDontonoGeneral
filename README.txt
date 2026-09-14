# Ferretería & Librería Don Toño — E-Commerce PWA

<div align="center">

  <img src="logo_FDT.svg" alt="Ferretería Don Toño Logo" width="280"/>

  ### 🏗️ Plataforma Web E-Commerce con IA, Visor 3D & Simulador de Pinturas
  
  [![Demo en Vivo](https://img.shields.io/badge/Demo_en_Vivo-PythonAnywhere-yellow?style=for-the-badge&logo=pythonanywhere&logoColor=black)](https://ferrolibreriateriadonantonio.pythonanywhere.com/)
  [![Estado](https://img.shields.io/badge/Estado-Producci%C3%B3n-success?style=for-the-badge)]()
  [![Equipo](https://img.shields.io/badge/Equipo-Vertex_Lab-blue?style=for-the-badge)]()

</div>

---

### 🧰 Tech Stack & Herramientas

#### **Backend & Base de Datos**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django_5.2-092E20?style=for-the-badge&logo=django&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

#### **Frontend & Renderizado 3D**
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)

#### **Inteligencia Artificial & Integraciones**
![Groq API](https://img.shields.io/badge/Groq_API-F05032?style=for-the-badge&logo=openai&logoColor=white)
![Web Push](https://img.shields.io/badge/Web_Push_VAPID-380556?style=for-the-badge&logo=pwa&logoColor=white)

---

### 🚀 Funcionalidades Principales

| Módulo | Descripción | Tecnología Clave |
| :--- | :--- | :--- |
| **🤖 Toñito IA (Clientes & Admin)** | Asistente virtual dual. Resuelve dudas de inventario en tiempo real para clientes y ejecuta comandos de gestión/ajuste de stock para administradores. | `Groq API` `LLM` |
| **🎨 Sistema de Pinturas** | Calculadora de litros/galones, simulador visual interactivo de color y control de stock independiente por combinación de tamaño y color. | `JavaScript` `Django ORM` |
| **📦 Catálogo 3D & `/estantes/`** | Visualización interactiva de herramientas en 3D (`.glb`), soporte para gestos táctiles y filtrado dinámico por pestañas. | `Next.js` `<model-viewer>` |
| **🧾 Facturación SV & Checkout** | Proceso de compra con desglose de IVA (13%), compatibilidad con Factura y Crédito Fiscal según normativa de El Salvador (NIT, DUI, NRC). | `Django Forms` `JSONField` |
| **📊 Carga Masiva & Reportes** | Importación masiva de productos desde archivos `.xlsx` y generación automática de reportes de ventas anuales/mensuales en Excel. | `openpyxl` `Signals` |
| **🔔 Notificaciones Push** | Alertas en tiempo real sobre productos agotados para el personal de administración. | `pywebpush` `VAPID` |

---

### 🏗️ Arquitectura del Proyecto

```text
FerreteriaDontonoGeneral/
├── tienda/                       # App principal de Django (Backend & Vistas)
│   ├── templates/tienda/         # Vistas HTML (Home, /pinturas/, Checkout)
│   ├── models.py                 # Modelos (Productos, Pinturas, Notificaciones, Pedidos)
│   ├── views.py                  # Lógica de APIs y procesamiento de pagos
│   ├── reportes_ventas.py        # Generación dinámica de reportes Excel
│   └── signals.py                # Disparadores de stock y notificaciones
├── static/                       # Assets estáticos, CSS personalizado y JS vanilla
├── logo_fdt.svg                  # Isologotipo oficial vectorial
└── manage.py                     # Script de gestión de Django