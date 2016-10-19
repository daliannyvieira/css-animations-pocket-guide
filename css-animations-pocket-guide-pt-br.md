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
		* [Transform rotateX](#transform-rotatex)
		* [Transform rotateY](#transform-rotatey)
		* [Transform rotateZ](#transform-rotatez)
* [Animations](#animations)
	* [Construindo](#construindo)
		* [Keyframe](#keyframe)
		* [Animation](#animation)

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

	/* Adicionando transição */
	.elemento {
 		 transition: background-color 1s;
	}
![transitions example](images/01.gif)

###More transitions

É possível adicionar também mais propriedades em uma mesma transição separando-as por vírgulas, e dar a elas o mesmo tempo de duração, ou não, exemplo:

	/* Adicionando mais transições */
	.elemento {
  		transition:
			background-color 1s,
			height 1s,
			width 1s,
			opacity 1s;
	}
	
	/* Adicionando mais modificações */
	.elemento:hover {
 		background-color: green;
  		height: 70px;
  		width: 70px;
  		opacity: 0;
	}

![More transitions](images/02.gif)

##Transforms

###Transforms 2D

Podemos adicionar transformações ao elementos, fazendo-os crescerem, girarem, ou se deslocarem, em 2D e também 3D. Transformações que podem ser usadas: scale, rotate, translate, e skew.

####Transform scale

Scale pode fazer com que um elemento cresça ou diminua sua dimensão. Exemplo: para fazer com que um elemento cresça em uma proporção equivalente à metade de seu tamanho usamos scale(1.5); Se quisessemos que ele crescesse o dobro do seu tamanho adicionaríamos scale(2); e assim por diante.

Se adicionadas como hover, por exemplo, pode ser interessante também continuar combinando transformações com transições, fazendo com que as trasnformações sejam mais agradáveis de se ver. Podemos usar all para manter a mesma duração por segundos em uma transição. Exemplo:

	/* Adicionando transição */
	.elemento {
		transition: all 1s;
	}
	
	/* Adicionando modificações */
	.elemento:hover {
		background-color: green;
		transform: scale(1.5);
	}
	
![Transform scale](images/03.gif)

####Transform rotate

Rotate como o próprio nome sugere, é capaz de fazer um elemento girar. Podemos fazer com que ele gire usando deg ou turn como valor, 1turn equivale a 360 graus.

	/* Adicionando transições */
	.elemento {
  		transition: all 1s;
	}
	
	/* Adicionando modificações */
	.elemento:hover {
 		background-color: green;
  		height: 70px;
  		width: 70px;
  		transform: rotate(360deg);
	}
![Transform rotate](images/04.gif)

####Transform translate

	/* Adicionando transições */
	.elemento {
 		 transition: all 1s;
	}
	
	/* Adicionando modificações */
	.elemento:hover {
  		background-color: green;
  		transform: translateY(30px);
	}
![Transform translate](images/05.gif)

####Transform skew

Skew é capaz de inclinar, ou distorcer, um elemento ao longo dos eixos X e Y.

	/* Adicionando mais transições */
	.elemento {
 		transition: all 1s;
	}
	
	/* Adicionando mais modificações */
	.elemento:hover {
	  background-color: green;
	  transform: skew(0deg, 20deg);
	}
![Transform skew](images/07.gif)

###Transforms 3D

####Transform rotateX

	/* Adicionando mais transições */
	.elemento {
 		transition: all 1s;
	}
	
	/* Adicionando mais modificações */
	.elemento:hover {
  		background-color: green;
  		transform: rotateX(90deg);
	}
![Transform rotateX](images/09.gif)
####Transform rotateY

	/* Adicionando mais transições */
	.elemento {
	  transition: all 1s;
	}
	/* Adicionando mais modificações */
	.elemento:hover {
	  background-color: green;
	  transform: rotateY(180deg);
	}
![Transform rotateY](images/10.gif)
####Transform rotateZ

  	/* Adicionando mais transições */
	.elemento {
	  transition: all 1s;
	}
	/* Adicionando mais modificações */
	.elemento:hover {
	  background-color: green;
	  transform: rotateZ(90deg);
	}
![Transform rotateZ](images/11.gif)
##Animations

###Construindo

Criar uma animação é criar uma lista do que deve acontecer com as propriedades de um elemento em um determinado período de tempo. Há dois passos que devem ser seguidos, primeiro criamos a animação, fazendo uso de um ou mais [Keyframes](#keyframe):

	/* Criando um keyframe */
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
	
Depois a adicionamos ao elemento:

	/* Adicionando o keyframe criado à animação */
	.elemento {
		animation: animacao 1s infinite;
	}
![keyframes-animations](images/06.gif)

###Keyframe

Um keyframe deve dizer onde, quando, e como devem ocorrer modificações nas propriedades.

###Animation
