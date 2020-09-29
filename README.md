# ari
https://wiki.asterisk.org/wiki/display/AST/Asterisk+12+Configuration_res_ari

# Configuracion

## Example http.conf
``` 
[general]
enabled = yes
bindaddr = 0.0.0.0
bindport = 8088
``` 

## Example ari.conf
``` 
[general]
enabled = yes
pretty = yes
allowed_origins = localhost:8088,http://ari.asterisk.org
 
[asterisk]
type = user
read_only = no
password = asterisk
 
; password_format may be set to plain (the default) or crypt. When set to crypt,
; crypt(3) is used to validate the password. A crypted password can be generated
; using mkpasswd -m sha-512.
;
[asterisk-supersecret]
type = user
read_only = no
password = $6$nqvAB8Bvs1dJ4V$8zCUygFXuXXp8EU3t2M8i.N8iCsY4WRchxe2AYgGOzHAQrmjIPif3DYrvdj5U2CilLLMChtmFyvFa3XHSxBlB/
password_format = crypt
``` 


