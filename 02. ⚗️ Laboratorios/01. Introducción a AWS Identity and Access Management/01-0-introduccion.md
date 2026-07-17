# Introducción

Este laboratorio introduce los conceptos básicos de **AWS Identity and Access Management (IAM)** mediante la creación y configuración de identidades y permisos dentro de una cuenta de AWS.

A lo largo del laboratorio se aprenderá a administrar el acceso a los recursos de AWS utilizando usuarios, grupos y políticas de permisos, aplicando el modelo de control de acceso proporcionado por IAM.

---

## Arquitectura

Este laboratorio utiliza principalmente el servicio **AWS Identity and Access Management (IAM)** para gestionar identidades y permisos dentro de una cuenta de AWS.

Al tratarse de un laboratorio centrado en la administración de identidades, no se despliega una arquitectura de infraestructura como en los laboratorios posteriores.

El flujo general del laboratorio es el siguiente:

```text
        Usuario
            │
            ▼
     AWS Management Console
            │
            ▼
 AWS Identity and Access Management
            │
     ┌──────┴──────┐
     ▼             ▼
  Usuarios      Grupos
                     │
                     ▼
                 Políticas
                     │
                     ▼
            Acceso a recursos AWS
```

---

## Servicios utilizados

- AWS Identity and Access Management (IAM)

---

## Objetivo del laboratorio

Al finalizar este laboratorio el estudiante será capaz de comprender cómo AWS gestiona la autenticación y la autorización mediante IAM, así como crear y administrar usuarios, grupos y políticas de permisos siguiendo las prácticas propuestas durante el ejercicio.

---
