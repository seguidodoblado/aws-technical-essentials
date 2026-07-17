# Almacenamiento en bloques

El **almacenamiento en bloques (Block Storage)** divide los datos en bloques de tamaño fijo que pueden actualizarse, consultarse y almacenarse de forma independiente.

AWS ofrece dos servicios de almacenamiento en bloques:

- **Amazon EC2 Instance Store**.
- **Amazon Elastic Block Store (Amazon EBS)**.

---

## Tipos de almacenamiento en bloques

```text
                 Almacenamiento en bloques
                          │
             ┌────────────┴────────────┐
             │                         │
             ▼                         ▼
   Amazon EC2 Instance Store     Amazon EBS
             │                         │
   Almacenamiento temporal   Almacenamiento persistente
```

---

### Amazon EC2 Instance Store

Amazon EC2 Instance Store proporciona almacenamiento temporal asociado físicamente al host donde se ejecuta la instancia.

Este almacenamiento es adecuado para datos temporales que pueden recrearse si es necesario.

Si la instancia se detiene, se hiberna o finaliza, los datos almacenados en el Instance Store se pierden.

---

### Amazon Elastic Block Store (Amazon EBS)

Amazon Elastic Block Store (Amazon EBS) proporciona almacenamiento persistente en bloques para instancias de Amazon EC2.

Los volúmenes de Amazon EBS permanecen disponibles independientemente del estado de la instancia y pueden utilizarse para almacenar datos que deben conservarse.

Para realizar copias de seguridad de un volumen Amazon EBS pueden crearse **instantáneas (Snapshots)**, que almacenan únicamente los bloques modificados desde la instantánea anterior.

---

## Amazon EBS Multi-Attach

**Amazon EBS Multi-Attach** permite asociar un mismo volumen **Provisioned IOPS SSD** a varias instancias Amazon EC2 que se ejecuten dentro de la misma **Availability Zone**.

Esta característica permite que varias instancias accedan simultáneamente al mismo volumen.

---

## Tipos de volúmenes Amazon EBS

AWS ofrece dos categorías de volúmenes Amazon EBS.

| SSD | HDD |
| :-- | :-- |
| Diseñados para cargas de trabajo que requieren baja latencia y un elevado número de operaciones de entrada/salida. | Diseñados para cargas de trabajo que requieren un alto rendimiento secuencial y gran capacidad de almacenamiento. |

---

### Volúmenes SSD

- Cargas de trabajo transaccionales.
- Almacenamiento de arranque (*boot volumes*).
- Alto rendimiento de E/S.
- Baja latencia.

---

### Volúmenes HDD

- Acceso secuencial a grandes volúmenes de datos.
- Cargas de trabajo con alto rendimiento secuencial.
- Grandes capacidades de almacenamiento.

---
