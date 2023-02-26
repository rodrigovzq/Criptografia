# Seguridad WEB

OWASP es un tipo de proteccion web
OWASPT TOP !10 para aplicaciones web es el qe vamos a ver
El objetivo es concientizar a los devs de las vulnerabilidades mas criticas de las aplicaciones web. 
Es un estandar de facto en las pentest
![[Pasted image 20220502195318.png]]


# Semana 7

## Perdida de control de acceso
Relacionado con la **autorizacion** -> lo que puedo hacer una vez que me autentiqué
Las restricciones sobre lo que los usuarios autenticados pueden hacer no se aplican correctamente. Los atacantes pueden explotar estos defectos para acceder, de forma no autorizada, a funcionalidades y/o datos, cuentas de otros usuarios, ver archivos sensibles, modificar datos, cambiar derechos de acceso y permisos, etc.

Es una falla en la logica del software
![[Pasted image 20220509195319.png]]
## Entidades XLM
![[Pasted image 20220509202103.png]]
Los interpretadores de XML si son viejos pueden ejecutar codigo y provocar vulnerabilidades. 
No es muy comun de encontrar pero esta en el puesto 4.
## Exposicion de datos sensibles
![[Pasted image 20220509202227.png]]
En ciertas auditorias se pregunta el cifrado en transito y en reposo. 
Aislar transito de datos sensibles del resto de la aplicacion.
## Perdida de Autenticacion
Relacionado con la **identificacion** del usuario mas que la autorizacion. Trata de bypassear las credenciales de autenticacion.

![[Pasted image 20220509203109.png]]
### Fuerza bruta
Es el ataque mas comun, los sistemas no estan preparados para lidiar con este ataque en general.

## Inyeccion
![[Pasted image 20220509211536.png]]
LDAP es una base de datos que se usa para autenticacion -> Active directory es el de microsoft


script Ransomware

- buscar archivos con  extension particular
- cifrar con algoritmo robusto y asimetrico
- borrar de manera segura
- eliminar shadowcopy