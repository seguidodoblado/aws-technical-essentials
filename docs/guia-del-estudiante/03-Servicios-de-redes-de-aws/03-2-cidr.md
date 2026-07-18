# Classless Inter-Domain Routing (CIDR)

**Classless Inter-Domain Routing (CIDR)** es un método para definir rangos de direcciones IP mediante una dirección de red y una longitud de prefijo.

AWS utiliza la notación CIDR para definir el rango de direcciones IP de una **Amazon Virtual Private Cloud (Amazon VPC)** y de las subredes que contiene.

---

## Ejemplo de organización mediante CIDR

```text
                 Amazon VPC
              10.0.0.0/16
                    │
      ┌─────────────┴─────────────┐
      │                           │
      ▼                           ▼
 Availability Zone A      Availability Zone B
      │                           │
 ┌────┴────┐                 ┌────┴────┐
 ▼         ▼                 ▼         ▼
10.0.1.0/24 10.0.2.0/24 10.0.3.0/24 10.0.4.0/24
 Subred       Subred      Subred       Subred
 pública      privada     pública      privada
```

En este ejemplo:

- La VPC utiliza el bloque CIDR `10.0.0.0/16`.
- Cada subred utiliza un bloque CIDR incluido dentro del bloque de la VPC.
- Cada subred pertenece a una única **Availability Zone**.

---

## Notación CIDR

Un bloque CIDR se representa mediante una dirección IP seguida de una barra (`/`) y un número que indica la longitud del prefijo.

Ejemplos:

| Bloque CIDR | Descripción |
| :---------: | :---------- |
| `10.0.0.0/16` | Define el rango de direcciones IP de una VPC. |
| `10.0.1.0/24` | Define el rango de direcciones IP de una subred. |

---

## Uso en Amazon VPC

Al crear una Amazon VPC es necesario especificar un bloque CIDR.

A partir de este bloque se crean posteriormente las distintas subredes de la VPC.

Cada subred utiliza un bloque CIDR que debe estar comprendido dentro del bloque CIDR de la VPC.

---

## Consideraciones

- Cada Amazon VPC dispone de un bloque CIDR propio.
- Las subredes utilizan bloques CIDR derivados del bloque de la VPC.
- Cada subred pertenece a una única Availability Zone.
- El tamaño del bloque CIDR determina el rango de direcciones IP disponible.

---
