# Cafetapp

Aplicación web para la gestión de compras y ventas en cafeterías escolares.

Cafetapp nació como un proyecto académico con la idea de facilitar las compras dentro de las cafeterías escolares, reducir el uso de dinero en efectivo y llevar un mayor control sobre el consumo de los estudiantes.

El proyecto fue desarrollado utilizando **Java, Spring Boot y MySQL**, junto con tecnologías frontend como **HTML, CSS, Bootstrap y Thymeleaf**.

## ¿Qué permite hacer?

La aplicación cuenta con diferentes funcionalidades para la gestión de la cafetería y sus usuarios:

* Gestión de colegios.
* Gestión de estudiantes.
* Gestión de acudientes.
* Gestión de administradores.
* Gestión de cafeterías.
* Registro de compras.
* Consulta del historial de compras.
* Gestión del saldo de los estudiantes.
* Configuración del tope diario de consumo.
* Gestión de restricciones de consumo.
* Manejo de diferentes tipos de usuario.

El sistema contempla los siguientes roles:

* **SuperAdministrador**
* **Administrador de Colegio**
* **Administrador de Cafetería**
* **Acudiente**
* **Estudiante**

## Funcionalidades principales

Una de las partes centrales de Cafetapp es el proceso de compra de un estudiante.

Antes de registrar una compra, el sistema verifica la información del estudiante y las condiciones necesarias para realizar la operación, incluyendo su saldo disponible y el consumo realizado durante el día.

Cuando la compra es válida, se actualiza el saldo del estudiante y se registra la operación para poder consultarla posteriormente en el historial de compras.

La idea es que el estudiante pueda realizar sus compras sin depender directamente del manejo de dinero en efectivo.

## Tecnologías

**Backend**

* Java 17
* Spring Boot
* Spring Data JPA
* Hibernate
* Maven

**Frontend**

* HTML
* CSS
* Bootstrap
* Thymeleaf

**Base de datos**

* MySQL

**Pruebas**

* JUnit
* Spring Boot Test

## Estructura del proyecto

La lógica principal de la aplicación se encuentra organizada de la siguiente manera:

```text
src/main/java/com/cafetapp/app
│
├── controller
├── entity
├── exception
└── repository
```

* `controller`: controla las solicitudes y el flujo de las diferentes funcionalidades.
* `entity`: contiene las entidades que representan la información manejada por el sistema.
* `repository`: contiene los repositorios utilizados para trabajar con la base de datos mediante Spring Data JPA.
* `exception`: contiene el manejo de excepciones de la aplicación.

Las interfaces de la aplicación se encuentran en:

```text
src/main/resources/templates
```

y los recursos estáticos, como hojas de estilos e imágenes, en:

```text
src/main/resources/static
```

## Base de datos

Cafetapp utiliza **MySQL** para almacenar la información del sistema.

La comunicación entre la aplicación y la base de datos se realiza mediante **Spring Data JPA e Hibernate**.

Para ejecutar el proyecto localmente es necesario crear una base de datos llamada `cafetapp` y configurar los datos de conexión en:

```text
src/main/resources/application.properties
```

Por ejemplo:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/cafetapp
spring.datasource.username=TU_USUARIO
spring.datasource.password=TU_CONTRASEÑA
```

## Requisitos

Para ejecutar el proyecto necesitas:

* Java 17
* MySQL
* Maven (el proyecto incluye Maven Wrapper)
* Un IDE para Java

## Ejecutar el proyecto

Clona el repositorio:

```bash
git clone https://github.com/JhondiLopez/Cafetapp.git
```

Entra en la carpeta:

```bash
cd Cafetapp
```

En Windows puedes ejecutar:

```bash
mvnw.cmd spring-boot:run
```

En Linux o macOS:

```bash
./mvnw spring-boot:run
```

## Contexto del proyecto

Cafetapp fue desarrollado como proyecto académico para aplicar conocimientos de desarrollo de software en una situación cercana a un contexto real.

Durante su desarrollo se trabajó en el levantamiento de requerimientos, diseño de la solución, desarrollo de la aplicación, integración con MySQL y pruebas de funcionamiento.

El proyecto se enfocó particularmente en la gestión de compras, ventas y consumo de los estudiantes en cafeterías escolares de la Calle de los Estudiantes de Bucaramanga.

## Estado actual

El proyecto funciona como una aplicación académica y continúa siendo una base para seguir mejorando aspectos como:

* Separación de responsabilidades.
* Organización de la lógica de negocio.
* Seguridad y autenticación.
* Pruebas automatizadas.
* Optimización de consultas.
* Mantenibilidad del código.

Interesado en desarrollo de software, especialmente en **Java y desarrollo backend**.

[GitHub](https://github.com/JhondiLopez)
