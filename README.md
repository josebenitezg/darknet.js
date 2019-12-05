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
Para procesar feeds de videos .pm4
Inslatar opencv4nodejs: https://github.com/justadudewhohacks/opencv4nodejs

```const fs = require('fs');
const cv = require('opencv4nodejs');
const { Darknet } = require('darknet');
 
const darknet = new Darknet({
  weights: '/home/ubuntu/darknet/data_train/models/yolov3-gondolas_final.weights',
  config: '/home/ubuntu/vending-fridge-api/configuracion.cfg',
  namefile: ''/home/ubuntu/darknet/data_train/data/gondolas.names'
});
 
const cap = new cv.VideoCapture('video.mp4');
 
let frame;
let index = 0;
do {
  frame = cap.read().cvtColor(cv.COLOR_BGR2RGB);
  console.log(darknet.detect(frame));
} while(!frame.empty);```
