```sql
-- 1. Crear la tabla 'products'
create table products (
 product_id SERIAL primary key,
 name VARCHAR(100) not null,
 description text,
 price DECIMAL(10,2) not null,
 stock INT not null check (stock >=0),
 category VARCHAR(50) not null
);

-- 2. Insertar registros en la tabla 'products' 'CREATE - INSERT'
insert into products (name, description, price, stock, category) values 
('Teclado Mecánico RGB', 'Teclado mecánico retroiluminacion RGB', 89.99, 50, 'teclado'),
('Mouse Gaming', 'Mouse gaming con sensor óptico de alta precisión y luces RGB',49.99, 100, 'mouse'),
('Monitor 4K', 'Monitor 4K de 27 pulgadas con 144hz de tasa de refresco', 399.99, 20, 'monitor');

-- 3. Consultar los datos almacenados - 'READ - SELECT'
select * from products;

-- 4. Actualizar información de un producto - 'UPDATE'
update products set price = 44.99 where product_id = 2;

-- 5. Vamos a eliminar el producto Teclado Mecánico RGB de la tabla products
delete from products where product_id = 1;

-- 6. Actualizar información de un producto - 'UPDATE'
update products set price = 44.99 where name = 'Mouse Gaming';

-- 7. Vamos a eliminar el producto Teclado Mecánico RGB de la tabla products
delete from products where name = 'Teclado Mecánico RGB';
```
