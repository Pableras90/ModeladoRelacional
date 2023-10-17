# Modelo de Datos para eLearning

El modelo sigue un enfoque relacional, en el cual la información se organiza en tablas (relaciones) y se establecen relaciones entre estas tablas.

## Entidades Principales

- **Cursos, Autores, Videos, Artículos, Temáticas, Headless_CMS_Storage_S3:**
  Estas son las entidades principales que representan los elementos centrales de la aplicación de eLearning.

## Relaciones Principales

- **Relación Muchos a Muchos entre Cursos y Autores:**
  Se utiliza una tabla intermedia `Cursos_Autores` para manejar la relación muchos a muchos entre cursos y autores.

- **Relación Muchos a Muchos entre Videos y Temáticas:**
  Se utiliza una tabla intermedia `Videos_Tematicas` para manejar la relación muchos a muchos entre videos y temáticas.

- **Relación Muchos a Uno entre Videos y Headless_CMS_Storage_S3:**
  La relación muchos a uno indica que un video puede estar asociado a un único almacenamiento externo en `Headless_CMS_Storage_S3`.

- **Relación Muchos a Uno entre Artículos y Headless_CMS_Storage_S3:**
  La relación muchos a uno indica que un artículo puede estar asociado a un único almacenamiento externo en `Headless_CMS_Storage_S3`.

## Uso de Claves Primarias y Foráneas

- **Claves Primarias (PK):**
  Cada tabla tiene una clave primaria que identifica de manera única cada registro en esa tabla (por ejemplo, `curso_id`, `autor_id`, `video_id`, etc.).

- **Claves Foráneas (FK):**
  Se utilizan claves foráneas para establecer relaciones entre las tablas. Por ejemplo, en la tabla `Videos`, la clave foránea `curso_id` hace referencia a la clave primaria `curso_id` en la tabla `Cursos`.






# ModeladoRelacional



### Cursos

- Relación muchos a muchos con Autores: Un curso puede tener varios autores y un autor puede contribuir a varios cursos.
- Relación uno a muchos con Videos: Un curso puede tener varios videos.
- Relación uno a muchos con Artículos: Un curso puede tener varios artículos.

### Videos

- Relación uno a uno con Autores: Un video tiene un autor.
- Relación mucho a muchos con Temáticas: Un video puede pertenecer a varias temáticas.
- Relación muchos a uno con Headless CMS/Storage S3: Un video se almacena en un sistema de almacenamiento externo.

### Artículos

- Relación mucho a uno con Cursos: Un artículo pertenece a un curso.
- Relación muchos a uno con Headless CMS/Storage S3: Un artículo se almacena en un sistema de almacenamiento externo.

### Autores

- Relación mucho a muchos con Cursos: Un autor puede contribuir a varios cursos.
- Relación uno a uno con Videos: Un autor está asociado a un video.

### Temáticas

- Relación mucho a muchos con Videos: Una temática puede tener varios videos y un video puede pertenecer a varias temáticas.

### Headless CMS/Storage S3

- Relación uno a muchos con Videos: Varios videos pueden almacenarse en el mismo sistema externo.
- Relación uno a muchos con Artículos: Varios artículos pueden almacenarse en el mismo sistema externo.

