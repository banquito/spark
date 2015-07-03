# Spark
[![Build Status](https://travis-ci.org/banquito/spark.svg)](https://travis-ci.org/banquito/spark)
Spark es un stack de Wordpress basado en [Bedrock](https://roots.io/bedrock/)

## Requerimientos

* PHP >= 5.4
* Composer - [Instalar](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx)
* WP-CLI (opcional) - [Instalar](http://wp-cli.org)

## Instalación

1. Clonar el repo - `git clone git@github.com:banquito/spark.git`
2. Ejecutar `composer install`
3. Copiar `.env.example` a `.env` y actualizar las variables de entorno:
  * `DB_NAME` - Database name
  * `DB_USER` - Database user
  * `DB_PASSWORD` - Database password
  * `DB_HOST` - Database host
  * `WP_ENV` - Entorno (`development`, `staging`, `production`)
  * `WP_HOME` - Full URL al home (http://site.local)
  * `WP_SITEURL` - Full URL al WordPress incluyendo el subdirectorio (http://site.local/wp)
  * `WP_LANG` - Idioma ('es_ES', 'en', etc)
4. Copiar el/los themes en `web/app/themes`.
5. Configurar el vhost http://site.local para que apunte a `/path/to/site/web/`
6. Restaurar el último backup de la db desde `web/app/uploads/wp-migrate-db`
  * gunzip < [backupfile.sql.gz] | mysql -u [uname] -p[pass] [dbname]
7. Ingrar al admin desde `http://site.local/wp/wp-admin`

## Extras

  * Starter theme reponsivo [Underscore](http://underscores.me/).

  * Descargar archivos de idiomas en `/path/to/site/web/app/languages`
