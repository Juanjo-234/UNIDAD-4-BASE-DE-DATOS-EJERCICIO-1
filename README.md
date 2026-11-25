# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-1
1. Configuración Inicial y Base de Datos
Se establece la codificación a UTF8 y se configura el esquema público por defecto.

Se define la creación de la base de datos principal llamada gestiobibliotecauniversitaria utilizando la configuración regional de España (Spanish_Spain.1252).

2. Estructura de las Tablas y sus Campos
El script define la creación de 7 tablas relacionales principales:

autor: Almacena la información básica de los creadores de las obras.

id_autor: Identificador único del autor.

nombre: Nombre completo del autor.

libro: Contiene los datos generales de los títulos bibliográficos.

isbn: Código internacional normalizado del libro (clave primaria).

titulo: Título de la obra.

edicion: Edición del libro.

editorial: Editorial que publica la obra.

libro_autor: Tabla intermedia que gestiona la relación de muchos a muchos entre libros y autores.

isbn e id_autor: Claves foráneas compuestas.

orden_auditoria: Orden de autoría del libro.

ejemplar: Representa las copias o ejemplares físicos disponibles de cada libro.

codigo_inventario: Código único del ejemplar físico.

isbn: Referencia al libro correspondiente.

estado: Condición actual del ejemplar (ej. disponible, prestado, dañado).

usuario: Registra a las personas que utilizan los servicios de la biblioteca.

id_usuario: Identificador único del usuario.

nombre y apellido: Datos personales.

telefono y correo: Canales de contacto.

tipo_usuario: Categoría o rol del usuario (ej. estudiante, docente).

prestamo: Registra los encabezados de los préstamos realizados.

id_prestamo: Identificador único del préstamo.

id_usuario: Usuario que realiza el préstamo.

fecha_prestamo: Fecha en la que se efectúa.

detalle_prestamo: Especifica los ejemplares concretos asociados a cada préstamo y sus plazos.

id_prestamo y codigo_inventario: Claves foráneas compuestas.

fecha_devolucion: Fecha límite estipulada para devolver el ejemplar.

fecha_real_devolucion: Fecha en la que efectivamente se devuelve.

num_legajo: Número de legajo del operador o administrativo a cargo.

3. Restricciones y Claves
Claves Primarias (PRIMARY KEY): Se configuran para garantizar la unicidad de los registros en cada una de las tablas (ej. autor_pkey, libro_pkey, usuario_pkey, etc.).


Claves Foráneas (FOREIGN KEY): Se establecen las restricciones de integridad referencial para conectar lógicamente las tablas entre sí (por ejemplo, vinculando los ejemplares con sus respectivos libros, los préstamos con sus usuarios, y los detalles de préstamo con los préstamos y ejemplares correspondientes).

IMAGEN DE EJEMPLO DE UNA CONSULTA:
<img width="1145" height="363" alt="Captura de pantalla 2026-11-25 104124" src="https://github.com/user-attachments/assets/1894cf71-2a80-4551-bb85-86a7f2ff9125" />
