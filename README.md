# 🐾 API Test Automation - PetStore (Karate DSL)

Este proyecto automatiza pruebas de API REST para el recurso [`/pet`](https://petstore3.swagger.io/) de [Swagger Petstore](https://petstore3.swagger.io/) utilizando [Karate DSL](https://github.com/karatelabs/karate), una poderosa herramienta para automatización de pruebas API en Java.

## 🚀 Tecnologías Utilizadas

| Tecnología      | Descripción                                  | Enlace oficial                                      |
|----------------|----------------------------------------------|----------------------------------------------------|
| 🐉 Karate DSL   | Framework de automatización para API testing | [karatelabs/karate](https://github.com/karatelabs/karate) |
| ☕ Java         | Lenguaje base del proyecto                   | [java.com](https://www.java.com/)                 |
| 🧪 JUnit 5      | Motor de ejecución para tests                | [junit.org](https://junit.org/junit5/)            |
| 📦 Maven        | Gestor de dependencias y build               | [maven.apache.org](https://maven.apache.org/)      |

---

## 📋 Endpoints Automatizados

Se han automatizado pruebas para los siguientes métodos del recurso `/pet` según el contrato público de Swagger Petstore:

🔗 [https://petstore3.swagger.io/](https://petstore3.swagger.io/)

- ✅ `POST /pet` → Crear una mascota
- ✅ `GET /pet/{petId}` → Obtener mascota por ID (incluye casos negativos)
- ✅ `PUT /pet` → Actualizar una mascota existente
- ✅ `DELETE /pet/{petId}` → Eliminar una mascota

---

## ⚙️ Instalación

1. **Clona el repositorio:**

```bash
git clone https://github.com/TribuQA/auto-api-karate-dsl.git
cd auto-api-karate-dsl.git
```

2. **Verifica que tienes instalado:**

- Java 8 o superior
- Maven 3.x
- Un IDE como IntelliJ o Eclipse (opcional)

---

## ▶️ Ejecución de Pruebas

### 🖥️ Desde el IDE (IntelliJ)

- Abre el proyecto
- Ejecuta cualquier clase runner como `PetRunner.java` o `GetPetRunner.java`
- Asegúrate de tener los `feature` y los `request-body.json` correctamente ubicados

### 💻 Desde terminal (Maven)

#### ✅ Ejecutar todos los tests:

```bash
mvn clean test
```

#### 🏷 Ejecutar por tags (uno o más):

```bash
# Ejecutar un solo escenario por tag
mvn test -Dkarate.options="--tags @escenario-id"

# Ejecutar múltiples escenarios (OR lógico)
mvn test -Dkarate.options="--tags @escenario-id,@escenario-body"

# Ejecutar un escenario e ignorar otro
mvn test -Dkarate.options="--tags @escenario-id,~@escenario-body"
```

---

## 🤖 Asistencia con ChatGPT

Parte de este proyecto fue construido con el apoyo de [ChatGPT](https://chat.openai.com/) para acelerar la generación de código y documentación técnica.

### 🧠 Ejemplo de prompt utilizado:

> _"Actúa como un experto en automatización de pruebas con Karate DSL y Java. Tengo un endpoint GET /pet/{petId} del contrato https://petstore3.swagger.io/ y necesito una feature que valide el status 200 y el tipo de datos de la respuesta usando expresiones embebidas."_

---

## 👤 Autor

- **Nombre:** Dídier Ramírez
- **Correo:** didierjavierr@gmail.com

---

## 📌 Buenas Prácticas Aplicadas

- ✅ Reutilización de código mediante `Background`
- ✅ Separación de datos (`request-body.json`) desde archivos externos
- ✅ Uso de ID dinámicos en escenarios POST
- ✅ Estructura modular por endpoint (GET, POST, PUT, DELETE)
- ✅ Manejo de pruebas negativas (`400`, `404`)
- ✅ Uso de tags para ejecución flexible
- ✅ Documentación legible y reproducible

---

¡Automatiza con confianza! 🧪💥
