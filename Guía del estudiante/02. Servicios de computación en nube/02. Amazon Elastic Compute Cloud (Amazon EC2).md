# Amazon Elastic Compute Cloud (Amazon EC2)

**Amazon Elastic Compute Cloud (Amazon EC2)** es el servicio de AWS que proporciona capacidad informática escalable mediante máquinas virtuales, denominadas **instancias**.

Permite ejecutar aplicaciones en la nube con un control muy similar al de un servidor físico, pero con la flexibilidad de aprovisionar y liberar recursos cuando sea necesario.

---

## Características principales

```text
                     Amazon EC2

               ┌──────────────────────┐
               │      Instancia EC2   │
               └──────────┬───────────┘
                          │
      ┌───────────────────┼────────────────────┐
      │                   │                    │
      ▼                   ▼                    ▼
 Seguridad        Rendimiento         Escalabilidad
```

---

Amazon EC2 ofrece las siguientes capacidades:

- Capacidad informática segura y redimensionable.
- Control completo sobre la instancia.
- Escalado rápido según las necesidades de la aplicación.

---

## Amazon Machine Image (AMI)

Antes de lanzar una instancia es necesario seleccionar una **Amazon Machine Image (AMI)**.

Una AMI contiene la información necesaria para crear una instancia EC2.

```text
                  Amazon Machine Image (AMI)

                ┌──────────────────────────┐
                │           AMI            │
                └─────────────┬────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
        ▼                     ▼                     ▼
 Sistema operativo      Configuración        Aplicaciones
```

Una AMI puede incluir:

- Sistema operativo.
- Configuración del sistema.
- Software adicional.
- Aplicaciones.

AWS proporciona AMIs preconfiguradas, aunque también es posible crear imágenes personalizadas.

---

## Tipos y tamaños de instancia

Las instancias EC2 se clasifican según su **familia** y su **tamaño**.

```text
                Instancia EC2

             m5.4xlarge
             │ │ └──── Tamaño
             │ └────── Generación
             └──────── Familia
```

La familia determina el tipo de recursos que ofrece la instancia, mientras que el tamaño define la cantidad de CPU, memoria y otros recursos disponibles.

AWS dispone de diferentes familias de instancias optimizadas para distintos tipos de cargas de trabajo.

---
