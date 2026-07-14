# Arquitectura de la aplicación Final Employee Directory

La siguiente arquitectura muestra cómo se integran varios de los servicios estudiados durante el curso para desplegar una aplicación web escalable y altamente disponible en AWS.

---

## Diagrama

```text
                           Internet
                               │
                               ▼
               Application Load Balancer
                               │
                               ▼
                      Internet Gateway
                               │
                               ▼
┌──────────────────── AWS Region ────────────────────┐
│ ┌───────────────────── VPC ──────────────────────┐ │
│ │                                                │ │
│ │ AZ 1          Auto Scaling Group          AZ 2 │ │
│ │                                                │ │
│ │ ┌──────────┐                    ┌──────────┐   │ │
│ │ │ Public   │                    │ Public   │   │ │
│ │ │ Subnet   │                    │ Subnet   │   │ │
│ │ │┌────────┐│                    │┌────────┐│   │ │
│ │ ││Security││                    ││Security││   │ │
│ │ ││ Group  ││                    ││ Group  ││   │ │
│ │ ││        ││                    ││        ││   │ │
│ │ ││Employee│◄────────────────────►│Employee││   │ │
│ │ ││Directory││                    ││Directory││  │ │
│ │ ││ App EC2││                    ││ App EC2││   │ │
│ │ │└────────┘│                    │└────────┘│   │ │
│ │ └──────────┘                    └──────────┘   │ │
│ └────────────────────────────────────────────────┘ │
└────────────────────────────────────────────────────┘
          ▲                               ▲
          │                               │
  Amazon S3 (Photos)          Amazon DynamoDB (Employee Data)
```

---

## Componentes

| Servicio | Función |
| :-------- | :------ |
| **Application Load Balancer** | Distribuye las solicitudes entre las instancias de la aplicación. |
| **Internet Gateway** | Permite la comunicación entre Internet y la VPC. |
| **Amazon VPC** | Proporciona una red virtual aislada para alojar la aplicación. |
| **Availability Zones** | Distribuyen las instancias entre zonas independientes. |
| **Public Subnets** | Alojan las instancias Amazon EC2. |
| **Security Groups** | Controlan el tráfico permitido hacia las instancias. |
| **Amazon EC2 Auto Scaling** | Ajusta automáticamente el número de instancias según la demanda. |
| **Amazon S3** | Almacena las fotografías de los empleados. |
| **Amazon DynamoDB** | Almacena la información de los empleados. |

---

## Objetivo de la arquitectura

Esta arquitectura integra varios de los servicios presentados durante el curso para proporcionar una aplicación con:

- Alta disponibilidad.
- Escalabilidad automática.
- Distribución del tráfico mediante Elastic Load Balancing.
- Almacenamiento de objetos con Amazon S3.
- Base de datos NoSQL administrada con Amazon DynamoDB.

---
