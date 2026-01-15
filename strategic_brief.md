# 3. Brief Estratégico: Roadmap y Viabilidad

Este documento define la hoja de ruta para llevar el proyecto de la idea a la escala.

---

## 1. Fases del Proyecto

### Fase 1: Validación "Concierge" (Mes 1-3)
*Objetivo*: Validar la demanda y el proceso logístico sin sobreinversión en software.
*   **Tecnología**: Scrapers básicos corriendo semanalmente (sin UI compleja). Base de datos simple.
*   **Operación**: Curaduría manual. Las "Alertas" se envían por WhatsApp o Email manualmente. Venta consultiva.
*   **Hito de Éxito**: Primeras 5 máquinas vendidas y entregadas.

### Fase 2: Plataforma Automatizada (Mes 4-9)
*Objetivo*: Reducir fricción operativa y permitir que el usuario se autogestione.
*   **Tecnología**: Web App completa. Dashboard de usuario (Mis Pedidos, Tracking). Scrapers 24/7.
*   **Operación**: El cliente busca y cotiza online. El equipo de Admin solo valida y aprueba operaciones.
*   **Hito de Éxito**: 50 transacciones mensuales.

### Fase 3: Escalamiento y Red LATAM (Año 1+)
*Objetivo*: Expansión geográfica y fidelización.
*   **Tecnología**: Machine Learning para predecir precios y oportunidades. App móvil.
*   **Operación**: Abrir envíos a Chile, Brasil y Perú.
*   **Hito de Éxito**: Ser el referente #1 de importación de maquinaria usada en la región.

## 2. Estimación de Costos Operativos (Infraestructura Fase 1-2)
Para un tráfico inicial moderado pero con scraping intensivo:

*   **Proxies Residenciales (Crítico)**: Para evitar bloqueos en sitios europeos.
    *   *Costo*: ~$150 - $300 USD/mes (dependiendo del volumen de datos, ej. Bright Data o Smartproxy).
*   **Servidores de Scraping (Workers)**:
    *   *Costo*: ~$40 - $80 USD/mes (AWS EC2 o DigitalOcean Droplets).
*   **Base de Datos y Backend**:
    *   *Costo*: ~$50 USD/mes (Postgres gestionado + Hosting tipo Railway/Render).
*   **Hosting Web (Frontend)**:
    *   *Costo*: ~$20 USD/mes (Vercel Pro o Netlify).
*   **Email Transaccional / Marketing**:
    *   *Costo*: ~$30 - $50 USD/mes (Resend / HubSpot Starter).

**Total Estimado Infraestructura Técnica: $300 - $500 USD Mensuales.**
*(Nota: Este costo escala linealmente con el volumen de scrapers y datos).*

## 3. Análisis de Riesgos y Mitigación

| Riesgo | Probabilidad | Impacto | Estrategia de Mitigación |
| :--- | :--- | :--- | :--- |
| **Bloqueo de Scrapers** | Alta | Crítico | 1. Usar redes de proxies residenciales rotativos.<br>2. Espaciar consultas ("Human-like delay").<br>3. Tener múltiples fuentes (no depender de un solo sitio source). |
| **Retrasos Aduaneros** | Media | Alto | 1. Claridad total en T&C ("Tiempos estimados").<br>2. Gestión experta (Partners: Esteban/Matías).<br>3. Seguros de caución o reembolso parcial. |
| **Calidad del Producto** | Baja | Medio | 1. Sistema de "Verificación in-situ" (servicio premium).<br>2. Reporte fotográfico detallado antes del embarque.<br>3. Calificación de vendedores europeos en la plataforma. |
| **Volatilidad Cambiaria** | Alta | Medio | 1. Fijar precios en divisa fuerte (Euros/Dólares).<br>2. Cobro de servicios en el exterior si es posible. |
