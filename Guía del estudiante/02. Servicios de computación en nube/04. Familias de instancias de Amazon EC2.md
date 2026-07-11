# Familias de instancias de Amazon EC2

Amazon EC2 ofrece diferentes **familias de instancias**, cada una optimizada para un tipo específico de carga de trabajo.

Seleccionar la familia adecuada permite optimizar el rendimiento y el coste de la aplicación.

---

## Clasificación de las familias

```text
                    Familias de Amazon EC2

                           Amazon EC2
                                │
    ┌──────────────┬────────────┼────────────┬──────────────┐
    │              │            │            │              │
    ▼              ▼            ▼            ▼              ▼
Propósito      Computación   Memoria   Almacenamiento   Computación
 general       optimizada   optimizada optimizado      acelerada
```

---

## Instancias de propósito general

Ofrecen un equilibrio entre:

- CPU
- Memoria
- Red

Son adecuadas para:

- Servidores web.
- Entornos de desarrollo.
- Aplicaciones empresariales.
- Repositorios de código.

---

## Instancias optimizadas para computación

Proporcionan una mayor capacidad de procesamiento.

Se utilizan habitualmente en:

- Servidores de aplicaciones.
- Procesamiento por lotes.
- Servidores de videojuegos.
- Análisis científico.
- Codificación multimedia.

---

## Instancias optimizadas para memoria

Están diseñadas para aplicaciones que requieren grandes cantidades de memoria RAM.

Casos de uso habituales:

- Bases de datos de alto rendimiento.
- Sistemas de análisis de datos.
- Cachés distribuidas.
- Aplicaciones empresariales de gran tamaño.

---

## Instancias optimizadas para almacenamiento

Proporcionan un acceso muy rápido a grandes volúmenes de almacenamiento local.

Se utilizan principalmente en:

- Bases de datos NoSQL.
- Sistemas de archivos distribuidos.
- Procesamiento de grandes volúmenes de datos.

---

## Instancias con computación acelerada

Incorporan hardware especializado para acelerar determinadas operaciones.

Se emplean en cargas de trabajo como:

- Inteligencia artificial.
- Machine Learning.
- Procesamiento gráfico.
- Simulaciones científicas.
- Procesamiento de vídeo.

---

## Familias de instancias

AWS ofrece distintas familias de instancias, cada una optimizada para un tipo específico de carga de trabajo.

| Familia | Optimizada para | Casos de uso habituales |
| :------: | :-------------- | :---------------------- |
| **T** | Uso general y bajo coste | Desarrollo, pruebas y pequeñas aplicaciones |
| **M** | Uso general equilibrado | Servidores de aplicaciones y microservicios |
| **C** | Alto rendimiento de CPU | Procesamiento intensivo y HPC |
| **R** | Gran cantidad de memoria | Bases de datos en memoria y cachés |
| **X** | Memoria extremadamente grande | SAP HANA y análisis de datos |
| **I** | Alto rendimiento de E/S | Bases de datos NoSQL y cargas con muchas IOPS |
| **D** | Gran capacidad de almacenamiento | Backups y Data Lakes |
| **H** | Almacenamiento HDD | Big Data y almacenamiento distribuido |
| **P** | GPU | IA, Machine Learning y renderizado |
| **G** | Procesamiento gráfico | Visualización y escritorios remotos |
| **Inf** | Inferencia de IA | Modelos ya entrenados |
| **Trn** | Entrenamiento de IA | Entrenamiento de modelos de Machine Learning |

---

## Ejemplos de tipos de instancia

| Tipo | Familia | Descripción |
| :--: | :-----: | :---------- |
| **t2** | T | Uso general con rendimiento en ráfagas |
| **m5** | M | Uso general equilibrado |
| **c5** | C | Optimizada para CPU |
| **r4** | R | Optimizada para memoria |
| **x1e** | X | Memoria muy grande |
| **p3** | P | GPU para IA |
| **h1** | H | Almacenamiento HDD |
| **i3** | I | SSD de alto rendimiento |
| **d2** | D | Alta densidad de almacenamiento |

---

## Regla mnemotécnica

| Familia | Ayuda para recordarla |
| :-----: | :-------------------- |
| **T** | **Tiny** o **Turbo** |
| **M** | **Main** o **Medium** |
| **C** | **Compute** |
| **R** | **RAM** |
| **X** | **Extreme memory** |
| **I** | **IOPS** |
| **D** | **Dense storage** |
| **H** | **HDD** |
| **P** | **Pictures** (GPU) |
| **G** | **Graphics** |
| **Inf** | **Inference** |
| **Trn** | **Training** |

---

## Selección de una instancia

La elección de una instancia depende principalmente de:

- Tipo de aplicación.
- Recursos necesarios.
- Rendimiento esperado.
- Coste.

---
