# StockFinderWeb

## Linux

gunicorn --workers 4 --bind 10.10.0.110:6000 -m 007 wgsi:app

## Windows

waitress-serve --listen=10.10.0.110:6000 wsgi:app

## pipreqs

pipreqs --encoding=utf8 --force

# Para ejecutar desarrollo

1. flask_back -> flask run

   - Importante -> Asegurarse que no hay telegram=0.0.1 en los requirements

2. nextjs_front -> npm run dev

# Para ejecutar producción

1. flask_back -> build Dockerfile and start the container

   ## Importante

   1. Asegurarse que no hay telegram=0.0.1 en los requirements y que está gunicorn==20.0.1
   2. Eliminar flask_back de todos los imports de los modulos

2. nextjs_front -> build Dockerfile and start the container
