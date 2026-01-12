Proyecto Base – Sistema Modular en Django y TailwindCSS 🚀

Este proyecto es una base unificada para desarrollar un sistema modular utilizando Django como backend y TailwindCSS como sistema de estilos. Cada grupo de alumnos puede crear su módulo como una app independiente, manteniendo autenticación, permisos y diseño centralizados.

IMPORTANTE: Se debe tener Node.js instalado para compilar TailwindCSS ⚠️

1. Características principales 🔧

Autenticación y seguridad 🔒
Login con Django Allauth personalizado.
El registro está bloqueado; solo administradores pueden crear usuarios.
Autenticación de dos factores (2FA / MFA).
Control de sesión con vencimiento a los 20 minutos de inactividad.
Solo se permite una sesión activa por usuario; si inicia sesión en otro dispositivo, se cierra la sesión anterior.

Gestión de usuarios 👥
Panel para listar usuarios con paginación.
Control de roles y permisos: Administrador, Gerencia y Usuario Normal.
Vista de usuarios conectados y registro de últimos accesos.
Perfil editable y opción para cambiar contraseña.
Subida de foto de perfil con recorte automático, reducción de peso y eliminación de la imagen anterior.

Interfaz y diseño 🎨
Diseño responsivo compatible con PC y móvil.
Sidebar con navegación organizada.
Estilos base homogéneos en todo el proyecto.
Gráfico de ejemplo en la pantalla de inicio usando Apache ECharts 📊

Organización del código 📁
Estructura modular y clara.
Apps incluidas: homeApp y UsuarioApp.
Carpeta templates organizada con componentes reutilizables.
Carpeta utils con funciones auxiliares, como tratamiento de imágenes.

2. Levantar el entorno ⚙️

Crear entorno virtual
python -m venv .venv

Activar entorno
Linux o Mac:
source .venv/bin/activate
Windows:
.venv\Scripts\activate

Instalar dependencias
pip install -r requirements.txt

Levantar el servidor
python manage.py runserver

Usuario por defecto 👤
Usuario: admin (si no funciona, usar administrador)
Clave: 123qaz***

3. Siguientes pasos ➕

Cómo agregar una nueva app o módulo
Crear la app con:
python manage.py startapp NombreModulo
Registrar la app en core/settings.py dentro de LOCAL_APPS.
Agregar las rutas en core/urls.py o en un urls.py dentro de la app.

Roles de usuario 🧩
Administrador: acceso total, creación de usuarios y acceso al ORM.
Gerencia: acceso total y creación de usuarios.
Usuario normal: acceso restringido.

