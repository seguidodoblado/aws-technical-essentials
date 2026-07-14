# Bases de datos relacionales

Una **base de datos relacional** es una colección de registros organizados como un conjunto de tablas compuestas por filas y columnas.

Cada fila contiene información sobre un registro y cada columna contiene un atributo de ese registro.

---

## Estructura de una base de datos relacional

```text
                   Tabla: Cursos
        ┌──────────┬──────────────┬────────────┐
        │ Course_ID│ Título       │ Estado     │
        ├──────────┼──────────────┼────────────┤
        │ 21       │ Cloud Comp.  │ Activo     │
        └──────────┴──────────────┴────────────┘
              ▲
              │ Clave primaria (Primary Key)
              │
     ┌────────┴────────┐
     │                 │
     ▼                 ▼

 Tabla: Libros      Tabla: Instructores
┌──────────────┐    ┌────────────────────┐
│ Books_ID     │    │ ID                 │
│ Introducción │    │ Martha Rivera      │
│ Course_ID=21 │    │ Course_ID=21       │
└──────────────┘    └────────────────────┘
         ▲                   ▲
         └─────────┬─────────┘
                   │
            Clave foránea
            (Foreign Key)
```

En una base de datos relacional:

- Cada fila representa un registro.
- Cada columna representa un atributo del registro.
- Cada registro dispone de un identificador único denominado **clave primaria (Primary Key)**.
- Un registro de otra tabla puede hacer referencia a esa clave mediante una **clave foránea (Foreign Key)**.

En el ejemplo del curso:

- La primera tabla contiene los cursos.
- La segunda tabla contiene los libros del curso.
- La tercera tabla contiene los instructores del curso.

Las tres tablas están relacionadas mediante el campo **Course_ID**.

---

## Beneficios

Las bases de datos relacionales ofrecen, entre otros, los siguientes beneficios:

- SQL para realizar consultas.
- Reducción de la redundancia de datos.
- Modelo ampliamente conocido.
- Cumplimiento de las propiedades **ACID**.

---

### SQL

El lenguaje utilizado para consultar una base de datos relacional es **Structured Query Language (SQL)**.

SQL permite consultar y administrar la información almacenada en las tablas.

---

### Reducción de la redundancia

La información relacionada se almacena una única vez y se reutiliza mediante las relaciones entre tablas.

Esto evita almacenar repetidamente los mismos datos y reduce el riesgo de inconsistencias.

---

### Familiaridad

Las bases de datos relacionales se utilizan desde la década de 1970 y constituyen uno de los modelos de bases de datos más conocidos y utilizados.

---

### Propiedades ACID

Las bases de datos relacionales garantizan la integridad de la información mediante las propiedades **ACID**:

- **Atomicidad (Atomicity)**.
- **Consistencia (Consistency)**.
- **Aislamiento (Isolation)**.
- **Durabilidad (Durability)**.

---
