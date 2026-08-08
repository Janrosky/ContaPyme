# ContaPyme — Libro contable digital

**ContaPyme** es una aplicación web de contabilidad y gestión financiera para pequeñas y medianas empresas (PyMEs) costarricenses, empaquetada en un único archivo HTML autocontenido. No requiere backend, base de datos ni instalación: se abre directamente en el navegador y persiste los datos con `localStorage`.

## ✨ Características

- **100% offline y sin dependencias de servidor.** Un solo archivo (`contapyme.html`) con HTML, CSS y JavaScript embebidos.
- **Persistencia local.** Los datos se guardan automáticamente en el `localStorage` del navegador.
- **Moneda en colones costarricenses (₡)** con formato numérico local (`es-CR`).
- **Facturación con exportación a PDF** mediante impresión del navegador (`window.print()`), con una plantilla de factura lista para imprimir/descargar.

## 📦 Módulos incluidos

| Módulo | Descripción |
|---|---|
| **Resumen** | Panel general (dashboard) con indicadores clave: cuentas por cobrar vs. pagar, KPIs del negocio. |
| **Facturas** | Creación de facturas con líneas de detalle, cálculo automático de totales y exportación a PDF. |
| **Clientes** | Directorio de clientes (nombre, identificación, teléfono, correo, notas). |
| **Cuentas por cobrar (CxC)** | Seguimiento de facturas pendientes de cobro, plazos y abonos. |
| **Proveedores** | Directorio de proveedores. |
| **Cuentas por pagar (CxP)** | Seguimiento de obligaciones con proveedores, plazos y abonos. |
| **Inventario** | Control de productos (código, existencia, costo unitario) con movimientos de entrada/salida. |
| **Planillas** | Cálculo de planilla con porcentajes de ley de Costa Rica (cuota obrera, cuota patronal, aguinaldo). |
| **Precio de venta** | Calculadora de precios sugeridos a partir de costo unitario, costos indirectos, costos fijos y margen de utilidad. |
| **Depreciación** | Registro de activos fijos con cálculo de depreciación según vida útil. |

## 🚀 Uso

1. Descarga o clona este repositorio.
2. Abre `contapyme.html` directamente en tu navegador (doble clic, o `Archivo > Abrir`).
3. Empieza a registrar clientes, facturas, inventario, etc. Todo se guarda automáticamente en tu navegador.
4. Usa el botón **"↺ Reiniciar datos de ejemplo"** en la barra lateral para restaurar los datos de demostración.

No requiere `npm install`, servidor local, ni configuración adicional.

## ⚠️ Limitaciones importantes

- **Los datos son locales al navegador.** Si abres el archivo desde otro equipo, otro navegador, o en modo incógnito, no verás la misma información — cada instancia de `localStorage` es independiente.
- **No hay sincronización ni respaldo en la nube.** Se recomienda exportar/respaldar la información periódicamente (por ejemplo, imprimiendo reportes a PDF) hasta que se implemente un mecanismo de exportación de datos completo.
- **No apto para múltiples usuarios simultáneos.** Al no tener backend, no hay control de concurrencia ni roles de usuario.
- Pensado como herramienta ligera para PyMEs; no reemplaza un sistema contable certificado para fines fiscales o de auditoría.

## 🛠️ Stack técnico

- HTML5 + CSS3 (variables CSS para theming, sin frameworks externos)
- JavaScript vanilla (sin frameworks ni build step)
- Web Storage API (`localStorage`) para persistencia
- Impresión nativa del navegador para generación de PDF

## 📁 Estructura del proyecto

```
contapyme/
└── contapyme.html   # Aplicación completa (HTML + CSS + JS)


Desarrollado por **Alejandro Chacón Garita** — [ACG Nextek](https://acg-nextek.vercel.app)
