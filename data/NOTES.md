## Repaso SQL

SQL es un lenguaje de programaciòn para bases de datos.Su traducciòn literal seria Lenguaje Estructurado De Consultas (Structured Query Language)

SQL es un lenguaje insensible a mayùscula y minùscula."select"== SELECT.
 
En SQL las tablas tienen columnas que tendran informacòn de cierto **tipo**

Como buena pràctica los nombres de las tablas deben ser en **plural**

Llave primaria: con valor ùnico y no nulo.

CSV: Es un formato de archivo muy polular en los negocios. A partir de XLS se pueden exportar datos en CSV y tambièn importar.'Valores separados por coma'

SELECT<columnas>
FROM<table>;

La sentencia **WHERE** es para filtrar la informaciòn


```sql
SELECT <column>
FROM <tale>;
WHERE <column> <condition>;
```
```sql
SELECT name, country, area
WHERE cities
FROM area < 1100
AND country = 'Japan';
```

Ejemplo usando **OR**
```sql
SELECT name, country, area
FROM cities
ORDER BY area;
```
## Ejemplo con WHERE, OR Y ORDER

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
OR country = 'Japan'
ORDER BY area;
```
>Nota: Distinto puede ser <> o !=

## Campos o columna calculados con AS (como)

```sql
SELECT name,population/area AS density
FROM cities
ORDER BY density DESC;
```

## Contando elementos con COUNT

```sql
SELECT COUNT(name)
FROM cities
WHERE country = 'India';
```
## Limitar los resultados con **Limit**

```sql
SELECT name,population/area AS density
FROM cities
ORDER BY density DESC
LIMIT 2;
```
