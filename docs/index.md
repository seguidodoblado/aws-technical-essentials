# AWS Technical Essentials

Material de estudio en español basado en los conceptos fundamentales del curso **AWS Technical Essentials**.

Este repositorio recopila apuntes, resúmenes y prácticas guiadas para aprender los servicios esenciales de Amazon Web Services de forma progresiva.

---

## Objetivo

El objetivo de este proyecto es ofrecer una guía de estudio clara y organizada para repasar los fundamentos de AWS, incluyendo conceptos de nube, infraestructura global, seguridad, cómputo, redes y otros servicios básicos.

El material está pensado como apoyo para:

- estudiantes que estén comenzando con AWS,
- personas que preparan una formación introductoria,
- profesionales que quieren repasar conceptos esenciales,
- instructores que necesitan una base estructurada en español.

---

## Estructura del repositorio

```text
.
├── 01-guia-estudiante/
│   ├── 00-vision-general-del-curso/
│   ├── 01-introduccion-a-amazon-web-services/
│   ├── 02-servicios-de-computacion-en-la-nube/
│   ├── 03-servicios-de-redes-de-aws/
│   ├── 04-servicios-de-almacenamiento-de-aws/
│   ├── 05-servicios-de-base-de-datos-de-aws/
│   ├── 06-monitorizacion-equilibrio-de-carga-y-escalado/
│   └── 07-resumen-del-curso/
├── 02-laboratorios/
│   ├── 00-general/
│   └── 01-introduccion-a-aws-iam/
├── LICENSE
└── README.md
```

### Guía del estudiante

Contiene todos los módulos teóricos del curso, organizados por tema. Cada módulo incluye documentos en Markdown con explicaciones, objetivos y conceptos clave.

### Laboratorios

Contiene las prácticas guiadas del curso. Actualmente está en desarrollo e incluye una sección general con el índice de laboratorios y el inicio del laboratorio de introducción a AWS Identity and Access Management.

---

## Contenido disponible

### Guía del estudiante

#### 00. Visión general del curso

- [Visión general del curso](01-guia-estudiante/00-vision-general-del-curso/00-0-vision-general.md)
- [Mapa del curso](01-guia-estudiante/00-vision-general-del-curso/00-1-mapa.md)
- [Resumen de los módulos](01-guia-estudiante/00-vision-general-del-curso/00-2-resumen-modulos.md)

#### 01. Introducción a Amazon Web Services

- [Objetivos](01-guia-estudiante/01-introduccion-a-amazon-web-services/01-0-objetivos.md)
- [¿Qué es la computación en la nube?](01-guia-estudiante/01-introduccion-a-amazon-web-services/01-1-computacion-nube.md)
- [Infraestructura global de AWS](01-guia-estudiante/01-introduccion-a-amazon-web-services/01-2-infraestructura-global.md)
- [Gestión de los servicios de AWS](01-guia-estudiante/01-introduccion-a-amazon-web-services/01-3-gestion-servicios.md)
- [Modelo de responsabilidad compartida de AWS](01-guia-estudiante/01-introduccion-a-amazon-web-services/01-4-responsabilidad-compartida.md)
- [AWS Identity and Access Management (IAM)](01-guia-estudiante/01-introduccion-a-amazon-web-services/01-5-iam.md)

#### 02. Servicios de computación en nube

- [Objetivos](01-guia-estudiante/02-servicios-de-computacion-en-la-nube/02-0-objetivos.md)
- [Computación como servicio en AWS](01-guia-estudiante/02-servicios-de-computacion-en-la-nube/02-1-computacion-servicio.md)
- [Amazon Elastic Compute Cloud (Amazon EC2)](01-guia-estudiante/02-servicios-de-computacion-en-la-nube/02-2-amazon-ec2.md)
- [Ciclo de vida de una instancia Amazon EC2](01-guia-estudiante/02-servicios-de-computacion-en-la-nube/02-3-ciclo-vida-ec2.md)
- [Familias de instancias de Amazon EC2](01-guia-estudiante/02-servicios-de-computacion-en-la-nube/02-4-familias-ec2.md)
- [Servicios de contenedores de AWS](01-guia-estudiante/02-servicios-de-computacion-en-la-nube/02-5-contenedores.md)
- [Computación sin servidor (Serverless)](01-guia-estudiante/02-servicios-de-computacion-en-la-nube/02-6-serverless.md)

#### 03. Servicios de redes de AWS

- [Objetivos](01-guia-estudiante/03-servicios-de-redes-de-aws/03-0-objetivos.md)
- [Amazon Virtual Private Cloud (Amazon VPC)](01-guia-estudiante/03-servicios-de-redes-de-aws/03-1-amazon-vpc.md)
- [Classless Inter-Domain Routing (CIDR)](01-guia-estudiante/03-servicios-de-redes-de-aws/03-2-cidr.md)
- [Acceso desde Internet y redes remotas](01-guia-estudiante/03-servicios-de-redes-de-aws/03-3-acceso-internet-redes-remotas.md)
- [Network Access Control List (NACL)](01-guia-estudiante/03-servicios-de-redes-de-aws/03-4-nacl.md)
- [Security Groups](01-guia-estudiante/03-servicios-de-redes-de-aws/03-5-security-groups.md)
- [Seguridad en múltiples capas](01-guia-estudiante/03-servicios-de-redes-de-aws/03-6-seguridad-multiples-capas.md)

#### 04. Servicios de almacenamiento de AWS

- [Objetivos](01-guia-estudiante/04-servicios-de-almacenamiento-de-aws/04-0-objetivos.md)
- [Tipos de almacenamiento](01-guia-estudiante/04-servicios-de-almacenamiento-de-aws/04-1-tipos-almacenamiento.md)
- [Almacenamiento en bloques](01-guia-estudiante/04-servicios-de-almacenamiento-de-aws/04-2-almacenamiento-bloques.md)
- [Almacenamiento de archivos](01-guia-estudiante/04-servicios-de-almacenamiento-de-aws/04-3-almacenamiento-archivos.md)
- [Almacenamiento de objetos](01-guia-estudiante/04-servicios-de-almacenamiento-de-aws/04-4-almacenamiento-objetos.md)
- [Clases de almacenamiento de Amazon S3](01-guia-estudiante/04-servicios-de-almacenamiento-de-aws/04-5-clases-amazon-s3.md)

#### 05. Servicios de base de datos de AWS

- [Objetivos](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-0-objetivos.md)
- [Beneficios de las bases de datos en AWS](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-1-beneficios-bases-datos.md)
- [Tipos de bases de datos](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-2-tipos-bases-datos.md)
- [Bases de datos relacionales](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-3-bases-datos-relacionales.md)
- [Bases de datos administradas](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-4-bases-datos-administradas.md)
- [Amazon Relational Database Service (Amazon RDS)](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-5-amazon-rds.md)
- [Amazon DynamoDB](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-6-amazon-dynamodb.md)
- [Características de Amazon DynamoDB](01-guia-estudiante/05-servicios-de-base-de-datos-de-aws/05-7-caracteristicas-dynamodb.md)

#### 06. Monitorización, equilibrio de carga y escalado

- [Objetivos](01-guia-estudiante/06-monitorizacion-equilibrio-de-carga-y-escalado/06-0-objetivos.md)
- [Monitorización](01-guia-estudiante/06-monitorizacion-equilibrio-de-carga-y-escalado/06-1-monitorizacion.md)
- [Escalado](01-guia-estudiante/06-monitorizacion-equilibrio-de-carga-y-escalado/06-2-escalado.md)
- [Equilibrio de carga](01-guia-estudiante/06-monitorizacion-equilibrio-de-carga-y-escalado/06-3-equilibrio-carga.md)

#### 07. Resumen del curso

- [Arquitectura de la aplicación Employee Directory](01-guia-estudiante/07-resumen-del-curso/07-1-arquitectura-employee-directory.md)
- [Arquitectura Serverless Employee Directory](01-guia-estudiante/07-resumen-del-curso/07-2-arquitectura-serverless-employee-directory.md)

### Laboratorios

#### 00. General

- [Contenidos](02-laboratorios/00-general/00-0-contenidos.md)

#### 01. Introducción a AWS Identity and Access Management

- [Introducción](02-laboratorios/01-introduccion-a-aws-iam/01-0-introduccion.md)
- [Objetivos](02-laboratorios/01-introduccion-a-aws-iam/01-1-objetivos.md)

---

## Estado del contenido

La guía del estudiante está completada. El trabajo actual se centra en desarrollar los laboratorios prácticos y ampliar el laboratorio de introducción a AWS Identity and Access Management.

| Área | Estado |
| --- | --- |
| Visión general del curso | Completado |
| Introducción a Amazon Web Services | Completado |
| Servicios de computación en nube | Completado |
| Servicios de redes de AWS | Completado |
| Servicios de almacenamiento de AWS | Completado |
| Servicios de base de datos de AWS | Completado |
| Monitorización, equilibrio de carga y escalado | Completado |
| Resumen del curso | Completado |
| Laboratorios | En progreso |
| Laboratorio de introducción a AWS Identity and Access Management | Iniciado |

---

## Cómo usar este material

Se recomienda seguir los módulos en orden:

1. Revisar la visión general del curso.
2. Estudiar los conceptos introductorios de AWS.
3. Avanzar por los servicios principales de cómputo, redes, almacenamiento, bases de datos, monitorización, escalado y equilibrio de carga.
4. Revisar el resumen del curso y las arquitecturas de referencia.
5. Realizar los laboratorios prácticos conforme se vayan incorporando.

---

## Próximos pasos

- Completar el laboratorio de introducción a AWS Identity and Access Management.
- Desarrollar los siguientes laboratorios prácticos del curso.
- Añadir instrucciones paso a paso y guía de limpieza de recursos para cada laboratorio.

---
