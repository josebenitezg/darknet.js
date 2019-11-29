# Darknet.JS
Basado en el repositorio de https://github.com/bennetthardwick/darknet.js

## Instalación
Instalar con npm desde el command:
```
npm install intuitivo_cv
```


## Modo de uso

```typescript
  GNU nano 2.5.3                                            File: prueba.js                                                                                                

const { Darknet } = require('intuitivo_cv');
 
const darknet = new Darknet({
  weights: '/home/ubuntu/darknet/data_train/models/yolov3-gondolas_final.weights',
  config: '/home/ubuntu/vending-fridge-api/configuracion.cfg',
  namefile: '/home/ubuntu/darknet/data_train/data/gondolas.names'

});
console.log(darknet.detect('/home/ubuntu/darknet/data_train/prueba.png'));
console.log(darknet.detect('/home/ubuntu/vending-fridge-api/pizza.png'));
```
