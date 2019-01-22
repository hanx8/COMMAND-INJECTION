En el ejercicio COMMAND INJECTION de DVWA, se tiene el código inicial(COMMAND-INJECTION-INICIAL.txt).


Se ingresa la dirección IP, luego del submit habrá una respuesta como se muestra: 


![image](https://user-images.githubusercontent.com/46895869/51512162-a16b1d00-1dd2-11e9-8eeb-725d8dcc9ee6.png)


El código permite realizar un listado al directorio (dir), luego de escribir el ping:


![image](https://user-images.githubusercontent.com/46895869/51512188-c8295380-1dd2-11e9-8ecc-4fc04e387094.png)


También permite hacer un listado de cierta ruta de un directorio:


![image](https://user-images.githubusercontent.com/46895869/51512223-f5760180-1dd2-11e9-9932-4b7c179a8dce.png)


Para corregir esta vulnerabilidad, se crea un blacklist de dichos caracteres especiales para ser denegados:


![image](https://user-images.githubusercontent.com/46895869/51512253-1c343800-1dd3-11e9-9b92-79370e5d6978.png)


Realizar la misma prueba que se realizó al inicio con el código corregido(COMMAND-INJECTION-FINAL.txt).
Luego de la corrección, verificamos que no permite el listado luego de escribir la dirección IP:


![image](https://user-images.githubusercontent.com/46895869/51512278-3ff77e00-1dd3-11e9-9b28-84e605d35dff.png)


![image](https://user-images.githubusercontent.com/46895869/51512307-5b628900-1dd3-11e9-873d-bb3c65c09cb6.png)


A su vez, si permite el ingreso de la dirección IP, dando como respuesta el ping:


![image](https://user-images.githubusercontent.com/46895869/51512347-851bb000-1dd3-11e9-966b-2d2cc9bb1e17.png)




