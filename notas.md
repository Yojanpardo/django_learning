# Manejo de urls en Django
```python
urlpatterns = [
    url(r'^admin/', admin.site.urls),
]
```
Esto significa que para cada URL que empieza con admin/ Django encontrará su correspondiente vista

para que las urls coincidan con las vistas, django utiliza una cosa que se llama regex "Regular Expressions" y son un montón de normas que forman un patron de busqueda.

>Nota: existen muchas formas de enrutar los modelos con las vistas. estas son unos patrones del proceso de enrutamiento

```
^ denota el principio del texto
$ denota el final del texto
\d representa un dígito
+ indica que el ítem anterior debería ser repetido por lo menos una vez
() para encerrar una parte del patrón
```
* hablando del ORM y QuerySet podemos hacer distintos tipos de consultas aplicando distintos filtros aquí voy a poner unos ejemplos que se originan a partir del ejercicio realizado.

* ```Post.objects.all() ``` para realizar una consulta de todos los posts.

* ```Post.objects.filter(author=me)``` para realizar una consulta que filtre los posts por el autor, en este caso va a seleccionar los posts que en la variable author contenga mi nombre.

* ```Post.objects.filter(title__contains='jueves')``` en este caso va a filtrar los posts que en su titulo contengan la plabra jueves.

* ```Post.objects.filter(published_date__lte=timezone.now())``` con esta consulta obtenemos como resultado los post que hayan sido publicados hoy.

* ```Post.objects.order_by('created_date')``` Con esta consulta no filtramos los posts sino que vamos a ordenar los objetos por su fecha de creación asi como se pede organizar por nombre o demas.
