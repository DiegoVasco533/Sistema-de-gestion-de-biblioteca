<!-- UNEMI -->
![](https://web-api.textin.com/ocr_image/external/8966bd92ae07954c.jpg)

# Informe Técnico - Sistema de Gestión de Biblioteca

**Universidad Estatal de Milagro (UNEMI)**  
Facultad de Ciencias e Ingeniería  
Carrera de Ingeniería de Software  

**Autores:**  
- Andino Anhyé  
- Barahona Edwadr  
- Coronel Karla  
- García Gilmar  
- Morán Maykel  
- Vasco Diego  

**Asignatura:** Introducción a la Ingeniería de Software  
**Docente:** Ing. Jorge Dumar Guevara Serrano  
**Fecha de entrega:** 05/10  
**Periodo:** Abril 2024 a Agosto 2025  

---

## Introducción

Este informe técnico documenta el análisis y aplicación del mantenimiento de software en un sistema de gestión bibliotecaria. A partir de problemas reales detectados en el funcionamiento del sistema, se identificaron los tipos de mantenimiento necesarios (correctivo, adaptativo, perfectivo y preventivo) y se justificó su implementación con base en autores como Sommerville y Pressman. El trabajo incluye requerimientos, pruebas técnicas, propuestas de mejora funcional y evidencia de validación, demostrando cómo el mantenimiento bien planificado garantiza la calidad, seguridad y evolución del sistema.

---

## Descripción del Sistema

El sistema de gestión bibliotecaria es una aplicación web diseñada para facilitar el registro, préstamo y devolución de libros en una biblioteca pequeña o mediana. Su propósito principal es optimizar el control del inventario bibliográfico, mejorar la experiencia del usuario y reducir errores en los procesos administrativos.

**Funciones principales:**
- Registrar libros con metadatos como título, autor, año y código único.
- Registrar usuarios y asociarlos a préstamos activos.
- Controlar el estado de los libros (disponible, prestado, devuelto).
- Consultar el historial de préstamos por usuario.
- Seguridad mediante autenticación y respaldo automático.

**Perfiles de usuario:**
- **Bibliotecario:** acceso completo.
- **Usuario lector:** consulta de disponibilidad e historial.

---

## Análisis de Problemas Técnicos

### 1. Préstamos duplicados

El sistema permite registrar préstamos de libros ya prestados, generando duplicaciones y errores en el inventario.

**Ejemplo:** El libro B001 ya está prestado, pero el sistema permite otro préstamo sin advertencia.

### 2. Fallos en devoluciones

El estado del libro no se actualiza correctamente tras la devolución, impidiendo nuevos préstamos legítimos.

---

## Áreas de Mejora Justificadas

- Validaciones estrictas al registrar préstamos.
- Actualización automática del estado del libro tras devolución.
- Casos de prueba para escenarios límite.
- Alertas en tiempo real para bibliotecarios.

---

## Tipos de Mantenimiento Aplicado

| Tipo         | Aplicación en el sistema | Justificación técnica |
|--------------|--------------------------|------------------------|
| Correctivo   | Corrección de errores como préstamos duplicados. | Mejora la lógica y experiencia del usuario. |
| Adaptativo   | Compatibilidad con navegadores y dispositivos. | Mantiene funcionalidad ante cambios tecnológicos. |
| Perfectivo   | Mejora de interfaz y tiempos de respuesta. | Incrementa eficiencia sin alterar funciones. |
| Preventivo   | Refactorización y copias de seguridad. | Reduce fallos futuros con acciones proactivas. |

---

## Concepto y Tipos de Mantenimiento

**Correctivo:** Corrige errores detectados.  
**Adaptativo:** Ajusta el sistema a nuevos entornos.  
**Perfectivo:** Optimiza rendimiento y funcionalidad.  
**Preventivo:** Previene futuros errores.

**Etapas según Sommerville y Pressman:**
- Análisis del problema
- Modificación del software
- Validación
- Entrega y documentación

---

## Costos Asociados

El mantenimiento representa entre el 60% y 80% del costo total del ciclo de vida del software. Factores como calidad del código, frecuencia de cambios y disponibilidad de personal influyen directamente.

---

## Propuesta de Cambio Funcional

**Autenticación en dos pasos:**
- Se añade un campo en la tabla `usuarios`.
- Se crea tabla temporal `codigos_verificacion`.
- Flujo: ingreso → verificación por código → acceso.

**Impacto:**

| Aspecto              | Impacto del cambio |
|----------------------|--------------------|
| Calidad del software | Mejora seguridad y confiabilidad. |
| Mantenibilidad       | Módulo independiente y escalable. |
| UX                   | Mayor protección con proceso guiado. |

---

## Simulación Técnica

**Configuración:**
- Lenguaje: PHP / Java / Python
- Base de datos: MySQL
- Entorno: XAMPP / VS Code
- Fecha de prueba: 04/11/2025

**Escenario:**  
El administrador programa mantenimiento preventivo para el 06/11/2025.  
Resultado esperado: Registro en historial y correo enviado exitosamente.

---

## Conclusión

Este informe técnico demuestra cómo el mantenimiento bien documentado mejora la calidad, seguridad y funcionalidad del sistema bibliotecario. La propuesta de doble verificación refuerza la evolución del sistema y responde a nuevas necesidades de los usuarios. El mantenimiento es un proceso continuo que garantiza sostenibilidad y confiabilidad.

---
