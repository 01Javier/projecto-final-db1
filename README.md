# Sistema de Gestión de Biblioteca Universitaria - División de Tareas Simplificada

## Resumen del Proyecto

Construir un sistema simple de gestión de biblioteca universitaria con frontend en React + TypeScript y backend en Go. El enfoque está en funcionalidad básica que funcione en lugar de código perfecto.

## Composición del Equipo

- **Persona A** (Con experiencia - Tú): Configuración del Backend + Funciones de Admin Simples
- **Persona B**: Interfaz de Usuario + Formularios  
- **Persona C**: Gestión de Libros + Sistema de Préstamos

---

## Fase 1: Configuración Básica

### Persona A - Fundamentos del Backend

**Backend (Primario):**

- Configurar backend básico en Go con el framework Gin
- Configurar conexión simple a base de datos Oracle
- Crear autenticación básica de usuarios (login/registro)
- Configurar tokens JWT para autenticación
- Crear middleware simple para rutas protegidas

**Frontend (Secundario):**

- Configurar React Router con rutas básicas
- Crear componente de rutas protegidas (ProtectedRoute)
- Hacer que las páginas de login/registro funcionen con el backend

### Persona B - Interfaz de Usuario y Layout

**Frontend (Primario):**

- Configurar React Router en el proyecto
- Crear componente de Layout con navbar usando Material-UI
- Construir formularios de login y registro
- Crear página de perfil de usuario
- Manejar validación de formularios y mensajes de error

**Backend (Secundario):**

- Ayudar con el endpoint de registro de usuarios
- Crear endpoints simples de perfil de usuario
- Hash básico de contraseñas

### Persona C - Gestión de Libros

**Backend (Primario):**

- Crear modelo simple de libro (título, autor, copias)
- Construir endpoints básicos CRUD para libros (agregar, listar, actualizar, eliminar)
- Seguimiento simple de inventario (copias disponibles vs total)

**Frontend (Secundario):**

- Crear lista de libros y tarjetas de libros
- Construir búsqueda simple de libros
- Crear formularios para agregar/editar libros

---

## Fase 2: Funcionalidades Principales

### Persona A - Funciones Admin Simples

**Backend (Primario):**

- Agregar roles básicos de usuario (estudiante, admin)
- Crear middleware para verificar si el usuario es admin
- Endpoints simples de admin para gestionar usuarios
- Registro básico de actividad (quién hizo qué, cuándo)

**Frontend (Secundario):**

- Crear página de admin para ver todos los usuarios
- Mostrar/ocultar funciones de admin según el rol del usuario
- Dashboard simple con estadísticas básicas

### Persona B - Completar Funciones de Usuario

**Frontend (Primario):**

- Terminar edición de perfil de usuario
- Crear dashboard de usuario mostrando sus préstamos
- Manejar visualización de rol de usuario (insignia de estudiante/profesor)
- Búsqueda simple de usuarios para admins

**Backend (Secundario):**

- Completar endpoints de actualización de perfil
- Obtener historial de préstamos del usuario
- Funcionalidad simple de búsqueda de usuarios

### Persona C - Sistema de Préstamos

**Backend (Primario):**

- Crear modelo de préstamo (usuario, libro, fechas)
- Endpoint para pedir prestado un libro (verificar disponibilidad)
- Endpoint para devolver libro
- Obtener préstamos actuales del usuario

**Frontend (Secundario):**

- Botón "Pedir Prestado" en tarjetas de libros
- Página "Mis Préstamos" mostrando libros prestados
- Botón "Devolver" para libros prestados
- Indicador simple de libros vencidos

---

## Fase 3: Pulir & Funciones Finales

### Persona A - Reportes Básicos

**Backend (Primario):**

- Endpoint simple de estadísticas (total libros, total préstamos, conteo de vencidos)
- Listar libros vencidos
- Visualización básica de registro de actividad de usuarios

**Frontend (Secundario):**

- Dashboard simple de admin con números
- Mostrar lista de libros vencidos
- Mostrar actividad reciente

### Persona B - Pulir Experiencia de Usuario

**Frontend (Primario):**

- Hacer que los formularios se vean lindos y sean fáciles de usar
- Agregar estados de carga y mensajes de error
- Hacer que funcione bien en móvil
- Pulir el aspecto general

**Backend (Secundario):**

- Arreglar cualquier bug en endpoints de usuario
- Agregar mejores mensajes de error

### Persona C - Completar Sistema de Libros

**Frontend (Primario):**

- Mejorar búsqueda de libros (filtrar por autor, título)
- Hacer la gestión de libros fácil para admins
- Pulir interfaz de préstamo/devolución
- Agregar estado de disponibilidad de libros

**Backend (Secundario):**

- Agregar filtros de búsqueda de libros
- Arreglar cualquier bug del sistema de préstamos
- Estadísticas simples de libros

---

## Fase 4: Integración Final & Preparación de Demo

### Todos Juntos - Empujón Final


- Arreglar bugs encontrados durante la integración
- Asegurar que todas las funciones trabajen juntas
- Pulir los flujos de usuario más importantes
- Preparar datos de demostración (libros, usuarios, préstamos de ejemplo)



- Arreglos finales de bugs
- Practicar la presentación de la demo
- Asegurar que todo funcione para la presentación final
- Crear README simple con instrucciones para ejecutar el proyecto

---

## Configuración del Frontend (Proyecto Inicial)

### Estructura de Carpetas a Crear

```
src/
├── components/
│   ├── layout/
│   │   ├── Navbar.tsx           # Persona B
│   │   └── Layout.tsx           # Persona B
│   ├── auth/
│   │   ├── LoginForm.tsx        # Persona B
│   │   ├── RegisterForm.tsx     # Persona B
│   │   └── ProtectedRoute.tsx   # Persona A
│   ├── books/
│   │   ├── BookCard.tsx         # Persona C
│   │   ├── BookList.tsx         # Persona C
│   │   └── BookForm.tsx         # Persona C
│   └── users/
│       └── UserProfile.tsx      # Persona B
├── pages/
│   ├── Home.tsx                 # Persona B
│   ├── Login.tsx                # Persona B
│   ├── Register.tsx             # Persona B
│   ├── Books.tsx                # Persona C
│   ├── MyLoans.tsx              # Persona C
│   ├── Profile.tsx              # Persona B
│   └── AdminDashboard.tsx       # Persona A
├── services/
│   └── api.ts                   # Persona A (base), todos contribuyen
├── types/
│   └── index.ts                 # Todos contribuyen
└── App.tsx                      # Configuración de rutas
```

## Lo Que Cada Persona Entrega

### Persona A

- Sistema de login/registro funcionando
- Funciones básicas de admin
- Roles simples de usuario
- Fundamentos de la API del backend
- Componente de rutas protegidas

### Persona B

- Interfaz de usuario atractiva
- Gestión de perfil de usuario
- Formularios que funcionan bien
- Diseño amigable para móviles
- Layout con navbar completo

### Persona C

- Gestión completa de libros
- Sistema de préstamo/devolución funcionando
- Funcionalidad de búsqueda de libros
- Gestión de libros para admin
