# Config Server

Servicio centralizado para la gestión de configuraciones de todos los microservicios del sistema.

## Tecnologías utilizadas
- Java 17
- Spring Boot
- Spring Cloud Config Server
- Git

## Funcionalidades
- Servidor centralizado de configuración.
- Provee archivos de configuración (`application.yml`) desde un repositorio Git privado.
- Carga dinámica de propiedades a los servicios registrados.

## Repositorio de configuración
- El servidor apunta a un repositorio remoto donde se almacenan los archivos `.yml` de cada servicio.

## Ejemplo de estructura

```yaml
config-repo/
├── discovery-service/
│   └── application.yml
├── gateway-service/
│   └── application.yml
├── inventory-service/
│   └── application.yml
├── report-service/
│   └── application.yml
└── application.yml  # Configuracion comun para todos los servicios
```

## 🏁 Recomendaciones para ejecucion local
- Este servicio se debe iniciar antes que los demás para que puedan cargar su configuración.

