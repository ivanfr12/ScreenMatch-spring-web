![Programação-Java_ Persistencia de datos y consultas con Spring Data JPA](https://github.com/genesysR-dev/2066-java-persitencia-de-datos-y-consultas-con-Spring-JPA/assets/91544872/e0e3a9f8-afc7-4e7b-be83-469351ef2d70)

# ScreenMatch

Proyecto desarrollado durante el segundo curso de la formación Avanzando con Java de Alura

## 🔨 Objetivos del proyecto

* Avanzar en el proyecto Screenmatch, iniciado en el primer curso de la formación, creando un menú con varias opciones;
* Modelar las abstracciones de la aplicación a través de clases, enums, atributos y métodos;
* Consumir la API del ChatGPT(Opcional;
* Utilizar Spring Data JPA para persistir datos en la base de datos;
* Conocer varios tipos de bases de datos y utilizar PostgreSQL;
* Trabajar con varios tipos de consultas a la base de datos;
* Profundizar en la interfaz JPA Repository.

* 📦 Estructura del Proyecto
🔙 Backend (Java + Spring Boot)
El backend está organizado en paquetes siguiendo buenas prácticas de arquitectura:

model: contiene la clase principal que representa una serie.

repository: interfaz que extiende JpaRepository para acceder a los datos.

service: lógica de negocio, como la consulta y conversión de datos (SerieService, ConvierteDatos, etc.).

dto: clases para la transferencia de datos desde y hacia la API externa.

controller: capa de exposición de endpoints REST.

config: configuraciones generales del proyecto.

Interfaces adicionales como IConvierteDatos para la conversión de JSON a objetos Java.
🔗 Endpoints típicos:
GET /series
GET /series/top
GET /series/{id}

🖥 Frontend (HTML + CSS + JavaScript)
La interfaz de usuario está compuesta por archivos:

index.html: estructura base de la página web.

style.css: estilos visuales.

Archivos .js: lógica para cargar datos dinámicamente desde el backend y mostrarlos en pantalla.

Este frontend permite consultar y visualizar información de las series almacenadas en la base de datos.

🛢 Base de datos
La aplicación utiliza PostgreSQL para persistencia de datos.

Ejemplo de configuración en application.properties:
spring.datasource.url=jdbc:postgresql://localhost:5432/screenmatch
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

🚀 Cómo ejecutar el proyecto
Prerrequisitos:
Java 17 o superior

PostgreSQL

Maven

Pasos:
Clona el repositorio:
git clone https://github.com/ivanfr12/ScreenMatch-spring-web
cd screenmatch-series

Crea la base de datos en PostgreSQL:
CREATE DATABASE screenmatch;

Configura el archivo application.properties con tus credenciales.

Ejecuta el proyecto:
./mvnw spring-boot:run
Abre el archivo index.html en tu navegador: el frontend se conecta al backend a través de JavaScript y muestra las series.

⚙️ Tecnologías utilizadas
Java 17

Spring Boot

Spring Data JPA

PostgreSQL

HTML5 + CSS + JavaScript

Fetch API para consumir el backend

💡 Funcionalidades
Consulta de series almacenadas.

Almacenamiento persistente en base de datos PostgreSQL.

Consumo de API externa y conversión automática de datos.

Interfaz amigable para el usuario.

Código modular, organizado y mantenible.

📸 Vista previa
![image](https://github.com/user-attachments/assets/5a460ac4-073c-4baf-9ba4-a09e86fbe71a)





