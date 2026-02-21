# Plan de Mejora: Portafolio Agéntico & ROI

## 1. Overview
Mejorar radicalmente el `index.html` para posicionar a Fabio Salinas como un **Desarrollador de Sistemas Agénticos y Experto en Automatización**. El objetivo es atraer a PYMES y empresas que buscan soluciones de alto valor y rápido ROI (eliminación de manualidades). Se utilizará un enfoque híbrido combinando un "Showcase de Arquitectura & ROI" (Opción C) con un "Widget de Agente Integrado" (Opción A). 

## 2. Project Type
**WEB** (Landing Page Estática interactiva)

## 3. Success Criteria
- [ ] El Hero Section comunica claramente el valor agéntico y la resolución a problemas de negocios (ROI).
- [ ] Existe una sección dedicada a "Casos de Uso / Arquitectura" con diagramas visuales (Mermaid u otros) que explican flujos como `WhatsApp -> n8n -> Supabase`.
- [ ] Existe una interfaz (widget flotante o integrado) visible de "Agente IA" (para demostración).
- [ ] El perfil corporativo se mantiene pero con menor peso visual respecto a las capacidades de desarrollo.
- [ ] El diseño sigue los principios de "Purple Ban" (revisar configuración de colores).

## 4. Tech Stack
- **HTML5/TailwindCSS (Vanilla Scripting):** Tecnologías actuales del sitio, manteniendo ligereza y velocidad.
- **Mermaid.js / Flowcharts:** Para diagramas de arquitectura ágiles e integrados nativamente.
- **Vanilla JS:** Para la interactividad del widget simulado o real del agente.

## 5. File Structure
```text
/
├── index.html                  # Modificación estructural profunda
├── docs/plans/
│   └── 20260221_portfolio-agente.md  # Este plan
```

## 6. Task Breakdown

### Task 1: Refactorización del Hero Section (Mensaje Central)
- **Agent:** `frontend-specialist`
- **Skills:** `frontend-design`, `clean-code`
- **INPUT:** `index.html` actual (líneas ~192-238).
- **OUTPUT:** Hero Section modificado con Copywriting directo ("Desarrollador de Software Agéntico & Automatización. Construyo sistemas IA que eliminan trabajo manual y escalan negocios.").
- **VERIFY:** Revisar visualmente que el título y subtítulo reflejen el nuevo giro, manteniendo la estética atractiva pero más enfocada en la solución.

### Task 2: Nueva Sección: Showcase Arquitectura & ROI (Opción C)
- **Agent:** `frontend-specialist` y `mermaid-expert`
- **Skills:** `mermaid-mastery`, `frontend-design`
- **INPUT:** Sección actual "Acto IV: Innovation Lab" en `index.html`.
- **OUTPUT:** Crear casos de uso para PYMES (Ej: Agente de Atención 24/7, Conciliación Bancaria, Analítica Express). Incluir un diagrama visual de arquitectura (Mermaid).
- **VERIFY:** Los casos de uso deben resaltar el pain point (dolor) y el ROI (tiempo/ahorro).

### Task 3: Implementación de Interfaz de Widget Agéntico (Opción A)
- **Agent:** `frontend-specialist`
- **Skills:** `frontend-design`, `clean-code`
- **INPUT:** `index.html`
- **OUTPUT:** Agregar un botón flotante y un panel de chat lateral/inferior simulando un "Asistente Ejecutivo de Fabio". El UI debe ser convincente, moderno y listo para ser conectado a un webhook de n8n en el futuro.
- **VERIFY:** El widget se abre y cierra correctamente y la interfaz parece un chat de asistencia real (glassmorphism/Tailwind).

### Task 4: Ajuste de Peso en Timeline Corporativo ("Dual Gateway" sutil)
- **Agent:** `frontend-specialist`
- **Skills:** `clean-code`
- **INPUT:** Secciones `hdi` y `legacy`.
- **OUTPUT:** Simplificar y agilizar visualmente la información corporativa para que sirva de "respaldo de madurez" pero sin saturar la atención que ahora es para el desarrollo agéntico. Eliminar colores púrpuras según directrices de diseño del frontend-specialist.
- **VERIFY:** La longitud de la página mejora y el foco técnico resalta por encima del gerencial.

## Phase X: Verificación Final
- [ ] Ejecutar lint y formateo.
- [ ] **Accesibilidad y UX:** `python .agent/skills/frontend-design/scripts/ux_audit.py .`
- [ ] **Lighthouse / Performance:** Verificar que no haya regresiones en tiempo de carga.
- [ ] **Regla Crítica:** Verificar que NO se hayan usado tonos púrpuras directos (Cumplir "Purple Ban" según frontend-specialist). En base a `frontend-specialist`, cambiar morado a "Acid Green", "Signal Orange" o "Deep Red".
