# CerebroMA — Sistema de Gestión de Malá Argenta

Aplicación web de gestión empresarial para **Malá Argenta** (Praga), desarrollada como un único archivo HTML autocontenido. Sin servidor, sin dependencias externas de instalación — funciona directamente en el navegador con persistencia en `localStorage`.

---

## Stack técnico

| Tecnología | Uso |
|---|---|
| React 18 (Babel standalone) | UI y estado |
| Tailwind CSS (CDN) | Estilos |
| SheetJS (XLSX) | Exportación Excel |
| localStorage | Persistencia de datos |

> **Un solo archivo `.html`** — sin build, sin npm, sin servidor. Abrí el archivo en Chrome y listo.

---

## Módulos

### 💰 Gestión de Sueldos (`PayrollManager`)
- **Legajos de empleados** — ficha completa con datos personales, contratación, estudios, domicilio, datos bancarios, otro empleo, hijos, y datos para la empresa
- Campos condicionales: visa de trabajo (número, vigencia), residencia temporal (número de permiso), residencia permanente, ciudadanía europea
- Exportación individual por legajo en PDF y Excel (ES / EN / CZ)
- Exportación grupal de todos los legajos en un único PDF y Excel multi-sheet
- Plantilla Excel en blanco descargable (ES / EN / CZ) e importación automática
- Archivar/desarchivar empleados (no afecta pagos ni horas)
- **Pagos mensuales** con registro por empleado
- **Horas trabajadas** con ajustes por período
- **Seguros médicos**
- **Sueldos pagados / pendientes**
- **📝 Notas** con fecha objetivo, pin, resolver/archivar y badge de pendientes

### 💵 Caja Diaria (`CashRegister`)
- Registro de ingresos y costos diarios con múltiples facturas por costo
- Campo de notas por transacción, exportado en PDF y Excel
- Filtros por tipo, origen (Banco / Efectivo / Apps / Otros), proveedor, período
- **Registro Diario** — tabla con exportación PDF y Excel
- **Planeación y Ahorro**
- **Resumen Mensual** — tabla anual por rubro con columna de % sobre costos totales
- **Estadísticas**
- **📝 Notas** con fecha objetivo, badge de pendientes y archivo

### 📊 Datos y Estadísticas (`DashboardModule`)
KPIs, comparativas multi-año y narrativa automática.

### 🔐 Usuarios y Contraseñas (`CredencialesModule`)
Almacén informativo de credenciales (servicio, URL, usuario, contraseña con máscara, notas). Solo a modo de referencia interna.

### 📋 Seguimiento de Préstamos (`PrestamosModule`)
Registro y seguimiento de préstamos.

---

## Permisos y roles

Sistema de permisos por módulo y usuario con roles: `admin`, `editor`, `viewer` y `custom`. Configurable desde el módulo de Configuración.

---

## Idiomas

Interfaz disponible en **Español**, **English** y **Čeština**. Las exportaciones PDF y Excel también están disponibles en los tres idiomas.

---

## Uso

1. Descargar `Malagestion.html`
2. Abrir en **Google Chrome**
3. Los datos se guardan automáticamente en el navegador (`localStorage`)
4. Para backup: usar la función de **Exportar** dentro de la app

> ⚠️ Los datos son locales al navegador. Para compartir entre dispositivos, usar la función de exportar/importar backup.

---

## Estructura del archivo

```
Malagestion.html
├── <style>          Estilos globales + Tailwind CDN
├── <script>         Babel + React + SheetJS (CDN)
└── <script type="text/babel">
    ├── Malagestion()          Componente raíz, login, permisos, routing
    ├── DashboardModule()      Estadísticas
    ├── CredencialesModule()   Usuarios y contraseñas
    ├── PrestamosModule()      Préstamos
    ├── ExternalAppsModule()   (deshabilitado)
    ├── CashRegister()         Caja Diaria
    └── PayrollManager()       Gestión de Sueldos
```

---

## Desarrollado por

Cristian — propietario y product owner de Malá Argenta, Praga.
