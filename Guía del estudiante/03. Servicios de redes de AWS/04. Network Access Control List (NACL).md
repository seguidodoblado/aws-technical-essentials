# Network Access Control Lists (NACL)

Una **Network Access Control List (NACL)** es una capa de seguridad opcional que controla el tráfico de red que entra y sale de una o varias subredes de una **Amazon Virtual Private Cloud (Amazon VPC)**.

Las NACL permiten definir reglas para permitir o denegar el tráfico en función de distintos criterios, como la dirección IP, el protocolo o el puerto.

---

## Funcionamiento

```text
                    Amazon VPC
                         │
            ┌────────────┴────────────┐
            │                         │
            ▼                         ▼
      Network ACL               Network ACL
            │                         │
      ┌─────┴─────┐             ┌─────┴─────┐
      │ Subred A  │             │ Subred B  │
      └───────────┘             └───────────┘
```

Las reglas de una NACL se aplican a todo el tráfico que entra y sale de la subred asociada.

---

## Reglas de entrada y salida

Cada Network ACL dispone de dos conjuntos independientes de reglas:

- **Reglas de entrada (Inbound rules):** controlan el tráfico que entra en la subred.
- **Reglas de salida (Outbound rules):** controlan el tráfico que sale de la subred.

Cada regla puede:

- Permitir el tráfico.
- Denegar el tráfico.

Las reglas se evalúan en orden numérico, desde el número más bajo hasta el más alto.

La primera regla que coincide con el tráfico determina si este se permite o se deniega.

---

## Características

Las Network ACL:

- Actúan a nivel de subred.
- Controlan el tráfico de entrada y salida.
- Permiten definir reglas de permiso y denegación.
- Se aplican a todos los recursos de la subred asociada.

---
