# Fabrica digital
Para desarollar el comisionamiento virtual de la linea de producción de baldosas cerámicas se utilizó el software Siemens NX debido a sus capacidades para implementar fisicas realistas, implementar sensores y actuadores, su compatibilidad con diferentes archivos de modelado 3D y su capacidad de comunicarse con softwares externos mediante protocolos de red como lo es OPC.
## Etapas para modelar
Las etapas que se modelaran con un nivel superior de detalle son el prensado que incluye tres maquinas: cargador, prensa y elevador. Y también el embalaje que incluye dos maquinas: apiladora y empacadora. Se eligieron estas etapas debido a la necesidad de interconexión entre ambas.
## Prensado:
Para esta etapa es necesario controlar el movimiento de la prensa y del elevador. La prensa baja cuando esta cargada de polvo ceramico y sube automaticamente. Para el elevador es necesario detectar que las piezas conformadas estan en la base de la prensa y que el molde esta a cierta latura para que el elevador desposite las piezas en las bandas transportadoras sin chocar con el molde.
## Embalaje:
Para esta etapa se deben ingresar un número concreto de baldosas a la maquina para poder apilarlas y enviarlas a la empacadora. En la empacadora es necesario contar también con las cajas para empacar las pilas de baldosas. Una vez salen las cajas de baldosas estan sales hasta un punto en donde son detectadas por la celda de manufactura robotizada.
