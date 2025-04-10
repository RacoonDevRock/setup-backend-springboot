# 🧠 Big Picture Eficientis 3.0

![Big Picture Eficientis 3.0](./img/bigpicture_eficientis.png)

## Descripcion

| Componente                 | ¿Para qué sirve?                                                            | Tecnologías                                               |
| -------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------- |
| API Gateway                | Entrada única al sistema. Maneja rutas, seguridad, balanceo, rate-limiting. | Spring Cloud Gateway, Spring Security                     |
| Discovery Server           | Registro y descubrimiento dinámico de microservicios.                  | Spring Cloud Netflix Eureka                               |
| Config Server              | Configuración centralizada, desacoplada y versionada para todos los servicios.                        | Spring Cloud Config, Git                                  |
| Circuit Breaker (opcional) | Evita que una falla afecte a todo el sistema.                               | Resilience4j
| Event bus          | Comunicación asíncrona y desacoplada entre microservicios.	| Apache Kafka                             |
| Auth Service                | Manejo de autenticación y generación de tokens.                             | Spring Security, JWT                    |


## 🏗️ Arquitectura recomendada en Spring Cloud
### 📦 Estructura de carpetas
```
└── 📁project-manager
        └── 📁api-gateway
        └── 📁discovery-server
        └── 📁config-server
        └── 📁circuit-breaker
        └── 📁auth-service
```

## ⚙️ Consideraciones clave
1. ✅ Repositorio Git exclusivo para configuración (config-repo)

2. 🔁 Circuit Breaker + Retry automático con Resilience4j

3. 📩 Comunicación asíncrona basada en eventos con Kafka

4. 🧪 Testing con JUnit y Mockito

5. 🚀 CI/CD con GitHub Actions, contenedores Docker


## 🛠 Herramientas en producción
| Necesidad             | Herramienta               |
| --------------------- | ------------------------- |
| Configuración central | Spring Cloud Config + Git |
| Comunicación interna  | Kafka + OpenFeign + WebClient        |
| Seguridad             | Spring Security / JWT   |
| Resiliencia           | Resilience4j              |
| Documentación         | Springdoc OpenAPI / Swagger         |
| Gateway               | Spring Cloud Gateway      |

## 🔗 Sitio oficial: 

* [Spring Boot Home](https://spring.io/)
* [Spring Boot Framwork](https://spring.io/projects/spring-boot) - [Spring Initializr](https://start.spring.io/)
* [Spring Boot Microservices](https://spring.io/microservices)
* [Spring Boot Cloud](https://spring.io/cloud)

## 📚 Pasos de instalación

0. [Big Picture – Arquitectura General](./00-big-picture.md)  
1. [Instalación de JDK y Maven](./01-instalacion-jdk-maven.md)  
2. [Instalación del IDE](./02-instalacion-ide.md)  
3. [Creación del proyecto con Spring Initializr](./03-spring-initializr.md)  
4. [Importación del proyecto](./04-importar-proyecto.md)  
5. [Configuración y ejecución](./05-configuracion-ejecucion.md)