# sistema de ventas de libros 

## glosario 

- **PK**: _Primari Key_
- **FK**: _Forein Key_
- **UQ**: _Unique Atribute_
- **ED**: Entidad de datos
- **EP**: Entidad pivote
- **EC**: entidad de catalogo

## Descripción
Se desea diseñar un **sistema de venta de libros**. Debe contemplar el **catálogo de libros actual** (identificador, clave, título, autor, editorial, ubicación, precio, costo, descuento)
los **proveedores** (editorial, clave, descripción, observaciones),
las **ventas**(numero cliente, datos facturación, cantidad, producto, precio, total a pagar, impuestos, fecha de compra, fecha de entrega, empleado que atendió la compra),
 la información de los **empleados** que atienden y los datos del **cliente** que realiza la compra (nombre, dirección, datos fiscales, puesto, etc).

objetivos
1. Diseñar el modelo de bases de datos para atender los requerimientos del problema.
2. Definir entidades, relaciones y atributos.
3. Aplicar las 3 formas normales.
4. Elaborar el diagrama entidad-relación.
5. Crear la base de datos en MySQL o PostgreSQL
6. Elaborar las sentencias SQL para ingresar datos en todas las tablas y validar que realiza las restricciones: que no se venda un producto a un cliente inexistente, que no se venda un producto del que no se tiene stock, verificar que la tarjeta del cliente tenga saldo para realizar la compra.
7. Elabora las sentencias SQL para elabora los siguientes reportes:
- lista de clientes
- lista de clientes que realizaron compras en los últimos 3 meses
- lista de empleados que realizaron más ventas del mes
- lista de productos
- lista de productos en stock
- lista de ventas por mes

## **Entidades** bosquejo inicial
### **c_libros**
- id_libros (PK) identificador
- clave 
- título
- id_autor
- id_editorial
- id_ubicacion
- precio
- costo
- descuento
## **venta**
- id_venta (PK)
- id_cliente
- datos_facturacion
- cantidad
- producto
- precio
- total_pagar
- impuestos
- fecha_compra
- fecha_entrega
- id_empleado
## **cliente**
- id_cliente (PK)
- nombre
- dirección
- datos_fiscales
- puesto
## **empleado**
- id_empleado (PK)
- nombre
- dirección
- datos_fiscales
- puesto
## **autor**
- id_autor (PK)
- nombre
### **editorial**
- id_editorial (PK)
- descripción
- id_ubicacion
### **proveedor**
- id_proveedor (PK)
- id_editorial
- clave
- descripción
- observaciones
### **ubicación**
### ****