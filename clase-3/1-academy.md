```sql
create table instructores(
  id serial primary key,
  nombre varchar(100) not null,
  email varchar(100) unique not null
);

create table cursos(
  id serial primary key,
  titulo varchar(100) not null,
  descripcion text,
  instructor_id int,
  constraint fk_instructor
    foreign key (instructor_id)
    references instructores(id)
);



```