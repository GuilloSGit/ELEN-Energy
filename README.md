# ELEN Energy

> Plataforma de gestión para compras de productos Europeos en Argentina.

## 1. Sobre el Producto (Visión)

### Propuesta de Valor
Facilitar la adquisición de productos europeos en Argentina, eliminando barreras geográficas y simplificando el proceso a un solo clic.

**Documentación de Negocio:**
* [Product Brief](product_brief.md): Definición detallada del producto y etapas.
* [Marketing Brief](marketing_brief.md): Estrategia de mercado.
* [Strategic Brief](strategic_brief.md): Visión estratégica a largo plazo.
* [Creative Brief](creative_brief.md): Lineamientos creativos.

---

## 2. Sobre el Proyecto (Ingeniería)

### Estado Actual (MVP)
El proyecto se encuentra en etapa de desarrollo activo.
* **Limitaciones actuales:** Alto grado de dependencia de procesos manuales en la gestión de pedidos.
* **Automatización:** Implementación progresiva de scrapers para la obtención de datos de productos.

### Arquitectura y Stack
Arquitectura mínima evolutiva orientada a componentes.

* **Core:** Node.js, Python (TypeScript opcional).
* **Frameworks:** FastAPI (scraper opcional), React ligero o web estática.
* **Data:** PostgreSQL (JSONB + índices GIN para atributos variables).
* **Infraestructura:** Docker, Docker Compose. Kubernetes solo si escala.

**Documentación Técnica:**
* [Technical Brief](technical_brief.md): Arquitectura detallada y componentes.

---

## 3. Despliegue y Desarrollo

**Requisitos:** Docker, Docker Compose (GitHub Actions opcional).

El despliegue es secuencial (Componentes -> Frontend). El desarrollo sigue las etapas descritas en el [Product Brief](product_brief.md).
