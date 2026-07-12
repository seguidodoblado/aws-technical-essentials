# Clases de almacenamiento de Amazon S3

Amazon S3 ofrece distintas clases de almacenamiento para adaptarse a diferentes requisitos de disponibilidad, frecuencia de acceso y coste.

---

## Clases de almacenamiento

| Clase | Uso principal |
| :----- | :------------ |
| **S3 Standard** | Datos a los que se accede con frecuencia. |
| **S3 Standard-Infrequent Access (S3 Standard-IA)** | Datos a los que se accede con poca frecuencia, pero que requieren acceso rápido cuando es necesario. |
| **S3 One Zone-Infrequent Access (S3 One Zone-IA)** | Datos a los que se accede con poca frecuencia y que pueden almacenarse en una única Availability Zone. |
| **S3 Intelligent-Tiering** | Datos con patrones de acceso desconocidos o cambiantes. |
| **S3 Glacier Instant Retrieval** | Datos archivados que necesitan recuperarse inmediatamente. |
| **S3 Glacier Flexible Retrieval** | Datos archivados cuyo tiempo de recuperación puede variar desde minutos hasta horas. |
| **S3 Glacier Deep Archive** | Datos archivados a largo plazo a los que se accede muy raramente. |

---

## Comparativa

```text
Acceso frecuente
        │
        ▼
S3 Standard
        │
        ▼
S3 Intelligent-Tiering
        │
        ▼
S3 Standard-IA
        │
        ▼
S3 One Zone-IA
        │
        ▼
S3 Glacier Instant Retrieval
        │
        ▼
S3 Glacier Flexible Retrieval
        │
        ▼
S3 Glacier Deep Archive
        ▲
Acceso muy poco frecuente
```

---

## Características

### Amazon S3 Standard

- Diseñado para datos a los que se accede con frecuencia.
- Baja latencia.
- Alto rendimiento.
- Alta disponibilidad.

---

### Amazon S3 Standard-Infrequent Access (S3 Standard-IA)

- Para datos a los que se accede con poca frecuencia.
- Acceso rápido cuando es necesario.
- Menor coste de almacenamiento que S3 Standard.

---

### Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)

- Almacena los datos en una única Availability Zone.
- Adecuado para datos que pueden recrearse si se pierden.

---

### Amazon S3 Intelligent-Tiering

- Optimiza automáticamente los costes.
- Mueve los objetos entre niveles de acceso según su patrón de utilización.

---

### Amazon S3 Glacier Instant Retrieval

- Archivo de bajo coste.
- Recuperación inmediata de los datos.

---

### Amazon S3 Glacier Flexible Retrieval

- Archivo de muy bajo coste.
- Recuperación configurable desde minutos hasta horas.

---

### Amazon S3 Glacier Deep Archive

- Menor coste de almacenamiento.
- Diseñado para archivado a muy largo plazo.
- Recuperación en un plazo aproximado de 12 horas.

---
