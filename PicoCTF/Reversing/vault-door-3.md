# vault-door-3
## Objetivo

This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/943ea40e3f54fca6d2145fa7aadc5e09/VaultDoor3.java)
## Solución

```js
var password = "jU5t_a_sna_3lpm18g947_u_4_m9r54f";
var i;
var buffer = Array(32);
for (i=0; i<8; i++) {
	buffer[i] = password.charAt(i);
}
for (; i<16; i++) {
	buffer[i] = password.charAt(23-i);
}

for (; i<32; i+=2) {
	buffer[i] = password.charAt(46-i);
}

for (i=31; i>=17; i-=2) {
	buffer[i] = password.charAt(i);
}
console.log("picoCTF{" + buffer.join("") + "}");
```

Tuve que hacer un script en JavaScript para poder descifrar la contraseña meramente proporcionada.

**Bandera:** picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_79958f}
## Notas adicionales
## Referencias