# Project_walter

# Proyecto de Demostración de Seguridad en Aplicaciones Web

Este proyecto demuestra los riesgos de seguridad al almacenar credenciales en `localStorage` y otras malas prácticas en el desarrollo de aplicaciones web.

## Problemas de Seguridad y Vulnerabilidades

### Almacenamiento de Credenciales en `localStorage`:

```javascript
localStorage.setItem('username', username);
localStorage.setItem('password', password);
```
###Credenciales debiles
```
if(username === 'admin' && password === 'admin123')
```
###Validación de Login Insegura:
La validación de credenciales se realiza en el lado del cliente, lo cual es muy inseguro. Esto permite a un atacante modificar el script para siempre pasar la validación, independientemente de las credenciales ingresadas.

###Posibilidad de Ataques de Inyección de HTML (HTML Injection):

```
document.body.innerHTML += `<p>Welcome, ${username}!</p>`;
```
Inyectar directamente datos ingresados por el usuario en el DOM sin escape adecuado puede llevar a ataques de inyección de HTML, permitiendo a un atacante inyectar scripts maliciosos.
