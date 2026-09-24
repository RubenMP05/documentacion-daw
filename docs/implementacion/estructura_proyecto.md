### 📄 `docs/implementación/estructura_proyecto.md`
```markdown
# Estructura del Proyecto

El proyecto sigue una arquitectura basada en componentes (Frontend en React) y una API RESTful (Backend en Node.js/Express). 

## Árbol de Directorios del Frontend
```text
src/
├── assets/         # Imágenes, iconos y estilos globales
├── components/     # Componentes UI reutilizables (Botones, Tarjetas)
├── features/       # Lógica agrupada por dominio (ej. /tasks, /auth)
├── hooks/          # Custom React hooks (ej. useAuth, useTasks)
├── services/       # Clientes de la API (Axios/Fetch)
├── utils/          # Funciones de ayuda y formateo de fechas
└── App.jsx         # Punto de entrada y enrutamiento principal
