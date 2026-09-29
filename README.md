# GiConnect — App web y móvil

Aplicación de GiConnect para gimnasios y academias de artes marciales: los maestros gestionan a sus atletas, clases, cinturones y solicitudes de ingreso al equipo, y los atletas siguen su progreso y se unen a su gimnasio.

Consume la API REST del backend: [GiConnectBack](https://github.com/GiConnectAdmins/GiConnectBack) (NestJS 11 + TypeScript + MongoDB Atlas).

> **Estado: en desarrollo.** El proyecto está inicializado y ahora mismo se está construyendo la primera versión de las pantallas.

## Stack tecnológico

- **[Angular 20](https://angular.dev/)** con componentes standalone
- **[Ionic 8](https://ionicframework.com/)** — componentes de interfaz para web y móvil
- **[Capacitor](https://capacitorjs.com/)** — la misma base de código como app nativa para Android e iOS
- **TypeScript** y **RxJS**
- **Karma + Jasmine** (tests) y **ESLint**

## Primera versión (en desarrollo)

- Estructura base: servicios de conexión con la API, sesión con JWT, interceptor HTTP y rutas protegidas según el rol (Admin, Maestro, Atleta).
- Registro e inicio de sesión.
- Perfil del atleta con su cinturón actual y su historial de grados.
- Listado de gimnasios y solicitud para unirse a un equipo.
- Portal del maestro para aceptar o rechazar solicitudes, y listado de clases.
- Demo pública con usuarios de prueba.

Más adelante: cuotas (mensualidades y bonos), reserva de clases y búsqueda pública de gimnasios.

## Requisitos previos

- Node.js 22+ y npm
- Ionic CLI (opcional): `npm install -g @ionic/cli`
- El backend arrancado en local (por defecto en `http://localhost:3000`)

## Instalación y uso

```bash
npm install
npm start          # servidor de desarrollo en http://localhost:4200 (o: ionic serve)
```

| Comando | Qué hace |
|---|---|
| `npm start` | Arranca la app en modo desarrollo con recarga automática |
| `npm run build` | Genera la versión de producción en `www/` |
| `npm test` | Ejecuta los tests unitarios (Karma) |
| `npm run lint` | Revisa el código con ESLint |

## Flujo de trabajo

- **Git flow**: `main` (versiones estables) ← `develop` (integración) ← una rama `ticket-X` por tarea.
- Cada ticket se integra mediante un pull request revisado por el otro miembro del equipo.
- Las tareas se planifican en un tablero de Trello, con requisitos y criterios de aceptación en cada ticket.
