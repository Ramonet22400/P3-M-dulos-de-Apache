## P3: Módulos de Apache 

### 1. Añade en tu servidor el módulo mod_info y explique para que se utiliza este plugin.

*Este módulo nos va a permitir ver la información de nuestro servidor de forma remota a través de una página HTML.*

En esta imagen podemos ver los modúlos que vienen por defecto y estan isntalados en el apache2.

![image](https://user-images.githubusercontent.com/113515330/200918175-d0f537af-53fc-4bb1-ab98-7e8b224aec23.png) 

Gracias al comando "ls /etc/apache2/mods-available", podemos ver el mod_info.

![image](https://user-images.githubusercontent.com/113515330/200918645-dc50052d-cab0-4edd-abce-2dd04cb1c073.png)

Y mediante el siguiente comando lo habilitaremos en el apache2

![image](https://user-images.githubusercontent.com/113515330/200919012-b3bd305b-5962-4f62-8e38-ebc097be160a.png)

Volvemos a ver los mods habilitados y vemos que info a sido habilitado correctamente.

![image](https://user-images.githubusercontent.com/113515330/200919316-098ca20d-cc45-44ab-8af2-a13bc97315ab.png)


### 2. Oculta la versión del sistema y sistema de apache.

*Esto es interesante de hacer ya que previene dar información sobre nuestro servidor y sistema, un capa de seguridad digamos*

Primero de todo accederemos a security.conf, en donde están las dos características. 

![image](https://user-images.githubusercontent.com/113515330/200922651-50f3cc16-90ed-47b1-aa9e-974085bbfbce.png)

Una vez dentro cmabiaremos su configuración, aplicando los siguientes cambios: 

![image](https://user-images.githubusercontent.com/113515330/200922967-7bde31f5-0b61-4a27-bbf2-1a47dcc8894e.png)

Guardaremos y reinicamos el servidor Apache: sudo service apache2 restart
