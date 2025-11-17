# TheFreed.v1 - Plataforma de Monetización para Creadores de Contenido

![TheFreed.v1](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![React](https://img.shields.io/badge/React-18.3-blue.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue.svg)
![Node.js](https://img.shields.io/badge/Node.js-25.1.0-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## 📋 Descripción General

TheFreed.v1 es una plataforma completa de monetización para creadores de contenido que permite a los usuarios conectar con sus audiencias y generar ingresos a través de suscripciones, contenido premium y pagos directos. La plataforma incluye funcionalidades de autenticación, gestión de contenido, sistema de pagos con Stripe, mensajería privada, notificaciones en tiempo real y un panel de administración completo.

### ✨ Características Principales

- **🔐 Autenticación Segura**: Sistema completo de registro/login con JWT
- **👤 Perfiles de Creadores**: Gestión avanzada de perfiles con verificación
- **📱 Contenido Multimedia**: Subida y gestión de contenido con diferentes tipos de visibilidad
- **💳 Sistema de Pagos**: Integración completa con Stripe para suscripciones y pagos
- **💬 Mensajería Privada**: Sistema de mensajería entre usuarios
- **🔔 Notificaciones**: Sistema de notificaciones en tiempo real
- **📊 Analytics**: Seguimiento de métricas y ganancias
- **🛡️ Moderación**: Sistema completo de reportes y moderación de contenido
- **🎯 Gamificación**: Sistema de insignias y logros
- **🔍 Descubrimiento**: Algoritmos de recomendación de contenido

## 🛠️ Tecnologías Utilizadas

### Frontend
- **React 18.3** - Framework de interfaz de usuario
- **TypeScript 5.x** - Tipado estático
- **Vite 6.0** - Build tool y servidor de desarrollo
- **Tailwind CSS 3.4** - Framework de estilos
- **Radix UI** - Componentes accesibles
- **React Router 6** - Enrutamiento del lado del cliente
- **Axios** - Cliente HTTP
- **Context API** - Gestión de estado global

### Backend
- **Express.js 5.1** - Framework web para Node.js
- **Prisma 6.19** - ORM con type-safety
- **SQLite** - Base de datos de desarrollo
- **JWT (jsonwebtoken)** - Autenticación basada en tokens
- **bcryptjs** - Hashing de contraseñas
- **Stripe 19.2** - Procesamiento de pagos
- **Winston** - Sistema de logging
- **Multer** - Manejo de archivos
- **Helmet** - Seguridad HTTP
- **CORS** - Configuración de recursos cross-origin

### Herramientas de Desarrollo
- **pnpm** - Gestor de paquetes eficiente
- **tsx** - Ejecutor de TypeScript
- **concurrently** - Ejecución de scripts en paralelo
- **nodemon** - Reinicio automático del servidor

## 📁 Estructura del Proyecto

```
TheFreed.v1/
├── 📂 public/                    # Archivos públicos estáticos
├── 📂 src/
│   ├── 📂 components/           # Componentes React reutilizables
│   ├── 📂 contexts/            # Contextos de React (AuthContext)
│   ├── 📂 pages/               # Páginas de la aplicación
│   │   ├── 📂 auth/            # Páginas de autenticación
│   │   └── 📂 dashboard/       # Página principal del dashboard
│   ├── 📂 services/            # Servicios API (api.ts)
│   ├── 📂 types/               # Definiciones de tipos TypeScript
│   ├── 📂 server/              # Backend (Express + Prisma)
│   │   ├── 📂 config/          # Configuraciones (CORS, Logger, etc.)
│   │   ├── 📂 controllers/     # Controladores de la API
│   │   ├── 📂 middleware/      # Middleware personalizado
│   │   ├── 📂 routes/          # Rutas de la API
│   │   ├── 📄 index.ts         # Servidor principal (con Prisma)
│   │   └── 📄 simple.ts        # ⚡ Servidor simplificado (FUNCIONANDO)
│   ├── 📄 App.tsx              # Componente raíz
│   ├── 📄 main.tsx             # Punto de entrada
│   └── 📄 index.css            # Estilos globales
├── 📂 prisma/
│   ├── 📄 schema.prisma        # Esquema de la base de datos
│   └── 📄 migrations/          # Migraciones de la BD
├── 📄 .env                     # Variables de entorno del backend
├── 📄 .env.local               # Variables de entorno del frontend
├── 📄 package.json             # Dependencias y scripts
├── 📄 tsconfig.json            # Configuración de TypeScript
├── 📄 vite.config.ts           # Configuración de Vite
└── 📄 tailwind.config.js       # Configuración de Tailwind
```

## 🗄️ Modelo de Base de Datos (26 Modelos)

### Modelos Principales
- **User** - Usuarios del sistema con roles (USER/CREATOR/ADMIN)
- **CreatorProfile** - Perfiles específicos de creadores con niveles de suscripción
- **Content** - Contenido multimedia con diferentes tipos de visibilidad
- **Subscription** - Suscripciones con auto-renovación

### Modelos Sociales
- **Message** - Mensajes privados entre usuarios
- **Comment** - Comentarios en contenido
- **Like** - Likes en contenido y comentarios
- **Follow** - Seguimiento entre usuarios
- **Notification** - Notificaciones del sistema

### Modelos Financieros
- **Payment** - Transacciones de pago (sin decidir aun)
- **Transaction** - Historial de transacciones
- **Earnings** - Ganancias de creadores
- **Dispute** - Disputas de pagos

### Modelos de Cumplimiento
- **KYC** - Verificación de identidad
- **TaxInfo** - Información fiscal
- **Account** - Cuentas de pago

### Modelos de Moderación
- **Report** - Reportes de contenido
- **Moderation** - Acciones de moderación
- **AuditLog** - Registro de auditorías

### Modelos de Gamificación
- **Badge** - Insignias del sistema
- **UserBadge** - Insignias de usuarios

### Modelos del Sistema
- **UserSettings** - Configuraciones de usuario
- **Analytics** - Métricas y analytics
- **ReferralCode** - Códigos de referidos

## 🚀 Instalación y Configuración

### Prerrequisitos
- Node.js 25.1.0 o superior
- pnpm (gestor de paquetes)

### 1. Clonar y Navegar al Proyecto
```bash
cd TheFreed.v1
```

### 2. Instalar Dependencias
```bash
pnpm install
```

### 3. Configurar Variables de Entorno

#### Backend (.env)
```env
# Base de datos
DATABASE_URL="file:./dev.db"

# Servidor
PORT=5174

# JWT
JWT_SECRET=thefreed-super-secret-jwt-key-2024-development-only

# Stripe
STRIPE_SECRET_KEY=sk_test_tu_clave_secreta_de_stripe
STRIPE_PUBLISHABLE_KEY=pk_test_tu_clave_publica_de_stripe
```

#### Frontend (.env.local)
```env
VITE_API_URL=http://localhost:5174
```

### 4. Inicializar la Base de Datos
```bash
# Generar cliente de Prisma
pnpx prisma generate

# Aplicar migraciones
pnpx prisma db push

# (Opcional) Ver la base de datos
pnpx prisma studio
```

### 5. Ejecutar el Proyecto

#### Opción 1: Ejecutar Ambos Simultaneously
```bash
pnpm dev
```

#### Opción 2: Ejecutar por Separado
```bash
# Terminal 1: Backend (Puerto 5174)
pnpm backend:dev

# Terminal 2: Frontend (Puerto 5173)
pnpm dev:frontend
```

## 🌐 Endpoints de la API

### 🔐 Autenticación
- `POST /api/auth/register` - Registro de usuario
- `POST /api/auth/login` - Inicio de sesión
- `POST /api/auth/logout` - Cerrar sesión
- `GET /api/auth/refresh` - Renovar token
- `GET /api/auth/verify` - Verificar token

### 👤 Usuarios
- `GET /api/users/profile` - Obtener perfil
- `PUT /api/users/profile` - Actualizar perfil
- `GET /api/users/settings` - Obtener configuraciones
- `PUT /api/users/settings` - Actualizar configuraciones
- `GET /api/users/:id` - Obtener usuario por ID

### 📱 Contenido
- `GET /api/content` - Listar contenido
- `POST /api/content` - Crear contenido
- `GET /api/content/:id` - Obtener contenido por ID
- `PUT /api/content/:id` - Actualizar contenido
- `DELETE /api/content/:id` - Eliminar contenido
- `POST /api/content/:id/like` - Dar like
- `POST /api/content/:id/comment` - Comentar
- `POST /api/content/:id/view` - Registrar vista

### 💳 Suscripciones
- `GET /api/subscriptions` - Listar suscripciones
- `POST /api/subscriptions` - Crear suscripción
- `GET /api/subscriptions/:id` - Obtener suscripción
- `PUT /api/subscriptions/:id` - Actualizar suscripción
- `DELETE /api/subscriptions/:id` - Cancelar suscripción

### 💰 Pagos
- `POST /api/payments/create-payment-intent` - Crear intención de pago
- `POST /api/payments/confirm` - Confirmar pago
- `GET /api/payments/history` - Historial de pagos
- `POST /api/payments/webhook` - Webhook de Stripe

### 💬 Mensajería
- `GET /api/messages` - Listar mensajes
- `POST /api/messages` - Enviar mensaje
- `GET /api/messages/conversation/:userId` - Conversación con usuario

### 🔔 Notificaciones
- `GET /api/notifications` - Listar notificaciones
- `PUT /api/notifications/:id/read` - Marcar como leída

### 🔧 Administrador
- `GET /api/admin/users` - Listar usuarios (Admin)
- `GET /api/admin/content` - Listar contenido (Admin)
- `POST /api/admin/moderate` - Moderar contenido (Admin)

## 🏃‍♂️ Ejecución del Proyecto

### Estado Actual del Proyecto
- ✅ **Frontend**: Ejecutándose en http://localhost:5173
- ✅ **Backend**: Servidor simplificado en http://localhost:5174
- ✅ **Base de datos**: SQLite configurada
- ✅ **Autenticación**: Sistema JWT funcionando
- ✅ **API**: Endpoints básicos operativos

### URLs de Desarrollo
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:5174
- **Health Check**: http://localhost:5174/health
- **API Status**: http://localhost:5174/api/health

### Características Funcionales
- ✅ Páginas de Login y Registro
- ✅ Dashboard principal con feed
- ✅ Sistema de autenticación con Context API
- ✅ Interfaz responsive con Tailwind CSS
- ✅ Validación de formularios
- ✅ Manejo de errores
- ✅ Navegación con React Router

## 🔧 Notas Técnicas Importantes

### Servidor Simplificado
**El servidor que está funcionando actualmente es `src/server/simple.ts`** - una versión simplificada sin dependencias de Prisma para garantizar estabilidad durante el desarrollo. El servidor completo con Prisma está en `src/server/index.ts` pero presenta problemas de importación del cliente de Prisma.

### Configuración de Puertos
- **Backend**: Puerto 5174
- **Frontend**: Puerto 5173
- La comunicación entre frontend y backend está configurada correctamente con CORS

### Base de Datos
- **Desarrollo**: SQLite (archivo local `dev.db`)
- **Esquema**: 26 modelos definidos en `prisma/schema.prisma`
- **Estado**: Configurada pero requiere resolución de problemas de Prisma Client

### Autenticación
- **Método**: JWT con tokens de acceso y refresh
- **Seguridad**: bcryptjs para hashing de contraseñas
- **Almacenamiento**: localStorage en el frontend

## 🛠️ Guía de Desarrollo

### Estructura de Código

#### Frontend (React + TypeScript)
```typescript
// Ejemplo de componente con contexto de autenticación
import { useAuth } from '@/contexts/AuthContext';

const Dashboard = () => {
  const { user, logout } = useAuth();
  
  return (
    <div>
      <h1>Bienvenido, {user?.username}</h1>
    </div>
  );
};
```

#### Backend (Express + TypeScript)
```typescript
// Ejemplo de controlador con middleware de autenticación
import { Request, Response } from 'express';
import { authMiddleware } from '@/middleware/authMiddleware';

export const getUserProfile = async (req: Request, res: Response) => {
  const userId = req.user.id;
  // Lógica del controlador
};
```

### Scripts Disponibles
```bash
# Desarrollo (frontend + backend)
pnpm dev

# Solo backend
pnpm backend:dev

# Solo frontend
pnpm dev:frontend

# Build de producción
pnpm build

# Linting
pnpm lint

# Base de datos
pnpx prisma studio    # Visor de base de datos
pnpx prisma generate  # Generar cliente
pnpx prisma db push   # Aplicar esquema
```

### Depuración y Logs
- **Winston**: Sistema de logging configurado para desarrollo
- **Health Checks**: Endpoints de salud para monitoreo
- **Error Handling**: Middleware centralizado de manejo de errores

## 📈 Próximos Pasos

### Pendientes de Implementación
1. **Resolución de Prisma Client**: Solucionar problemas de importación
2. **Autenticación JWT Completa** (Paso 3)
3. **Panel de Administración** (Paso 5)
4. **Algoritmos de Descubrimiento** (Paso 6)
5. **Configuración de Entorno** (Paso 7)

### Mejoras Técnicas
- [ ] Integración completa de Prisma
- [ ] Tests unitarios y de integración
- [ ] Documentación de componentes
- [ ] Optimización de performance
- [ ] Implementación de caching
- [ ] Migración a PostgreSQL para producción

## 🤝 Contribución

Este proyecto está en desarrollo activo. Para contribuir:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 📞 Soporte

Para soporte técnico o preguntas:
- **Proyecto**: TheFreed.v1
- **Versión**: 1.0.0
- **Estado**: En desarrollo activo

---

**⚡ Estado Actual**: Frontend y Backend funcionando en puertos 5173 y 5174 respectivamente. Servidor simplificado operativo con endpoints básicos de salud.

**🚀 Funcionalidades Implementadas**: Autenticación básica, interfaz de usuario, navegación, formularios de registro/login.

**🎯 Próximo Objetivo**: Resolver integración completa de Prisma y implementar funcionalidades avanzadas de la plataforma.
