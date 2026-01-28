[particle_heart.html](https://github.com/user-attachments/files/24916968/particle_heart.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>粒子爱心</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            overflow: hidden;
            background-color: #000;
        }
        canvas {
            display: block;
        }
    </style>
</head>
<body>
    <canvas id="heartCanvas"></canvas>

    <script>
        const canvas = document.getElementById('heartCanvas');
        const ctx = canvas.getContext('2d');

        let width, height;
        let particles = [];

        // 爱心公式
        function getHeartPoint(t) {
            const x = 16 * Math.pow(Math.sin(t), 3);
            const y = -(13 * Math.cos(t) - 5 * Math.cos(2 * t) - 2 * Math.cos(3 * t) - Math.cos(4 * t));
            return { x, y };
        }

        class Particle {
            constructor() {
                // 1. 计算最终目标位置（爱心形状）
                const t = Math.random() * 2 * Math.PI;
                const heartPoint = getHeartPoint(t);
                
                // 随机分布在心形内部或边缘
                let r = Math.random();
                r = 1 - Math.pow(r - 1, 4); 
                
                // 屏幕中心
                const cx = width / 2;
                const cy = height / 2;
                // 基础缩放
                const scale = Math.min(width, height) / 35; 
                
                // 目标坐标
                this.targetX = cx + heartPoint.x * scale;
                this.targetY = cy + heartPoint.y * scale;
                
                // 加上一点随机偏移，让爱心看起来毛茸茸的
                this.targetX += (Math.random() - 0.5) * 15;
                this.targetY += (Math.random() - 0.5) * 15;

                // 2. 初始位置：全屏随机分布（或者从屏幕边缘进来）
                // 这里设置为全屏随机，营造“散落的星光汇聚”的感觉
                this.x = Math.random() * width;
                this.y = Math.random() * height;

                // 速度/移动参数
                this.vx = 0;
                this.vy = 0;
                // 摩擦力越接近1越滑，越小停得越快。0.94-0.98之间比较平滑
                this.friction = 0.94 + Math.random() * 0.04; 
                // 弹力/吸引力：越小汇聚越慢
                this.ease = 0.005 + Math.random() * 0.01; 

                this.size = Math.random() * 2 + 1;
                
                // 颜色
                const hue = Math.random() * 50 + 320; 
                this.color = `hsla(${hue}, 80%, 60%, ${Math.random() * 0.5 + 0.5})`;
            }

            update() {
                // 简单的缓动跟随：向目标点加速
                const dx = this.targetX - this.x;
                const dy = this.targetY - this.y;

                this.vx += dx * this.ease;
                this.vy += dy * this.ease;

                this.vx *= this.friction;
                this.vy *= this.friction;

                this.x += this.vx;
                this.y += this.vy;
            }

            draw() {
                ctx.fillStyle = this.color;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function init() {
            resize();
            createParticles();
            animate();
        }

        function resize() {
            width = canvas.width = window.innerWidth;
            height = canvas.height = window.innerHeight;
        }

        function createParticles() {
            particles = [];
            const particleCount = 2000; // 增加一点粒子
            for (let i = 0; i < particleCount; i++) {
                particles.push(new Particle());
            }
        }

        function animate() {
            // 拖尾效果稍微淡一点，让移动轨迹更清晰一点，或者深一点让画面干净
            ctx.fillStyle = 'rgba(0, 0, 0, 0.05)'; 
            ctx.fillRect(0, 0, width, height);

            particles.forEach(p => {
                p.update();
                p.draw();
            });

            requestAnimationFrame(animate);
        }

        window.addEventListener('resize', () => {
            resize();
            createParticles();
        });

        init();
    </script>
</body>
</html>
