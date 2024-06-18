```sql
CREATE TABLE products (
  product_id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  descripcion TEXT,
  price DECIMAL(10,2) NOT NULL, -- 349.94  10.15
  stock INT not null check (stock >= 0), -- >= esto es mayor o igual
  category VARCHAR(50) NOT NULL
);

```