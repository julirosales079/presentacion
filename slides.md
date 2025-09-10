---
theme: seriph
background: https://images.unsplash.com/photo-1557804506-669a67965ba0?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80
class: 'text-center'
highlighter: shiki
lineNumbers: false
info: |
  ## Sistema de Pedidos - Requerimientos
  Documentación técnica de requerimientos funcionales y no funcionales
drawings:
  persist: false
css: unocss
---

# Sistema de Pedidos
## Requerimientos Funcionales y No Funcionales

Documentación técnica del sistema para Parrilleros Fast Food

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Comenzar presentación <carbon:arrow-right class="inline"/>
  </span>
</div>

---
layout: default
---

# Contenido

<div class="grid grid-cols-2 gap-8 mt-8">
<div>

## Requerimientos Funcionales
- **RF1-RF4**: Funcionalidades del menú y carrito
- **RF5-RF7**: Pedidos y validaciones  
- **RF8-RF10**: Procesamiento de pedidos
- **RF11-RF13**: Integraciones y usabilidad

</div>
<div>

## Requerimientos No Funcionales
- **RNF1-RNF4**: Rendimiento y usabilidad
- **RNF5-RNF8**: Compatibilidad y seguridad
- **RNF9-RNF11**: Mantenimiento y escalabilidad
- **RNF12-RNF14**: Disponibilidad y monitoreo

</div>
</div>

<div class="absolute bottom-10 left-1/2 transform -translate-x-1/2">
  <span class="text-sm opacity-70">Total: 13 Requerimientos Funcionales + 14 Requerimientos No Funcionales</span>
</div>

---
layout: default
---

# Requerimientos Funcionales (RF1-RF4)
## Menú y Carrito de Compras

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RF1: Visualización de menú** | Categoría seleccionada, búsqueda opcional | El sistema muestra el menú completo organizado por categorías, incluyendo imagen, nombre, descripción, precio y subcategorías de bebidas. | Menú visualizado en pantalla con la información del producto. |
| **RF2: Búsqueda de productos** | Nombre, descripción | Permite al cliente buscar productos específicos en tiempo real. | Lista de productos coincidentes mostrada en pantalla o mensaje de "sin resultados". |
| **RF3: Personalización de productos** | Selección de ingredientes adicionales, tipo de papas, instrucciones especiales. | El cliente puede personalizar productos agregando extras o notas. | Producto personalizado agregado al carrito con precio recalculado. |
| **RF4: Administración del carrito** | Producto, cantidad | Permite agregar, modificar o eliminar productos del carrito y ver el total en tiempo real. | Carrito actualizado con total reflejado automáticamente. |

</div>

---
layout: default
---

# Requerimientos Funcionales (RF5-RF7)
## Gestión de Pedidos y Validaciones

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RF5: Resumen de pedido** | Productos seleccionados, personalizaciones | El sistema muestra el detalle del pedido con subtotal, impuestos (INC 8%) y total. | Resumen editable presentado al cliente antes de confirmar. |
| **RF6: Selección de sede** | Sede seleccionada o parámetro ?sedes= | El cliente puede elegir sede manualmente o detectarla desde la URL. | Sede definida para procesar el pedido. |
| **RF7: Validación de productos por sede** | Carrito de compras, sede | El sistema valida disponibilidad de productos según la sede elegida. | Pedido validado o alerta de productos no disponibles. |

</div>

<div class="mt-8 p-4 bg-blue-50 rounded-lg">
  <h4 class="text-blue-800 font-semibold">💡 Funcionalidades Clave</h4>
  <p class="text-blue-700 text-sm mt-2">Los requerimientos RF5-RF7 aseguran que el pedido sea válido y esté correctamente configurado antes del procesamiento final.</p>
</div>

---
layout: default
---

# Requerimientos Funcionales (RF8-RF10)
## Procesamiento de Pedidos

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RF8: Pedido a domicilio** | Datos cliente (nombre, teléfono, dirección, barrio), método de pago | El cliente solicita entrega a domicilio y se genera un número de pedido único. | Pedido registrado y enviado a la sede por WhatsApp. |
| **RF9: Pedido para recoger en sede** | Datos básicos del cliente, sede | El cliente realiza pedido para recoger en sede con código único. | Confirmación enviada por WhatsApp con código de recogida. |
| **RF10: Generación de facturas** | Cédula, correo electrónico, datos tributarios | El sistema genera factura en PDF con desglose de impuestos. | Factura descargable o imprimible entregada al cliente. |

</div>

<div class="mt-8 p-4 bg-green-50 rounded-lg">
  <h4 class="text-green-800 font-semibold">📦 Modalidades de Entrega</h4>
  <p class="text-green-700 text-sm mt-2">El sistema soporta tanto entrega a domicilio como recogida en sede, con facturación automática incluida.</p>
</div>

---
layout: default
---

# Requerimientos Funcionales (RF11-RF13)
## Integraciones y Experiencia del Usuario

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RF11: Integración con WhatsApp** | Pedido confirmado, datos cliente | El sistema genera mensaje estructurado con pedido y lo envía al WhatsApp de la sede. | Pedido enviado automáticamente a la sede. |
| **RF12: Tours guiados** | Primer ingreso o activación manual | Muestra un recorrido explicativo por la aplicación. | Usuario orientado en el uso del sistema. |
| **RF13: Navegación responsiva** | Dispositivo utilizado (móvil, tablet, desktop) | La aplicación se adapta al dispositivo manteniendo funcionalidad completa. | Interfaz ajustada y usable en cualquier dispositivo. |

</div>

<div class="mt-8 p-4 bg-purple-50 rounded-lg">
  <h4 class="text-purple-800 font-semibold">🔗 Integración y UX</h4>
  <p class="text-purple-700 text-sm mt-2">Estos requerimientos aseguran una experiencia fluida desde la colocación del pedido hasta su procesamiento en la sede.</p>
</div>

---
layout: section
class: text-center
---

# Requerimientos No Funcionales
## Calidad y Rendimiento del Sistema

<div class="text-lg opacity-80 mt-4">
Especificaciones técnicas para garantizar un sistema robusto y eficiente
</div>

---
layout: default
---

# Requerimientos No Funcionales (RNF1-RNF4)
## Rendimiento y Usabilidad

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RNF1: Tiempo de respuesta** | Solicitudes del usuario | El sistema debe responder en menos de 3 segundos para carga inicial y menos de 500ms en búsquedas. | Respuesta rápida validada en pruebas de rendimiento. |
| **RNF2: Optimización de recursos** | Imágenes, recursos JS/CSS | Se deben usar imágenes optimizadas, bundle <2MB y lazy loading. | Aplicación ligera y optimizada para web. |
| **RNF3: Usabilidad** | Interacción del usuario | La interfaz debe ser intuitiva, con botones grandes y feedback visual. | Usuarios completan pedidos sin dificultad. |
| **RNF4: Accesibilidad** | Navegación con teclado, lectores de pantalla | Cumplimiento de estándares WCAG 2.1 nivel AA. | Aplicación accesible para todo tipo de usuarios. |

</div>

<div class="mt-6 flex gap-4">
  <div class="flex items-center gap-2">
    <span class="w-3 h-3 bg-green-500 rounded-full"></span>
    <span class="text-sm">⚡ Rendimiento</span>
  </div>
  <div class="flex items-center gap-2">
    <span class="w-3 h-3 bg-blue-500 rounded-full"></span>
    <span class="text-sm">🎨 UX/UI</span>
  </div>
</div>

---
layout: default
---

# Requerimientos No Funcionales (RNF5-RNF8)
## Compatibilidad y Seguridad

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RNF5: Compatibilidad navegadores** | Navegador usado por cliente | Funciona en Chrome, Firefox, Safari y Edge en versiones mínimas definidas. | Aplicación accesible en todos los navegadores soportados. |
| **RNF6: Compatibilidad dispositivos** | Dispositivo móvil o desktop | Funciona en iOS 12+, Android 8+ y pantallas de 320px a 2560px, con PWA. | Aplicación instalada como PWA y funcionando en múltiples dispositivos. |
| **RNF7: Seguridad de datos** | Datos del cliente | Todo tráfico por HTTPS y sanitización de entradas. | Datos transmitidos y validados de forma segura. |
| **RNF8: Privacidad** | Datos del cliente | Cumplimiento de regulaciones, uso solo para procesar pedidos. | Datos protegidos y tratados bajo consentimiento. |

</div>

<div class="mt-8 p-4 bg-orange-50 rounded-lg">
  <h4 class="text-orange-800 font-semibold">🔒 Seguridad y Compatibilidad</h4>
  <p class="text-orange-700 text-sm mt-2">El sistema garantiza funcionamiento seguro en múltiples plataformas y dispositivos.</p>
</div>

---
layout: default
---

# Requerimientos No Funcionales (RNF9-RNF11)
## Mantenimiento y Escalabilidad

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RNF9: Mantenibilidad** | Código fuente, documentación | Código modular, pruebas ≥70% y documentación clara. | Sistema mantenible y escalable. |
| **RNF10: Configuración dinámica** | Archivos de configuración (sedes, menú, precios) | Permite actualizar sedes y precios sin modificar el código. | Sistema parametrizable desde archivos externos. |
| **RNF11: Escalabilidad** | Número de usuarios concurrentes, pedidos por hora | Soporta hasta 1000 usuarios simultáneos y 500 pedidos/hora. | Sistema estable bajo alta demanda. |

</div>

<div class="mt-8 grid grid-cols-3 gap-4 text-center">
  <div class="p-3 bg-indigo-50 rounded-lg">
    <div class="text-2xl font-bold text-indigo-600">≥70%</div>
    <div class="text-sm text-indigo-800">Cobertura de Pruebas</div>
  </div>
  <div class="p-3 bg-indigo-50 rounded-lg">
    <div class="text-2xl font-bold text-indigo-600">1000</div>
    <div class="text-sm text-indigo-800">Usuarios Simultáneos</div>
  </div>
  <div class="p-3 bg-indigo-50 rounded-lg">
    <div class="text-2xl font-bold text-indigo-600">500</div>
    <div class="text-sm text-indigo-800">Pedidos/Hora</div>
  </div>
</div>

---
layout: default
---

# Requerimientos No Funcionales (RNF12-RNF14)
## Disponibilidad y Monitoreo

<div class="text-sm">

| Nombre | Entradas | Descripción | Resultado |
|--------|----------|-------------|-----------|
| **RNF12: Disponibilidad** | Eventos de error o mantenimiento | Uptime ≥99.5% con autorecuperación y mensajes de mantenimiento. | Sistema siempre disponible para el cliente. |
| **RNF13: Integración con APIs externas** | Servicios externos (WhatsApp, etc.) | Manejo de errores y timeouts en integraciones. | Sistema resiliente a fallos externos. |
| **RNF14: Monitoreo** | Logs, métricas de uso | Registro de errores, métricas y alertas críticas. | Sistema monitoreado y con alertas activas. |

</div>

<div class="mt-8 p-6 bg-gradient-to-r from-green-50 to-blue-50 rounded-lg">
  <div class="flex items-center gap-4">
    <div class="text-4xl">📊</div>
    <div>
      <h4 class="text-lg font-semibold text-gray-800">Monitoreo Continuo</h4>
      <p class="text-sm text-gray-600">Disponibilidad ≥99.5% con sistema de alertas y autorecuperación</p>
    </div>
  </div>
</div>

---
layout: default
---

# 👥 Historias de Usuario - Índice
## 7 Épicas | 13 Historias de Usuario

<div class="grid grid-cols-2 gap-8 mt-8">
<div>

### **Épica 1: Exploración del Menú**
- HU-001: Descubrir productos disponibles
- HU-002: Encontrar mi hamburguesa ideal
- HU-003: Personalizar mi pedido

### **Épica 2: Gestión del Pedido**
- HU-004: Armar mi pedido gradualmente
- HU-005: Revisar antes de confirmar

### **Épica 3: Selección de Ubicación**
- HU-006: Elegir la sede más conveniente
- HU-007: Acceso directo por ubicación

</div>
<div>

### **Épica 4: Modalidades de Entrega**
- HU-008: Recibir mi pedido en casa
- HU-009: Recoger en sede para ahorrar

### **Épica 5: Facturación y Pagos**
- HU-010: Obtener factura para mi empresa

### **Épica 6: Comunicación y Seguimiento**
- HU-011: Confirmar mi pedido fácilmente

### **Épica 7: Experiencia de Usuario**
- HU-012: Aprender a usar la aplicación
- HU-013: Usar desde cualquier dispositivo

</div>
</div>
---
layout: default
---

# HU-001: Descubrir productos disponibles
## Épica 1: Exploración del Menú

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente hambriento que visita por primera vez,  
**Quiero** explorar fácilmente el menú completo de hamburguesas y productos,  
**Para** conocer todas las opciones disponibles y tomar una decisión informada.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo ver productos organizados por categorías claras</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Cada producto muestra imagen apetitosa, nombre, descripción y precio</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo navegar entre categorías sin perder mi lugar</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>La información se carga rápidamente en mi dispositivo móvil</span>
    </div>
  </div>
</div>

---
layout: default
---

# HU-002: Encontrar mi hamburguesa ideal
## Épica 1: Exploración del Menú

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente con preferencias específicas,  
**Quiero** buscar productos por nombre o ingredientes,  
**Para** encontrar rápidamente lo que se me antoja sin revisar todo el menú.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo escribir en un buscador y ver resultados inmediatos</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Los resultados incluyen productos que coincidan con mi búsqueda</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Recibo un mensaje claro cuando no hay coincidencias</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo limpiar la búsqueda y volver al menú completo</span>
    </div>
  </div>
</div>

---
layout: default
---

# HU-003: Personalizar mi pedido
## Épica 1: Exploración del Menú

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente con gustos particulares,  
**Quiero** personalizar mis hamburguesas agregando o quitando ingredientes,  
**Para** obtener exactamente lo que deseo comer.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo agregar papas francesas o rústicas a mi hamburguesa</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo añadir ingredientes extra como quesos adicionales o carnes</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo escribir instrucciones especiales para el chef</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Veo el precio actualizado automáticamente con mis personalizaciones</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

# HU-004: Armar mi pedido gradualmente
## Épica 2: Gestión del Pedido

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente indeciso,  
**Quiero** agregar productos a un carrito mientras sigo explorando,  
**Para** construir mi pedido completo sin prisa y sin perder lo que ya elegí.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo agregar productos al carrito desde cualquier página</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Veo un contador que me indica cuántos productos llevo</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo modificar cantidades directamente desde el carrito</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>El total se actualiza automáticamente con cada cambio</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

# HU-005: Revisar antes de confirmar
## Épica 2: Gestión del Pedido

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente cuidadoso con mi dinero,  
**Quiero** ver un resumen detallado de mi pedido antes de enviarlo,  
**Para** asegurarme de que todo esté correcto y conocer el costo total.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Veo todos los productos con sus personalizaciones específicas</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>El desglose incluye subtotal, impuestos (INC 8%) y total final</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo editar o eliminar productos desde el resumen</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Las instrucciones especiales se muestran claramente</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

# HU-006: Elegir la sede más conveniente
## Épica 3: Selección de Ubicación

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente que conoce las diferentes sedes,  
**Quiero** seleccionar la sede de mi preferencia,  
**Para** hacer mi pedido en la ubicación que me resulte más cómoda.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Veo todas las sedes disponibles con sus direcciones</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo ver información de contacto de cada sede</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>La selección se mantiene mientras navego por la aplicación</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo cambiar de sede en cualquier momento antes de confirmar</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

---
layout: default
---

# HU-008: Recibir mi pedido en casa
## Épica 4: Modalidades de Entrega

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente que prefiere comodidad,  
**Quiero** solicitar entrega a domicilio,  
**Para** disfrutar mi comida sin salir de casa.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo ingresar mi dirección completa y datos de contacto</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Selecciono mi método de pago preferido (efectivo, Bancolombia, Nequi)</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Recibo un número de pedido para hacer seguimiento</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>El pedido se envía automáticamente por WhatsApp a la sede</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

---
layout: default
---

# HU-009: Recoger en sede para ahorrar
## Épica 4: Modalidades de Entrega

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente que quiere evitar costo domicilio,  
**Quiero** recoger mi pedido directamente en la sede,  
**Para** ahorrar dinero y obtener mi comida más rápido.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo seleccionar la sede donde quiero recoger</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Solo necesito proporcionar datos básicos de contacto</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Recibo un código de recogida único</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Obtengo confirmación por WhatsApp con los detalles</span>
    </div>
  </div>
</div>

</div>

</div>

---
layout: default
---

# HU-010: Obtener factura para mi empresa
## Épica 5: Facturación y Pagos

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente empresarial,  
**Quiero** solicitar factura con mis datos tributarios,  
**Para** poder deducir el gasto o presentar comprobantes contables.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo marcar la opción de facturación durante el pedido</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Ingreso mi cédula y email para recibir la factura</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>La factura se genera en formato PDF profesional</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo descargar e imprimir la factura inmediatamente</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

# HU-011: Confirmar mi pedido fácilmente
## Épica 6: Comunicación y Seguimiento

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente que completa su pedido,  
**Quiero** que el sistema envíe automáticamente mi orden por WhatsApp,  
**Para** confirmar rápidamente sin tener que escribir todo manualmente.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>El mensaje incluye todos los detalles de mi pedido</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Se abre WhatsApp automáticamente con el mensaje pre-escrito</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo revisar y modificar el mensaje antes de enviarlo</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>El mensaje llega al WhatsApp correcto de la sede seleccionada</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

# HU-012: Aprender a usar la aplicación
## Épica 7: Experiencia de Usuario

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente nuevo en la plataforma,  
**Quiero** recibir orientación sobre cómo hacer mi pedido,  
**Para** completar mi orden sin confusiones ni errores.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Se me ofrece un tour guiado en mi primera visita</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo activar ayuda contextual cuando la necesite</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Los tours son específicos para cada sección de la aplicación</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Puedo saltar o repetir el tour según mi preferencia</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

# HU-013: Usar desde cualquier dispositivo
## Épica 7: Experiencia de Usuario

<div class="mt-8">

<div class="text-lg mb-6">
**Como** cliente moderno,  
**Quiero** hacer pedidos desde mi celular, tablet o computadora,  
**Para** tener flexibilidad total sin importar dónde esté.
</div>

<div class="bg-orange-50 p-6 rounded-lg border border-orange-200">
  <h4 class="text-orange-800 font-semibold text-lg mb-4">📋 Criterios de Aceptación</h4>
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>La aplicación funciona perfectamente en mi dispositivo móvil</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Todas las funciones están disponibles en pantallas pequeñas</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>La navegación es intuitiva con gestos táctiles</span>
    </div>
    <div class="flex items-start gap-3">
      <span class="text-green-600 text-xl">✅</span>
      <span>Los botones son suficientemente grandes para tocar fácilmente</span>
    </div>
  </div>
</div>

</div>

---
layout: default
---

# Tecnologías Utilizadas
## Stack Tecnológico del Sistema

<div class="grid grid-cols-4 gap-6 mt-8">

<div>
  <h3 class="text-lg font-bold text-blue-600 mb-4">🚀 Frontend</h3>
  <div class="space-y-2 text-sm">
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-blue-500 rounded-full"></span>
      <span><strong>React 18.3.1</strong> - Framework principal</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-blue-500 rounded-full"></span>
      <span><strong>TypeScript</strong> - Tipado estático</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-blue-500 rounded-full"></span>
      <span><strong>Vite</strong> - Build tool y dev server</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-blue-500 rounded-full"></span>
      <span><strong>Tailwind CSS</strong> - Framework de estilos</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-blue-500 rounded-full"></span>
      <span><strong>React Router DOM</strong> - Navegación</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-blue-500 rounded-full"></span>
      <span><strong>GSAP</strong> - Animaciones</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-blue-500 rounded-full"></span>
      <span><strong>Leaflet</strong> - Mapas interactivos</span>
    </div>
  </div>
</div>

<div>
  <h3 class="text-lg font-bold text-red-600 mb-4">🔧 Backend</h3>
  <div class="space-y-2 text-sm">
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-red-500 rounded-full"></span>
      <span><strong>API REST</strong> - Gestión de menú</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-red-500 rounded-full"></span>
      <span><strong>CRUD Productos</strong> - Operaciones completas</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-red-500 rounded-full"></span>
      <span><strong>Gestión Categorías</strong> - Organización del menú</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-red-500 rounded-full"></span>
      <span><strong>Control de Sedes</strong> - Disponibilidad por ubicación</span>
    </div>
  </div>
</div>

<div>
  <h3 class="text-lg font-bold text-green-600 mb-4">📚 Librerías Adicionales</h3>
  <div class="space-y-2 text-sm">
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-green-500 rounded-full"></span>
      <span><strong>Lucide React</strong> - Iconografía</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-green-500 rounded-full"></span>
      <span><strong>Driver.js</strong> - Tours guiados</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-green-500 rounded-full"></span>
      <span><strong>jsPDF</strong> - Generación de PDFs</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-green-500 rounded-full"></span>
      <span><strong>QRCode</strong> - Generación de códigos QR</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-green-500 rounded-full"></span>
      <span><strong>UUID</strong> - Identificadores únicos</span>
    </div>
  </div>
</div>

<div>
  <h3 class="text-lg font-bold text-purple-600 mb-4">🛠️ Herramientas de Desarrollo</h3>
  <div class="space-y-2 text-sm">
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-purple-500 rounded-full"></span>
      <span><strong>ESLint</strong> - Linting de código</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-purple-500 rounded-full"></span>
      <span><strong>PostCSS</strong> - Procesamiento de CSS</span>
    </div>
    <div class="flex items-center gap-2">
      <span class="w-2 h-2 bg-purple-500 rounded-full"></span>
      <span><strong>Autoprefixer</strong> - Prefijos CSS automáticos</span>
    </div>
  </div>
</div>

</div>

<div class="mt-8 p-4 bg-gradient-to-r from-blue-50 to-purple-50 rounded-lg">
  <h4 class="text-lg font-semibold text-gray-800 mb-2">🎯 Stack Moderno y Escalable</h4>
  <p class="text-sm text-gray-600">Arquitectura completa frontend-backend con tecnologías de vanguardia que garantizan rendimiento, mantenibilidad y experiencia de usuario excepcional.</p>
</div>

---
layout: center
class: text-center
---

# Resumen del Sistema

<div class="grid grid-cols-2 gap-12 mt-8">

<div class="text-left">
  <h3 class="text-xl font-bold text-blue-600 mb-4">📋 Requerimientos Funcionales</h3>
  <div class="space-y-2 text-sm">
    <div>✅ <strong>13 requerimientos</strong> definidos</div>
    <div>🛒 Gestión completa de pedidos</div>
    <div>📱 Experiencia responsiva</div>
    <div>💬 Integración con WhatsApp</div>
    <div>🧾 Facturación automática</div>
  </div>
</div>

<div class="text-left">
  <h3 class="text-xl font-bold text-green-600 mb-4">⚙️ Requerimientos No Funcionales</h3>
  <div class="space-y-2 text-sm">
    <div>✅ <strong>14 requerimientos</strong> definidos</div>
    <div>⚡ Respuesta &lt; 3s / &lt; 500ms</div>
    <div>🔒 Seguridad HTTPS + WCAG 2.1</div>
    <div>📊 Disponibilidad ≥99.5%</div>
    <div>🚀 1000 usuarios simultáneos</div>
  </div>
</div>

</div>

<div class="mt-12 text-lg font-semibold text-gray-700">
  Sistema robusto y escalable para gestión de pedidos gastronómicos
</div>

---
layout: end
class: text-center
---

# ¡Gracias!

¿Preguntas sobre los requerimientos?

<div class="mt-8 text-sm opacity-70">
Documentación técnica - Sistema de Pedidos v1.0
</div>