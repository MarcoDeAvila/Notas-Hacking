# ReadMyCert
## Objetivo

How about we take you on an adventure on exploring certificate signing requestsTake a look at this CSR file [here](https://artifacts.picoctf.net/c/421/readmycert.csr).
## Solución

```shell
┌──(kali㉿kali)-[~/picoCTF/Cryptography]
└─$ cat readmycert.csr 
-----BEGIN CERTIFICATE REQUEST-----
MIICpzCCAY8CAQAwPDEmMCQGA1UEAwwdcGljb0NURntyZWFkX215Y2VydF8zYWE4
MDA5MH0xEjAQBgNVBCkMCWN0ZlBsYXllcjCCASIwDQYJKoZIhvcNAQEBBQADggEP
ADCCAQoCggEBAN1PdpW4sKum7AhFubDl86sflki20dWKkZ/iZBYYX/RYqZIWm9ve
pdfwkeiDdz7KriPzM9tTDuJm1kWv8/3AxHrYwliFHK0lsmUYdOcPfrvlh6SIuZwH
vxhrR0DJ0+W5vU+4j9G/hk2+JLMURh8WZadwBhRcfIxk97OXujjvHS9KplMAs5ul
cSSQcv77QkIcxVg1OSDVZoEjTr131g+/Jox3T+uFPEvzF9iq03JMU39oqfGaFL02
EQTaTl8efLIDkGxrKCc+Jhn4e1mD+9UlUmIn9nsOBCYNrnfq4usAL10ZPMDty2Sx
yVTl0171trvCA9DF5PRG6eMYirJOmF18oSUCAwEAAaAmMCQGCSqGSIb3DQEJDjEX
MBUwEwYDVR0lBAwwCgYIKwYBBQUHAwIwDQYJKoZIhvcNAQELBQADggEBAMa7s/l3
mAwJi7LsosPS6/VlZwfTdiJAv+WOKN9T1q2JRHsAGRrW9Gz5p7nSBKJxevRaOMwn
XWK0HqmN3y2/lor50jWzqLhM4TnbKsakXnEIo90XgHoy+n0DL0296Lg/xoXrRgrh
2o3rtZTc+irqUzTRM7Q1F76LNmgtEXqvbOm6Gx2dASPhVAAfylRBCTyz2dYwg2vM
kwt4e5bTvpze/xyTyI8Pydq09YYJe0+a2cHSgcoyGoWXjIK4CUxjBNXAFxSPCcS3
5JRkBnyGo+KL+XtuK9yCX7xBFkwLybK7Mj4TeGiwDsR/0SwqyWGb7Q2m58ay8RVm
pmAIEs21M3236Z4=
-----END CERTIFICATE REQUEST-----
                                                                                               
┌──(kali㉿kali)-[~/picoCTF/Cryptography]
└─$ 
```

Use cyberchef para decodificar este texto, la bandera se encontraba aquí.

**Bandera:** picoCTF{read_mycert_3aa80090}
## Notas adicionales
## Referencias

[From Base64 - CyberChef (gchq.github.io)](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=TUlJQ3B6Q0NBWThDQVFBd1BERW1NQ1FHQTFVRUF3d2RjR2xqYjBOVVJudHlaV0ZrWDIxNVkyVnlkRjh6WVdFNA0KTURBNU1IMHhFakFRQmdOVkJDa01DV04wWmxCc1lYbGxjakNDQVNJd0RRWUpLb1pJaHZjTkFRRUJCUUFEZ2dFUA0KQURDQ0FRb0NnZ0VCQU4xUGRwVzRzS3VtN0FoRnViRGw4NnNmbGtpMjBkV0trWi9pWkJZWVgvUllxWklXbTl2ZQ0KcGRmd2tlaURkejdLcmlQek05dFREdUptMWtXdjgvM0F4SHJZd2xpRkhLMGxzbVVZZE9jUGZydmxoNlNJdVp3SA0KdnhoclIwREowK1c1dlUrNGo5Ry9oazIrSkxNVVJoOFdaYWR3QmhSY2ZJeGs5N09YdWpqdkhTOUtwbE1BczV1bA0KY1NTUWN2NzdRa0ljeFZnMU9TRFZab0VqVHIxMzFnKy9Kb3gzVCt1RlBFdnpGOWlxMDNKTVUzOW9xZkdhRkwwMg0KRVFUYVRsOGVmTElEa0d4cktDYytKaG40ZTFtRCs5VWxVbUluOW5zT0JDWU5ybmZxNHVzQUwxMFpQTUR0eTJTeA0KeVZUbDAxNzF0cnZDQTlERjVQUkc2ZU1ZaXJKT21GMThvU1VDQXdFQUFhQW1NQ1FHQ1NxR1NJYjNEUUVKRGpFWA0KTUJVd0V3WURWUjBsQkF3d0NnWUlLd1lCQlFVSEF3SXdEUVlKS29aSWh2Y05BUUVMQlFBRGdnRUJBTWE3cy9sMw0KbUF3Smk3THNvc1BTNi9WbFp3ZlRkaUpBditXT0tOOVQxcTJKUkhzQUdSclc5R3o1cDduU0JLSnhldlJhT013bg0KWFdLMEhxbU4zeTIvbG9yNTBqV3pxTGhNNFRuYktzYWtYbkVJbzkwWGdIb3krbjBETDAyOTZMZy94b1hyUmdyaA0KMm8zcnRaVGMraXJxVXpUUk03UTFGNzZMTm1ndEVYcXZiT202R3gyZEFTUGhWQUFmeWxSQkNUeXoyZFl3ZzJ2TQ0Ka3d0NGU1YlR2cHplL3h5VHlJOFB5ZHEwOVlZSmUwK2EyY0hTZ2NveUdvV1hqSUs0Q1V4akJOWEFGeFNQQ2NTMw0KNUpSa0JueUdvK0tMK1h0dUs5eUNYN3hCRmt3THliSzdNajRUZUdpd0RzUi8wU3dxeVdHYjdRMm01OGF5OFJWbQ0KcG1BSUVzMjFNMzIzNlo0PQ)