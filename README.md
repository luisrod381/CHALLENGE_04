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

2. Gif usando todos los scripts de movement ya hechos en clase y el PlayerJump que hicimos.

![ca40666474466f7e4b383feb2f41e5ae](https://github.com/user-attachments/assets/1241e4b5-40a8-4ff0-bcc9-82dc90aa176e)


<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/e9020e2e-bf5a-4012-967a-0237455e08ce" />
<img width="600" height="200" alt="image" src="https://github.com/user-attachments/assets/eddb931a-b29f-452b-a61b-5c3b0ea8b17f" />



2. Gif usando todos los visual scripts de movement ya hechos en clase y el visual script de PlayerJump que hicimos, y cambios al de PlayerMovement para permitir fast movement.

![b479755209b51fbfa0c0b1534bc7c8e5](https://github.com/user-attachments/assets/82c9b230-73b3-4766-beb5-e75bda6eb211)

![2ec1820e-22b0-4be4-b31f-a013694c51f1](https://github.com/user-attachments/assets/7ecf75ac-03f0-4644-baec-6899108fee4c)
![431eb8c8-072b-482c-9637-7fedf55dbfd4](https://github.com/user-attachments/assets/a58d679e-e982-47fc-b870-681ccf3d0551)
