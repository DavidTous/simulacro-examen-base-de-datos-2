# simulacro-examen-base-de-datos-2
### 1.-
SELECT titulo
FROM libros
WHERE fecha_prestamo = (
SELECT MIN(fecha_prestamo)
from prestamos);
### 2.-
SELECT titulo
FROM libros
WHERE libros.id_libro
IN(
SELECT id_libro
FROM prestamos
WHERE fecha_prestamo<'2023-04-01');
### 4.-
SELECT autor
FROM libros
GROUP BY autor
HAVING COUNT AVG(id_prestamo)<3;
### 5.-
SELECT * FROM prestamos
WHERE fecha_devolucion is null;
### 9.-
SELECT titulo
FROM libros
WHERE id_libro NOT IN(id_libro); 
