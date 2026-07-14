# Arquitectura Serverless Employee Directory

Esta arquitectura muestra una implementación **serverless** de la aplicación *Employee Directory*, utilizando servicios administrados de AWS para alojar el sitio web, ejecutar la lógica de negocio y almacenar la información de los empleados.

---

## Diagrama

```text
                     Usuario
                        │
                        ▼
                  Amazon Route 53
                        │
                        ▼
               Amazon CloudFront
                        │
                        ▼
          Amazon S3 (Static Website)
                        │
                        ▼
                 JavaScript (Browser)
                        │
                        ▼
                Amazon API Gateway
                        │
        ┌───────────────┼───────────────┐
        ▼               ▼               ▼
 Create employee   List employee   Update employee
        │               │               │
        └───────────────┼───────────────┘
                        │
                        ▼
               AWS Lambda Functions
                        │
        ┌───────────────┴───────────────┐
        ▼                               ▼
 Amazon DynamoDB                 Amazon S3
(Employee data)            (Employee photos)
                        │
                        ▼
                 Amazon Cognito
             (Authentication)
```

---

## Componentes

| Servicio | Función |
| :-------- | :------ |
| **Amazon Route 53** | Dirige las solicitudes de los usuarios hacia la aplicación. |
| **Amazon CloudFront** | Distribuye el contenido mediante una red global de entrega de contenido (CDN). |
| **Amazon S3** | Aloja el sitio web estático y almacena las fotografías de los empleados. |
| **Amazon API Gateway** | Publica la API utilizada por la aplicación web. |
| **AWS Lambda** | Ejecuta la lógica de negocio de la aplicación. |
| **Amazon DynamoDB** | Almacena la información de los empleados. |
| **Amazon Cognito** | Proporciona autenticación para los usuarios de la aplicación. |

---

## Flujo de la aplicación

1. El usuario accede a la aplicación mediante Amazon Route 53.
2. Amazon CloudFront entrega el sitio web estático alojado en Amazon S3.
3. El código JavaScript invoca la API publicada mediante Amazon API Gateway.
4. API Gateway ejecuta la función AWS Lambda correspondiente.
5. La función Lambda consulta o modifica la información almacenada en Amazon DynamoDB y, cuando es necesario, accede a las fotografías almacenadas en Amazon S3.
6. Amazon Cognito gestiona la autenticación de los usuarios de la aplicación.

---
