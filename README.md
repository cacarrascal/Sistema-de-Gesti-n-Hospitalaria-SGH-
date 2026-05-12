# Sistema de Gestión Hospitalaria (SGH)

Sistema de gestión hospitalaria desarrollado en Python con Programación Orientada a Objetos para Google Colab. Interfaz con tema oscuro.

## Características

- **Gestión de Pacientes**: Registrar, consultar, listar y actualizar datos de pacientes
- **Gestión de Médicos**: Administrar especialidades y médicos
- **Gestión de Citas**: Programar, consultar, cancelar citas médicas
- **Registro Clínico**: Registrar consultas médicas y ver historial de pacientes
- **Análisis de Datos**: Estadísticas hospitalarias

## Estructura del Notebook

El archivo `SGH_completo.ipynb` contiene todo el código en un solo libro:

1. **Montar Google Drive** - Conexión y configuración de rutas
2. **Instalar Dependencias** - Librería ipywidgets para interfaz interactiva
3. **Modelos de Datos** - Clases: Paciente, Medico, Cita, Consulta, etc.
4. **Repositorios** - Capa de persistencia en archivos CSV
5. **Servicios** - Lógica de negocio
6. **Interfaz de Usuario** - Componentes visuales con ipywidgets (tema oscuro)
7. **Ejecutar Aplicación** - Menu principal

## Requisitos

- Cuenta de Google Drive
- Acceso a Google Colab
- Carpeta `SGH/datos/` en Google Drive (se crea automáticamente)

## Instalación

1. Descarga el archivo `SGH_completo.ipynb`
2. Abre el archivo en Google Colab
3. Ejecuta todas las celdas (Ctrl+F9 o Runtime > Run All)
4. La aplicación se mostrará automáticamente

## Uso

### Gestión de Pacientes
- **Registrar**: Número de documento (campo numérico), nombre, fecha de nacimiento (selector de fecha), tipo de sangre, EPS, régimen, antecedentes. Formulario se reinicia automáticamente después de registrar.
- **Consultar**: Busque por número de documento. Botón "Limpiar" para buscar otro paciente.
- **Listar**: Vea todos los pacientes registrados en tabla
- **Actualizar**: Seleccione un paciente de la lista desplegable y actualice sus datos

### Gestión de Médicos
- **Especialidad**: Agregue nuevas especialidades médicas
- **Médico**: Registre médicos con su especialidad, consultorio y horario
- **Listar**: Vea todos los médicos o filtre por especialidad

### Gestión de Citas
- **Programar**: Asigne cita a un paciente con un médico específico
- **Consultar/Cancelar**: Busque una cita por código y cancele si es necesario
- **Por paciente**: Vea todas las citas de un paciente
- **Por médico**: Vea todas las citas de un médico

### Registro Clínico
- **Registrar consulta**: Registre síntomas, signos vitales, diagnóstico CIE-10 y medicamentos
- **Historial clínico**: Vea el historial completo de un paciente

### Análisis de Datos
- **Consultas por médico**: Promedio de consultas en un periodo
- **Diagnósticos frecuentes**: Top N diagnósticos CIE-10 más comunes
- **Ocupación por especialidad**: Tasa de atención por especialidad
- **Distribución EPS/Régimen**: Porcentaje de pacientes por EPS y régimen
- **Medicamentos más recetados**: Top N medicamentos más formulados

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

## Interfaz

- **Tema oscuro** con colores vibrantes
- Diseño moderno con gradientes y sombras
- Iconos y badges para estados de citas
- Validación de campos obligatorios
- Mensajes de éxito y error claramente diferenciados

## Tecnologías

- Python 3
- Google Colab
- ipywidgets (interfaz interactiva)
- Google Drive (persistencia en CSV)

## Autor

Proyecto de Programación Orientada a Objetos - Ingeniería de Software