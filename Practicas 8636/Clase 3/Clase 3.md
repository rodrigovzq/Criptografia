Config ip 

![[IMG_F491CF4E2C3E-1.jpeg]]

# Seguridad Perimetral
- Acceso a servicios restringidos
- Escaneo de puertos
- escaneo de vulnerabilidades
- explotacion de vulnerabilidades
- denegacion de servicio
- navegacion irrestricta


## Escaneo de puertos
NMAP: permite escanear la red e identificar los hosts. Ver los puertos de los hosts y puertos disponibles. Puede mostrar servicios default o reales. Puede descubrir vulnerabildiades aunque no es su objetivo

Se usa en el proceso de pentesting

Escaneo con nmap sobre ip de 0wned
![[IMG_1FF4C0C28701-1.jpeg]]

- Escanea 1000
- trabaja con TCP

## Wireshark

![[IMG_67F5528D31B9-1.jpeg]]

- filtrar con ip.addr== (aca poner ip)
- triple handshake de tcp 
	- nmap responde al final con un reset, por eso no establece conexion y logra escanear todos los puertos
### Escaneo mas profundo
![[Pasted image 20220418201424.png]]

## Firewall
Controla las comunicaciones, permitiendola o prohibiendolas segun las politicas de seguridad

### Firewall de red
![[Pasted image 20220418202607.png]]
El firewall establece politicas, permisivas o restricticas

**Tipos**
- El firewall de host permite que ingresen o egresen a un host determinado. Se encuentra instalado y confiurado dentro del host a proteger
- Firewall de hardware y de software
- Por generacion
	- 1ra gen o stateless: son aquellos que nicamente van a estar analizando la ip 
	- 2da gen o statefull: se le agrega el estado de la conexion
	- ![[Pasted image 20220418203341.png]]
### UTM
Agrega al firewall multiples funcionalidades, estan apuntados a pymes. Reune features en un solo aparato

### NGFW
NExt generation firewall, agrega funcionalidades y tiene mayor throughput que un UTM. Estan apuntados a empresas grandes

### DMZ
En la dmz se ubican los servidores de la organizacion que deben permanecer accesibles desde la red exterior
De esta forma si un servicio publciado a internet es comprometido el ciberdelincuente no estara dentro de nuestra LAN interna.

### NAT
Es la conversion de IP a otra IP
![[Pasted image 20220418204037.png]]

### Ejemplo
- Poner firewall de frontera
- dmz con servidor web 
	- firewall entre ese y serv de aplicacion
- Puerto 443 de tcp es el seguro
- Configurar firewall de host de cada pc
- Poner un firweall mas abajo que separa la red interna de servidores con la red de workstation -> evita que cualquier usuario acceda a servicios de gestion
![[Pasted image 20220418205522.png]]
![[Pasted image 20220418205549.png]]

# IP Tables 
![[Pasted image 20220418212142.png]]

condiciones a matechear - destino
Acciones:
- accept 
- drop
- queue
- return
Hay tablas: filtrar, nat, mangle
![[Pasted image 20220418212743.png]]
Si no matchea con ninguna, se aplica la politica de firewall
### ejemplos:
![[Pasted image 20220418213014.png]]
