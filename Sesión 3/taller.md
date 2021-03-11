---
marp: true
---

# Pequeña introducción a markdown

[Pedro A. García Sánchez](http://www.ugr.es/local/pedro)

***

# Estructura

## Subtítulo

### Otro nivel

##### Y otro

Podemos usar de una a seis \#s para indicar nivel de profundidad

```markdown
# Título

## Subtítulo

...
```

***


# Listas

Podemos empezar una lista con `-` o bien `*`
```
* Sin enumerar
* Y con sublistas
	* 1
	* y dos
```
Da lugar a

* Sin enumerar
* Y con sublistas
	* 1
	* y dos

Si queremos numeradas, cambiamos los `*` por un `1.`

1. numeradas
2. y tambíen anidadas
	1. Eso, ahora otra numeración

***

# Fórmulas

Esto es una fórmula en línea $(x^2+1)^3$ y además podemos hacer una centrada

$$\int_a^b \frac{x+1}{x-1} \mathrm d x.$$

Las fórmulas en línea las escribimos con `$..$` las centradas con doble `$$` o bien `\[..\]`

---

# Tablas

```markdown
|Cabecera 1|Cabecera 2| Y 3|
| ----| :---: | ---: |
| Normal | Centrado | a derecha|
```

|Cabecera 1|Cabecera 2| Y 3|
| ----| :---: | ---: |
| Normal | Centrado | a derecha|

---

# Resaltado

```markdown
En *itálica*, **negrita** y en las dos **_ambos_**.
```
En *itálica*, **negrita** y en las dos **_ambos_**.

___

# Enlaces

Sintáxis

```markdown
[ugr](http://www.ugr.es)
```

Un enlace a la [ugr](http://www.ugr.es)

O con citas [Universidad de Granada][UGR]. En la página de esa [universidad][UGR], se encuentran muchas cosas.

[UGR]: https://www.ugr.es "Universidad de Granada"

Para ello usamos el formato `[texto enlace][id]` y en cualquier sitio

```markdown

[id]: https://dondesea.io "Descripción"

```

***

# Imágenes

y si queremos imágenes, ponemos un ! delante
```markdown
![Una foto](imagen.jpg)
```

![Una afoto](imagen.jpg "una imagen")

---


# Citas

> La citas comienzan con \>
> > y se pueden anidar

	Si indentamos también obtenemos bloques
	Del tamaño que escribamos, como un verbatim



---

# Código insertado

Código en línea `printf("Hello world\n")`

O bien un trozo de código

```c
printf("Hello world\n");
return void;
```

Para el código en línea usamos acentos simples

	`printf("Hello world\n")`


Para varias líneas de código

	```c
	printf("Hello world\n");
	return void;
	```

Se puede especificar el lenguaje usado

***

# Transparencias

Para convertirlo en transparencias hacemos

```bash
pandoc -s --mathjax -t slidy resumen.md -o resumen.html
```

o podemos utilizar `revealjs` o [remark](https://remarkjs.com)
