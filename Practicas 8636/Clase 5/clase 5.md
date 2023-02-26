# Intrusion Prevention System / Intrusion Detection System

Se diferencian entre activos y pasivos
- Pasivos detecta y alertan -> IDS
- Activos: bloquean -> IPS

IPS llega hasta capa de aplicacion (desde la fisica)


- **exploit**: Porcion de codigo que permite la explotacion de los pilares de la seguridad
- **vulnerabilidad 0-day**: exploits que no poseen un parche al salir.
- Los IPS podrian prevenir los 0-day si conocieran los exploit


## opciones de IPS
### Detras del firewall

![[Pasted image 20220425202742.png]]
### Delante al firewall
![[Pasted image 20220425202921.png]]
Tiene mas latencia que el anterior pero se usa mucho porque se lo contrata desde el ISP y él lo pone desde tu infraestructira

### Al costado del firewall
![[Pasted image 20220425203029.png]]
Es mas cercano a un IDS

# Honey Pot 🍯
Señuelo con el fin de atraer ciber-delincuentes, poder investigarlos y detectarlos. Un honey pot no tiene funcion util.
**Categorizacion**
- Produccion: desvia el ataque
- Investigacion: recolectar informacion para identificar herramientas y acciones de los ciberdelincuente con el fin de mejorar la infraestructura de la organizacion
- tengo hambre

**Ejemplos**
- Archivo robots.txt: tiene las siguientes lineas para evitar que por ej no se indexe en google.
- ![[Pasted image 20220425203841.png]]
- Podes poner referencias falsas para saber si alguien entra, es por culpa de haber accedido al robots porque esa informacion no esta en otro lado.
- el /admins podria ser falso y en el robots especifique que ahi no queria que entren, entonces si alguien entra al /admins de mi pagina (que es falso) lo puedo bloquear automaticamente porque sé que es un atacante.
- 
