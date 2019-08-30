QRLogo

QRLogo is a Node package developed to allow for the creation of QR codes with embedded logo images.


## Installation

Use node package manager ([npm](https://www.npmjs.com/get-npm)) to install  install QRLogo.

```bash
npm install --save qrlogo
```

## Saving as PNG

```node
const QRLogo = require('qrlogo');

const data = JSON.stringify({name: "Zacharie Happel",
              job:  "Student/Intern", 
              grade: "Senior"
})
 
await QRLogo.createQRWithLogo(data, "logo.png", {}, "PNG", "qrlogo.png") 

```
## Base64 

```node
const QRLogo = require('qrlogo');

const data = JSON.stringify({name: "Zacharie Happel",
              job:  "Student/Intern", 
              grade: "Senior"
})
 
await QRLogo.createQRWithLogo(data, "logo.png", {}, "Base64", "qrlogo.png") 

```



## Information 
QRLogo currently only supports saving images as PNG and the exportation of Base64 formatted data. 

 [qrcode](https://www.npmjs.com/package/qrcode) to facilitate the creation of the QR codes, and the [sharp](https://www.npmjs.com/package/sharp) npm package as the means to which images are overlaid. 

qrcode [options](https://www.npmjs.com/package/qrcode#example-1)  may be included when creating the QR code image:

```node
const opts = {
   errorCorrectionLevel:'H',
   rendererOpts: { quality: 0.3 }
}; 

```
## License
[MIT](https://choosealicense.com/licenses/mit/)