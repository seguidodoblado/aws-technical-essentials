# Bases de datos administradas

Las bases de datos pueden desplegarse en diferentes entornos, lo que determina quién es responsable de las tareas de administración.

AWS permite ejecutar bases de datos en instancias Amazon EC2 o utilizar servicios de bases de datos completamente administrados.

---

## Comparación de modelos de administración

```text
                     Administración de bases de datos

                                 │
        ┌────────────────────────┼─────────────────────────┐
        │                        │                         │
        ▼                        ▼                         ▼
   On-premises             Amazon EC2          Servicio administrado
        │                        │                         │
 Cliente gestiona         AWS gestiona          AWS gestiona
 la infraestructura       la infraestructura    la infraestructura
 física                   física                física

 Cliente gestiona         Cliente gestiona      Cliente solo gestiona
 la base de datos         la base de datos      los datos y la aplicación
```

---

## Base de datos on-premises

Cuando una base de datos se ejecuta en las instalaciones del cliente, este es responsable de administrar todos los aspectos de la infraestructura y de la propia base de datos.

Entre estas responsabilidades se incluyen:

- Optimización.
- Alta disponibilidad.
- Copias de seguridad.
- Parches e instalaciones del software de la base de datos.
- Mantenimiento del sistema operativo.
- Virtualización.
- Servidores.
- Almacenamiento.
- Redes.
- Centro de datos.

---

## Base de datos en Amazon EC2

Cuando la base de datos se ejecuta en una instancia Amazon EC2, AWS administra la infraestructura física.

El cliente continúa siendo responsable de administrar la base de datos, incluyendo:

- Optimización.
- Alta disponibilidad.
- Copias de seguridad.
- Parches e instalaciones del software de la base de datos.
- Mantenimiento del sistema operativo.

AWS es responsable de:

- Virtualización.
- Servidores.
- Almacenamiento.
- Redes.
- Centro de datos.

---

## Base de datos administrada por AWS

Cuando la base de datos utiliza un servicio administrado de AWS, el cliente únicamente es responsable de:

- Los datos.
- La aplicación.

AWS administra:

- Optimización.
- Alta disponibilidad.
- Copias de seguridad.
- Parches e instalaciones del software de la base de datos.
- Mantenimiento del sistema operativo.
- Virtualización.
- Servidores.
- Almacenamiento.
- Redes.
- Centro de datos.

---
