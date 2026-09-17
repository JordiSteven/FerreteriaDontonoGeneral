FerreteriaDontonoGeneral
<div align="center">
.
  <img src="logo_fdt.svg" alt="Ferretería Don Toño Logo" width="280"/>

  # 🛠️ Ferretería Don Toño — E-Commerce & PWA

  **Plataforma web integral de comercio electrónico, PWA, renderizado 3D y asistencia con IA para el sector ferretero en El Salvador.**

  [![Demo en Vivo](https://img.shields.io/badge/Demo_en_Vivo-PythonAnywhere-brightgreen?style=for-the-badge&logo=pythonanywhere&logoColor=white)](https://ferrolibreriateriadonantonio.pythonanywhere.com/)
  [![Django](https://img.shields.io/badge/Django-5.2-092E20?style=for-the-badge&logo=django&logoColor=white)](https://www.djangoproject.com/)
  [![Next.js](https://img.shields.io/badge/Next.js-App_Router-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
  [![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
  [![Groq AI](https://img.shields.io/badge/Groq-AI_LLM-orange?style=for-the-badge&logo=openai&logoColor=white)](https://groq.com/)
  [![Estado](https://img.shields.io/badge/Estado-Producci%C3%B3n-success?style=for-the-badge)]()

</div>

---

### 🌐 Demo en Vivo

Puedes acceder a la plataforma desplegada en producción a través del siguiente enlace:  
👉 **[https://ferrolibreriateriadonantonio.pythonanywhere.com/](https://ferrolibreriateriadonantonio.pythonanywhere.com/)**

---

### 🧰 Tech Stack & Herramientas

#### **Backend & Base de Datos**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

#### **Frontend & Renderizado 3D**
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Model Viewer](https://img.shields.io/badge/3D_Model_Viewer-000000?style=for-the-badge&logo=three.js&logoColor=white)

#### **Inteligencia Artificial & Integraciones PWA**
![Groq API](https://img.shields.io/badge/Groq_API-F05032?style=for-the-badge&logo=openai&logoColor=white)
![Web Push](https://img.shields.io/badge/Web_Push_VAPID-380556?style=for-the-badge&logo=pwa&logoColor=white)
![Service Workers](https://img.shields.io/badge/PWA_Service_Workers-5B067D?style=for-the-badge&logo=pwa&logoColor=white)

---

### 🚀 Funcionalidades Destacadas

| Módulo / Característica | Descripción | Stack Tecnológico |
| :--- | :--- | :--- |
| **🤖 Agentes Inteligentes "Toñito IA"** | **Clientes (`gpt-oss-20b`):** Asistente conversacional inyectado con inventario en tiempo real, búsqueda de equivalencias y redirección interactiva `[BUSCAR_ESTANTES]`.<br>**Admin (`gpt-oss-120b`):** Agente de gestión masiva de stock, creación de ítems, reportes fiscales y comandos por voz/chat. | `Groq LLM API` `Python` `Django REST` |
| **🎨 Simulador & Calculadora de Pinturas (`/pinturas/`)** | Estimación automática de rendimiento por $m^2$ para 5 presentaciones (1L, 1/4 Galón, 1/2 Galón, Galón, Cubeta 5 Gal). Control multidimensional de inventario por **Tamaño + Color** (27 swatches). | `JavaScript` `Django ORM` `Tailwind` |
| **📦 Catálogo 3D e Interactivo (`/estantes/`)** | Modelos `.glb` interactivos con 360°, soporte táctil/gestual, pestañas de filtrado dinámico (*Promociones*, *Nuevos*, *Más Vendidos*) y carrito synchronizado. | `Next.js App Router` `<model-viewer>` |
| **🧾 Checkout & Cumplimiento Fiscal SV** | Procesamiento de órdenes adaptado a la normativa fiscal de El Salvador: **Factura de Consumidor Final** (NIT o DUI) y **Comprobante de Crédito Fiscal (CCF)** (valida obligatoriamente NIT + NRC). Generación de JSON tipo DTE. | `Django Forms` `JSONField` |
| **🔔 Push Notifications & Reportes Excel** | Sistema de alertas VAPID en tiempo real para productos agotados dirigidas al staff. Carga masiva de catálogo desde plantillas `.xlsx` e historial de ventas desglosado. | `pywebpush` `VAPID` `openpyxl` |

---

### 📁 Estructura del Proyecto

```text
Ferreteria/                        # Raíz del proyecto (Django) — /home/.../Ferreteria en PythonAnywhere
├── manage.py                      # CLI de administración de Django
├── wsgi.py                        # WSGI de producción (PythonAnywhere)
├── sembrar_pinturas.py            # Script de siembra del catálogo de pinturas
├── crear_productos.py             # Scripts de carga de datos iniciales
├── crear_productos_3d.py
├── asignar_categorias.py
├── asignar_categorias_v2.py
├── ferreteria/                    # Configuración principal del proyecto
│   ├── settings.py                # Variables de entorno y ajustes generales
│   ├── urls.py                    # Enrutador general de rutas
│   └── wsgi.py                    # Entry point WSGI
├── tienda/                        # App principal del sistema
│   ├── models.py                  # Modelos de BD (Productos, Pinturas, Notificaciones, Pedidos)
│   ├── views.py                   # Lógica de endpoints, Checkout y APIs REST
│   ├── admin.py                   # Configuración del panel de administración
│   ├── urls.py                    # Rutas de la app tienda
│   ├── signals.py                 # Disparadores para stock y notificaciones PWA
│   ├── notificaciones.py          # Lógica de notificaciones push y stock agotado
│   ├── reportes_ventas.py         # Generador de reportes contables en Excel
│   ├── migrations/                # Migraciones de la base de datos
│   ├── templates/tienda/          # Plantillas HTML (index, pinturas, estantes, admin custom)
│   │   ├── index.html
│   │   ├── pinturas.html
│   │   ├── estantes.html
│   │   ├── agregar_producto.html
│   │   └── _tonito_widget.html
│   ├── static/                    # PWA (sw.js, manifest, icons) + imágenes de productos
│   └── estantes_assets/           # Build estático Next.js para /estantes/ — _next/, images/, seo/
├── templates/admin/               # Overrides del admin de Django (tema amarillo/dorado)
└── static/                        # Assets globales + admin_custom (CSS del tema)
```

---

### 🚀 Instalación y Configuración Local

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/JordiSteven/FerreteriaDontonoGeneral.git
   cd FerreteriaDontonoGeneral
   ```

2. **Crear y activar entorno virtual:**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate

   # Linux / macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Instalar dependencias de Python:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configurar Variables de Entorno (`.env`):**
   ```env
   SECRET_KEY=tu_clave_secreta_django
   GROQ_API_KEY=tu_api_key_groq_clientes
   GROQ_API_KEY_ADMIN=tu_api_key_groq_admin
   WEBPUSH_VAPID_PUBLIC_KEY=tu_clave_publica_vapid
   WEBPUSH_VAPID_PRIVATE_KEY=ruta_o_clave_privada_pem
   WEBPUSH_VAPID_ADMIN_EMAIL=tu_correo_admin@dominio.com
   ```

5. **Migraciones e Inserción de Datos:**
   ```bash
   python manage.py migrate
   python manage.py shell < sembrar_pinturas.py
   python manage.py createsuperuser
   ```

6. **Ejecutar el servidor de desarrollo:**
   ```bash
   python manage.py runserver
   ```
   Abre [http://127.0.0.1:8000/](http://127.0.0.1:8000/) en tu navegador.

---

### 👥 Equipo de Desarrollo — Vertex Lab

<div align="center">

Este proyecto fue ideado, diseñado y desarrollado por el equipo de **Vertex Lab**:

| Integrante | Código | Rol |
| :--- | :--- | :--- |
| *Jordi Steven Menéndez Orellana* | 1C-26 | Sublíder y Programador |
| *Anthony Alexander Hernández Arias* | 1C-16 | Líder y Programador |
| *Marcos Isaías Estrada López* | 1C-07 | Diseñador |
| *Jason Gabriel Flores Alas* | 1C-08 | Programador |
| *Alexandra Elizabeth López Ávalos* | 1C-20 | Investigadora |
| *Anthony Joan Méndez Pérez* | 1C-25 | Diseñador 2 |
| *Emanuel Abraham Villegas Barrera* | 1C-41 | Analista |

</div>

---

### 📄 Licencia

Este proyecto está distribuido bajo la licencia **MIT**. Consulta el archivo `LICENSE` para obtener más información.

---

<div align="center">

***"Innovación tecnológica aplicada al comercio local salvadoreño."*** 🇸🇻💡

</div>
