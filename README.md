# Plataforma Web de Novelas, Webnovels y Manga

Plataforma web de lectura online para webnovels, manga y novelas traducidas, orientada a la comunidad hispanohablante. Proyecto intermodular del módulo PIMDA (2º DAW, I.E.S Azarquiel).

**Equipo:** Mario García, Víctor Chen y Jorge Rodríguez

## Características principales

- Lector integrado con ajustes de tipografía, brillo y velocidad.
- Recomendaciones personalizadas mediante un motor de IA.
- Panel de autor con subida de capítulos, estadísticas y chequeo antiplagio.
- Comunidad de creadores y lectores, con comentarios y noticias.
- Suscripción premium, propinas y publicidad controlada por el usuario.

## Stack tecnológico

| Capa            | Tecnologías                                                |
| --------------- | ---------------------------------------------------------- |
| Backend         | Java, Spring Boot, Spring Security, JPA/Hibernate          |
| Frontend        | React, Tailwind CSS, Jest                                  |
| Motor de IA     | Python, Pandas, TensorFlow / Scikit-learn, FastAPI o Flask |
| Base de datos   | PostgreSQL                                                 |
| Caché           | Redis                                                      |
| Infraestructura | Docker, Kubernetes, AWS (EKS, CloudFront, CloudWatch)      |

## Estructura del repositorio

```
plataforma-novelas/
├── backend/        # API REST con Spring Boot
├── frontend/       # Interfaz de usuario en React
├── ia/             # Motor de recomendaciones en Python
├── docs/           # Documentación técnica (arquitectura, endpoints, BD)
├── docker-compose.yml
└── README.md
```

## Requisitos previos

- Git
- Docker Desktop
- Java 17 o superior
- Node.js 18 o superior
- Python 3.10 o superior
- IntelliJ IDEA (o cualquier IDE compatible con Java) y Visual Studio Code

## Instalación en local

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/JorgeDip/Luminaria.git
   cd luminaria
   ```

2. Levantar PostgreSQL y Redis con Docker:

   ```bash
   docker compose up -d
   ```

3. Arrancar el backend:

   ```bash
   cd backend
   ./mvnw spring-boot:run
   ```

4. Arrancar el frontend:

   ```bash
   cd frontend
   npm install
   npm run dev
   ```

5. Arrancar el servicio de IA:

   ```bash
   cd ia
   pip install -r requirements.txt
   uvicorn main:app --reload
   ```

## Flujo de trabajo con Git

- `main`: versión estable y desplegable. Solo se fusiona con revisión de un compañero.
- `develop`: rama de integración.
- `feature/<nombre>`: una rama por tarea, por ejemplo `feature/4.1.1-entidad-usuario`. Se fusiona en `develop` mediante pull request.

Antes de abrir un pull request, ejecutar las pruebas en local. Los commits deben describir el cambio con claridad.

## Pruebas

- Backend: `./mvnw test` (JUnit)
- Frontend: `npm test` (Jest)

## Documentación

La documentación técnica está en la carpeta `docs/`. Los manuales de usuario y administración se entregan en PDF con la documentación final del proyecto.

## Licencia

Proyecto académico. Pendiente de definir la licencia.
