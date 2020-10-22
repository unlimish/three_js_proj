# three_js_proj

Three.js Template
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <script src="./node_modules/three/build/three.min.js"></script>
    <script>
        window.addEventListener('load', init);

        const width = 960;
        const height = 540;

        function init() {
            const renderer = new THREE.WebGLRenderer({
                canvas: document.querySelector('#myCanvas')
            });
            renderer.setSize(width, height);

            const scene = new THREE.Scene();

            const camera = new THREE.PerspectiveCamera(45, width / height, 1, 10000);
            camera.position.set(0, 0, +1000);

            tick();

            function tick() {
                renderer.render(scene, camera);

                requestAnimationFrame(tick);
            }
        }
    </script>
</head>
<body>
    <canvas id="myCanvas"></canvas>
</body>
</html>
```
