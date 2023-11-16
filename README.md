# MUTANTES
* Nombre: Fiamma Brizuela
* Legajo: 51494
* DNI: 43544191
* Emai: brizuelafiamma6@gmail.com

<h2> De que trata:</h2>
El proyecto trata de analizar una secuencia de ADN y verfificar si es mutante o no.
# Explicacion para usuario
Al ingresar se le pedira que ingrese una secuencia de adn de 6 letras de rango  y solo son validas las letras  "C"T"G"A" en distintas combinaciones,  si hay menos o más de 6 letras de  rango el programa no avanzara a la siguiente secuencia, te pedira que vuelvas a ingresar la secuencia por una correcta y lo mismo pasaria si se ingresa una secuencia con alguna letra diferente a las permitidas.
Una vez ingresadas las seis secuencias que se necesitan para averiguar si adn pertenece a un mutante o no, se creara una matriz, se analizara dicha matriz y si encuentra más de una secuencia con  más de cuatro letras iguales(ya sea oblicua,vertical u orizontal)se mostrara un mensjae diciendo que el adn es de un mutante,al contrario se mostrara un mensaje diciendo que el adn no es de un mutante y el programa habra terminado.

 <h3> caso 1</h3>

* A	T	G	C	G	A
* C	A	G	T	G	C
* T	T	A	T	T	T
* A	G	A	C	G	G
* G	C	G	T	C	A
* T	C	A	C	T	G

Si ingresa la secuencia mostrada en el caso 1  el programa le mostrara el mensaje "No es un mutante".

<h3> caso 2</h3>

* A	T	G	C	G	A
* C	A	G	T	G	C
* T	T	A	T	G	T
* A	G	A	A	G	G
* C	C	C	C	T	A
* T	C	A	C	T	G

Si ingresa la secuencia mostrada  en el caso 2 el programa le mostrara el mensaje " Es un mutante"

<h2>Resolucion</h2>
Como primer paso realize la clase <Strong>CrearAdn</Strong> su funcion es que el usuario ingrese las secuencias para definir la matriz, en cada iteración que haga va a llamar a la clase <Strong>Validate</Strong> que verificara si la secuencia cumple con los requisitos pedidos, cada vez que la secuencia sea correcta se guardara en una lista de la clase <Strong>CrearAdn</Strong>.Cuando termina de llenar la matriz esta lista se retorna.
Como segundo paso guarde la matriz en una varaiable global llamada <Strong>dna</Strong> esta variable se la pase como parametro a la función <Strong>isMutant</Strong>, que se encarga de instanciar la clase <Strong>Analizardna</Strong> y llamar a sus respectivos metodos(AnalizarOblicuas,AnalizarOblicuasInversas, AnalizarColumnas, analizarfilas) cuales analizan la matriz y retornan la cantidad de veces que se cumplio la condición, el resultado es alamasenado en un acumulador de la función <Strong>isMutant</Strong> si el acumulador es mayor a uno retorna true si no false.
En el último paso  hice un if en bloque principal, su función es imprimir dependiendo lo que retorne  <Strong>isMutant</Strong>.

