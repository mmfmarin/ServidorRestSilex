El proyecto original lo pueden encontrar en
https://github.com/micayael/com.micayael.blog.ServidorRestSilex. El único fin
de este fork es hacerlo compatible con postgresql, para esto se debe
crear una tabla en la base de datos 'restsilex' con la siguiente sentencia:

CREATE TABLE comments
(
    id serial NOT NULL,
    author character varying(30) NOT NULL,
    email character varying(100) NOT NULL,
    content text NOT NULL,
    created_at timestamp without time zone NOT NULL,
    updated_at timestamp without time zone NOT NULL DEFAULT now(),
    CONSTRAINT comments_pkey PRIMARY KEY (id)
)

= Notas del autor original: =
Este proyecto se crea como consecuencia al artículo "Servicios REST usando Silex micro-framework" publicado en en http://blog.micayael.com/2012/01/16/servicios-rest-usando-silex-micro-framework-php-symfony-i/

Para revisión de la documentación favor ir a https://github.com/micayael/com.micayael.blog.ServidorRestSilex/wiki
