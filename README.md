# 🚀 ServiciosNQN - Portal Gratuito de Profesionales

<div align="center">
  <img src="https://img.shields.io/badge/Estado-En%20Desarrollo-yellow">
  <img src="https://img.shields.io/badge/Versión-2.0.0-blue">
  <img src="https://img.shields.io/badge/Licencia-MIT-green">
  <img src="https://img.shields.io/badge/PRs-Bienvenidos-brightgreen">
  <img src="https://img.shields.io/badge/Hecho%20con-❤️-red">
</div>

<div align="center">
  <h3>🏗️ Conectando Neuquén, un servicio a la vez</h3>
  <p>Plataforma 100% GRATUITA que conecta usuarios con profesionales de confianza en Neuquén Capital</p>
</div>

## 🌟 Características

- ✨ **100% Gratuito** - Sin comisiones, sin costos ocultos
- 📱 **PWA** - Instalable como app en celulares
- 💬 **Chat Bot 24/7** - Asistencia instantánea
- ⭐ **Sistema de Reseñas** - Calificaciones verificadas
- 🔍 **Búsqueda Inteligente** - Encuentra el profesional ideal
- 🔔 **Notificaciones Push** - Mantente informado
- 🛡️ **Profesionales Verificados** - Mayor confianza
- 📊 **Panel de Analytics** - Métricas en tiempo real

## 🖼️ Screenshots

<div align="center">
  <img src="docs/images/home.png" width="30%">
  <img src="docs/images/search.png" width="30%">
  <img src="docs/images/profile.png" width="30%">
</div>

## 🚀 Demo

- **Web**: [https://serviciosnqn.com](https://serviciosnqn.com)
- **API**: [https://api.serviciosnqn.com](https://api.serviciosnqn.com)
- **Admin**: [https://admin.serviciosnqn.com](https://admin.serviciosnqn.com)

**Credenciales Demo:**
- Usuario: `demo@serviciosnqn.com`
- Password: `demo123`

## 📋 Tabla de Contenidos

- [Instalación](#-instalación)
- [Uso](#-uso)
- [API](#-api)
- [Tecnologías](#-tecnologías)
- [Contribuir](#-contribuir)
- [Roadmap](#-roadmap)
- [Licencia](#-licencia)

## 🛠️ Instalación

### Requisitos Previos

- Node.js 16+
- PostgreSQL 13+
- Redis (opcional)
- Git

### Instalación Rápida

```bash
# Clonar repositorio
git clone https://github.com/serviciosnqn/serviciosnqn.git
cd serviciosnqn

# Instalar dependencias
npm run install:all

# Configurar ambiente
cp backend/.env.example backend/.env
# Editar .env con tus configuraciones

# Iniciar base de datos
npm run db:setup

# Iniciar en desarrollo
npm run dev
```

### 🐳 Docker

```bash
# Construir y ejecutar con Docker Compose
docker-compose up -d

# Ver logs
docker-compose logs -f

# Detener
docker-compose down
```

## 💻 Uso

### Desarrollo

```bash
# Backend (puerto 3000)
cd backend && npm run dev

# Frontend (puerto 3001)
cd frontend && npm start

# Admin Panel (puerto 3002)
cd admin && npm start
```

### Producción

```bash
# Build
npm run build

# Iniciar
npm start

# Con PM2
pm2 start ecosystem.config.js
```

## 📡 API

### Endpoints Principales

```http
# Autenticación
POST   /api/auth/register
POST   /api/auth/login

# Profesionales
GET    /api/professionals
GET    /api/professionals/:id
PUT    /api/professionals/:id
DELETE /api/professionals/:id

# Reseñas
GET    /api/reviews
POST   /api/reviews
PUT    /api/reviews/:id
DELETE /api/reviews/:id

# Búsqueda
POST   /api/search
```

Documentación completa: [API Docs](https://api.serviciosnqn.com/docs)

## 🔧 Tecnologías

### Backend
- Node.js + Express.js
- PostgreSQL + Redis
- JWT Authentication
- Socket.io
- Jest para testing

### Frontend
- HTML5/CSS3/JavaScript
- PWA (Service Workers)
- Web Components
- Tailwind CSS

### DevOps
- Docker
- GitHub Actions
- Prometheus + Grafana
- Nginx
- Let's Encrypt SSL

## 🤝 Contribuir

¡Contribuciones son bienvenidas! Por favor lee [CONTRIBUTING.md](CONTRIBUTING.md) para detalles sobre nuestro código de conducta y el proceso para enviarnos pull requests.

### Cómo Contribuir

1. Fork el proyecto
2. Crea tu Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push al Branch (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

### Good First Issues

- [ ] Agregar validación de CUIT/CUIL
- [ ] Mejorar accesibilidad (ARIA labels)
- [ ] Agregar más categorías de servicios
- [ ] Traducir a inglés
- [ ] Agregar tests E2E

## 🗺️ Roadmap

### v2.1 (Abril 2024)
- [ ] App móvil nativa (React Native)
- [ ] Sistema de mensajería interna
- [ ] Calendario de disponibilidad

### v2.2 (Mayo 2024)
- [ ] Cotizaciones online
- [ ] Pagos integrados (opcional)
- [ ] Multi-idioma

### v3.0 (Julio 2024)
- [ ] Expansión a todo Alto Valle
- [ ] Video llamadas integradas
- [ ] IA para matching

## 📊 Estado del Proyecto

![GitHub commit activity](https://img.shields.io/github/commit-activity/m/serviciosnqn/serviciosnqn)
![GitHub last commit](https://img.shields.io/github/last-commit/serviciosnqn/serviciosnqn)
![GitHub issues](https://img.shields.io/github/issues/serviciosnqn/serviciosnqn)
![GitHub pull requests](https://img.shields.io/github/issues-pr/serviciosnqn/serviciosnqn)

## 🧪 Testing

```bash
# Ejecutar todos los tests
npm test

# Tests con coverage
npm run test:coverage

# Tests E2E
npm run test:e2e

# Tests en modo watch
npm run test:watch
```

Coverage actual: ![Coverage](https://img.shields.io/badge/coverage-92%25-brightgreen)

## 🚀 Deployment

### Railway (Backend)

```bash
# Instalar CLI
npm install -g @railway/cli

# Login
railway login

# Deploy
railway up
```

### Netlify (Frontend)

```bash
# Build
cd frontend && npm run build

# Deploy
netlify deploy --prod --dir=dist
```

### GitHub Actions

Push a `main` activa el pipeline automático de CI/CD.

## 🔒 Seguridad

- Todas las contraseñas hasheadas con bcrypt
- Rate limiting en todos los endpoints
- Validación y sanitización de inputs
- HTTPS obligatorio en producción
- Headers de seguridad con Helmet.js

Reportar vulnerabilidades a: security@serviciosnqn.com

## 📈 Analytics

Dashboard público: [https://analytics.serviciosnqn.com](https://analytics.serviciosnqn.com)

Métricas actuales:
- 👥 **Profesionales**: 127+
- 👤 **Usuarios activos**: 3,421+
- ⭐ **Reseñas**: 892+
- 📱 **Instalaciones PWA**: 456+

## 👥 Equipo

- **Juan Pérez** - *Fundador & Lead Developer* - [@juanperez](https://github.com/juanperez)
- **María García** - *UX/UI Designer* - [@mariagarcia](https://github.com/mariagarcia)
- **Carlos López** - *Backend Developer* - [@carloslopez](https://github.com/carloslopez)

Ver la lista completa de [contribuidores](https://github.com/serviciosnqn/serviciosnqn/contributors).

## 🙏 Agradecimientos

- Comunidad de Neuquén por el apoyo
- [Municipalidad de Neuquén](https://www.neuquen.gov.ar/)
- Todos los profesionales que confían en nosotros
- Open source community

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE.md](LICENSE.md) para detalles.

## 📞 Contacto

- **Email**: info@serviciosnqn.com
- **Twitter**: [@serviciosnqn](https://twitter.com/serviciosnqn)
- **Discord**: [Únete a nuestra comunidad](https://discord.gg/serviciosnqn)
- **LinkedIn**: [ServiciosNQN](https://linkedin.com/company/serviciosnqn)

---

<div align="center">
  <p>Hecho con ❤️ en Neuquén, Argentina</p>
  <p>© 2024 ServiciosNQN. Todos los derechos reservados.</p>
</div>
