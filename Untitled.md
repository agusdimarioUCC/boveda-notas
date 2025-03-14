---
aliases:
  - Structured Query Language
  - SQL Joins
  - SQL Basics
tags:
  - Flashcards
  - Database
  - SQL
  - Programming

---

> [!wikipedia]+ [Wikipedia](<https://en.wikipedia.org/wiki/SQL>)
> <iframe width="100%" height="1000" frameBorder="0" src="https://en.m.wikipedia.org/wiki/SQL"></iframe>

> [!summary]+ Resumen  
> **SQL (Structured Query Language)** es un lenguaje de programación utilizado para gestionar bases de datos relacionales. Permite la manipulación y consulta de datos mediante sentencias como **SELECT, INSERT, UPDATE, DELETE** y la combinación de tablas con **JOINS**. Entre los tipos de **JOIN**, los más comunes son **INNER JOIN, LEFT JOIN, RIGHT JOIN** y **FULL OUTER JOIN**, cada uno con un propósito específico para unir datos de múltiples tablas.

> [!commands]+ Comandos básicos en SQL
> Aquí están los comandos esenciales en SQL:
> 
> - **`SELECT`** – Recupera datos de una tabla.  
> - **`INSERT INTO`** – Agrega registros a una tabla.  
> - **`UPDATE`** – Modifica datos existentes en una tabla.  
> - **`DELETE`** – Elimina registros de una tabla.  
> - **`CREATE TABLE`** – Crea una nueva tabla en la base de datos.  
> - **`DROP TABLE`** – Elimina una tabla y su contenido.  
> - **`ALTER TABLE`** – Modifica la estructura de una tabla.  
> - **`WHERE`** – Filtra resultados según una condición.  
> - **`GROUP BY`** – Agrupa filas que tienen valores comunes.  
> - **`ORDER BY`** – Ordena los resultados de una consulta.  

> [!joins]+ Tipos de JOINS en SQL
> Los **JOINS** permiten combinar filas de dos o más tablas en función de una columna común.
> 
> | Tipo de JOIN      | Descripción |
> |------------------|-------------|
> | **INNER JOIN**   | Devuelve solo las filas con coincidencias en ambas tablas. |
> | **LEFT JOIN**    | Devuelve todas las filas de la tabla izquierda y las coincidencias en la tabla derecha (las no coincidentes se rellenan con NULL). |
> | **RIGHT JOIN**   | Devuelve todas las filas de la tabla derecha y las coincidencias en la tabla izquierda (las no coincidentes se rellenan con NULL). |
> | **FULL OUTER JOIN** | Devuelve todas las filas cuando hay coincidencias en cualquiera de las tablas. |
> | **CROSS JOIN**   | Genera todas las combinaciones posibles entre las dos tablas. |

> **Ejemplo de cada tipo de JOIN**  
> 
> ```sql
```sql
 -- INNER JOIN
 SELECT empleados.nombre, departamentos.nombre
 FROM empleados
 INNER JOIN departamentos ON empleados.departamento_id = departamentos.id;
 ```
> 
```sql
> -- LEFT JOIN
> SELECT empleados.nombre, departamentos.nombre
> FROM empleados
> LEFT JOIN departamentos ON empleados.departamento_id = departamentos.id;
> ```
> 
```sql
> -- RIGHT JOIN
> SELECT empleados.nombre, departamentos.nombre
> FROM empleados
> RIGHT JOIN departamentos ON empleados.departamento_id = departamentos.id;
> ```
> 
```sql
> -- FULL OUTER JOIN
> SELECT empleados.nombre, departamentos.nombre
> FROM empleados
> FULL OUTER JOIN departamentos ON empleados.departamento_id = departamentos.id;
> ```

> [!trivia]+ Trivia
> **¿Sabías que...?**  
> SQL fue desarrollado en los años 70 en IBM como parte del proyecto *System R*, y su sintaxis está basada en el álgebra relacional.

> [!quote]+ Cita  
> "*El lenguaje de SQL es como el latín de las bases de datos: una vez que lo aprendes, puedes comunicarte con cualquier sistema de bases de datos relacional.*" – Autor desconocido.

> [!flashcard]- Comando SELECT
START
Obsidian - Question
Question: ¿Qué comando en SQL se usa para recuperar datos de una tabla?
Réponse: `SELECT`
END

> [!flashcard]- Uso de INNER JOIN
START
Obsidian - Question
Question: ¿Qué tipo de JOIN devuelve solo las filas que tienen coincidencias en ambas tablas?
Réponse: `INNER JOIN`
END

> [!flashcard]- LEFT JOIN
START
Obsidian - Question
Question: En un `LEFT JOIN`, ¿qué sucede con las filas de la tabla izquierda sin coincidencia en la tabla derecha?
Réponse: Se muestran con valores NULL en las columnas de la tabla derecha.
END

> [!flashcard]- Diferencia entre DELETE y DROP
START
Obsidian - Question
Question: ¿Cuál es la diferencia entre `DELETE` y `DROP TABLE` en SQL?
Réponse: `DELETE` elimina registros, mientras que `DROP TABLE` elimina toda la tabla.
END

> [!flashcard]- Agrupación de datos
START
Obsidian - Question
Question: ¿Qué comando en SQL se usa para agrupar filas con valores comunes?
Réponse: `GROUP BY`
END
