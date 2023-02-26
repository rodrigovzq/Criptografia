# PKI - Administracion de claves asimetricas
crear un PKI con XCA -> kali
como saber que una clave publica sea legitima? con pki
repartir claves publicas de forma segura
- Anuncio publico: anunciar la clave
	- debilidad: cualquiera puede enviar un maail con esa
- **Directorio publico**
	- debe ser confiable
	- no es escalable
	- unico punto de falla
	- deberia estar autenticado
- **Autoridad de claves publicas**
	- un tercero que da confianza -> A y B confian en la autoridad
	- requiere que los usuarios conozcan la clave de la autoridad
	- A y B obtienen sus claves comunicandose con la autoridad
	- ![[Pasted image 20220520194331.png]]
	- certificad =archivo encriptado con la clave de autoridad
	- con un certificado hecho por la autoridad, no hace falta preguntarle la clave a la autoridad
	- ![[Pasted image 20220520194950.png]]
	- Los certificados tienen vencimientos
		- por si se necesita actualizar algoritmo
		- por si se comprometio informacion y se necesita renovar
		- 1 año para personas
	- Certificado
		- contiene identidad
		- nro de serie
		- periodo de validez
		- derechos de uso
		- puede ser verificado por cualquiera

## Infraestructura de clave publica PKI

- registracion
- emision de certificados
- Cada entidad tiene autoridad certificantes
	- AFIP
	- empleadores para recibo de sueldo
- Usos
	- login
	- identificador de interlocutor
	- garantida de no repudio
		- si hiciste una operacion, no podes negar que la hiciste
- Norma CCITT X.500 
- Time stamp protcol
	- Una stampa con la fecha actual
- Modelo simple de PKI
- ![[IMG_66B415647CE1-1.jpeg]]
- CA: Autoridad  Certificante
- Recuperacion de claves en PKI -> es que conoce la clave
	- es una vulnerabilidad mas
## Certificados digitales
![[IMG_65181D4031B0-1.jpeg]]
