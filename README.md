1º El primer error es a la hora de poner la ip en el terminal de visual "ssh alumno@localhost -p 2222" en lugar de @localhost es @127.0.0.1

2º A la hora de copiar la llave debo entrar en alumno@127.0.0.1 y poner este comando()

3º A la hora de crear la llave me seguia pidiendo la contraseña, y era porque no le di permisos al archivo en donde lo cree, entonces puse este comando "chmod 600 ~/.ssh/authorized_keys"

## Captura de la conexión SSH sin contraseña.
![alt text](image.png)