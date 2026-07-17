# Almacenamiento de archivos

El **almacenamiento de archivos (File Storage)** organiza los datos mediante un sistema de archivos jerárquico y permite que varios clientes accedan simultáneamente al mismo sistema de archivos.

AWS proporciona **Amazon Elastic File System (Amazon EFS)** como servicio de almacenamiento de archivos completamente administrado.

---

## Arquitectura

```text
          Amazon EFS
               │
      ┌────────┴────────┐
      │                 │
      ▼                 ▼
 Instancia EC2     Instancia EC2
      │                 │
      └────────┬────────┘
               │
      Sistema de archivos
          compartido
```

Varias instancias de Amazon EC2 pueden montar simultáneamente el mismo sistema de archivos Amazon EFS.

---

## Amazon Elastic File System (Amazon EFS)

Amazon EFS proporciona un sistema de archivos compartido y elástico para utilizar con servicios de AWS y recursos locales.

Entre sus características se encuentran:

- Servicio completamente administrado.
- Escalado automático de la capacidad de almacenamiento.
- Acceso simultáneo desde varias instancias.
- Compatible con el protocolo **NFS (Network File System)**.

---

## Casos de uso

Amazon EFS es adecuado para:

- Sistemas de gestión de contenido.
- Entornos de desarrollo.
- Aplicaciones web.
- Directorios compartidos.
- Plataformas de análisis de datos.

---

## Amazon FSx

AWS también ofrece **Amazon FSx**, un conjunto de servicios de almacenamiento de archivos administrados compatibles con distintos sistemas de archivos especializados.

---
