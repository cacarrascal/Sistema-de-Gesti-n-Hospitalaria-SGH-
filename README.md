# 🏥 Sistema de Gestion Hospitalaria (SGH)

Sistema de gestión hospitalaria desarrollado en Python con Programación Orientada a Objetos para Google Colab. Interfaz moderna con tema oscuro profesional.

## Caracteristicas

- **Dashboard Principal**: Contador de pacientes en tiempo real que se actualiza automáticamente al registrar nuevos pacientes
- **Gestion de Pacientes**: Registrar, consultar, listar y actualizar datos de pacientes
- **Gestion de Medicos**: Administrar especialidades y médicos con dropdown dinámico de especialidades
- **Gestion de Citas**: Programar, consultar, mostrar todas y cancelar citas médicas
- **Navegación SPA**: Un solo módulo visible a la vez, sin duplicados

## Estructura del Notebook

El archivo `SGH.ipynb` contiene todo el código en un solo libro:

1. **Google Drive** - Montar y configurar rutas de archivos CSV
2. **Dependencias** - Instalar ipywidgets para interfaz interactiva
3. **Codigo Completo** - Modelos, Repositorios, Servicios y UI

## Requisitos

- Cuenta de Google Drive
- Acceso a Google Colab
- Carpeta `SGH/datos/` en Google Drive (se crea automáticamente)

## Instalacion

1. Descarga el archivo `SGH.ipynb`
2. Abre el archivo en Google Colab
3. Ejecuta todas las celdas (Ctrl+F9 o Runtime > Run All)
4. La aplicación se mostrará automáticamente

## Uso

### Dashboard Principal
- Muestra el número total de pacientes registrados
- Se actualiza automáticamente al registrar nuevos pacientes
- Diseño visual profesional con tema oscuro

### Gestion de Pacientes
- **Registrar**: Número de documento, nombre, fecha de nacimiento (selector de fecha), tipo de sangre, EPS, régimen, antecedentes
- **Consultar**: Busque por número de documento
- **Listar**: Vea todos los pacientes en tabla con botón "Refrescar"
- **Actualizar**: Seleccione un paciente y actualice sus datos

### Gestion de Medicos
- **Especialidad**: Código, nombre, descripción
- **Médico**: 
  - Número de registro
  - Nombre del especialista
  - Especialidad (dropdown dinámico que se actualiza automáticamente)
  - Consultorio
  - Fecha y hora (dropdown de horas de 07:00 a 18:30)
- **Listar**: Vea todos los médicos con botón "Refrescar"

### Gestion de Citas
- **Programar**: 
  - Paciente (dropdown)
  - Médico (dropdown)
  - Fecha (selector de fecha)
  - Hora (dropdown de 07:00 a 18:30)
  - Motivo
- **Consultar/Cancelar**: 
  - Buscar cita por código
  - "Mostrar Todas" para listar todas las citas
  - Cancelar citas programadas

## Navegacion

- **Comportamiento SPA**: Solo un módulo visible a la vez
- **Botones de navegación**: Estado activo (verde = activo, gris = inactivo)
- Al hacer clic en un módulo, el contenido anterior se limpia automáticamente
- Al cargar la aplicación, muestra "Pacientes" por defecto

## Interfaz

- **Tema oscuro** profesional con colores médicos modernos
- Diseño limpio con gradientes y sombras sutiles
- Badges coloridos para estados de citas (PROGRAMADA, CANCELADA, COMPLETADA)
- Validación de campos obligatorios
- Mensajes de éxito y error claramente diferenciados
- Formularios reorganizados con diseño profesional
- Dropdowns modernos para especialidades y horas

## Datos

Los datos se almacenan en Google Drive en formato **CSV** (`/content/drive/MyDrive/SGH/datos/`):
- `pacientes.csv`
- `medicos.csv`
- `especialidades.csv`
- `citas.csv`
- `consultas.csv`
- `tratamientos.csv`
- `medicamentos.csv`

## Validaciones

- Número de documento: solo permite números
- Fecha: selector de calendario (DatePicker)
- Hora: selector desplegable con horas predefinidas (07:00 - 18:30)
- Listas desplegables: valores dinámicos y opción "Seleccionar..."
- Todos los campos obligatorios son validados antes de guardar
- Encabezados de tabla se ignoran automáticamente al cargar datos

## Tecnologias

- Python 3
- Google Colab
- ipywidgets (interfaz interactiva)
- Google Drive (persistencia en CSV)

## Arquitectura

```
SGH.ipynb
├── Modelos (Paciente, Medico, Especialidad, Cita, etc.)
├── Repositorios (manejo de archivos CSV)
├── Servicios (logica de negocio)
└── UI (ipywidgets - panels interactivos)
```

## Autor

Proyecto de Programación Orientada a Objetos - Ingeniería de Software