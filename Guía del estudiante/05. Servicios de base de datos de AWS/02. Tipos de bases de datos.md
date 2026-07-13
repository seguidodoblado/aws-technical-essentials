# Tipos de bases de datos

AWS ofrece distintos tipos de bases de datos, cada uno diseñado para un caso de uso específico.

---

## Diagrama de tipos de bases de datos

```text
                    Bases de datos
                           │
     ┌──────────┬──────────┬──────────┬──────────┐
     │          │          │          │          │
     ▼          ▼          ▼          ▼          ▼
 Relacional Documento Clave-valor  En memoria  Grafos
     │
     ├──────────┬──────────┐
     ▼          ▼          ▼
 Serie temporal  Ledger   Wide column
```

---

### Base de datos relacional

Almacena los datos en tablas relacionadas entre sí.

Se utiliza para aplicaciones que requieren integridad de los datos y consultas mediante SQL.

---

### Base de datos clave-valor

Almacena los datos como pares de clave y valor.

Está diseñada para aplicaciones que necesitan un acceso muy rápido a la información.

---

### Base de datos documental

Almacena la información en documentos.

Es adecuada para datos semiestructurados y modelos de datos flexibles.

---

### Base de datos en memoria

Mantiene los datos en memoria para proporcionar tiempos de respuesta muy bajos.

Se utiliza cuando la velocidad de acceso es un requisito fundamental.

---

### Base de datos de grafos

Representa los datos mediante nodos y relaciones.

Está diseñada para analizar relaciones complejas entre grandes volúmenes de información.

---

### Base de datos de series temporales

Optimizada para almacenar datos asociados al tiempo.

Es adecuada para métricas, registros, sensores y monitorización.

---

### Base de datos ledger

Mantiene un registro inmutable y verificable de las transacciones.

Se utiliza cuando es necesario disponer de un historial completo y verificable.

---

### Base de datos de columnas anchas (Wide Column)

Organiza los datos por familias de columnas.

Está diseñada para aplicaciones que requieren una gran escalabilidad y alto rendimiento.

---

## Servicios de AWS

| Tipo de base de datos | Servicios de AWS |
| :--------------------- | :--------------- |
| Relacional | Amazon Aurora, Amazon RDS y Amazon Redshift |
| Clave-valor | Amazon DynamoDB |
| Documental | Amazon DocumentDB (compatible con MongoDB) |
| En memoria | Amazon ElastiCache y Amazon MemoryDB |
| Wide Column | Amazon Keyspaces |
| Grafos | Amazon Neptune |
| Serie temporal | Amazon Timestream |
| Ledger | Amazon QLDB |

---
