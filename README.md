# sql-select-fundamentals
Práctica de consultas básicas SELECT y alias en SQL Server.

-- TechStore - Consultas Basicas SELECT

-- Descripcion
Este repositorio contiene tres consultas SQL realizadas sobre la tabla `sales` de la empresa ficticia TechStore.
El objetivo es practicar la seleccion de datos mediante SELECT, la eleccion de columnas especificas y el uso de alias para facilitar la interpretacion de la informacion.

-- 1. ¿Por que es mala practica usar SELECT * en produccion?

Utilizar `SELECT *` en produccion no es recomendable por varias razones:
- **Rendimiento:** al seleccionar todas las columnas, se puede recuperar informacion innecesaria y aumentar el consumo de recursos.
- **Mantenibilidad:** si se agregan nuevas columnas a la tabla, la consulta tambien podria devolver esos datos sin que sea necesario.
- **Seguridad:** se pueden exponer datos que no son necesarios para quien consulta la informacion.

Por ejemplo, si el equipo de finanzas solamente necesita conocer el importe de las ventas, es mejor seleccionar `total_amount` en lugar de utilizar `SELECT *`.

-- 2. ¿Por que son importantes los alias para un stakeholder no tecnico?
Los alias permiten cambiar los nombres tecnicos de las columnas por nombres mas claros y faciles de interpretar.
Por ejemplo, la columna `total_amount` puede mostrarse como `monto_total`.
De esta manera, una persona del equipo de finanzas puede comprender directamente que ese dato representa el importe total de una venta, sin necesidad de conocer la estructura interna de la base de datos.
En esta practica tambien se utilizaron alias como `fecha_pedido`, `nombre_producto` y `cantidad_unidades` para facilitar la lectura de los resultados.

-- Consultas realizadas
1. Exploracion general de la tabla `sales`.
2. Seleccion de columnas especificas para el equipo de finanzas.
3. Renombramiento de columnas mediante alias en español.
