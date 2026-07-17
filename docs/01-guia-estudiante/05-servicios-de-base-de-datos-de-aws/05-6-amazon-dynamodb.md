# Amazon DynamoDB

**Amazon DynamoDB** es un servicio de base de datos NoSQL completamente administrado que proporciona un rendimiento rápido y predecible con escalado prácticamente ilimitado.

Está diseñado para aplicaciones que requieren baja latencia y un elevado número de solicitudes por segundo.

---

## Estructura de Amazon DynamoDB

Los datos en Amazon DynamoDB se organizan mediante tablas.

Cada tabla contiene **elementos (Items)** y cada elemento está formado por uno o varios **atributos (Attributes)**.

```text
                 Amazon DynamoDB
                        │
                        ▼
                     Tabla
                        │
          ┌─────────────┴─────────────┐
          │                           │
          ▼                           ▼
      Item (Elemento)            Item (Elemento)
          │                           │
      ┌───┴───┐                   ┌───┴───┐
      ▼       ▼                   ▼       ▼
  Atributo A Atributo B      Atributo A Atributo B
```

---

## Tablas

Una tabla almacena una colección de elementos relacionados.

Cada tabla debe disponer de una clave primaria que identifique de forma única cada elemento.

---

## Elementos (Items)

Un elemento representa un único registro almacenado en una tabla.

Cada elemento está formado por uno o varios atributos.

Aunque dos elementos pertenezcan a la misma tabla, no es necesario que tengan exactamente los mismos atributos.

---

## Atributos (Attributes)

Los atributos contienen la información almacenada en cada elemento.

Cada atributo está formado por un nombre y un valor.

---

## Clave primaria

Amazon DynamoDB utiliza una **clave primaria (Primary Key)** para identificar de forma única cada elemento de una tabla.

La clave primaria puede estar formada por:

- Una **clave de partición (Partition Key)**.
- Una **clave de partición y una clave de ordenación (Sort Key)**.

### Clave de partición

La clave de partición determina la partición física donde se almacenará un elemento.

Todos los elementos con el mismo valor de clave de partición se almacenan juntos.

### Clave de ordenación

La clave de ordenación permite almacenar varios elementos con la misma clave de partición y ordenarlos según el valor de dicha clave.

La combinación de la clave de partición y la clave de ordenación identifica de forma única cada elemento.

---
