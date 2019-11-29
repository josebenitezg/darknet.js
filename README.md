# Darknet.JS
Basado en el repositorio de https://github.com/bennetthardwick/darknet.js

## Instalación
You can install darknet with npm using the following command:
```
npm install intuitivo_cv
```
Si deseamos incorporar GPU y CuDNN...
```
export DARKNET_BUILD_WITH_GPU=1
export DARKNET_BUILD_WITH_CUDNN=1
npm rebuild darknet
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
