<div align="center">
<img src="logo_fdt.svg" alt="Ferretería Don Toño Logo" width="280"/>
🛠️ Ferretería Don Toño — E-Commerce & PWA
Plataforma web de comercio electrónico, PWA y asistencia impulsada por Inteligencia Artificial para el sector ferretero en El Salvador.
![Live Demo](https://img.shields.io/badge/Demo-En%20Vivo-brightgreen?style=for-the-badge&logo=pythonanywhere)
![Django](https://img.shields.io/badge/Django-5.2-092E20?style=for-the-badge&logo=django)
![Next.js](https://img.shields.io/badge/Next.js-App%20Router-000000?style=for-the-badge&logo=next.js)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css)
![Groq AI](https://img.shields.io/badge/Groq-AI%20LLM-orange?style=for-the-badge)
</div>
---
🌐 Demo en Vivo
Puedes explorar la aplicación desplegada en producción a través del siguiente enlace:
👉 Visitar Ferretería Don Toño
---
📌 Sobre el Proyecto
Ferretería Don Toño es una solución digital integral diseñada para modernizar la experiencia de compra de herramientas, pinturas y materiales de construcción. Combina una arquitectura robusta en el backend con tecnologías frontend modernas y de renderizado 3D, ofreciendo además asistentes inteligentes contextuales impulsados por modelos LLM para clientes y administradores.
---
✨ Funcionalidades Principales
🤖 1. Agentes Inteligentes "Toñito IA" (Groq LLM)
Toñito Clientes (`openai/gpt-oss-20b`): Asistente de ventas inyectado con el catálogo real en tiempo real. Soporta búsqueda dinámica, sugerencia de equivalencias de productos, agregado automático de ítems al carrito y redirección inteligente a estantes interactivos mediante marcadores `[BUSCAR_ESTANTES]`.
Toñito Admin (`openai/gpt-oss-120b`): Agente de gestión integrado en el panel administrativo (`/admin/`). Permite la actualización masiva de stock, creación de productos, generación de reportes fiscales, consultas estadísticas y cambio de tema claro/oscuro por voz/chat.
🎨 2. Módulo de Pinturas y Calculadora de Áreas (`/pinturas/`)
Calculadora de Consumo: Estimación de material según el área en $m^2$ para 5 presentaciones estándar de la industria (1L, Cuarto de Galón, Medio Galón, Galón y Cubeta de 5 Galones).
Control de Inventario Multidimensional: Gestión independiente de stock por combinación única de Tamaño + Color (27 colores disponibles con swatches interactivos).
📦 3. Catálogo 3D e Interactivo (`/estantes/`)
Modelos 3D Interactivos: Integración con `<model-viewer>` para visualización de productos clave en 360° y realidad aumentada.
Micro-Frontend en Next.js: Interfaz optimizada con soporte gestual/táctil, filtrado dinámico por pestañas (Promociones, Nuevos, Más Vendidos) y carrito de compras sincronizado.
🧾 4. Checkout y Cumplimiento Fiscal (El Salvador)
Documentación Fiscal Real: Soporte legal salvadoreño para Factura de Consumidor Final (NIT o DUI) y Comprobante de Crédito Fiscal (CCF) (valida obligatoriamente NIT + NRC).
Simulación DTE: Generación automática de comprobantes, envío de resúmenes desglosados (Subtotal, IVA 13% y Total) por correo electrónico y exportación de estructuras JSON fiscales.
🔔 5. Notificaciones PWA & Administración
Web Push (VAPID): Sistema de notificaciones en tiempo real para alertas de inventario agotado enviadas al personal administrativo.
Carga Masiva Excel: Importación de catálogo desde plantillas `.xlsx` con validación y actualización omnicanal (`update_or_create`).
Reportes Internos: Exportación de libros de ventas en Excel desglosados por meses, días, horas con mayor flujo y productos más vendidos.
---
🛠️ Stack Tecnológico
Capa	Tecnologías
Backend	Python 3.12, Django 5.2, SQLite3
Frontend Principal	HTML5, JavaScript Vanilla, Tailwind CSS
Frontend Estantes	Next.js (App Router, Export Estático)
Inteligencia Artificial	Groq API (`gpt-oss-20b` / `gpt-oss-120b`)
Visualización 3D	Google `<model-viewer>`, FontAwesome Icons
PWA & Push	Web Push API, `py-vapid`, Service Workers
Infraestructura	Hosting en PythonAnywhere
---
📁 Estructura del Repositorio
```text
FerreteriaDontonoGeneral/
├── logo_fdt.svg               # Logo vectorizado oficial del proyecto
├── Logo_FDT.png               # Isotipo/Logo en formato PNG
├── .gitattributes             # Configuración de atributos Git
├── sembrar_pinturas.py        # Script de inicialización de inventario de pinturas
├── manage.py                  # CLI de Django
├── Ferreteria/                # Configuración principal del proyecto Django
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── tienda/                    # Aplicación core de e-commerce
    ├── models.py              # Modelos (Producto, Pedido, ColorPintura, etc.)
    ├── views.py               # Endpoints API y vistas renderizadas
    ├── reportes_ventas.py     # Generador de reportes Excel
    ├── static/                # Assets estáticos (CSS custom admin, JS, imágenes)
    └── templates/             # Plantillas HTML (index, pinturas, admin custom)
```
---
🚀 Guía de Instalación y Configuración Local
Prerrequisitos
Python 3.10+
Node.js 18+ (opcional, para desarrollo frontend en `/estantes/`)
Git
Paso 1: Clonar el repositorio
```bash
git clone https://github.com/TuUsuario/FerreteriaDontonoGeneral.git
cd FerreteriaDontonoGeneral
```
Paso 2: Crear y activar entorno virtual
```bash
# En Windows:
python -m venv venv
venv\Scripts\activate

# En Linux / macOS:
python3 -m venv venv
source venv/bin/activate
```
Paso 3: Instalar dependencias de Python
```bash
pip install -r requirements.txt
```
Paso 4: Variables de Entorno
Crea un archivo `.env` en la raíz del proyecto o configura tus variables de entorno con las siguientes claves:
```env
SECRET_KEY=tu_clave_secreta_django
GROQ_API_KEY=tu_api_key_groq_clientes
GROQ_API_KEY_ADMIN=tu_api_key_groq_admin
WEBPUSH_VAPID_PUBLIC_KEY=tu_vapid_public_key
WEBPUSH_VAPID_PRIVATE_KEY=ruta_o_clave_privada_pem
WEBPUSH_VAPID_ADMIN_EMAIL=tu_correo_admin@dominio.com
```
Paso 5: Migraciones e Inserción de Datos Iniciales
```bash
python manage.py migrate
python manage.py shell < sembrar_pinturas.py
python manage.py createsuperuser
```
Paso 6: Iniciar Servidor de Desarrollo
```bash
python manage.py runserver
```
Accede a la aplicación en tu navegador en `http://127.0.0.1:8000/`.
---
👥 Equipo de Desarrollo — Vertex Lab
Este proyecto fue ideado, diseñado y desarrollado por el equipo de Vertex Lab:
👨‍💻 Jordi Menéndez
👨‍💻 Anthony Alexander
👨‍💻 Joan
👨‍💻 Emanuel
👩‍💻 Alexandra Gallegos
👨‍💻 Jason
👨‍💻 Marcos Estrada
---
📄 Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para obtener más información.
---
<div align="center">
  <sub>Desarrollado con ❤️ por <b>Vertex Lab</b> — El Salvador 🇸🇻</sub>
</div>