# Sistema de Gestión Académica - Unit Tests

## Descripción General

Este proyecto contiene la implementación de un **Sistema de Gestión Académica** con pruebas unitarias comprensivas para validar la funcionalidad del sistema.

## Estructura del Proyecto

```
UnibeNicolle/
├── Student.java                 # Modelo de datos para Estudiantes
├── StudentManager.java          # Gestor de estudiantes
├── Course.java                  # Modelo de datos para Cursos
├── CourseManager.java           # Gestor de cursos
├── StudentManagerTest.java      # Pruebas del gestor de estudiantes
├── CourseManagerTest.java       # Pruebas del gestor de cursos
├── TEST_DOCUMENTATION.md        # Documentación de pruebas
└── README.md                    # Este archivo
```

## Casos de Uso Cubiertos

### Caso de Uso 1: Gestión de Estudiantes
- ✅ Registrar nuevo estudiante
- ✅ Validar datos únicos (matrícula no duplicada)
- ✅ Consultar información de estudiante
- ✅ Dar de baja estudiante
- ✅ Actualizar promedio académico
- ✅ Validación de rangos de promedio (0.0 - 4.0)

### Caso de Uso 2: Gestión de Cursos
- ✅ Crear nuevos cursos académicos
- ✅ Inscribir estudiantes en cursos
- ✅ Prevenir inscripciones duplicadas
- ✅ Consultar estudiantes de un curso
- ✅ Remover estudiantes de cursos
- ✅ Manejo de cursos inexistentes
- ✅ Escalabilidad con múltiples cursos y estudiantes

## Pruebas Unitarias Implementadas

### StudentManagerTest (7 pruebas)

1. **testAgregarEstudianteExitoso**
   - Propósito: Validar registro exitoso de estudiante
   - Relacionado con: Registrar nuevo estudiante

2. **testAgregarEstudianteMatriculaDuplicada**
   - Propósito: Prevenir matrículas duplicadas
   - Relacionado con: Validar datos únicos

3. **testObtenerEstudiante**
   - Propósito: Consultar información de estudiante
   - Relacionado con: Consultar información

4. **testDarBajaEstudiante**
   - Propósito: Remover estudiante del sistema
   - Relacionado con: Dar de baja

5. **testEstudianteNoEncontrado**
   - Propósito: Manejo de errores
   - Relacionado con: Validación de inexistencia

6. **testActualizarPromedioValido**
   - Propósito: Actualizar promedio dentro de rango válido
   - Relacionado con: Actualizar información

7. **testActualizarPromedioInvalido**
   - Propósito: Rechazar promedios fuera de rango
   - Relacionado con: Validación de datos

### CourseManagerTest (9 pruebas)

1. **testCrearCursoExitoso**
   - Propósito: Crear nuevo curso
   - Relacionado con: Crear cursos académicos

2. **testCrearCursoDuplicado**
   - Propósito: Prevenir códigos duplicados
   - Relacionado con: Validar unicidad

3. **testInscribirEstudianteEnCursoExitoso**
   - Propósito: Inscribir estudiante en curso
   - Relacionado con: Inscribir estudiantes

4. **testInscripcionDuplicada**
   - Propósito: Prevenir inscripciones duplicadas
   - Relacionado con: Validación de duplicados

5. **testObtenerEstudiantesDeCurso**
   - Propósito: Recuperar lista de inscritos
   - Relacionado con: Consultar estudiantes

6. **testEliminarEstudianteDelCurso**
   - Propósito: Remover estudiante del curso
   - Relacionado con: Remover estudiantes

7. **testInscribirEnCursoInexistente**
   - Propósito: Manejo de errores
   - Relacionado con: Validación de inexistencia

8. **testObtenerCursoInexistente**
   - Propósito: Manejo de errores
   - Relacionado con: Validación de inexistencia

9. **testMultiplesCursosYEstudiantes**
   - Propósito: Validar escalabilidad
   - Relacionado con: Escalabilidad del sistema

## Compilación y Ejecución

### Requisitos
- Java JDK 8 o superior
- JUnit 4.13.2 o superior
- Hamcrest 1.3 o superior

### Pasos para compilar

```bash
# Descargar JUnit y Hamcrest (si no están disponibles)
# Compilar todos los archivos Java
javac *.java

# O compilar con JUnit
javac -cp .:junit-4.13.2.jar:hamcrest-core-1.3.jar *.java
```

### Pasos para ejecutar las pruebas

```bash
# Ejecutar todas las pruebas
java -cp .:junit-4.13.2.jar:hamcrest-core-1.3.jar org.junit.runner.JUnitCore StudentManagerTest CourseManagerTest

# O ejecutar pruebas individuales
java -cp .:junit-4.13.2.jar:hamcrest-core-1.3.jar org.junit.runner.JUnitCore StudentManagerTest
java -cp .:junit-4.13.2.jar:hamcrest-core-1.3.jar org.junit.runner.JUnitCore CourseManagerTest
```

## Cobertura de Pruebas

- **Total de Pruebas**: 16 pruebas unitarias
- **Casos de Uso Cubiertos**: 2
- **Funcionalidades Validadas**: 
  - Operaciones CRUD (Create, Read, Update, Delete)
  - Validación de datos
  - Manejo de errores
  - Escalabilidad del sistema

## Documentación Adicional

Para más detalles sobre cada prueba, consulte el archivo `TEST_DOCUMENTATION.md`

---

**Clase**: TI3312-02-2026-2-ASEGURAMIENTO DE LA CALIDAD DEL SOFTWARE  
**Actividad**: Actividad -6: Diseño e Implementación de Pruebas Unitarias  
**Fecha de Entrega**: 14 de febrero de 2026