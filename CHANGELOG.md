# Changelog — CerebroMA

Todos los cambios relevantes del proyecto ordenados cronológicamente.

---

## [Actual] — Abril 2026

### Módulo Sueldos — Legajos
- Legajo ampliado con datos personales completos: Rodné číslo, ČSSZ, sexo, estado civil, ciudad/país de nacimiento, DNI, pasaporte
- Sección **Contratación**: fecha de ingreso, puesto de trabajo, tipo de contrato, seguro médico + número, visa de trabajo (con número y vigencia), residencia temporal (con número de permiso + permiso de residencia), residencia permanente (con número), ciudadanía europea
- Sección **Estudios** con desplegable de niveles y área de estudios
- Sección **Pensión**, **Domicilio**, **Datos bancarios**, **Otro empleo** (con deducción fiscal), **Hijos** (por hijo: apellido, nombre, fecha nac., Rodné číslo)
- Sección **Datos para la empresa**: salario bruto, valor hora, frecuencia de pago
- Dos correos electrónicos separados: empresa y personal
- Campos condicionales: número de visa + vigencia (si tiene visa), número de permiso + permiso de residencia (si tiene residencia temporal), número de residencia permanente (si tiene residencia permanente)
- Exportación individual en PDF y Excel en ES/EN/CZ con traducción de sexo, estado civil y nivel de estudios
- Exportación grupal: todos los legajos en un único PDF (con salto de página por empleado) y Excel multi-sheet (sheet = nombre del empleado)
- Plantilla Excel en blanco en tres idiomas + importación automática con mapa exhaustivo de etiquetas
- Importación corrige fechas seriales de Excel a formato ISO
- Archivar/desarchivar empleados (gris, al final de la lista, sin afectar pagos ni horas)
- Cards de legajo plegables por defecto
- Botón eliminar movido dentro del modal de edición
- Botones de exportación discretos en cada card
- Badge de notas pendientes en el tab

### Módulo Sueldos — Notas
- Nuevo segmento **📝 Notas** idéntico al de Caja Diaria
- Fecha objetivo con destacado visual (vencida / hoy)
- Pin, resolver, reabrir, eliminar
- Badge rojo con cantidad de notas activas en el tab
- Persistencia en `payrollNotes` (localStorage separado)

### Caja Diaria
- Campo **Notas** disponible al cargar cualquier costo (no solo al editar)
- Columna Notas en la tabla de registro diario
- Notas exportadas en los 3 PDFs y Excel
- Columna **%** en el Resumen Mensual (% de cada rubro sobre el total de costos)
- Notas: fecha objetivo, badge de pendientes en el botón naranja, cards cuadradas en grid 2 columnas, orden por urgencia

### Módulo Usuarios y Contraseñas (nuevo)
- Almacén informativo de credenciales: servicio, URL, usuario, contraseña (con máscara y toggle), notas
- Búsqueda, edición, eliminación
- Aviso informativo sobre seguridad
- Persistencia en `credencialesData` (localStorage)

### General
- Botón **"Abrir en Chrome"** en el header (descarga el HTML actual)
- Módulo **Aplicaciones Externas** eliminado del home
- Badge de notas activas en botón de Notas de Caja Diaria

---

## [Anterior] — 2025

### Caja Diaria
- Módulo completo con registro de ingresos y costos, múltiples facturas por costo, filtros, exportación PDF y Excel
- Planeación y Ahorro, Resumen Mensual, Estadísticas, Notas

### Gestión de Sueldos
- Legajos básicos, pagos mensuales, horas trabajadas, seguros médicos, sueldos pagados/pendientes
- Sistema de permisos por módulo

### Sistema general
- Login con usuario + PIN
- Roles: admin, editor, viewer, custom
- Soporte trilingüe: ES / EN / CZ
- Dark mode
- Orden de módulos personalizable por usuario (localStorage)
- Módulo Dashboard con KPIs y comparativas
- Módulo Préstamos (placeholder)
