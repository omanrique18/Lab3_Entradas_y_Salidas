# Lab3_Entradas_y_Salidas
## WorkObject

Se reutiliza el workobject y la rutina de movimiento del repositorio [Lab2_Robotica_de_Desarrollo](https://github.com/omanrique18/Lab2_Robotica_de_Desarrollo.git), realizando pequeños ajustes como la orientación de la herramienta al momento de iniciar la rutina de dibujo de las letras JO y el cambio de la ubicación del workspace paralela al suelo. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/194682884-dbbdc21f-4722-4ad8-b42f-79a7f03121ab.jpeg" width="350" />
</p>

## Rutina de mantenimiento

Se propone una rutina de mantenimiento en la cual el robot gira su primer articulación lara ubicarse cerca de las mesas y gira la articulación 5 hacia arriba para facilitar el montaje y desmontaje de herramientas.

## Declaración de entradas y salidas

Para crear entradas y salidas en RobotStudio nos dirigimos a la pestaña de configuraciones I/O del controlador y en la ventana __Signal__ se crean 3 señales digitales, dos de tipo _Digital Input_ y una de tipo _Digital Output_.

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/194682920-6c222031-4545-4b53-8bf5-13e0d57bc474.jpeg" width="350" />
</p>

### Entradas digitales

Se tienen 2 entradas correspondientes a dos botones push, nombradas en el entorno de RobotStudio de la siguiente forma:
- __Entrada1__: Botón verde de la esquina superior derecha del tablero de control.
- __Entrada2__: Segundo botón verde de derecha a izquierda.

## Salida digital

La salida digital que se usa es una bombilla de señalización verde, la cual se nombra como __Salida1__.

## Simulación

Para la simulación en RobotStudio se crea una nueva lista de usuario con las dos entradas y la salida declaradas en forma de botones, de modo que el usuario puede simular los botones y la bombilla físicas.

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/194683079-1ac27a3c-7b6a-4c29-84af-a13af50e8942.jpeg" width="350" />
</p>

[![Alt text](https://img.youtube.com/vi/gXlmvXHTyYI/0.jpg)](https://youtu.be/gXlmvXHTyYI)

## Rutina principal

Se plantea la siguiente rutina: 
1. El robot se dirige a Home (pose __q=[0 0 0 0 30 0]__).
2. El programa espera a que el primer botón sea presionado para encender la bombilla de señalización e iniciar la rutina de dibujo de las letras JO, pasando por un punto intermedio para evitar errores en el programa. Al finalizar la rutina de dibujo, el robot vuelve a home.
3. El programa espera a que el segundo botón sea presionado para apagar la bombilla e iniciar la rutina de mantenimiento.
4. Fin del programa.

<p align="center">
  <img src="https://user-images.githubusercontent.com/51519737/194682930-c5c0a08e-d7f8-4a3c-aa7b-3f71c446a32a.jpeg" width="350" />
</p>

## Resultados

Se cambia el nombre de las Entradas y salidas en el código para que correspondan a los nombres predeterminados de los elementos del tablero de control en el FlexPendant de la siguiente forma:
- __Entrada1__: _DI_01_
- __Entrada2__: _DI_02_
- __Salida1__: _DO_01_

A continuación se muestra la puesta en escena de la rutina propuesta:

[![Alt text](https://img.youtube.com/vi/aS6jAE1T6fY/0.jpg)](https://youtu.be/aS6jAE1T6fY)

## Integrantes
- Juan Andres Bueno Hortua
- Oscar Javier Manrique Merchan

## Profesores
- Ricardo Emiro Ramirez Heredia
- Jhoan Sebastian Rodriguez Rodriguez
