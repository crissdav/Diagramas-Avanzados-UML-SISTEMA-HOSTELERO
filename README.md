# 📊 Diagramas de Secuencia - Sistema de Gestión Hotelera

## 📋 Descripción General

Este repositorio contiene los **diagramas de secuencia** para el Sistema de Gestión Hotelera, desarrollados como parte de la especificación detallada de casos de uso. Los diagramas representan las interacciones entre actores y objetos del sistema, siguiendo la notación UML (Lenguaje Unificado de Modelado) mediante PlantUML.

---

## 🗂️ Estructura del Proyecto
diagramas-secuencia/
├── README.md # Este archivo
├── 01-autenticacion/ # Módulo de Autenticación y Seguridad
│ ├── CU-01-inicio-sesion-exitoso.puml
│ ├── CU-01-credenciales-incorrectas.puml
│ └── CU-01-cerrar-sesion.puml
├── 02-gestion-habitaciones/ # Módulo de Gestión de Habitaciones
│ ├── CU-02-visualizar-estado.puml
│ ├── CU-02-cambiar-estado.puml
│ └── CU-02-gestionar-tarifas.puml
├── 03-consultar-disponibilidad/ # Consulta de Disponibilidad
│ └── CU-03-buscar-disponibilidad.puml
├── 04-gestion-huespedes/ # Gestión de Huéspedes
│ ├── CU-04-registrar-nacional.puml
│ └── CU-04-registrar-extranjero.puml
├── 05-check-in/ # Módulo de Check-in
│ └── CU-05-check-in-completo.puml
├── 06-gestion-reservas/ # Módulo de Reservas
│ ├── CU-06-registrar-reserva.puml
│ ├── CU-06-confirmar-reserva.puml
│ ├── CU-06-modificar-reserva.puml
│ ├── CU-06-cancelar-reserva.puml
│ └── CU-06-consultar-reservas.puml
├── 07-ampliacion/ # Módulo de Ampliación de Estadía
│ ├── CU-07-ampliacion-exitosa.puml
│ └── CU-07-conflicto-reservas.puml
├── 08-pagos/ # Módulo de Pagos
│ └── CU-08-registrar-pago.puml
├── 09-check-out/ # Módulo de Check-out
│ ├── CU-09-check-out-exitoso.puml
│ └── CU-09-saldo-pendiente.puml
├── 10-limpieza/ # Módulo de Limpieza
│ └── CU-10-finalizar-limpieza.puml
├── 11-historial/ # Módulo de Historial
│ └── CU-11-consultar-historial.puml
├── 12-reporte-ocupacion/ # Módulo de Reporte de Ocupación
│ └── CU-12-reporte-ocupacion.puml
├── 13-reporte-ingresos/ # Módulo de Reporte de Ingresos
│ └── CU-13-reporte-ingresos.puml
└── 14-auditoria/ # Módulo de Auditoría
└── CU-14-consultar-auditoria.puml

---

## 📊 Resumen de Diagramas

| Módulo | Casos de Uso | Diagramas | RF Relacionados |
|--------|--------------|-----------|-----------------|
| **Autenticación** | CU-01 | 3 | RF-01, RF-01.1 |
| **Habitaciones** | CU-02 | 3 | RF-02.1, RF-02.2, RF-02.3 |
| **Disponibilidad** | CU-03 | 1 | RF-02, RF-07.5 |
| **Huéspedes** | CU-04 | 2 | RF-03, RF-03.1, RF-03.3, RF-03.4 |
| **Check-in** | CU-05 | 1 | RF-03.2, RF-04.6 |
| **Reservas** | CU-06 | 5 | RF-04.1, RF-04.2, RF-04.3, RF-04.4, RF-04.5, RF-04.6 |
| **Ampliación** | CU-07 | 2 | RF-05.1, RF-05.2, RF-05.3, RF-05.4, RF-05.5 |
| **Pagos** | CU-08 | 1 | RF-06.5, RF-06.6 |
| **Check-out** | CU-09 | 2 | RF-06.1, RF-06.7, RF-06.8 |
| **Limpieza** | CU-10 | 1 | RF-07.1, RF-07.2, RF-07.3 |
| **Historial** | CU-11 | 1 | RF-07.4 |
| **Reporte Ocupación** | CU-12 | 1 | RF-08 |
| **Reporte Ingresos** | CU-13 | 1 | RF-08.1 |
| **Auditoría** | CU-14 | 1 | RF-01.2 |
| **TOTAL** | **14** | **25** | **23 RF** |

---

## 🔍 Descripción de Diagramas por Módulo

### 1️⃣ Autenticación y Seguridad (01-autenticacion/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-01-inicio-sesion-exitoso.puml` | Inicio de sesión con credenciales válidas | Principal |
| `CU-01-credenciales-incorrectas.puml` | Manejo de intentos fallidos y bloqueo de cuenta | Alternativo |
| `CU-01-cerrar-sesion.puml` | Cierre seguro de sesión | Principal |

**RF Relacionados:** RF-01, RF-01.1  
**RN Aplicables:** RN-17

---

### 2️⃣ Gestión de Habitaciones (02-gestion-habitaciones/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-02-visualizar-estado.puml` | Mapa/lista de habitaciones con estados | Principal |
| `CU-02-cambiar-estado.puml` | Cambio a "Fuera de Servicio" con validaciones | Principal |
| `CU-02-gestionar-tarifas.puml` | Configuración de precios por tipo y temporada | Principal |

**RF Relacionados:** RF-02.1, RF-02.2, RF-02.3  
**RN Aplicables:** RN-09, RN-10

---

### 3️⃣ Consulta de Disponibilidad (03-consultar-disponibilidad/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-03-buscar-disponibilidad.puml` | Búsqueda con filtros (tipo, capacidad, fechas) | Principal |

**RF Relacionados:** RF-02, RF-07.5  
**RN Aplicables:** -

---

### 4️⃣ Gestión de Huéspedes (04-gestion-huespedes/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-04-registrar-nacional.puml` | Registro con DNI y validación MINCETUR | Principal |
| `CU-04-registrar-extranjero.puml` | Registro con pasaporte y datos adicionales | Principal |

**RF Relacionados:** RF-03, RF-03.1, RF-03.3, RF-03.4  
**RN Aplicables:** RN-01, RN-02, RN-03, RN-04, RN-16, RN-17

**Nota:** La validación de mayoría de edad (RF-03.4 anterior) ha sido eliminada. Ahora RF-03.4 corresponde únicamente a "Validar Campos Obligatorios MINCETUR".

---

### 5️⃣ Check-in (05-check-in/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-05-check-in-completo.puml` | Registro completo de ingreso de huésped | Principal |

**RF Relacionados:** RF-03.2, RF-04.6  
**RN Aplicables:** RN-01, RN-02, RN-03, RN-04, RN-06, RN-12, RN-13, RN-14, RN-16, RN-17

**Nota:** La validación de mayoría de edad ha sido eliminada del flujo de check-in.

---

### 6️⃣ Gestión de Reservas (06-gestion-reservas/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-06-registrar-reserva.puml` | Creación de reserva para fechas futuras | Principal |
| `CU-06-confirmar-reserva.puml` | Cambio de estado a "Confirmada" | Principal |
| `CU-06-modificar-reserva.puml` | Actualización de fechas, tipo o datos | Principal |
| `CU-06-cancelar-reserva.puml` | Cancelación con validación de anticipación | Principal |
| `CU-06-consultar-reservas.puml` | Búsqueda con filtros | Principal |

**RF Relacionados:** RF-04.1, RF-04.2, RF-04.3, RF-04.4, RF-04.5, RF-04.6  
**RN Aplicables:** RN-10, RN-15

---

### 7️⃣ Ampliación de Estadía (07-ampliacion/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-07-ampliacion-exitosa.puml` | Verificación, cálculo y actualización de fecha | Principal |
| `CU-07-conflicto-reservas.puml` | Manejo de superposición con reservas | Alternativo |

**RF Relacionados:** RF-05.1, RF-05.2, RF-05.3, RF-05.4, RF-05.5  
**RN Aplicables:** RN-05, RN-11

---

### 8️⃣ Gestión de Pagos (08-pagos/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-08-registrar-pago.puml` | Registro de pago parcial o total | Principal |

**RF Relacionados:** RF-06.5, RF-06.6  
**RN Aplicables:** RN-06, RN-07

---

### 9️⃣ Check-out (09-check-out/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-09-check-out-exitoso.puml` | Validación de saldo y registro de salida | Principal |
| `CU-09-saldo-pendiente.puml` | Manejo de saldo pendiente | Alternativo |

**RF Relacionados:** RF-06.1, RF-06.7, RF-06.8  
**RN Aplicables:** RN-09

---

### 🔟 Gestión de Limpieza (10-limpieza/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-10-finalizar-limpieza.puml` | Marcar habitación como "Disponible" | Principal |

**RF Relacionados:** RF-07.1, RF-07.2, RF-07.3  
**RN Aplicables:** RN-09

---

### 1️⃣1️⃣ Historial de Estadías (11-historial/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-11-consultar-historial.puml` | Consulta con filtros por fechas, huésped, habitación | Principal |

**RF Relacionados:** RF-07.4  
**RN Aplicables:** RN-17

---

### 1️⃣2️⃣ Reporte de Ocupación (12-reporte-ocupacion/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-12-reporte-ocupacion.puml` | Generación por período (diario, semanal, mensual) | Principal |

**RF Relacionados:** RF-08  
**RN Aplicables:** -

---

### 1️⃣3️⃣ Reporte de Ingresos (13-reporte-ingresos/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-13-reporte-ingresos.puml` | Desglose por tipo de habitación y método de pago | Principal |

**RF Relacionados:** RF-08.1  
**RN Aplicables:** -

---

### 1️⃣4️⃣ Auditoría del Sistema (14-auditoria/)

| Archivo | Descripción | Flujo |
|---------|-------------|-------|
| `CU-14-consultar-auditoria.puml` | Filtros por usuario, fecha, tipo de acción | Principal |

**RF Relacionados:** RF-01.2  
**RN Aplicables:** RN-17

---

## 🛠️ Requisitos de Herramientas

Para visualizar y editar los diagramas, necesitas:

| Herramienta | Versión | Enlace |
|-------------|---------|--------|
| **Visual Studio Code** | v1.80+ | https://code.visualstudio.com/ |
| **Extensión PlantUML** | v2.17+ | https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml |
| **Java (JRE)** | v11+ | https://adoptium.net/ |
| **Graphviz** | v9.0+ | https://graphviz.org/download/ |

### 📌 Configuración del Entorno

1. **Instalar Java**: `java -version` (debe mostrar v11 o superior)
2. **Instalar Graphviz**: `dot -V` (debe mostrar la versión)
3. **Instalar extensión PlantUML** en VS Code
4. **Configurar VS Code** con el archivo `.vscode/settings.json`:

```json
{
    "plantuml.render": "plantuml.jar",
    "plantuml.previewAutoUpdate": true,
    "plantuml.theme": "light",
    "plantuml.encoding": "UTF-8"
}

📖 Cómo Visualizar un Diagrama
Abrir el archivo .puml en VS Code
Presionar Alt + D (Windows/Linux) o Cmd + Shift + V (Mac)
Ver la vista previa del diagrama en tiempo real
Exportar a PNG/SVG: Ctrl+Shift+P → PlantUML: Export Current Diagram

📝 Convenciones de Nombramiento
Elemento	Convención	Ejemplo
Archivo	CU-XX-nombre.puml	CU-05-check-in-completo.puml
Actor	actor "Nombre" as A	actor "Recepcionista" as R
Participante	participant ":Nombre" as P	participant ":ControladorCheckIn" as CCI
Base de Datos	database ":Nombre" as DB	database ":BaseDatos" as BD
Mensaje	A -> B: 1. acción()	R -> I: 1. iniciarCheckIn()
Retorno	B --> A: resultado	BD --> CCI: 4. datosUsuario
Condicional	alt condición	alt Credenciales válidas

📌 Notación de Mensajes
Símbolo	Significado
->	Mensaje síncrono (llamada)
-->	Mensaje de retorno
activate	Activar línea de vida
deactivate	Desactivar línea de vida
alt ... else ... end	Condicional (alternativa)
loop ... end	Bucle (iteración)
note right	Nota explicativa

🔗 Matriz de Trazabilidad (CU ↔ RF)
Caso de Uso	Requisitos Funcionales
CU-01	RF-01, RF-01.1
CU-02	RF-02.1, RF-02.2, RF-02.3
CU-03	RF-02, RF-07.5
CU-04	RF-03, RF-03.1, RF-03.3, RF-03.4, RF-03.5
CU-05	RF-03.2, RF-04.6
CU-06	RF-04.1, RF-04.2, RF-04.3, RF-04.4, RF-04.5, RF-04.6
CU-07	RF-05.1, RF-05.2, RF-05.3, RF-05.4, RF-05.5
CU-08	RF-06.5, RF-06.6
CU-09	RF-06.1, RF-06.7, RF-06.8
CU-10	RF-07.1, RF-07.2, RF-07.3
CU-11	RF-07.4
CU-12	RF-08
CU-13	RF-08.1
CU-14	RF-01.2

🏷️ Reglas de Negocio Aplicables
Código	Descripción
RN-01	Registro obligatorio previo
RN-02	Cumplimiento de normativa MINCETUR
RN-03	Documento de identidad obligatorio
RN-04	Registro de menores acompañantes
RN-05	Cobro por permanencia adicional
RN-06	Pago garantizado para el hospedaje
RN-07	Responsabilidad por daños
RN-09	Limpieza obligatoria de habitaciones
RN-10	Confirmación obligatoria de reserva
RN-11	Restricción para ampliación de estadía
RN-15	Política de cancelación de reservas
RN-16	Validación de huéspedes extranjeros
RN-17	Confidencialidad de la información

📚 Recursos Adicionales
PlantUML - Guía Oficial: https://plantuml.com/es/

Sintaxis de Diagramas de Secuencia: https://plantuml.com/es/sequence-diagram

UML - Diagramas de Secuencia: https://www.uml-diagrams.org/sequence-diagrams.html