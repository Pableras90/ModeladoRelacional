# ModeladoRelacional


### Cursos

- Relación muchos a muchos con Autores: Un curso puede tener varios autores y un autor puede contribuir a varios cursos.
- Relación uno a muchos con Videos: Un curso puede tener varios videos.
- Relación uno a muchos con Artículos: Un curso puede tener varios artículos.

### Videos

- Relación uno a uno con Autores: Un video tiene un autor (restricción según el ejercicio).
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
