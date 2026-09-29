# Tarea2_PSP

## Instalación Docker en Debian



#### - Desinstalamos paquetes conflictivos
<img width="1920" height="363" alt="imagen" src="https://github.com/user-attachments/assets/96d643d8-7bb5-40aa-be64-7406516d3fc7" />


#### - Configuramos el repositorio apt de Docker 
<img width="1842" height="642" alt="imagen" src="https://github.com/user-attachments/assets/bbee630d-25e2-429d-a5c6-0ae5403c739e" />
<img width="701" height="309" alt="imagen" src="https://github.com/user-attachments/assets/8e534200-6111-4803-9c67-91927ee4dff5" />


#### - Instalamos Docker
<img width="1882" height="882" alt="imagen" src="https://github.com/user-attachments/assets/5f929fd8-2434-4a29-80d5-d135db830ae0" />
<img width="997" height="313" alt="imagen" src="https://github.com/user-attachments/assets/41d061e2-a4f4-49c8-9c25-3a62bc131d86" />


#### - Comprobamos que está activo
<img width="1920" height="530" alt="imagen" src="https://github.com/user-attachments/assets/2b3a94a7-9ab3-4981-897a-dfc676bd18be" />


#### - Verificamos la instalación
<img width="770" height="496" alt="imagen" src="https://github.com/user-attachments/assets/1a9d450a-71f8-49a3-a003-908b0d399f68" />



#### - Instalamos Alpine sin arrancarlo
<img width="811" height="318" alt="imagen" src="https://github.com/user-attachments/assets/2138e815-c5d9-4e32-9094-f58a6263ce95" />


#### - Creamos un contenedor sin nombre y sin arrancarlo
<img width="1199" height="203" alt="imagen" src="https://github.com/user-attachments/assets/98228646-c822-4fad-8735-a81167e8f362" />

*Queda en estado Created, existe pero no está en ejecución

#### - Creamos y arrancamos dam_alp1 con shell
<img width="1199" height="471" alt="imagen" src="https://github.com/user-attachments/assets/1e9c8113-e9ab-458e-b084-398db5b2cd3c" />

* Necesitamos -i y -t. Sin -i no puedes escribir y sin -t no tienes una terminal interactiva

#### - Dejamos dos contenedores en marcha
<img width="1199" height="248" alt="imagen" src="https://github.com/user-attachments/assets/a59df4f6-149a-4d15-a72e-48ae5e1e3bfe" />
 
 * Control P + Control Q para salir sin pararlo *

#### - Averiguamos las ip desde fuera
<img width="946" height="93" alt="imagen" src="https://github.com/user-attachments/assets/b831574f-eb7a-4dda-8c9b-3cae0e585647" />


#### - Hacemos IP de ambos contendores
<img width="586" height="420" alt="imagen" src="https://github.com/user-attachments/assets/b1d598c1-ec2e-4f82-9d98-872934c7da38" />

* Por IP funciona pero por nombre falla *

#### - Salimos de ambos con exit

<img width="941" height="95" alt="imagen" src="https://github.com/user-attachments/assets/b47fedb6-802a-4a22-b8b9-ba69474151f3" />
<img width="1203" height="305" alt="imagen" src="https://github.com/user-attachments/assets/e2414ef9-7b7f-46c1-a8af-f23be91337a3" />

* Al salir con exit termina el proceso, así que el contenedor se para pero no se elimina. Al repetir docker stats la tabla sale vacía porque solo muestra contenedores en ejecución *


#### - Ocupación del disco

<img width="1920" height="948" alt="imagen" src="https://github.com/user-attachments/assets/0cf64e5e-4322-4202-bd22-d258a468d68e" />

*Distingue las filas Images y Containers,

Imágenes ==> ocupa lo que pesa Alpine más hello-world de la instalación. Si varios contenedores salen de la misma imagen sus capas se comparten y solo se cuentan una vez
Contenedores ==> ocupan casi nada, porque solo guardan su capa de escritura, y no he escrito nada. Los parados siguen ocupando sitio hasta que se eliminen










