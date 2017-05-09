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
