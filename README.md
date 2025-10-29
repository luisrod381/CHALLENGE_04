# CHALLENGE_04
Durante la clase creamos unos scripts de movimientos simples usando el Unity Input System package que contrario al input system antiguo que verificaba si una tecla se habia presionado cada frame, el Sistema
nuevo esta basado en eventos y el mapeo de teclas a sus acciones correspondientes dadas por un Input Map. Ademas, este es mucho mas portatil y modular, permitiendo diferentes tipos de Input.

1. Input Matrix
-----------------------------------------------------------------------------------------------------
|Action Mappings          |                                                                          |
-----------------------------------------------------------------------------------------------------
|Horizontal movement      |                                       A and D keys, Left and Right arrows|
-----------------------------------------------------------------------------------------------------
|Vertical movement        |                                       W and S keys, Up and Down arrows   |
-----------------------------------------------------------------------------------------------------
|Shoot                    |                                       Left click mouse                   |
-----------------------------------------------------------------------------------------------------
|Jump                     |                                       Spacebar, double jump possible     |
-----------------------------------------------------------------------------------------------------
|Look                     |                                       Mouse, Joystick                    |
-----------------------------------------------------------------------------------------------------
|Fast horizontal movement |                                       Left Shift                                   |
-----------------------------------------------------------------------------------------------------
|Fast vertical movement   |                                       Left Shift                                   |
-----------------------------------------------------------------------------------------------------

En nuestro sistema de Inputs para hacer el salto cada vez que el jugador presiona la Tecla de Espacio (Tecla asignada al salto) se llama el metodo de OnJump, este mantiene un record de la cantidad de 
saltos que tiene el jugador, si es mayor que 0, le da update a una variable yValue donde cada frame se le sube al jugador la posicion en Y usando yValue*Time*deltaTime. Despues, para similar el descenso,
se le baja la variable y el jugador empieza a perder velocidad para que descienda de manera fluida. Luego de tocar el piso se active el OnTriggerEnter que resetea la cantidad de saltos que le quedan el jugador a 2.
En adicion, asignamos a Left Shift la accion de rapid movement, parecido a un dash. Esto permite al jugador hacer un Sprint al presionar la Tecla y hasta sortarla.

2. Gif usando todos los scripts de movement ya hechos en clase y el PlayerJump que hicimos y cambios al de PlayerMovement para permitir fast movement.

![ca40666474466f7e4b383feb2f41e5ae](https://github.com/user-attachments/assets/1241e4b5-40a8-4ff0-bcc9-82dc90aa176e)

<img width="617" height="375" alt="image" src="https://github.com/user-attachments/assets/b2fd5af9-eada-4cd9-b25b-db3601e983e5" />
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/e9020e2e-bf5a-4012-967a-0237455e08ce" />
<img width="600" height="200" alt="image" src="https://github.com/user-attachments/assets/eddb931a-b29f-452b-a61b-5c3b0ea8b17f" />


Este gif es lo mismo que el pasado, solo demostrando el player usando los visual scripts en vez de los scripts regulares de CSharp, usamos ya los que hemos hecho en clase y el que nosotros añadimos de PlayerJump.

3. Gif usando todos los visual scripts de movement ya hechos en clase y el visual script de PlayerJump que hicimos.

![b479755209b51fbfa0c0b1534bc7c8e5](https://github.com/user-attachments/assets/82c9b230-73b3-4766-beb5-e75bda6eb211)

<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/64a5b955-4529-44a9-a9ee-f0349fbbd3b4" />
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/9624902a-9b68-4aad-b1b6-cd927ff216a0" />
