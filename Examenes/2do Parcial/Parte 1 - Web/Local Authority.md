# Local Authority
## Objetivo

Can you get the flag?Go to this [website](http://saturn.picoctf.net:49386/) and see what you can discover.
## Solución

```js
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

Cuando se ingresa un usuario y contraseña incorrectos se nos dirige a una pagina donde si inspeccionamos su estructura HTML podemos observar un archivo JavaScript que contiene la función para validad el Password, dicha función muestra los datos correctos para poder hacer login y dar con la bandera. 

**Bandera:** picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}
## Notas adicionales
## Referencias