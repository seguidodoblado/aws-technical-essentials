# Tipos de almacenamiento

AWS ofrece tres tipos principales de almacenamiento, cada uno diseñado para satisfacer diferentes necesidades.

## Diagrama de tipos de almacenamiento

```text
                     Almacenamiento AWS
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
        ▼                    ▼                    ▼
 Almacenamiento        Almacenamiento      Almacenamiento
    en bloques          de archivos          de objetos
   (Block Storage)      (File Storage)      (Object Storage)
```

---

### Almacenamiento en bloques

Los datos se almacenan en bloques de tamaño fijo.

Está diseñado para aplicaciones que requieren acceso frecuente y de baja latencia a los datos.

---

### Almacenamiento de archivos

Los datos se organizan mediante un sistema de archivos jerárquico.

Permite que varios clientes accedan simultáneamente al mismo sistema de archivos.

---

### Almacenamiento de objetos

Los datos se almacenan como objetos dentro de un contenedor.

Cada objeto incluye tanto los datos como la información descriptiva asociada.

---
