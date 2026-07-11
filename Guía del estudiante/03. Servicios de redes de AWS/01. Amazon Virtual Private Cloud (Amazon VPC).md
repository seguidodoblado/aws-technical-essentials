# Amazon Virtual Private Cloud (Amazon VPC)

**Amazon Virtual Private Cloud (Amazon VPC)** permite crear una red virtual aislada dentro de AWS donde desplegar y administrar recursos de forma segura.

Una VPC proporciona control sobre la configuración de la red, incluyendo el rango de direcciones IP, las subredes, las tablas de enrutamiento y los mecanismos de seguridad.

---

## Arquitectura básica de una Amazon VPC

```text
                    Región AWS
                        │
                        ▼
                    Amazon VPC
                        │
                        ▼
┌─────────────────────────────────────────────────────┐
│                                                     │
│ Availability Zone A        Availability Zone B      │
│ ┌─────────────────────┐    ┌─────────────────────┐  │
│ │ Subred pública      │    │ Subred pública      │  │
│ │                     │    │                     │  │
│ │ Subred privada EC2  │    │ Subred privada EC2  │  │
│ │                     │    │                     │  │
│ │ Subred privada DB   │    │ Subred privada DB   │  │
│ └─────────────────────┘    └─────────────────────┘  │
│                                                     │
└─────────────────────────────────────────────────────┘
```

Todos los recursos que se crean dentro de una Amazon VPC se comunican utilizando la red privada definida para esa VPC.

---

## Características principales

Amazon VPC permite:

- Crear una red virtual aislada dentro de AWS.
- Definir el rango de direcciones IP de la red.
- Crear una o varias subredes.
- Configurar tablas de enrutamiento.
- Controlar el tráfico mediante mecanismos de seguridad.

---

## Componentes de una VPC

Una Amazon VPC puede incluir diferentes componentes de red, entre ellos:

- Subredes.
- Tablas de rutas.
- Puertas de enlace (*Gateways*).
- Grupos de seguridad (*Security Groups*).
- Listas de control de acceso a la red (*Network Access Control Lists* o **NACL**).

Estos componentes trabajan conjuntamente para controlar la conectividad y proteger los recursos desplegados en la red.

---
