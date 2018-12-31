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

* No es necesario poner la extención del archivo

```scss
@import 'nombreArchivo';
```

## Mixins

```scss
@mixin cuadrado {
    background-color: #444;
    width: 200px;
    height: 200px;
    margin-top: 5px;
    padding: 10px;
}

.cuadrado-1{
   @include cuadrado;
}
.cuadrado-2{
    @include cuadrado;
}
.cuadrado-3{
    @include cuadrado;
}
```

### Mixins(parametros)

* Se recomienda poner un parametro por default en las variables.  

```scss
@mixin cuadrado ($fondo, $ancho: 200px) {
    background-color: $fondo;
    width: $ancho;
    height: 200px;
    margin-top: 5px;
    padding: 10px;
}

.cuadrado-1{
   @include cuadrado(#111, 200px);
}
.cuadrado-2{
    @include cuadrado(red);
}
.cuadrado-3{
    @include cuadrado(blue, 600px);
}
```

