# 4. Brief de Producto: Funcionalidad y UX

Definición de la experiencia de usuario y arquitectura del sistema.

---

## 1. User Journey (El Viaje del Usuario)

1.  **Descubrimiento**: La PyME llega por un anuncio de "Torno CNC al 50% de valor nuevo".
2.  **Validación**: Aterriza en la Home. Ve "Sello de Garantía", "Tracking en vivo de otros pedidos" (Social Proof). Se siente seguro.
3.  **Registro y Onboarding**: Para ver precios finales, debe registrarse como empresa (filtro de calidad).
4.  **Búsqueda/Alerta**: Busca su maquinaria. Si no está, configura una **"Alerta de Oportunidad"**.
5.  **Cotización**: Encuentra una máquina. Solicita cotización final puesta en su planta (DDP - Delivered Duty Paid).
6.  **Cierre**: Recibe el contrato, realiza el pago inicial.
7.  **Seguimiento (Anxiety Reduction)**: Entra al panel de "Mis Pedidos". Ve el tracking visual paso a paso.
8.  **Recepción y Lealtad**: Recibe la máquina. El sistema le pide calificar la experiencia para alimentar la "Red de Confianza".

## 2. Funcionalidades Clave (Must-haves)

*   **Sistema de "Alertas de Oportunidad"**:
    *   *Qué es*: El usuario define "Quiero un autoelevador marca Linde, año >2015".
    *   *Cómo funciona*: Cuando los scrapers encuentran un match, envían un email/WhatsApp automático al usuario antes de publicarlo en la web general. Sensación de exclusividad.

*   **Panel de Tracking Visual (Logística Transparente)**:
    *   *Inspiración*: Domino's Pizza Tracker pero industrial.
    *   *Estados*: "En depósito origen" -> "Inspección completada" -> "En altamar" -> "Aduana Argentina" -> "En transporte final".
    *   *Objetivo*: Eliminar la ansiedad de la "caja negra" de la importación.

*   **Sistema de Calificación (Trust Network)**:
    *   Calificación del *Vendedor Europeo* (basado en el estado real vs. declarado).
    *   Calificación de la *Experiencia Logística*.

## 3. Arquitectura de Información (Mapa del Sitio)

### A. Público (Frontend Web)
*   **Home**: Propuesta de valor, Máquinas destacadas, Calculadora de ahorro.
*   **Catálogo**: Filtros potentes (Marca, Modelo, Año, Ubicación, Horas de uso).
*   **Página de Producto**: Fotos HD, Video de funcionamiento, Ficha técnica, Botón "Cotizar puesta en fábrica".
*   **Blog/Guías**: Contenido educativo para SEO y confianza.

### B. Privado (Dashboard Usuario)
*   **Mis Alertas**: Gestión de búsquedas guardadas.
*   **Mis Pedidos**: Tracking visual y documentación (Facturas, despachos).
*   **Perfil de Empresa**: Datos fiscales y de entrega.

### C. Admin (Backoffice Intranet)
*   **Scraper Manager**: Ver qué están trayendo los bots, aprobar/descartar productos.
*   **Control de Pedidos**: Actualización de estados de tracking.
*   **CRM**: Gestión de clientes y leads.
