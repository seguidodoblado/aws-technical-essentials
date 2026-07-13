# Amazon Relational Database Service (Amazon RDS)

**Amazon Relational Database Service (Amazon RDS)** es un servicio administrado que facilita la configuración, el funcionamiento y el escalado de bases de datos relacionales en AWS.

Amazon RDS automatiza las tareas administrativas habituales para que los usuarios puedan centrarse en el desarrollo de sus aplicaciones.

---

## Arquitectura

```text
                    Aplicación
                         │
                         ▼
                 Amazon RDS
                         │
        ┌────────────────┼────────────────┐
        │                │                │
        ▼                ▼                ▼
  Administración     Alta disponibilidad  Copias de seguridad
    automatizada
```

---

## Motores de bases de datos compatibles

Amazon RDS admite varios motores de bases de datos relacionales:

- Amazon Aurora
- PostgreSQL
- MySQL
- MariaDB
- Oracle Database
- Microsoft SQL Server

Esto permite utilizar el motor que mejor se adapte a las necesidades de la aplicación sin tener que administrar la infraestructura subyacente.

---

## Clases de instancia de Amazon RDS

Las **clases de instancia** determinan la capacidad de procesamiento, memoria y red disponible para la base de datos.

AWS ofrece diferentes familias de instancias para adaptarse a distintos tipos de cargas de trabajo.

| Familia | Uso recomendado |
| :------ | :-------------- |
| **db.t** | Desarrollo, pruebas y cargas de trabajo con utilización variable. |
| **db.m** | Uso general con equilibrio entre CPU, memoria y red. |
| **db.r** | Aplicaciones que requieren grandes cantidades de memoria. |

La elección de la clase de instancia dependerá de los requisitos de rendimiento de la aplicación.

---

## Tipos de almacenamiento

Amazon RDS ofrece distintos tipos de almacenamiento para responder a diferentes necesidades de rendimiento.

| Tipo de almacenamiento | Características |
| :---------------------- | :-------------- |
| **SSD de uso general (General Purpose SSD)** | Equilibrio entre coste y rendimiento para la mayoría de aplicaciones. |
| **SSD con IOPS aprovisionadas (Provisioned IOPS SSD)** | Diseñado para aplicaciones que requieren un elevado número de operaciones de entrada/salida por segundo. |
| **Magnético** | Opción de almacenamiento de generaciones anteriores para cargas de trabajo que no requieren un alto rendimiento. |

La capacidad de almacenamiento puede modificarse conforme evolucionan las necesidades de la base de datos.

---

## Alta disponibilidad

Amazon RDS permite implementar despliegues **Multi-AZ** para aumentar la disponibilidad de la base de datos.

```text
             Aplicación
                  │
                  ▼
          Instancia principal
                  │
          Replicación síncrona
                  │
                  ▼
          Instancia en espera
         (Otra Availability Zone)
```

En un despliegue Multi-AZ:

- Existe una instancia principal y otra en espera.
- Los datos se replican de forma síncrona.
- Si se produce un fallo, Amazon RDS realiza automáticamente la conmutación por error (*failover*).

---

## Seguridad

Amazon RDS incorpora distintos mecanismos para proteger las bases de datos.

Entre ellos se encuentran:

- Aislamiento mediante Amazon VPC.
- Control de acceso mediante AWS Identity and Access Management (IAM).
- Cifrado de los datos almacenados.
- Cifrado de las conexiones mediante SSL/TLS.

Estos mecanismos ayudan a proteger tanto los datos almacenados como las comunicaciones con la base de datos.

---

## Copias de seguridad

Amazon RDS proporciona dos mecanismos para proteger la información.

### Copias de seguridad automáticas

Permiten restaurar la base de datos a un momento determinado dentro del período de retención configurado.

### Instantáneas (Snapshots)

Las instantáneas son copias de seguridad iniciadas manualmente por el usuario.

Permanecen disponibles hasta que se eliminan explícitamente y pueden utilizarse para crear nuevas instancias de base de datos.

---

## Buenas prácticas

AWS recomienda:

- Seleccionar la clase de instancia adecuada para la carga de trabajo.
- Elegir el tipo de almacenamiento que mejor se adapte a los requisitos de rendimiento.
- Utilizar implementaciones **Multi-AZ** cuando se requiera alta disponibilidad.
- Configurar copias de seguridad automáticas y realizar instantáneas cuando sea necesario.
- Aplicar controles de seguridad para proteger el acceso a la base de datos y los datos almacenados.

---
