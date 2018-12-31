# Instalar SASS

```
    gem install sass
```
## Enlazar archvios sass con css

```
    sass -w sass:css
```

## Organización de archivos

### CSS

```css
    footer {
    background: #444; 
    }
    footer h4 {
        color: red; 
    }
    footer h4 a {
        color: blue; 
    }
```

### SASS

```scss
    footer{
        background: #444;
        h4{
        color: red;
        a{
            color: blue;
        }
        }
    }
```

## Variables con SASS

```scss
    $nombreVariable: #f9ed69;

    section{
        background: $nombreVariable;
    }
```

## Import

```scss
@import 'nombreArchivo';
```



