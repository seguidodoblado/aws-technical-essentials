# Equilibrio de carga

El **equilibrio de carga (Load Balancing)** consiste en distribuir automáticamente el tráfico entrante entre varios recursos para mejorar la disponibilidad, la tolerancia a fallos y el rendimiento de una aplicación.

AWS proporciona **Elastic Load Balancing (ELB)** como servicio administrado para distribuir el tráfico entre varios destinos disponibles.

---

## Elastic Load Balancing

Elastic Load Balancing distribuye automáticamente las solicitudes entrantes entre varios destinos, como:

- Instancias Amazon EC2.
- Contenedores.
- Direcciones IP.
- Funciones AWS Lambda.

```text
                 Clientes
                     │
                     ▼
        Elastic Load Balancer (ELB)
                     │
      ┌──────────────┼──────────────┐
      │              │              │
      ▼              ▼              ▼
    EC2-1          EC2-2          EC2-3
```

---

## Beneficios

Elastic Load Balancing proporciona los siguientes beneficios:

- Alta disponibilidad y elasticidad.
- Seguridad.
- Amplio conjunto de características.
- Supervisión y visibilidad.
- Integración con otros servicios de AWS y alcance global.

---

## Componentes

Elastic Load Balancing se basa en tres componentes principales:

| Componente | Descripción |
| :--------- | :---------- |
| **Listeners** | Comprueban las solicitudes de conexión utilizando el protocolo y el puerto configurados. |
| **Target Groups** | Agrupan los recursos que recibirán el tráfico distribuido por el balanceador. |
| **Rules** | Determinan cómo se enrutan las solicitudes hacia los distintos grupos de destinos. |

---

## Tipos de Elastic Load Balancer

AWS ofrece cuatro tipos de balanceadores de carga:

- **Application Load Balancer (ALB)**
- **Network Load Balancer (NLB)**
- **Gateway Load Balancer (GWLB)**
- **Classic Load Balancer (CLB)**

En este curso se estudian **Application Load Balancer** y **Network Load Balancer**.

---

## Application Load Balancer (ALB)

El **Application Load Balancer** está diseñado para distribuir tráfico **HTTP** y **HTTPS** en la capa de aplicación (Layer 7).

Proporciona las siguientes capacidades:

| Característica | Descripción |
| :------------- | :---------- |
| **Seguridad** | Integra certificados TLS para proteger las comunicaciones. |
| **TLS Offloading** | Finaliza las conexiones TLS en el balanceador, reduciendo la carga sobre los destinos. |
| **Sticky Sessions** | Mantiene las solicitudes de un mismo cliente dirigidas al mismo destino cuando es necesario. |
| **Redirects** | Permite redirigir automáticamente solicitudes HTTP y HTTPS. |
| **Fixed Responses** | Puede responder directamente a determinadas solicitudes sin enviarlas al destino. |
| **Content-based Routing** | Enruta el tráfico según reglas basadas en el contenido de la solicitud, como el host o la ruta URL. |

---

## Network Load Balancer (NLB)

El **Network Load Balancer** está diseñado para distribuir tráfico **TCP**, **UDP** y **TLS** en la capa de transporte (Layer 4).

Está orientado a aplicaciones que requieren un rendimiento muy elevado y una latencia muy baja.

Proporciona las siguientes capacidades:

| Característica | Descripción |
| :------------- | :---------- |
| **Sticky Sessions** | Permite mantener la afinidad de las conexiones cuando la aplicación lo requiere. |
| **Baja latencia** | Optimizado para ofrecer tiempos de respuesta muy reducidos. |
| **Conservación de la IP de origen** | Los destinos reciben la dirección IP original del cliente. |
| **Compatibilidad con direcciones IP estáticas** | Permite utilizar direcciones IP estáticas para el balanceador. |
| **Compatibilidad con Elastic IP** | Puede asociarse con direcciones Elastic IP. |
| **DNS Failover** | Redirige el tráfico automáticamente cuando un destino deja de estar disponible. |

---
