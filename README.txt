# INASsoftware_1°C_2026_Jordi_Steven_Menendez_Orellana
Repo creado para actividad con profesora Reina Cruz 

# Ferretería Don Toño — E-Commerce PWA & AI Platform 🛠️

<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=auto&height=200&section=header&text=Ferreteria%20Don%20Tono&fontSize=42&animation=fadeIn)

<img src="Logo_FDT.png" alt="Ferretería Don Toño Logo" width="220" style="border-radius:16px;"/>

### 🚀 Plataforma Web E-Commerce, PWA, Visor 3D y Asistente con IA
📍 **El Salvador** | 💻 **Vertex Lab** (Instituto Nacional de Apopa - INAS)

[![Demo en Vivo](https://img.shields.io/badge/Demo_en_Vivo-PythonAnywhere-brightgreen?style=for-the-badge&logo=pythonanywhere&logoColor=white)](https://ferrolibreriateriadonantonio.pythonanywhere.com/)
[![Django](https://img.shields.io/badge/Django-5.2-092E20?style=for-the-badge&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![Next.js](https://img.shields.io/badge/Next.js-App_Router-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![Estado](https://img.shields.io/badge/Estado-Producci%C3%B3n-success?style=for-the-badge)]()

</div>

---

### 🧰 Tech Stack & Tools

#### **Backend & Databases**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

#### **Frontend & 3D Graphics**
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)

#### **AI Systems & Web Integrations**
![Groq API](https://img.shields.io/badge/Groq_AI-F05032?style=for-the-badge&logo=openai&logoColor=white)
![Web Push](https://img.shields.io/badge/Web_Push_VAPID-380556?style=for-the-badge&logo=pwa&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

### 📌 About The Project

- 🌐 **E-Commerce local adaptado a El Salvador:** Sistema integral diseñado para agilizar la venta e inventariado de herramientas y productos ferreteros.
- 🤖 **Agente dual inteligente "Toñito IA":** Respuestas en tiempo real para clientes con consulta de stock e interacción por comandos avanzados en el panel de administración.
- 🎨 **Simulador y Calculadora de Pinturas:** Módulo interactivo con cálculo automático de rendimiento por $m^2$ para 5 presentaciones y control de inventario por color y tamaño.
- 📦 **Catálogo 3D e Interactivo:** Modelos tridimensionales `.glb` con soporte gestual 360°, selector de cantidades y carrito en tiempo real.
- 🧾 **Cumplimiento Fiscal Salvadoreño:** Procesamiento con Factura de Consumidor Final (DUI/NIT) y Crédito Fiscal (CCF con validación obligatoria de NIT + NRC).

---

### 🚀 Key Features & Modules

| Módulo / Característica | Descripción | Tech Stack |
| :--- | :--- | :--- |
| **🤖 Agentes Inteligentes "Toñito IA"** | **Clientes:** Búsqueda conversacional, productos equivalentes e interacción interactiva `[BUSCAR_ESTANTES]`.<br>**Admin:** Gestión masiva de stock, creación de productos, reportes contables y acciones rápidas. | `Groq API` `Django REST` `Python` |
| **🎨 Calculadora & Simulador de Pinturas** | Estimación exacta por área ($m^2$), 27 swatches de color y gestión multidimensional de stock por **Tamaño + Color**. | `JavaScript` `Django ORM` `Tailwind` |
| **📦 Catálogo 3D (`/estantes/`)** | Modelos 3D interactivos con `<model-viewer>`, pestañas dinámicas (*Promociones*, *Nuevos*, *Más Vendidos*) y sincronización directa con el carrito. | `Next.js App Router` `Three.js` |
| **🧾 Checkout & Módulo Fiscal SV** | Facturación adaptada a la normativa fiscal de El Salvador: Factura (NIT/DUI) y Crédito Fiscal (NIT + NRC obligatorio). Generación de estructura DTE en JSON. | `Django Forms` `JSONField` |
| **🔔 Push Notifications & Excel Reports** | Sistema de alertas VAPID en tiempo real para avisos de stock agotado y exportación de reportes de ventas anuales/mensuales en Excel. | `pywebpush` `VAPID` `openpyxl` |

---

### 👥 Development Team — Vertex Lab

<div align="center">

Proyecto desarrollado colaborativamente por el equipo **Vertex Lab** (Instituto Nacional de Apopa):

| Integrante | Rol / Área de Contribución |
| :--- | :--- |
| **Jordi Steven Menéndez Orellana** | Full-Stack Developer & Arquitectura de Software |
| **Anthony Alexander** | Software Developer |
| **Joan** | Software Developer |
| **Emanuel** | Software Developer |
| **Alexandra Gallegos** | Software Developer |
| **Jason** | Software Developer |
| **Marcos Estrada** | Software Developer |

</div>

---

### 📁 Project Structure

```text
FerreteriaDontonoGeneral/
├── logo_fdt.svg               # Vector del logotipo oficial
├── Logo_FDT.png               # Isotipo en formato PNG
├── sembrar_pinturas.py        # Script de inicialización de catálogo de pinturas
├── manage.py                  # CLI de administración de Django
├── Ferreteria/                # Configuración principal del proyecto
│   ├── settings.py            # Variables de entorno y ajustes generales
│   ├── urls.py                # Enrutador general de rutas
│   └── wsgi.py                # Servidor de despliegue en producción
└── tienda/                    # App principal del sistema
    ├── models.py              # Modelos de BD (Productos, Pinturas, Notificaciones, Pedidos)
    ├── views.py               # Lógica de endpoints, Checkout y APIs REST
    ├── reportes_ventas.py     # Generador de reportes contables en Excel
    ├── signals.py             # Disparadores para stock y notificaciones PWA
    ├── static/                # Assets, estilos CSS custom y JS vanilla
    └── templates/             # Plantillas HTML (index, pinturas, checkout, admin custom)
```

---

### ⚙️ Installation & Local Setup

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/JordiSteven/FerreteriaDontonoGeneral.git
   cd FerreteriaDontonoGeneral
   ```

2. **Crear y activar el entorno virtual:**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate

   # Linux / macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configurar variables de entorno (`.env`):**
   ```env
   SECRET_KEY=tu_clave_secreta_django
   GROQ_API_KEY=tu_api_key_groq_clientes
   GROQ_API_KEY_ADMIN=tu_api_key_groq_admin
   WEBPUSH_VAPID_PUBLIC_KEY=tu_clave_publica_vapid
   WEBPUSH_VAPID_PRIVATE_KEY=ruta_o_clave_privada_pem
   WEBPUSH_VAPID_ADMIN_EMAIL=tu_correo_admin@dominio.com
   ```

5. **Ejecutar migraciones y datos iniciales:**
   ```bash
   python manage.py migrate
   python manage.py shell < sembrar_pinturas.py
   python manage.py createsuperuser
   ```

6. **Iniciar servidor local:**
   ```bash
   python manage.py runserver
   ```
   Accede a [http://127.0.0.1:8000/](http://127.0.0.1:8000/) en tu navegador.

---

<div align="center">

🌐 **[Visitar Proyecto en Vivo](https://ferrolibreriateriadonantonio.pythonanywhere.com/)**

***"Innovación tecnológica aplicada al comercio local salvadoreño."*** 🇸🇻💡

</div>