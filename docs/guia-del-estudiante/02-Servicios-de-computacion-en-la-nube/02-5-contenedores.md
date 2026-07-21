# Servicios de contenedores de AWS

Los contenedores permiten empaquetar una aplicación junto con todas sus dependencias en una unidad estandarizada, facilitando su despliegue y ejecución en diferentes entornos.

AWS ofrece servicios para ejecutar y administrar aplicaciones basadas en contenedores.

---

## Máquinas virtuales y contenedores

```text
              Máquinas virtuales                  Contenedores

        ┌───────────────────────┐          ┌───────────────────────┐
        │ Aplicación            │          │ Aplicación            │
        ├───────────────────────┤          ├───────────────────────┤
        │ Sistema operativo     │          │                       │
        │ invitado              │          │      Contenedor       │
        ├───────────────────────┤          ├───────────────────────┤
        │ Hipervisor            │          │ Motor de contenedores │
        ├───────────────────────┤          ├───────────────────────┤
        │ Sistema operativo     │          │ Sistema operativo     │
        │ anfitrión             │          │ anfitrión             │
        ├───────────────────────┤          ├───────────────────────┤
        │ Servidor              │          │ Servidor              │
        └───────────────────────┘          └───────────────────────┘
```

---

Un contenedor es una unidad estandarizada que incluye el código de una aplicación y sus dependencias.

A diferencia de las máquinas virtuales, los contenedores:

- Comparten el sistema operativo y el núcleo (*kernel*) del servidor anfitrión.
- Se inician en cuestión de segundos.
- Facilitan el mantenimiento y el despliegue de aplicaciones.
- Permiten ejecutar una misma aplicación de forma consistente en distintos entornos.

Un ejemplo de plataforma de contenedores es **Docker**.

En el caso de las máquinas virtuales, la virtualización se realiza mediante un **hipervisor**, que puede ser:

- **Tipo 1 (bare-metal):** se ejecuta directamente sobre el hardware.
- **Tipo 2 (hosted):** se ejecuta sobre un sistema operativo.

---

## Servicios de orquestación de contenedores

AWS proporciona dos servicios para administrar aplicaciones basadas en contenedores:

```text
                  Servicios de contenedores de AWS

                           Contenedores
                                │
                ┌───────────────┴───────────────┐
                │                               │
                ▼                               ▼
         Amazon ECS                     Amazon EKS
                │                               │
      Ejecuta y escala             Ejecuta y escala
      aplicaciones en              aplicaciones en
      contenedores                 Kubernetes
```

---

### Amazon Elastic Container Service (Amazon ECS)

Amazon ECS es un servicio de orquestación de contenedores altamente escalable y de alto rendimiento.

Permite:

- Ejecutar aplicaciones en contenedores.
- Escalar aplicaciones basadas en contenedores.
- Administrar aplicaciones compatibles con Docker mediante llamadas a la API.

Amazon ECS admite contenedores Docker.

---

### Amazon Elastic Kubernetes Service (Amazon EKS)

Amazon EKS es un servicio administrado que permite ejecutar aplicaciones basadas en Kubernetes.

Permite:

- Ejecutar y escalar aplicaciones Kubernetes.
- Automatizar el aprovisionamiento de nodos.
- Automatizar el parcheo y las actualizaciones.
- Crear clústeres altamente disponibles y seguros.

---
