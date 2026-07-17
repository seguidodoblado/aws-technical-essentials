# Características de Amazon DynamoDB

Amazon DynamoDB incorpora diversas características que permiten optimizar el rendimiento, mejorar la flexibilidad de las consultas y facilitar la integración con otras aplicaciones y servicios de AWS.

---

## Índices secundarios

Los **índices secundarios (Secondary Indexes)** permiten realizar consultas utilizando atributos distintos de la clave primaria de la tabla.

Amazon DynamoDB admite dos tipos de índices secundarios:

- **Índice secundario global (Global Secondary Index - GSI)**.
- **Índice secundario local (Local Secondary Index - LSI)**.

### Índice secundario global (GSI)

Un índice secundario global puede utilizar una clave de partición y una clave de ordenación diferentes de las definidas en la tabla principal.

Permite realizar consultas utilizando distintos atributos sin modificar la estructura de la tabla.

### Índice secundario local (LSI)

Un índice secundario local comparte la misma clave de partición que la tabla principal, pero puede utilizar una clave de ordenación diferente.

Permite realizar consultas alternativas sobre los elementos pertenecientes a una misma partición.

---

## Modelos de consistencia

Amazon DynamoDB admite dos modelos de consistencia para las operaciones de lectura.

### Lectura con consistencia eventual (Eventually Consistent Read)

Es el modelo utilizado de forma predeterminada.

Los datos devueltos pueden no reflejar inmediatamente la actualización más reciente.

### Lectura con consistencia fuerte (Strongly Consistent Read)

Garantiza que la lectura devuelve siempre la información más reciente almacenada en la tabla.

---

## DynamoDB Accelerator (DAX)

**Amazon DynamoDB Accelerator (DAX)** es un servicio de almacenamiento en caché en memoria totalmente administrado y compatible con Amazon DynamoDB.

Su objetivo es reducir la latencia de lectura y mejorar el rendimiento de aplicaciones con un elevado número de consultas.

```text
             Aplicación
                  │
                  ▼
                DAX
                  │
                  ▼
          Amazon DynamoDB
```

---

## DynamoDB Streams

**Amazon DynamoDB Streams** captura los cambios realizados sobre los elementos de una tabla.

Cada vez que un elemento se crea, modifica o elimina, el cambio queda registrado en el flujo de eventos.

Esto permite que otras aplicaciones o servicios procesen dichos cambios de forma automática.

```text
          Amazon DynamoDB
                  │
        Crear / Modificar / Eliminar
                  │
                  ▼
          DynamoDB Streams
                  │
                  ▼
     Aplicaciones y servicios
```

---
