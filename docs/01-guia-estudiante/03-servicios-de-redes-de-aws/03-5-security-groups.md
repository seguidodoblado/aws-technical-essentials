# Security Groups

Un **Security Group** actúa como un firewall virtual que controla el tráfico permitido hacia y desde un recurso de AWS, como una instancia de Amazon EC2.

Cada Security Group está formado por un conjunto de reglas que especifican qué tráfico está permitido.

---

## Funcionamiento

```text
                   Amazon VPC
                        │
                  ┌─────┴─────┐
                  │  Subred   │
                  └─────┬─────┘
                        │
                 ┌──────▼──────┐
                 │ Security    │
                 │   Group     │
                 └──────┬──────┘
                        │
                        ▼
                  Instancia EC2
```

Los Security Groups se asocian directamente a los recursos de AWS que deben proteger.

---

## Reglas

Un Security Group contiene dos conjuntos de reglas:

- **Reglas de entrada (Inbound rules):** controlan el tráfico que puede llegar al recurso.
- **Reglas de salida (Outbound rules):** controlan el tráfico que puede salir del recurso.

Las reglas permiten definir el tráfico autorizado utilizando distintos criterios, como:

- Protocolo.
- Puerto.
- Dirección IP de origen o destino.

---

## Características

Los Security Groups:

- Actúan a nivel de recurso.
- Controlan el tráfico de entrada y salida.
- Se asocian directamente a los recursos que protegen.
- Permiten definir reglas para autorizar el tráfico de red.

---
