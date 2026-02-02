# Brief de Producto: Funcionalidad y UX

Definición de la experiencia de usuario y arquitectura del sistema.

---

## 1. User Journey (El Viaje del Usuario)

1.  **Descubrimiento**: La PyME llega por un anuncio de "Torno CNC al 50% de valor nuevo".
2.  **Validación**: Aterriza en la Home. <!-- Ve "Sello de Garantía", "Tracking en vivo de otros pedidos" (Social Proof). Se siente seguro. -->
3.  **Registro y Onboarding**: No ve precios finales, debe contactarse con el equipo de ventas y asesoramiento técnico.
4.  **Búsqueda/Alerta**: Busca su maquinaria. Si no está, configura una **"Alerta de Oportunidad"**.
5.  **Cotización**: Encuentra una máquina. Solicita cotización final y/o puesta en su planta (DDP - Delivered Duty Paid).
6.  **Cierre**: Recibe la proforma y condiciones de garantía. Emite orden de compra y realiza el pago inicial/seña.
7.  **Recepción y Lealtad**: Recibe la máquina. No requiere calificación ni seguimiento.

## 2. Funcionalidades Clave (MVP)
- Catálogo público con filtros básicos (categoría, marca, año).
- Ficha de producto simple (fotos, descripción, especificaciones clave).
- Botón “Solicitar cotización” (captura de lead).
- Admin Back Office básico: alta/edición de productos, publicación/despublicación.
- Seguimiento manual (texto/estados simples) opcional.

Roadmap (no MVP): Alertas de oportunidad automáticas, tracking visual avanzado, sistema de calificaciones.

## 3. Arquitectura de Información (Mapa del Sitio)

### A. Público (Frontend Web)
- Home: propuesta de valor + destacados
- Catálogo: filtros básicos
- Ficha de producto: info clave + CTA “Cotizar”

### B. Admin (Back Office)
- Productos: ABM básico
- Leads: ver solicitudes y exportar
