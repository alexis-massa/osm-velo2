Installation
============

sudo su - postgres
psql
create database coocyclette;
grant all privileges on database coocyclette to coocyclette;
C-d

psql -d coocyclette -U coocyclette -h localhost
create schema coocyclette_schema;
C-d

Aller configurer l’accès à la BD dans le settings.py

python manage.py migrate

python manage.py shell
from dijk.pour_shell import *
charge_villes()