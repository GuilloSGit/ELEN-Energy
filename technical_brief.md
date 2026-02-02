# Brief de Arquitectura

En este documento definimos las decisiones técnicas y el stack tecnológico para el desarrollo del producto.

---

## 1. Stack Tecnológico por Componente

| Componente       | Tecnología Recomendada                 | Justificación                                           |
| ---              | ---                                     | ---                                                     |
| Scraper          | Python (Requests/Playwright o FastAPI)  | Ecosistema maduro para scraping y automatización        |
| DB Writer        | Node.js (servicio/script ligero)        | Pipeline simple para insertar/actualizar datos          |
| Base de Datos    | PostgreSQL                              | Integridad + flexibilidad con JSONB; índices GIN para búsquedas rápidas |
| Frontend         | Web estática o React ligero             | Suficiente para listar/consultar datos al inicio        |
| Admin Back Office| Página simple protegida                 | Edición/verificación mínima para operar                 |

## 2. Justificación del Enfoque Mixto

> Python para scraping y procesamiento de datos:

    Ventaja en scraping y procesamiento de datos
    Ecosistema maduro para scraping (Requests, Playwright, BeautifulSoup)
    FastAPI ofrece rendimiento comparable a Node.js
    
> Node.js para escritura en BD y utilidades:

    Excelente para I/O asíncrono (conexiones múltiples)
    Servicio/script ligero para pipelines de datos
    Opcional: TypeScript para tipado y mejor DX

## 3. Flujo y Diagrama de Datos

<a href="https://mermaid.ai/d/dbaedb51-ba63-4583-9369-264cb629f7a0" target="_blank" rel="noopener noreferrer">
    <img src="diagram.png" alt="Diagrama" width="600" style="display:block; margin:0;" />
    Click para ver el diagrama en la web - Mermaid
</a>

## 4. Consideraciones de Escalabilidad

📈 Evolución de la Infraestructura:

Componente | Fase Inicial | Fase de Escala
| --- | --- | --- |
Colas/Mensajería | No aplica | Agregar RabbitMQ/Kafka si sube el volumen
Base de Datos | PostgreSQL único | Particionamiento por categoría o fecha + réplicas de lectura
Despliegue | Docker Compose | Kubernetes/Orquestación si aparecen más servicios
API de Lectura | No aplica (lectura directa/servicio mínimo) | API dedicada para clientes externos

🐋 Contenedorización:

    Docker desde el inicio para consistencia de entornos
    Docker Compose para desarrollo local
    CI/CD pipeline con pruebas automatizadas

## 5. Ventajas del Stack Propuesto

✅ Beneficios Clave:

Ventaja | Impacto
| --- | --- |
Arquitectura mínima viable | Menor complejidad y time-to-market
Lenguaje óptimo por tarea (Python/Node) | Eficiencia en scraping y pipelines de datos
Base sólida en PostgreSQL | Consultas y reportes fiables desde el inicio
Escalabilidad progresiva | Agregar colas/APIs solo cuando haya demanda

🎯 Ventajas Adicionales:

    🔧 Flexibilidad tecnológica: Se pueden agregar servicios (colas, APIs) sin reescribir el núcleo
    📊 Monitoreo unificado: Compatible con Prometheus/Grafana
    🔐 Seguridad por capas: Evoluciona desde credenciales simples a políticas por servicio
    🌍 Compatibilidad cloud: Despliegue en AWS/GCP/Azure sin cambios estructurales
