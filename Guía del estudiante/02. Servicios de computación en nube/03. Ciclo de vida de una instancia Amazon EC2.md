# Ciclo de vida de una instancia Amazon EC2

Una instancia de **Amazon EC2** pasa por diferentes estados durante su ciclo de vida. Cada estado representa una fase concreta desde su creación hasta su eliminación definitiva.

Comprender estos estados resulta fundamental para administrar correctamente las instancias y conocer cuándo es posible iniciarlas, detenerlas o terminarlas.

---

## Ciclo de vida de una instancia

```text
                              Lanzamiento
                                   │
                                   ▼
                          ┌─────────────────┐
                          │    Pending      │
                          │   (Pendiente)   │
                          └────────┬────────┘
                                   │
                                   ▼
                          ┌─────────────────┐
                          │    Running      │
                          │ (En ejecución)  │
                          └───┬─────────┬───┘
                              │         │
                  Reiniciar ──┘         │
                                        │
                              Detener   │ Terminar
                                        │
                                        ▼
                          ┌─────────────────┐
                          │    Stopping     │
                          │  (Deteniendo)   │
                          └────────┬────────┘
                                   │
                                   ▼
                          ┌─────────────────┐
                          │    Stopped      │
                          │   (Detenida)    │
                          └──────┬──────┬───┘
                                 │      │
                            Iniciar  Terminar
                                 │      │
                                 ▼      ▼
                             Running  Shutting down
                                           │
                                           ▼
                                   ┌─────────────────┐
                                   │  Terminated    │
                                   │   (Finalizada) │
                                   └─────────────────┘
```

---

## Estados de una instancia

### Pending (Pendiente)

Es el estado inicial tras solicitar el lanzamiento de una instancia.

Durante esta fase AWS prepara la máquina virtual y asigna los recursos necesarios para su ejecución.

---

### Running (En ejecución)

La instancia está completamente operativa.

En este estado:

- Ejecuta aplicaciones.
- Atiende solicitudes.
- Consume recursos de computación.
- Se factura según el modelo de precios correspondiente.

---

### Stopping (Deteniendo)

AWS está apagando el sistema operativo de la instancia.

Es un estado transitorio previo a que la instancia quede detenida.

---

### Stopped (Detenida)

La instancia permanece creada, pero no está ejecutándose.

En este estado:

- No consume recursos de CPU.
- Puede volver a iniciarse.
- Continúan existiendo los recursos asociados, como el volumen raíz de Amazon EBS.

---

### Shutting down (Finalizando)

La instancia está siendo eliminada.

Es un estado temporal inmediatamente anterior a su terminación definitiva.

---

### Terminated (Finalizada)

La instancia ha sido eliminada permanentemente.

Una vez alcanzado este estado, no puede volver a iniciarse.

## Consideraciones

- Una instancia puede pasar varias veces entre los estados **Running** y **Stopped**.
- El estado **Terminated** es irreversible.
- Los estados **Pending**, **Stopping** y **Shutting down** son transitorios y normalmente tienen una duración muy breve.

---
