# Los docs del curso ✌️
Estamos usando [mkdocs.org](https://www.mkdocs.org).

Para agregar / modificar se editan los archivos de markdown dentro de `docs/`.

Hay uno por cada clase. Si tomás la clase_1 de ejemplo verás cómo se hacen los recuadritos y todas esas pavadas.

Si querés instalarte el mkdocs en tu local para ver los cambios cómo quedarían, en la página están las instrucciones:
https://www.mkdocs.org/getting-started/

## Correr en local
1. Clonar el repo
    ```shell
    cd /path/donde/lo/quieras/tener
    
    git clone git@github.com:anairamzap/curso-polito.git
    ```
2. Pararse en el dir raíz del repo
    ```shell
    cd curso-polito
    ```
3. Crear un virtualenv para instalar mkdocs y sus dependencias (o en su defecto usar un IDE para crearlo)
    ```shell
    python3.9 -m venv venv
    ```
    **NOTA**: Tuve problemas con python 3.11, pero tal vez fue cosa de mi local, por si querés hacer la prueba. Sino con 3.9
    va ok.


4. Activar el virtual env (si usaste una IDE, entiendo te lo hace automáticamente)
    ```shell
    source venv/bin/activate
    ```
5. Chequeemos que el entorno está OK (no sea cosa te pase como al gobernador :P)
    ```shell
    python -V && pip -V
    ```
6. Ahora si todo fue bien (es decir python es 3.9 y pip es para esa versión), instalamos dependencias
    ```shell
    pip install -r requirements.txt
    ```
7. Si todo sale bien, ya podemos correr mkdocs
    ```shell
    mkdocs serve
    ```
---

### "Servir" los docs en local (cada cambio autorefresca el browser).
Muy útil pa escribir y ver cómo va quedando.
```shell
mkdocs serve
```

Se puede servir en local generando el pdf también para ver cómo queda:
```shell
ENABLE_PDF_EXPORT=1 mkdocs serve
```
Pero OJO :eyes: porque le lleva un rato hacer el rebuild. O sea, sirve para debuggear alguna cosa puntual, pero no
recomiendo.

### Buildear los docs en local.
Puede ser útil para ver cómo arma los html y chequear si está todo OK.

**Sin** generar pdf:
```shell
mkdocs build
```

Generando el pdf:
```shell
ENABLE_PDF_EXPORT=1 mkdocs build
```
Esto va a tirar el pdf en `site/pdf/prog_polito_2025.pdf`

### Publicar cambios en github pages (o deployar)
```shell
ENABLE_PDF_EXPORT=1 mkdocs gh-deploy
```
Este comando sí lo corremos siempre con el pdf export así lo incluye en github. Salvo que por algún motivo no queramos
incluir el export a PDF, lógicamente.

