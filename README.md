# Guía de instalación y conexión del sistema Notion

Esta guía detalla los pasos necesarios para configurar el sistema de gestión en Notion con sus integraciones externas.

Algunos pasos serán realizados por el equipo técnico y otros requieren acción del cliente.

---

## 1. Preparación (a cargo del implementador)

No requiere acción del cliente.

Antes de comenzar, el equipo técnico realizará las siguientes configuraciones:

- Asignar al cliente como propietario del espacio de trabajo de Notion.
- Configurar el proyecto de Google Workspace con los permisos correspondientes.
- Activar las APIs necesarias y verificar los usuarios de prueba.

> Estas acciones son necesarias para que las integraciones funcionen correctamente más adelante.
> 

---

## 2. Configuración de Notion

**Acciones a realizar por el cliente:**

- [ ]  Acceder al espacio de trabajo compartido de Notion.
- [ ]  Crear una integración propia desde [Notion My Integrations](https://www.notion.so/my-integrations).
- [ ]  Copiar el código secreto (Internal Integration Token) generado por Notion.
- [ ]  Guarda el código para cargarlo en la credencial en n8n, según se indique.
- [ ]  Activar la integración en la base de datos principal (DB) del sistema.

---

## 3. Conexión con Notion Calendar

**Acciones a realizar por el cliente:**

- [ ]  Abrir Notion Calendar.
- [ ]  Hacer clic en “Obtener Calendar” (parte superior derecha).
- [ ]  Seleccionar la cuenta de Notion correspondiente al sistema.
- [ ]  En el panel lateral izquierdo, añadir los siguientes calendarios del sistema unificado:
    - [ ]  Eventos
    - [ ]  Tareas
    - [ ]  Ideas
    - [ ]  Notas (generales y sin fecha)
- [ ]  Eliminar los calendarios predeterminados de Notion que no se utilicen.

---

## 4. Configuración en Gmail

**Acciones a realizar por el cliente:**

- [ ]  Ingresar a la cuenta de Gmail vinculada al sistema.
- [ ]  Crear las siguientes etiquetas:
    - [ ]  `<Notion>` → para los correos que deben sincronizarse con el sistema.
    - [ ]  `<Listo_Notion>` → para los correos ya procesados por Notion o n8n.

> Estas etiquetas permiten automatizar el flujo de correos y su integración con Notion.
> 

---

## 5. Integración con n8n

**Acciones conjuntas (cliente y equipo técnico):**

- [ ]  Importar las plantillas de flujos (workflows) proporcionadas por el equipo técnico.
- [ ]  Crear las siguientes credenciales en n8n:
    - [ ]  Notion
    - [ ]  Gmail (una por cada cuenta vinculada)
    - [ ]  Notion Calendar
    - [ ]  OpenAI
    - [ ]  Redis
    - [ ]  WhatsApp Cloud API
- [ ]  Verificar que todos los flujos estén correctamente conectados y activos.
