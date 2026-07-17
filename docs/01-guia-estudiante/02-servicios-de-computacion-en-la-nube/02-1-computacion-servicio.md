# Computación como servicio en AWS

AWS ofrece diferentes formas de ejecutar aplicaciones en la nube. Dependiendo del nivel de control y administración deseado, es posible elegir entre distintos modelos de computación.

```text
              Computación como servicio en AWS

        ┌──────────────┬──────────────┬────────────────┐
        │ Infraestructura │ Contenedores │  Serverless   │
        └──────────────┴──────────────┴────────────────┘
                │               │                 │
                ▼               ▼                 ▼
              Amazon EC2      Amazon ECS/      AWS Lambda
                              Amazon EKS
```

AWS proporciona servicios adaptados a diferentes necesidades:

- **Infraestructura**: el cliente administra las máquinas virtuales y el sistema operativo.
- **Contenedores**: el cliente administra las aplicaciones ejecutadas en contenedores, mientras AWS puede encargarse de parte de la infraestructura.
- **Serverless**: el cliente únicamente desarrolla el código de la aplicación y AWS administra toda la infraestructura necesaria para su ejecución.

---
