# Sisban Front-End


El workflow de desarrollo front-end de Sisban ejecuta tareas automatizadas de la siguiente forma:

- Compila, autoprefija `(cross-browser css)` y minifica nuestros estilos (SCSS).
- Minifica con uglify nuestros archivos javascript
- Optimiza y comprime imágene
- Genera un URL local para desarrollo en vivo


## Para correr el proyecto y compilar automáticamente

0. Instalamos node.js : https://nodejs.org/en/download/

1. Clonamos el repositorio

```bash
git clone https://alejandro-dev@bitbucket.org/anagrama/sisban-front.git
```
2. Entramos al directorio

```bash
cd sisban-front
```

3. Una vez que descarguemos y entremos al directorio corremos:

```bash
npm install
```

4. Y corremos el kit

```bash
gulp
```

Si todo sale bien se abrirá una ventana del navegador.

5. En caso de que no funcione:

A. Asegurarnos de tener el puerto libre para el webserver

B. Reinstalar

- Node.js ```https://nodejs.org/en/download/```
- Gulp ```npm install gulp```


C. Instalar dependencias manualmente

```bash
npm install gulp-autoprefixer gulp-imagemin gulp-plumber gulp-rename
gulp-sass gulp-uglify imagemin-pngquant
```


## Si no queremos usar gulp existen apps para compilar

- Prepros (https://prepros.io) <- Recomendado
- Koala (http://koala-app.com/)
- Scout (http://scout-app.io/)
- LiveReload (http://livereload.com/)

## Para producción

1. Subir todo excepto el directorio 'sass' ya que solo ocupará espacio

2. Para mandar a back con rob solo se utilizarán los contenidos de la carpeta
'sass'

# Si todo falla

1. Desinstalamos modulos de node por completo en nuestro directorio

```bash
rm -rf node_modules
```

2. Instalamos gulp manualmente


```bash
npm install gulp -g
```

3. Reinstalamos nuestros modulos de node

```bash
npm install
```

4. Instalamos dependencias manualmente

```bash
npm install gulp-autoprefixer gulp-imagemin gulp-plumber gulp-rename
gulp-sass gulp-uglify imagemin-pngquant
```

5. Reiniciamos la terminal (Cmd+Q) y la abrimos de nuevo luego corremos:


```bash
gulp
```
