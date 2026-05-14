# Sistema de Gestion Hospitalaria (SGH)

Sistema de gestion hospitalaria desarrollado en Python con Programacion Orientada a Objetos para Google Colab. Interfaz con tema oscuro.

## Caracteristicas

- **Gestion de Pacientes**: Registrar, consultar, listar y actualizar datos de pacientes
- **Gestion de Medicos**: Administrar especialidades y medicos
- **Gestion de Citas**: Programar, consultar y cancelar citas medicas
- **Analisis de Datos**: Estadisticas hospitalarias

## Estructura del Notebook

El archivo `SGH.ipynb` contiene todo el codigo en un solo libro:

1. **Google Drive** - Montar y configurar rutas de archivos CSV
2. **Dependencias** - Instalar ipywidgets para interfaz interactiva
3. **Codigo Completo** - Modelos, Repositorios, Servicios y UI

## Requisitos

- Cuenta de Google Drive
- Acceso a Google Colab
- Carpeta `SGH/datos/` en Google Drive (se crea automaticamente)

## Instalacion

1. Descarga el archivo `SGH.ipynb`
2. Abre el archivo en Google Colab
3. Ejecuta todas las celdas (Ctrl+F9 o Runtime > Run All)
4. La aplicacion se mostrara automaticamente

## Uso

### Gestion de Pacientes
- **Registrar**: Numero de documento (campo numerico), nombre, fecha de nacimiento (selector de fecha), tipo de sangre, EPS, regimen, antecedentes. Formulario se reinicia automaticamente.
- **Consultar**: Busque por numero de documento. Boton "Limpiar" para buscar otro paciente. Fechas en formato DD/MM/AAAA.
- **Listar**: Vea todos los pacientes en tabla. Boton "Refrescar" para actualizar.
- **Actualizar**: Seleccione un paciente de la lista desplegable y actualice sus datos. Incluye boton "Refrescar".

### Gestion de Medicos
- **Especialidad**: Codigo (numerico), nombre, descripcion (placeholder: "Color")
- **Medico**: Numero de registro, nombre, especialidad (dropdown), consultorio, horario (fecha y hora)
- **Listar**: Vea todos los medicos o filtre por especialidad

### Gestion de Citas
- **Programar**: Seleccione paciente y medico de las listas, fecha (selector), hora (selector), motivo (placeholder: "ej. Control mensual")
- **Consultar/Cancelar**: Busque una cita por codigo y cancele si es necesario

## Navegacion

- Botones de navegacion con estado activo (verde = activo, gris = inactivo)
- Al hacer clic en un modulo, el boton correspondiente se activa automaticamente

## Interfaz

- **Tema oscuro** con colores vibrantes
- Diseño moderno con gradientes y sombras
- Badges para estados de citas
- Validacion de campos obligatorios
- Mensajes de exito y error claramente diferenciados

## Datos

Los datos se almacenan en Google Drive en formato **CSV** (`/content/drive/MyDrive/SGH/datos/`):
- `pacientes.csv`
- `medicos.csv`
- `especialidades.csv`
- `citas.csv`
- `consultas.csv`
- `tratamientos.csv`
- `medicamentos.csv`

Cada archivo CSV incluye encabezados con los nombres de las columnas.

## Validaciones

- Numero de documento: solo permite numeros (IntText)
- Fecha: selector de calendario (DatePicker)
- Hora: selector de hora (TimePicker)
- Listas desplegables: valores predefinidos y "Seleccionar..."
- Todos los campos obligatorios son validados antes de guardar

## Tecnologias

- Python 3
- Google Colab
- ipywidgets (interfaz interactiva)
- Google Drive (persistencia en CSV)

## Autor

Proyecto de Programacion Orientada a Objetos - Ingenieria de Software