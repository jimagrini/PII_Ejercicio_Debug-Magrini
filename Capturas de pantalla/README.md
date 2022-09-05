En "capt1" podemos apreciar el error en si. Observando la variable actual
y expected, vemos que son diferentes y por lo tanto se ejecuta la condicion
else.

En "capt2" nos adentramos en el metodo GetPhrase(), para ir paso por paso 
viendo como construye la variable "phrase", y aqui nos podemos dar cuenta que
la condicion else siempre se ejecutara por dos cosas:
	1- text1 y text2 tienen un " " por delante, por lo que siempre seran
		diferentes debido a que expected no contiene un espacio en blanco
		al principio del string
	2- La otra razon es porque el metodo GetPhrase() hace un append de un
		string que es un espacio en blanco " ", cuando text1 y text2 ya 
		tienen un espacio en blanco al final, por lo tanto quedaría en un
		doble espacio en blanco. Si observamos la variable "expected", vemos
		que tiene un solo espacio en blanco por lo que, nunca seran iguales 
		y siempre se ejecutara la condicion else.
