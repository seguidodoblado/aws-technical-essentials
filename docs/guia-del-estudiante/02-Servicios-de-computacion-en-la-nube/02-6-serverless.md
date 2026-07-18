# Computación sin servidor (Serverless)

La **computación sin servidor (serverless)** es un modelo de ejecución en el que AWS administra la infraestructura necesaria para ejecutar una aplicación.

Con este enfoque, no es necesario aprovisionar ni administrar servidores. El desarrollador únicamente proporciona el código de la aplicación y AWS se encarga de su ejecución.

AWS ofrece servicios de computación sin servidor como **AWS Lambda** y **AWS Fargate**.

---

## Ventajas

```text
              Computación sin servidor

                    Serverless
                         │
          ┌──────────────┴──────────────┐
          │                             │
          ▼                             ▼
     AWS Lambda                  AWS Fargate

                Beneficios

        • Sin administración de servidores
        • Escalado según la demanda
        • Pago únicamente por el uso
        • Alta disponibilidad integrada
        • Tolerancia a fallos integrada
```

Las principales ventajas de la computación sin servidor son:

- No es necesario aprovisionar ni administrar servidores.
- Escala automáticamente según la carga de trabajo.
- Solo se paga por los recursos consumidos.
- La alta disponibilidad y la tolerancia a fallos están integradas en el servicio.

---

## AWS Lambda

**AWS Lambda** es un servicio de computación que permite ejecutar código sin aprovisionar ni administrar servidores.

Con AWS Lambda únicamente es necesario cargar el código de la aplicación. AWS Lambda administra automáticamente la infraestructura necesaria para ejecutar ese código.

---

### Funcionamiento

```text
                 Funcionamiento de AWS Lambda

┌──────────────┐     Invocación      ┌──────────────┐
│ Origen del   │ ─────────────────▶ │  AWS Lambda  │
│ evento       │                    └──────┬───────┘
└──────────────┘                           │
                                           │ Ejecuta
                                           ▼
                                    Código de la función
                                           │
                                           ▼
                                   ┌────────────────┐
                                   │ Servicio       │
                                   │ externo        │
                                   └────────────────┘
```

---

### Conceptos fundamentales

Antes de utilizar AWS Lambda es importante comprender los siguientes conceptos:

- **Origen del evento (Event source):** desencadena la ejecución de la función.
- **Lenguaje de programación:** lenguaje utilizado para desarrollar la función.
- **Rol de ejecución:** permisos que la función necesita para acceder a recursos de AWS.

---

### Funciones Lambda

El código que ejecuta AWS Lambda se denomina **función Lambda**.

Cada función incluye su propia configuración, como:

- Nombre.
- Descripción.
- Punto de entrada.
- Recursos necesarios.

Las funciones Lambda se ejecutan en un entorno aislado administrado por AWS y están diseñadas para responder a eventos.

---
