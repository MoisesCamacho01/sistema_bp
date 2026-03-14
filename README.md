# Reto de Arquitectura de Soluciones - Entidad Financiera "BP" 🏦☁️

Este repositorio contiene la propuesta formal de Arquitectura de Soluciones para el nuevo Sistema de Banca por Internet de la entidad financiera "BP". 

El diseño ha sido estructurado para garantizar alta disponibilidad, baja latencia, seguridad de grado bancario y optimización de costos mediante un enfoque Cloud-Native.

## 📄 Entregable Principal

Toda la resolución técnica, justificaciones, análisis de patrones y diagramas se encuentran en el documento oficial adjunto en este repositorio:

👉 **[SISTEMA_DEBANCA_POR_INTERNET.pdf](./SISTEMA_DEBANCA_POR_INTERNET.pdf)**

## 🚀 Tecnologías y Patrones Clave Propuestos

La solución arquitectónica se fundamenta en las siguientes decisiones estratégicas:

* **Estrategia Cloud & FinOps:** Infraestructura en **AWS** con enfoque *Serverless* (API Gateway, Lambda, DynamoDB) para pago por uso y escalado automático.
* **Frontend & Móvil:** **React.js** para la SPA web (preparado para micro-frontends) y **Flutter** para la aplicación móvil (rendimiento nativo y código base único).
* **Seguridad y Autenticación:** Implementación del estándar **OAuth 2.0 con flujo PKCE** e integración de biometría local (Secure Enclave/Keystore) y en la nube (AWS Rekognition) para el onboarding.
* **Patrones de Arquitectura:**
    * **Cache-Aside:** Uso de Amazon ElastiCache (Redis) para reducir la carga de lectura sobre el Core bancario heredado y garantizar baja latencia.
    * **Event-Driven Architecture (EDA):** Desacoplamiento de microservicios usando Amazon EventBridge para orquestar la auditoría y el envío de notificaciones de forma asíncrona.
    * **Circuit Breaker:** Protección de las integraciones con sistemas de terceros.
* **Modelado Visual:** Diseño estructurado utilizando el **Modelo C4** (Contexto, Contenedores y Componentes).

## 🛠️ Herramientas Utilizadas para el Modelado
* **Visual Studio y PlantUML** Para la generación de los diagramas C4.
* **Markdown / Microsoft Word:** Para la redacción y estructuración del documento de arquitectura.

---
**Autor:** Moises Daniel Camacho Pilco
**Fecha:** Marzo 2026