# Celda Robotizada

## Prototipo de layout
![image](https://github.com/EdoCuadros/APM-ProyectoIntegrador/assets/69473568/f714995e-361f-49ae-90cd-6ea02d37029d)

## Requerimientos del robot

### Masas soportadas
Teniendo en cuenta los productos seleccionados y sus correspondientes dimensiones se realizó la siguiente tabla con valores como densidad, área de baldosa, masa unitaria y masa total de la caja.

|      Baldosa     | Ancho [cm] | Largo [cm]  | Espesor [cm] | Área [cm^2] | Densidad [g/cm^3] | Masa unitaria  [kg] | Masa total de caja [kg] |
|:----------------:|:----------:|:-----------:|:------------:|:-----------:|:-----------------:|:-------------------:|:-----------------------:|
|    Gres simple   |     30     |      30     |     0.95     |     3600    |        1.92       |        6.5664       |         39.3984         |
|    Gres pulido   |     30     |      30     |     0.95     |     3600    |        1.92       |        6.5664       |         39.3984         |
| Gres tecnificado |     30     |      30     |     0.95     |     3600    |        1.92       |        6.5664       |         39.3984         |


### Rutina del robot
La rutina del robot incluye la ubicación de las cajas de baldosas en el palet y también la ubicación del palet vacío en una banda transportadora cada vez que se llena la anterior.
La rutina inicia con el PLC dando la señal al robot de que la posición está libre para ubicar un nuevo palet, el robot recoge el palet de un dispensador. Lugar donde los trabajadores de la empresa llevan las estibas luego de usarlas. Este es el lugar donde un humano estará más cerca del robot en un funcionamiento normal, por lo que se tienen sensores de cercanía en esta posición para que el robot detenga su movimiento en presencia de una persona por cuestiones de seguridad. 

Una vez que el robot ubicó la estiba en la banda transportadora de salida, queda esperando la señal del PLC que le diga que hay una caja de baldosas en una posición de recogida, ya que el robot no cuenta con visión. Dentro de la programación del robot se tienen las ubicaciones que tendrán las cajas en la estiba, las cuales el robot irá rellenando para completar cada nivel. 

![image](https://github.com/EdoCuadros/APM-ProyectoIntegrador/assets/69473568/38d76166-22db-42b4-9cf4-874020c48b55)

Al estar utilizando una estiba de dimensiones 1 x 1.2 metros de área, solo es posible tener 6 cajas de baldosas por nivel. Se decidió posicionar las baldosas horizontalmente debido a que su centro de gravedad es bajo y no hay posibilidad de que caigan. Contrariamente con la ubicación vertical, que puede dar espacio para más cajas por nivel pero con riesgo de caída. La estiba se llena con 8 niveles. Una vez el robot sabe que llenó la estiba, da la señal al PLC para que inicie el funcionamiento de la banda transportadora que lleva la estiba llena a otra ubicación, ya sea de transporte o almacenamiento. Una vez que la banda ha llevado a la estiba fuera de la celda robotizada, se le manda la señal al robot para que vuelva a ubicar otra estiba y se inicie el procedimiento de nuevo.

### Video

En el siguiente video se pueden observar los movimientos detalladados anteriormente.

https://drive.google.com/file/d/10fq71gCOpTh7L4pjiUI0Q3WhzutRpyB9/view?usp=sharing

