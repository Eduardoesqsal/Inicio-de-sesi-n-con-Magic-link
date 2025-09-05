# Inicio-de-sesi-n-con-Magic-link
Gestión de autenticación con supabase

# 🔐 Inicio de Sesión con Supabase y Magic Link (React)

Este proyecto implementa un sistema de **autenticación con Supabase** utilizando el método de **Magic Link**.  
El usuario ingresa su correo electrónico, recibe un enlace seguro en su email y al hacer clic queda autenticado en la aplicación.  

## 🚀 Tecnologías utilizadas
- [React.js](https://reactjs.org/) – Frontend de la aplicación.
- [Supabase](https://supabase.com/) – Backend como servicio para autenticación y base de datos.
- [Create React App](https://create-react-app.dev/) – Entorno de desarrollo rápido.
- [Tailwind CSS](https://tailwindcss.com/) (opcional) – Estilización moderna.

## 📂 Estructura del proyecto
.
├── src/
│ ├── App.jsx # Componente principal con lógica de login/logout
│ ├── supabaseClient.js # Configuración de Supabase
│ ├── index.css # Estilos globales
│ └── index.js # Punto de entrada de React
├── package.json
├── README.md
└── public/ # Archivos estáticos

bash
Copiar código

## ⚙️ Configuración inicial

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/mi-proyecto-supabase.git
   cd mi-proyecto-supabase
Instalar dependencias

bash
Copiar código
npm install
Configurar Supabase

Crear un proyecto en Supabase.

Ir a Project Settings > API y copiar:

SUPABASE_URL

SUPABASE_ANON_KEY

Crear un archivo .env.local en la raíz del proyecto:

env
Copiar código
REACT_APP_SUPABASE_URL=https://xxxxx.supabase.co
REACT_APP_SUPABASE_ANON_KEY=tu_api_key
Ejecutar la app

bash
Copiar código
npm start
Esto levantará un servidor local en http://localhost:3000 y abrirá la app en tu navegador.

🧑‍💻 Uso
El usuario ingresa su correo electrónico en el formulario.

La app llama a Supabase con supabase.auth.signInWithOtp({ email }).

Supabase envía un Magic Link al correo del usuario.

Al hacer clic en el enlace, el usuario queda autenticado y redirigido a la app.

