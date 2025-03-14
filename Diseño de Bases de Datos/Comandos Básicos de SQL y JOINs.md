## Comandos Básicos de SQL

### 1. Seleccionar datos

```sql
SELECT columna1, columna2 FROM tabla;
```

- Obtiene datos de una tabla.
- Usa `SELECT * FROM tabla;` para seleccionar todas las columnas.

### 2. Filtrar datos

```sql
SELECT * FROM tabla WHERE condicion;
```

Ejemplo:

```sql
SELECT * FROM empleados WHERE edad > 30;
```

### 3. Ordenar resultados

```sql
SELECT * FROM tabla ORDER BY columna ASC|DESC;
```

Ejemplo:

```sql
SELECT * FROM empleados ORDER BY salario DESC;
```

### 4. Insertar datos

```sql
INSERT INTO tabla (columna1, columna2) VALUES (valor1, valor2);
```

Ejemplo:

```sql
INSERT INTO empleados (nombre, edad) VALUES ('Juan', 35);
```

### 5. Actualizar datos

```sql
UPDATE tabla SET columna1 = valor1 WHERE condicion;
```

Ejemplo:

```sql
UPDATE empleados SET salario = 5000 WHERE id = 1;
```

### 6. Eliminar datos

```sql
DELETE FROM tabla WHERE condicion;
```

Ejemplo:

```sql
DELETE FROM empleados WHERE id = 3;
```

### 7. Crear una tabla

```sql
CREATE TABLE tabla (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    edad INT
);
```

### 8. Eliminar una tabla

```sql
DROP TABLE tabla;
```

### 9. Contar registros

```sql
SELECT COUNT(*) FROM tabla;
```

### 10. Agrupar resultados

```sql
SELECT columna, COUNT(*) FROM tabla GROUP BY columna;
```

## Tipos de JOINs en SQL

### 1. INNER JOIN (Intersección de dos tablas)

```sql
SELECT A.columna, B.columna
FROM tablaA A
INNER JOIN tablaB B ON A.id = B.id;
```

Devuelve solo los registros que tienen coincidencias en ambas tablas.

### 2. LEFT JOIN (Todos los registros de la tabla izquierda y coincidencias de la derecha)

```sql
SELECT A.columna, B.columna
FROM tablaA A
LEFT JOIN tablaB B ON A.id = B.id;
```

Si no hay coincidencias en la tabla derecha, devuelve NULL en esas columnas.

### 3. RIGHT JOIN (Todos los registros de la tabla derecha y coincidencias de la izquierda)

```sql
SELECT A.columna, B.columna
FROM tablaA A
RIGHT JOIN tablaB B ON A.id = B.id;
```

Si no hay coincidencias en la tabla izquierda, devuelve NULL en esas columnas.

### 4. FULL OUTER JOIN (Todos los registros de ambas tablas, con NULL en donde no hay coincidencias)

```sql
SELECT A.columna, B.columna
FROM tablaA A
FULL OUTER JOIN tablaB B ON A.id = B.id;
```

### 5. CROSS JOIN (Producto cartesiano)

```sql
SELECT A.columna, B.columna
FROM tablaA A
CROSS JOIN tablaB B;
```

Cada fila de `tablaA` se combina con cada fila de `tablaB`.

### 6. SELF JOIN (Un JOIN consigo misma)

```sql
SELECT A.nombre, B.nombre
FROM empleados A
JOIN empleados B ON A.jefe_id = B.id;
```

Útil para representar relaciones jerárquicas como empleados y sus jefes.

---

### Notas Finales

- `WHERE` se usa para filtrar filas antes de agrupar.
- `HAVING` se usa para filtrar después de aplicar `GROUP BY`.
- `LIMIT` restringe la cantidad de resultados devueltos.

```sql
SELECT * FROM empleados LIMIT 5;
```