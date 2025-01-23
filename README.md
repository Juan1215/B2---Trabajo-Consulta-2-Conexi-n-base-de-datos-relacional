# B2 - Trabajo-Consulta2 - Conexion base de datos relacional

## ¿Qué es JDBC y cuáles son sus componentes?
---

Java Database Connectivity (JDBC) es una especificación de interfaz de programación de aplicaciones (API) estándar de JavaSoft que permite a los programas Java acceder a sistemas de gestión de bases de datos. La API JDBC consta de un conjunto de interfaces y clases escritas en el lenguaje de programación Java. 

Utilizando estas interfaces y clases estándar, los programadores pueden escribir aplicaciones que se conecten a bases de datos, envíen consultas escritas en lenguaje de consulta estructurado (SQL) y procesen los resultados.

* Componentes principales de JDBC:

1. Controladores JDBC: estos controladores actúan como intermediarios entre las aplicaciones Java y las bases de datos. Cada sistema de gestión de bases de datos tiene su propio controlador JDBC, que es esencial para establecer una comunicación adecuada.

2.  URL de conexión: es una cadena que identifica la base de datos a la que se accederá desde la aplicación Java. Contiene el tipo de base de datos, la dirección del servidor y la información del puerto necesaria para la conexión.

3. Conexión: Indica una conexión activa a la base de datos. Se utiliza para enviar comandos SQL y gestionar transacciones.

4. Declaración: Le permite ejecutar consultas SQL. Hay diferentes tipos:
   
    * Declaración: Para consultas SQL simples sin parámetros. 
    * PreparedStatement: permite construir consultas SQL con parámetros variables, proporcionando mayor seguridad y eficiencia. 
    * CallableStatement: se utiliza para ejecutar procedimientos almacenados en una base de datos.

5. ResultSet: contiene los datos devueltos por una consulta SQL y permite iterarlos para recuperar la información requerida.

--- 

## Librerías de Scala que permiten conectarse a una base de datos relacional

Scala tiene varias bibliotecas que facilitan la conexión y el trabajo con bases de datos relacionales. Los más famosos de ellos son: Slick y Doobie. Ambos ofrecen diferentes formas de interactuar con el repositorio para adaptarse a las necesidades y preferencias de diferentes desarrolladores.

Slick: Slick es una biblioteca que proporciona asignaciones relacionales funcionales para que puedas escribir consultas SQL en código Scala de manera tipada y segura. Facilita las conexiones a bases de datos relacionales y proporciona soporte para diversas operaciones como seleccionar, insertar, actualizar y eliminar datos.

Doobie: Es una biblioteca Scala pura para trabajar con JDBC. Se centra en proporcionar una capa de abstracción mínima sobre JDBC, lo que permite a los desarrolladores escribir consultas SQL directamente y manejar interacciones de bases de datos de forma segura y eficiente.

* Tabla de diferencias.

| Característica             | **Slick**                                                                                             | **Doobie**                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| **Paradigma**              | Mapeo relacional funcional, permitiendo escribir consultas de manera tipada y segura.                | Enfoque minimalista, permite escribir consultas SQL directamente, proporcionando una capa ligera sobre JDBC. |
| **Curva de aprendizaje**   | Moderada, requiere familiarizarse con su DSL y conceptos de mapeo relacional funcional.              | Baja, se basa en conceptos de JDBC y SQL estándar, facilitando su adopción para quienes ya conocen estas tecnologías. |
| **Flexibilidad en consultas** | Alta, permite componer consultas de manera funcional y tipada, facilitando la reutilización y composición de consultas complejas. | Alta, al permitir escribir consultas SQL directamente, ofrece total flexibilidad en la construcción de las mismas. |
| **Integración con otras libs** | Buena, cuenta con soporte y extensiones para integrarse con otras bibliotecas del ecosistema Scala. | Excelente, su diseño minimalista facilita la integración con otras bibliotecas y frameworks en el ecosistema Scala. |
| **Manejo de errores**      | Proporciona mecanismos integrados para el manejo de errores en operaciones con la base de datos.     | Ofrece un control explícito sobre el manejo de errores, permitiendo a los desarrolladores gestionar excepciones según sus necesidades. |

---

Cómo establecer una conexión a una base de datos relacional (mysql). Siga los siguientes pasos:

* Genere una base de datos en mysql
* Genere una tabla con datos de prueba
* Desde Scala establezca la conexión a la base datos

--- 

## Citas Bibliograficas

  * IBM. (n.d.). *What is JDBC?* IBM Documentation. [https://www.ibm.com/docs/es/informix-servers/12.10?topic=started-what-is-jdbc](https://www.ibm.com/docs/es/informix-servers/12.10?topic=started-what-is-jdbc)
  * Tokio School. (n.d.). *¿Qué es JDBC?*. [https://www.tokioschool.com/noticias/jdbc/](https://www.tokioschool.com/noticias/jdbc/)
  * Delft Stack. (n.d.). *SQL Query in Scala.* [https://www.delftstack.com/es/howto/scala/sql-query-in-scala/](https://www.delftstack.com/es/howto/scala/sql-query-in-scala/)
