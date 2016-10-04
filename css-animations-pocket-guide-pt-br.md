![cover](images/cover01.png)

Todos os [exemplos](http://codepen.io/collection/XmZvqo/) inclusos nesse guia estão disponíveis no codepen.
## Mapa

* [Introdução](#introdução)
	* [Recomendações](#recomendações)
* [Transitions](#transitions)
	* [More transitions](#more-transitions)
* [Transforms](#transforms)
	* [Transform scale](#transform-scale)
	* [Transform rotate](#transform-rotate)
	* [Transform translate](#transform-translate)
* [Keyframes Animations](#keyframes-animations)
* [SVG Animations](#svg-animations)

## Introdução

###Recomendações

Para aproveitar melhor esse guia, é recomendado que se tenha um conhecimento prévio sobre HTML e CSS básico.

##Transitions

Podemos adicionar uma transição de tempo em uma modificação por um determinado elemento. Adicionamos ao elemento a seguinte propriedade:

	.elemento {
		transition: <property> <duration>;
	}
	
Um exemplo prático:
Queremos modificar a cor de um elemento quando o usuário posicionar o cursor sobre ele.

	/* Adicionando uma modificação */
	.elemento:hover {
		  background-color: tomato;
	}
	
Mas queremos que essa mudança aconteça de forma suave. Então adicionamos uma transição, com a propriedade modificada e a duração que queremos, 1 segundo, por exemplo:

	.elemento {
		 /* Adicionando transição */
 		 transition: background-color 1s;
	}
![transitions example](images/01.gif)

###More transitions

É possível adicionar também mais propriedades em uma mesma transição separando-as por vírgulas, e dar a elas o mesmo tempo de duração, ou não, exemplo:

	.elemento:hover {
		 /* Adicionando mais modificações */
 		background-color: green;
  		height: 70px;
  		width: 70px;
  		opacity: 0;
	}
	
	.elemento {
		/* Adicionando mais transições */
  		transition:
			background-color 1s,
			height 1s,
			width 1s,
			opacity 1s;
	}


![More transitions](images/02.gif)

##Transforms

Podemos adicionar transformações ao elementos, fazendo-os crescerem, girarem, ou se deslocarem, em 2D e também 3D. Transformações que podem ser usadas: scale, rotate, translate, e skew.
###Transform scale

	/* Adicionando modificações */
	.elemento:hover {
		background-color: green;
		transform: scale(1.5);
	}

	.elemento {
		/* Adicionando transição */
		transition: all 1s;
	}
![Transform scale](images/03.gif)

###Transform rotate
![Transform rotate](images/04.gif)
###Transform translate
![Transform translate](images/05.gif)
##Keyframes Animations
![keyframes-animations](images/06.gif)


