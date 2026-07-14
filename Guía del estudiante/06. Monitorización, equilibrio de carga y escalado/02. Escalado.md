# Escalado

El escalado permite adaptar automáticamente la capacidad de una aplicación para responder a los cambios en la demanda.

AWS proporciona **Amazon EC2 Auto Scaling** para ajustar el número de instancias Amazon EC2 en función de las necesidades de la carga de trabajo.

---

## Tipos de escalado

Existen dos formas principales de aumentar la capacidad de una aplicación.

### Escalado vertical (Vertical Scaling)

Consiste en aumentar los recursos de una única instancia, por ejemplo:

- Más CPU.
- Más memoria.
- Mayor capacidad de almacenamiento.

```text
        Escalado vertical

      ┌───────────────┐
      │   EC2 grande  │
      │ CPU ↑         │
      │ RAM ↑         │
      └───────────────┘
```

### Escalado horizontal (Horizontal Scaling)

Consiste en aumentar el número de instancias que ejecutan la aplicación.

```text
        Escalado horizontal

      ┌──────┐
      │ EC2  │
      └──────┘

             │

             ▼

 ┌──────┐ ┌──────┐ ┌──────┐
 │ EC2  │ │ EC2  │ │ EC2  │
 └──────┘ └──────┘ └──────┘
```

---

## Amazon EC2 Auto Scaling

Amazon EC2 Auto Scaling supervisa la carga de trabajo y ajusta automáticamente el número de instancias Amazon EC2.

Su objetivo es:

- Mantener el rendimiento de la aplicación.
- Adaptarse a los cambios en la demanda.
- Optimizar el coste de la infraestructura.

---

## Launch Templates

Un **Launch Template** define la configuración que utilizarán las nuevas instancias Amazon EC2.

Puede incluir, entre otros:

- Amazon Machine Image (AMI).
- Tipo de instancia.
- Par de claves.
- Grupos de seguridad.
- Configuración de almacenamiento.
- Scripts de inicialización.

El Launch Template sirve como plantilla para crear nuevas instancias de forma consistente.

---

## Auto Scaling Groups

Un **Auto Scaling Group (ASG)** administra un conjunto de instancias Amazon EC2.

Permite definir:

- Número mínimo de instancias.
- Capacidad deseada.
- Número máximo de instancias.

Amazon EC2 Auto Scaling mantiene automáticamente el número de instancias dentro de esos límites.

```text
               Auto Scaling Group

             Mínimo: 2 instancias
             Deseado: 3 instancias
             Máximo: 6 instancias

        ┌──────┐  ┌──────┐  ┌──────┐
        │ EC2  │  │ EC2  │  │ EC2  │
        └──────┘  └──────┘  └──────┘
```

---

## Políticas de escalado

Las **políticas de escalado (Scaling Policies)** determinan cuándo Amazon EC2 Auto Scaling debe añadir o eliminar instancias.

Estas políticas pueden basarse en métricas de Amazon CloudWatch.

Por ejemplo:

- Aumentar el número de instancias cuando la utilización de CPU supera un determinado umbral.
- Reducir el número de instancias cuando la utilización disminuye.

---

## Beneficios de Amazon EC2 Auto Scaling

Amazon EC2 Auto Scaling permite:

- Ajustar automáticamente la capacidad según la demanda.
- Mejorar la disponibilidad de las aplicaciones.
- Optimizar el uso de los recursos.
- Reducir costes al ejecutar únicamente las instancias necesarias.

---
