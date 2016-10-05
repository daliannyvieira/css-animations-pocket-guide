![cover](images/cover01.png)

Todos os [exemplos](http://codepen.io/collection/XmZvqo/) inclusos nesse guia estão disponíveis no codepen.
## Mapa

* [Introdução](#introdução)
	* [Recomendações](#recomendações)
* [Transitions](#transitions)
	* [More transitions](#more-transitions)
* [Transforms](#transforms)
	* [Transforms 2D](#transforms-2d)
		* [Transform scale](#transform-scale)
		* [Transform rotate](#transform-rotate)
		* [Transform translate](#transform-translate)
		* [Transform skew](#transform-skew)
	* [Transforms 3D](#transforms-3d)
		* [Transform rotateX](#rotate-x)
		* [Transform rotateY](#rotate-y)
		* [Transform rotateZ](#rotate-z)
* [Animations](#animations)
	* [Construindo](#construindo)
	* [Keyframes](#keyframes)
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

##Transforms 2D

Podemos adicionar transformações ao elementos, fazendo-os crescerem, girarem, ou se deslocarem, em 2D e também 3D. Transformações que podem ser usadas: scale, rotate, translate, e skew.

###Transform scale

Scale pode fazer com que um elemento cresça ou diminua sua dimensão. Exemplo: para fazer com que um elemento cresça em uma proporção equivalente à metade de seu tamanho usamos scale(1.5); Se quisessemos que ele crescesse o dobro do seu tamanho adicionaríamos scale(2); e assim por diante.

Se adicionadas como hover, por exemplo, pode ser interessante também continuar combinando transformações com transições, fazendo com que as trasnformações sejam mais agradáveis de se ver. Podemos usar all para manter a mesma duração por segundos em uma transição. Exemplo:

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

Rotate como o próprio nome sugere, é capaz de fazer um elemento girar. Podemos fazer com que ele gire usando deg ou turn como valor, 1turn equivale a 360graus.

	.elemento {
  		/* Adicionando transições */
  		transition: all 1s;
	}
	/* Adicionando modificações */
	.elemento:hover {
		/* Alterando a cor */
 		background-color: green;
		/* Diminuindo a altura e largura */
  		height: 70px;
  		width: 70px;
		/* Girando uma volta completa */
  		transform: rotate(360deg);
	}
![Transform rotate](images/04.gif)

###Transform translate

	.elemento {
  		/* Adicionando transições */
 		 transition: all 1s;
	}
	/* Adicionando modificações */
	.elemento:hover {
  		background-color: green;
  		transform: translateY(30px);
	}
![Transform translate](images/05.gif)

##Transforms 3D

##Animations
###Construindo

Há dois passos que devem ser seguidos, primeiro criamos a animação, fazendo uso de [Keyframes](#keyframes) depois a adicionamos.

	.elemento {
		/* Adicionando o keyframe criado à animação */
		animation: animacao 1s infinite;
	}
	/* Criando o keyframe */
	@keyframes animacao {
		0% {
			transform: scale(0.9);
			opacity: 0;
		}
		50% {
			transform: scale(1.1);
			opacity: 1;
		}
		100% {
			transform: scale(1);
		}
	}
![keyframes-animations](images/06.gif)
