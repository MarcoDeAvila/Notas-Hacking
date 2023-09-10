# Level 15-16
## Objetivo

The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit15
> **Password:** jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit15@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit15@bandit.labs.overthewire.org's password:
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  9 01:47:01 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  9 01:47:01 2023 GMT
verify return:1
---
Certificate chain
---
Server certificate
-----BEGIN CERTIFICATE-----
...
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: E12C754F899AB9E1775DDB97915E6203C9FDE484EC0FCC8E223A7B4AB4FE66D3
    Session-ID-ctx:
    Resumption PSK: 
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
...
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```

**Password encontrado:** JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Notas adicionales

| Comando | Descripción |
|-|-|
| s_client| El comando **s_client** implementa un cliente SSL/TLS genérico que se conecta a un host remoto mediante SSL/TLS.|
## Referencias

[/docs/man1.0.2/man1/openssl-s_client.html](https://www.openssl.org/docs/man1.0.2/man1/openssl-s_client.html)