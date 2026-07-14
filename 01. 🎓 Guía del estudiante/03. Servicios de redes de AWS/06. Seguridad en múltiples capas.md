# Seguridad en múltiples capas

La seguridad en una **Amazon Virtual Private Cloud (Amazon VPC)** se basa en varias capas que trabajan conjuntamente para proteger los recursos desplegados.

Cada componente desempeña una función específica dentro de la arquitectura de red.

---

## Arquitectura de seguridad

```text
                          Internet
                              │
                              ▼
                     Internet Gateway
                              │
                              ▼
                    ┌──────────────────┐
                    │    Amazon VPC    │
                    └────────┬─────────┘
                             │
              ┌──────────────┴──────────────┐
              │                             │
              ▼                             ▼
       Availability Zone A          Availability Zone B
              │                             │
      ┌───────┴────────┐           ┌────────┴───────┐
      │                │           │                │
      ▼                ▼           ▼                ▼
  Network ACL      Network ACL Network ACL      Network ACL
      │                │           │                │
      ▼                ▼           ▼                ▼
  Subred pública  Subred privada Subred pública  Subred privada
      │                │           │                │
      ▼                ▼           ▼                ▼
Security Group  Security Group Security Group  Security Group
      │                │           │                │
      ▼                ▼           ▼                ▼
 Instancia EC2     Base de datos Instancia EC2   Base de datos
```

---

## Capas de seguridad

La arquitectura de una Amazon VPC utiliza varias capas de protección:

- **Network Access Control Lists (NACL)** controlan el tráfico de las subredes.
- **Security Groups** controlan el tráfico de los recursos individuales.
- Las distintas capas trabajan conjuntamente para proteger la infraestructura desplegada dentro de la VPC.

---

## Buenas prácticas

Al diseñar la seguridad de una Amazon VPC se recomienda:

- Aplicar varias capas de protección.
- Utilizar Security Groups para controlar el acceso a los recursos.
- Utilizar Network ACL para controlar el tráfico de las subredes.
- Aplicar el principio del mínimo privilegio.
- Revisar periódicamente las reglas de seguridad.

---
