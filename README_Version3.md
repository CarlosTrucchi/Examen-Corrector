# Corrector de Examen - Matemática II

Este proyecto es una aplicación web para la corrección automática de exámenes de opción múltiple en la asignatura Matemática II. Permite configurar una clave de respuestas, cargar datos de alumnos desde un archivo Excel, registrar respuestas y obtener la nota final y calificación. Además, puedes exportar los resultados a un archivo CSV.

## Características

- **Configuración de clave de respuestas:** Selecciona las respuestas correctas para cada pregunta.
- **Carga de datos de alumnos:** Importa una lista de alumnos desde un archivo Excel (.xls o .xlsx) para autocompletar la información.
- **Ingreso y corrección de respuestas:** Registra las respuestas del alumno y calcula la nota y calificación automáticamente.
- **Exportación de resultados:** Descarga el listado completo con notas en formato CSV compatible con Excel.
- **Edición fácil del tema del parcial:** Haz clic en el título para cambiar el tema del examen.

## Estructura del archivo Excel esperado

El sistema espera un archivo con las siguientes columnas y orden:

1. DNI
2. Comisión
3. Número de Alumno
4. Apellido y Nombre
5. Aula

## Modo de uso

1. Configura la clave de respuestas en la sección 1.
2. Carga el archivo Excel con la lista de alumnos.
3. Ingresa el DNI del alumno y presiona "Confirmar" para autocompletar los datos.
4. Marca las respuestas del alumno y completa los datos del profesor.
5. Presiona "Corregir y Cargar" para registrar el resultado.
6. Exporta los resultados usando el botón "Exportar a Excel (CSV)".

## Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript
- [read-excel-file](https://github.com/ramonak/read-excel-file) para la lectura de archivos Excel en el navegador

## Autor

Carlos Trucchi

## Licencia

Este proyecto está bajo la licencia MIT. Siéntete libre de modificar y adaptar para tus necesidades.