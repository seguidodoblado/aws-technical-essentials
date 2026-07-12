# Almacenamiento de objetos

El **almacenamiento de objetos (Object Storage)** almacena los datos como objetos dentro de un contenedor.

Cada objeto está compuesto por:

- Los datos.
- Los metadatos.
- Una clave (*Key*) que identifica el objeto de forma única.

AWS proporciona **Amazon Simple Storage Service (Amazon S3)** como servicio de almacenamiento de objetos.

---

## Componentes de un objeto

```text
                 Objeto
                    │
        ┌───────────┼───────────┐
        │           │           │
        ▼           ▼           ▼
      Datos     Metadatos      Clave
                               (Key)
```

---

## Amazon Simple Storage Service (Amazon S3)

Amazon S3 es un servicio de almacenamiento de objetos.

Los objetos se almacenan dentro de **buckets**.

Cada objeto está identificado mediante una **clave (Key)** única dentro de su bucket.

Un objeto puede almacenar hasta **5 TB** de datos.

---

## Organización de Amazon S3

```text
             Amazon S3
                 │
          ┌──────┴──────┐
          │             │
          ▼             ▼
       Buckets       Objetos
                         │
                 ┌───────┼────────┐
                 │       │        │
                 ▼       ▼        ▼
              Datos  Metadatos   Key
```

---

## Seguridad de Amazon S3

AWS proporciona varios mecanismos para controlar el acceso a los datos almacenados en Amazon S3.

Entre ellos se encuentran:

- Políticas de IAM.
- Políticas de bucket.
- Listas de control de acceso (ACL).
- Cifrado de Amazon S3.

---

### Cifrado

Amazon S3 permite proteger los datos mediante:

- Cifrado del lado del servidor (*Server-side encryption*).
- Cifrado del lado del cliente (*Client-side encryption*).

---

## Versionado de Amazon S3

Amazon S3 permite conservar varias versiones de un mismo objeto mediante la característica **Versioning**.

Cuando el versionado está habilitado:

- Se genera una nueva versión cada vez que se modifica un objeto.
- Se conservan las versiones anteriores del objeto.
- Permite recuperar objetos modificados o eliminados accidentalmente.
- Está deshabilitado de forma predeterminada.

Cuando se elimina un objeto de un bucket con Versioning habilitado, Amazon S3 añade un **marcador de eliminación (*Delete Marker*)**, manteniendo las versiones anteriores del objeto.

---

## Buenas prácticas

- Utilizar políticas de IAM para controlar el acceso.
- Utilizar políticas de bucket cuando sea necesario.
- Habilitar el cifrado para proteger los datos almacenados.
- Habilitar el versionado para facilitar la recuperación de objetos modificados o eliminados accidentalmente.

---
