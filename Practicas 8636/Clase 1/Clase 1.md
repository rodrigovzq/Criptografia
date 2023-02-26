# Elementos de Criptografia

- win y kali
- el otro es el disco
- Minimo la de Kali y aunet para el lunes

## Conceptos iniciales
Para asegurar acceso a la ifnormacion se deben cumplir.
- Identificacion
	- Indicarle al sistema cual es la cuenta usuario
- Autenticacion
	- Demostrarle al sismtea mediante clave por ejemplo, que el usuario es quien dice ser
- Autorizacion
	- Probar que el usuario tiene permiso

Pilares -> CID: Confidencialidad, Integridad, Disponibilidad

---

Metodos de autenticar
- Algo que se conoce -> contraseña
- Algo que se posee -> tarjeta magnetica/coordenadas/token
- Algo que es -> caracteristica personal unica/huella
Lo ideal es combinar 2 factores

--- 
## Criptografia Clasica
Ciencia que hace uso de metodos y herramientas matematicas con el objetivo de cifrar y proteger un mensaje o archivo por medio de un algoritmo para lograr la confidencialidad, en otros la autencididad o ambas

- Codfificar ≉ Cifrar
	- ASCII. hexa, etc no es cifrar

Codificar es la accion estatica donde un elemento representara siempre por el mismo elemento

![[Pasted image 20220328201701.png]]

**Criptograma**: Un texto que resulta de la cifra de cualquier informacion que no es legible ni comprensible salvo por el destinatario legitimo.
**Cifrar**: Al momento de querer transformar el texto plano en un criptograma estamos cifrando dicho texto plano
**Criptologia**: ciencia que estudia la criptografia y el criptoanalisis (quien encuentra fallas para llegar al texto plano sin la llave)
**Criptografo/ Criptologo:** persona que estudia la criptologia

### Tipos de ataque
- Solo texto cifrado
	- se conoce el algoritmo
- Texto conocido
- Texto elegido
- Texto cifrado elegido

Seguridad Incondicional
	No importa la potencia computacional, no se puede romper
Seguridad Computacional
	El cifrador esta limitado por el poder computacional
Fuerza bruta:
	Trabajar sobre todo el universo de contraseña

Criptosistemas simetricos:unica clave que deben compartir emisor y receptor
Criptosistemas asimetricos: cada usuario crea un par de claves

### Cifradores simetricos clasicos
![[Pasted image 20220328202853.png]]

Metodos antiguos son sustitucion y transposicion

![[Pasted image 20220328202935.png]]
Transposicion -> pasar un caracter a otra posicion.

Parece mas una codificacion que un cifrado porque no hay clave

#### Escitala
![[Pasted image 20220328203126.png]]

Lo usaban los espartanos
El diametro del palo es la clave

#### Cifrado del Cesar
 

El algoritmo consiste en el desplazamiento de tres espacios hacia la derecha de los caracteres del texto en claro.

Es un cifrador por sustitución monoalfabético en el que las operaciones se realizan *módulo* n, siendo n el número de elementos del alfabeto (en aquel entonces el latín).

![[Pasted image 20220328203345.png]]

![[Pasted image 20220328203451.png]]

Cuanto mas largo es el mensaje, mas facil de decifrar.
Si es por corrimiento, es inmediato porque todas las letras tendrian el mismo corrimiento.

![[Pasted image 20220328203705.png]]![[Pasted image 20220328203729.png]]

>>>  A partir de la técnica vista, sabiendo que se utiliza el cifrado del Cesar, criptoanalizar el siguiente mensaje con el fin de llegar al texto plano del mismo:

EIMAXLFTGIMMXTGÑGBWIMJILKÑXXMTXMETEXRJLBFXLTNXGZ TGÑGBIGOXLWTWXLTXGVÑTEKÑBXLNBXFJIKÑXMXTJILKÑXMBX GNLXXEEIMMXJXEXTGEIMWXOILTGEIMWXTYÑXLT

LOSHERMANOSSEANTUNIDOSPORQTUEESAESLALEYPRIMERATENGANTUNIONVERDADERAENCTUALQTUIERTIEMPOQTUESEAPORQTUESIENTREELLOSSEPELEANLOSDEVORANLOSDEAFTUERA

## Vignere
 

Cifrador polialfabético. Soluciona la debilidad del cifrado del César en que una letra se cifra siempre igual.

Se usa una clave K de longitud L y se cifra carácter a carácter sumando módulo n el texto en claro con los elementos de esta clave.

Ci = Mi + Ki mod 27

## vernam
 

En 1917 Gilbert Vernam propone un cifrador por sustitución binaria con clave de un solo uso (one-time pad) basado en el código Baudot de 5 bits:

-   – La operación de cifra es la función XOR.
    
-   – Usa una secuencia cifrante binaria y aleatoria S
    
-   – El algoritmo de descifrado es igual al de cifrado por la involución de la función XOR.
    
-   – La clave será tan larga o más que el mensaje y se usará una sola vez.

## Maquina enigma
- Usaron los alemanes al fin de WWII

 

## Principios de Kerckhoff

1. Si el sistema no es teóricamente irrompible, al menos debe serlo en la práctica.
2. La efectividad del sistema no debe depender de que su diseño permanezca en secreto.
3. La clave debe ser fácilmente memorizable de manera que no haya que recurrir a notas escritas.
4. Los criptogramas deberán dar resultados alfanuméricos.
5. El sistema debe ser operable por una única persona.
6. El sistema debe ser fácil de utilizar.