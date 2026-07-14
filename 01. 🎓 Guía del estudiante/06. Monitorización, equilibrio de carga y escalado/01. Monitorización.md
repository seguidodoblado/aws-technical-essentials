# Monitorización

La monitorización permite recopilar, visualizar y analizar información sobre los recursos y las aplicaciones para conocer su estado y detectar posibles incidencias.

AWS proporciona **Amazon CloudWatch** como servicio de monitorización para recursos y aplicaciones que se ejecutan en AWS y en entornos híbridos.

---

## Beneficios de la monitorización

La monitorización ayuda a:

- Conocer el estado de los recursos.
- Detectar problemas de funcionamiento.
- Analizar tendencias de uso.
- Automatizar respuestas ante determinados eventos.

---

## Amazon CloudWatch

Amazon CloudWatch recopila y supervisa métricas, registros (*Logs*) y eventos generados por los recursos de AWS.

La información recopilada permite supervisar el estado de los recursos y tomar acciones cuando se cumplen determinadas condiciones.

---

## Métricas

Las **métricas (Metrics)** son datos que describen el rendimiento y el estado de un recurso a lo largo del tiempo.

Algunos ejemplos de métricas son:

- Utilización de CPU.
- Utilización de memoria.
- Tráfico de red.
- Operaciones de lectura y escritura.
- Latencia.

Las métricas se representan como series temporales y pueden utilizarse para generar gráficos y alarmas.

---

## Paneles (Dashboards)

Los **CloudWatch Dashboards** permiten visualizar varias métricas en un único panel.

Un panel puede contener información procedente de distintos recursos y servicios de AWS, facilitando la supervisión del entorno desde una única vista.

```text
                 CloudWatch Dashboard

        ┌────────────────────────────────────┐
        │ CPU Utilization        ███▆▅▃▂      │
        ├────────────────────────────────────┤
        │ Network In            █▂▃▅▆██      │
        ├────────────────────────────────────┤
        │ Read Operations       ▂▃▅▆███      │
        ├────────────────────────────────────┤
        │ Write Operations      ███▇▅▃▂      │
        └────────────────────────────────────┘
```

---

## Alarmas

Las **CloudWatch Alarms** supervisan una métrica y comparan su valor con un umbral definido.

Cuando una métrica supera o desciende por debajo del umbral establecido, la alarma cambia de estado y puede ejecutar automáticamente una acción.

Entre las acciones posibles se incluyen:

- Enviar una notificación.
- Ejecutar una acción de Amazon EC2 Auto Scaling.
- Realizar otras acciones configuradas mediante servicios de AWS.

```text
                 CloudWatch Metric
                         │
                         ▼
                Comparación con umbral
                         │
             ┌───────────┴───────────┐
             │                       │
             ▼                       ▼
       Valor normal           Umbral superado
             │                       │
             ▼                       ▼
      Sin acciones          CloudWatch Alarm
                                     │
                                     ▼
                          Notificación / Acción
```

---
