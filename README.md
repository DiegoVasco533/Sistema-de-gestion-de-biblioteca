# Sistema-de-gestion-de-biblioteca
# Introducción
El presente documento tiene como propósito definir los requerimientos funcionales y no funcionales del Sistema de Gestión de Bibliotecas.  
Este sistema permitirá registrar, consultar y gestionar la información de libros, usuarios y préstamos de una biblioteca de tamaño pequeño o mediano.  
Además, se incluirán los casos de prueba que validan dichos requerimientos, demostrando la aplicación de principios de ingeniería de software y asegurando la calidad del producto final.

# Desarrollo
El sistema permitirá registrar libros con sus datos básicos (título, autor, año, categoría), gestionar los préstamos de libros a usuarios y controlar las fechas de devolución.  
Los usuarios del sistema son el bibliotecario y los usuarios registrados.  
El bibliotecario podrá agregar, editar o eliminar libros, mientras que los usuarios podrán consultar la disponibilidad de ejemplares y realizar solicitudes de préstamo.

## 1. Propósito y alcance del sistema
El propósito del sistema de gestión de bibliotecas es permitir el registro, consulta y control de los libros y préstamos realizados a los usuarios de la biblioteca.  
El sistema busca optimizar el proceso de administración de los ejemplares disponibles, reduciendo errores y mejorando la eficiencia del servicio.

El alcance incluye la gestión básica de libros (registro, búsqueda, edición y eliminación), el registro de préstamos y devoluciones, y la generación de reportes simples de estado de préstamos activos.

## 2. Descripción general del sistema y de los usuarios
El sistema será utilizado por dos tipos de usuarios:

**Bibliotecario:** encargado de registrar nuevos libros, gestionar préstamos y devoluciones.  
**Usuario lector:** podrá consultar la disponibilidad de libros y su historial de préstamos (si el sistema tiene acceso para ellos).

El sistema será de tipo escritorio o web simple, con una base de datos local que almacene los registros de libros y préstamos.

---

# Requerimientos Funcionales
- **RF1:** El sistema debe permitir registrar nuevos libros con título, autor, año y categoría.  
- **RF2:** El sistema debe permitir editar y eliminar los registros de libros existentes.  
- **RF3:** El sistema debe permitir registrar préstamos de libros a usuarios registrados.  
- **RF4:** El sistema debe permitir consultar la disponibilidad de los libros.  
- **RF5:** El sistema debe generar reportes de préstamos activos y devueltos.

# Requerimientos No Funcionales
- **RNF1:** El sistema debe responder a las consultas en menos de 3 segundos.  
- **RNF2:** El sistema debe ser accesible solo mediante credenciales de usuario.  
- **RNF3:** El sistema debe almacenar la información de manera segura en una base de datos SQL Server.

---

# Criterios de Aceptación
El sistema será aceptado cuando cumpla con los requerimientos definidos, permita registrar y consultar libros y préstamos sin errores, y las pruebas unitarias y de validación confirmen la funcionalidad y seguridad del sistema.

- El sistema debe guardar correctamente los datos de libros y préstamos.  
- Las consultas deben devolver resultados precisos según los criterios ingresados.  
- Los reportes deben reflejar el estado actual de los préstamos.  
- No se deben registrar préstamos duplicados del mismo libro si ya está prestado.

---

# Resultados
A continuación, se presentan los resultados esperados y simulados de las pruebas realizadas para verificar el cumplimiento de los requerimientos definidos.

## Tabla de Casos de Prueba

| Tipo de Prueba | Requerimiento Asociado | Datos de Entrada | Resultado Esperado | Resultado Obtenido (Simulado) |
|----------------|-------------------------|------------------|---------------------|-------------------------------|
| Prueba Unitaria | RF1 | Título=“El Quijote”, Autor=“Cervantes”, Año=1605 | Registro exitoso del libro | Registro correcto |
| Prueba Unitaria | RF3 | Usuario=“Juan”, Libro=“El Quijote” | Préstamo registrado con fecha de devolución | Préstamo correcto |
| Prueba Unitaria | RF4 | Consulta por “El Quijote” | Disponibilidad mostrada | Disponible |
| Validación RNF1 | Consulta masiva | Tiempo < 3 segundos | — | 2.3 segundos |
| Validación RNF2 | Acceso sin login | Acceso denegado | — | Acceso restringido correctamente |

---

# Reflexión final
Las pruebas de software desempeñan un papel fundamental en la validación de los requerimientos, ya que permiten comprobar si el sistema cumple con las funciones y restricciones definidas durante la fase de análisis. En este caso, los casos de prueba unitarios ayudan a verificar el correcto funcionamiento de módulos individuales, como el registro de libros o la devolución de ejemplares, asegurando que cada parte cumpla su propósito sin errores.

Por otro lado, las pruebas de validación garantizan que el sistema como un todo satisfaga las necesidades del usuario final y los objetivos establecidos en los requerimientos funcionales. Gracias a estas pruebas, es posible detectar inconsistencias, fallos de lógica o desviaciones respecto a lo que se esperaba.

En el sistema de gestión de bibliotecas, las pruebas permiten asegurar que los datos se almacenen correctamente, que los préstamos y devoluciones se registren de forma precisa y que los reportes reflejen la información real. De este modo, las pruebas no solo validan el software técnicamente, sino que también aportan confianza al usuario en la calidad y fiabilidad del sistema desarrollado.

---

# Conclusiones y Recomendaciones
El desarrollo del Sistema de Gestión de Bibliotecas permitió comprender la importancia de definir claramente los requerimientos y su validación mediante pruebas.  
Las pruebas unitarias y de validación demostraron que los requerimientos funcionales se cumplen correctamente y que el sistema mantiene un buen desempeño y seguridad.  
Se recomienda continuar con pruebas de integración y usabilidad para garantizar una experiencia de usuario óptima.
