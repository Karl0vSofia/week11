<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MindAR Face Mask</title>
    <script src="https://mindar-frontend-sdk.oss-cn-shenzhen.aliyuncs.com/2.0.1/mind.ar.js"></script>
    <script src="https://threejs.org/build/three.js"></script>
</head>
<body>
    <!-- MindAR canvas -->
    <script src="https://mindar-frontend-sdk.oss-cn-shenzhen.aliyuncs.com/2.0.1/mind.ar-sdk.js"></script>
    <script>
        MindAR.init({
            type: '3d',
            canvas: MindAR.createCanvas()
        });

        // // 
var maskTexture = new THREE.TextureLoader().load('path/to/your/face-mask.png');
var maskMaterial = new THREE.MeshBasicMaterial({ map: maskTexture, transparent: true, side: THREE.DoubleSide });
var maskGeometry = new THREE.PlaneGeometry(1, 1); // Задайте розміри маски
var maskMesh = new THREE.Mesh(maskGeometry, maskMaterial);
scene.add(maskMesh); 


        // Запустіть MindAR
        MindAR.start();
    </script>
</body>
</html>
