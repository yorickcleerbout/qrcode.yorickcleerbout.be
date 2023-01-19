<template>
    <div class="container">
        <div class="items">
            <input type="text" id="input" :placeholder="placeholder" />
            <button @click="generateQRCode">Generate QR Code</button>
        </div>

        <hr /> 

        <canvas id="canvas"></canvas>

    </div>
  </template>
    
  <script>
  import QrCodeWithLogo from "qrcode-with-logos";
  export default {
    name: 'LogicComponents',
    props: {
        placeholder: String
    },
    methods: {
        generateQRCode() {
            const content = document.getElementById('input').value;

            new QrCodeWithLogo({
                canvas: document.getElementById("canvas"),
                content: content,
                width: 300,
                download: false,
                logo: {
                    src: "https://raw.githubusercontent.com/yorickcleerbout/yorickcleerbout.be/qrcode/src/assets/logo.png",
                    logoSize: 0.2
                }
            }).toImage();
        }
    }
  }
  </script>
  
  <style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap');

    .container {
        width: 35%;
        margin: auto;
        margin-top: 50px;
        
    }
    .items {
        display: flex;
        justify-content: space-between;
    }

    input {
        flex: 4 0 0;
        padding: 10px;
        margin-right: 50px;
        background-color: white;
        border: 2px solid white;
        border-radius: 10px 10px 10px 10px;
    }
    
    button {
        flex: 2 0 0;
        background-color: #db8ed1;
        color: white;
        font-weight: bold;
        font-size: 15px;
        border: 2px solid white;
        border-radius: 50px 50px 50px 50px;
        cursor: pointer;
    }

    hr {
        margin-top: 5vh;
        width: 70%;
        margin: 5vh auto;
    }

    canvas {
        margin-left: 50%;
        transform: translateX(-50%);
        border-radius: 50px 50px 50px 50px;
    }
  </style>
    