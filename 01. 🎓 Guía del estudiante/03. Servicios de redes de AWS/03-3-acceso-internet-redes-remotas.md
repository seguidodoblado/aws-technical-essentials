# Acceso desde Internet y redes remotas

Una **Amazon Virtual Private Cloud (Amazon VPC)** es una red virtual aislada. Para permitir la comunicación con Internet o con redes externas es necesario utilizar distintos componentes de conectividad.

AWS proporciona diferentes opciones para conectar una Amazon VPC con otras redes y controlar el camino que seguirá el tráfico.

---

## Componentes de conectividad

```text
                          Amazon VPC
                               │
                        Tabla de rutas
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
        ▼                      ▼                      ▼
 Internet Gateway             VPN         AWS Direct Connect
        │                      │                      │
        ▼                      ▼                      ▼
    Internet             Red remota          Centro de datos
```

La **tabla de rutas** determina qué camino seguirá el tráfico de red para alcanzar su destino.

Dependiendo de la ruta configurada, el tráfico puede dirigirse hacia Internet, una red remota conectada mediante una VPN o un centro de datos conectado mediante AWS Direct Connect.

---

## Internet Gateway

Un **Internet Gateway** permite la comunicación entre una Amazon VPC e Internet.

Para que una instancia pueda acceder a Internet es necesario:

- Asociar un Internet Gateway a la Amazon VPC.
- Configurar una ruta hacia el Internet Gateway en la tabla de rutas.
- Disponer de una dirección IP pública cuando corresponda.

---

## Virtual Private Network (VPN)

Una **Virtual Private Network (VPN)** permite establecer una conexión cifrada entre una red local y una Amazon VPC utilizando Internet.

Este tipo de conexión proporciona una forma segura de comunicar recursos locales con recursos desplegados en AWS.

---

## AWS Direct Connect

**AWS Direct Connect** proporciona una conexión de red dedicada entre un centro de datos local y AWS.

A diferencia de una VPN, esta conexión no utiliza Internet como medio de transporte.

AWS Direct Connect permite:

- Reducir la latencia.
- Obtener un ancho de banda más constante.
- Disponer de una conexión privada con AWS.

---

## Tablas de rutas (Route Tables)

Una **tabla de rutas** contiene un conjunto de reglas que determinan cómo se dirige el tráfico dentro de una Amazon VPC.

Cada regla especifica:

- El destino del tráfico.
- El siguiente salto (*target*) al que debe enviarse.

Las tablas de rutas permiten controlar cómo se comunican los recursos de una Amazon VPC con Internet, redes remotas u otros destinos configurados.

---

## Comparativa

| Método | Medio de conexión | Caso de uso |
| :------ | :---------------- | :---------- |
| **Internet Gateway** | Internet | Acceso público a recursos de una Amazon VPC |
| **VPN** | Internet (conexión cifrada) | Comunicación segura con una red local |
| **AWS Direct Connect** | Enlace dedicado | Conectividad privada entre AWS y un centro de datos |

---
