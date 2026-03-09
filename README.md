<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ለኔ ልዩ ስጦታ | አፈቅርሻለሁ</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/framer-motion/10.16.4/framer-motion.umd.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Ethiopic:wght@100;400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">
    <style>
        :root {
            --accent: #ff4d6d;
            --bg: #050505;
        }
        body {
            background-color: var(--bg);
            color: #fff;
            font-family: 'Noto Sans Ethiopic', sans-serif;
            overflow: hidden;
            margin: 0;
        }
        .glass {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 32px;
        }
        .text-gradient {
            background: linear-gradient(45deg, #ff4d6d, #ff8fa3, #c9184a);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-size: 200% auto;
            animation: shine 4s linear infinite;
        }
        @keyframes shine {
            to { background-position: 200% center; }
        }
        .floating-dove {
            position: absolute;
            pointer-events: none;
            opacity: 0.15;
            animation: float 10s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            50% { transform: translate(20px, -40px) rotate(5deg); }
        }
        #bg-canvas {
            position: fixed;
            top: 0;
            left: 0;
            z-index: -1;
        }
        .step { display: none; opacity: 0; transform: scale(0.95); transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1); }
        .step.active { display: flex; opacity: 1; transform: scale(1); }
    </style>
</head>
<body>

    <canvas id="bg-canvas"></canvas>

    <main class="relative z-10 min-h-screen flex items-center justify-center p-6 text-center">
        
        <section id="step-1" class="step active flex-col items-center">
            <div class="mb-6 p-5 rounded-full glass border-pink-500/30 animate-bounce">
                <i data-lucide="heart" class="w-10 h-10 text-pink-500 fill-pink-500"></i>
            </div>
            <h2 class="text-lg tracking-[0.3em] uppercase opacity-60 mb-2">ለአንቺ ብቻ የተዘጋጀ</h2>
            <h1 class="text-4xl md:text-6xl font-bold mb-10">አንድ መልዕክት አለኝ...</h1>
            <button onclick="goToStep(2)" class="glass px-12 py-5 text-xl font-semibold hover:bg-white/10 transition-all group overflow-hidden relative">
                <span class="relative z-10 flex items-center gap-3">
                    ክፈቺው <i data-lucide="sparkles" class="w-5 h-5"></i>
                </span>
                <div class="absolute inset-0 bg-gradient-to-r from-pink-500/20 to-transparent translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-700"></div>
            </button>
        </section>

        <section id="step-2" class="step flex-col items-center max-w-2xl">
            <h2 class="text-gradient text-4xl md:text-6xl font-bold mb-8">የኔ ርግብ...</h2>
            <p class="text-xl md:text-2xl leading-loose text-gray-300 font-light italic">
                "በአለም ላይ ብዙ ቆንጆ ነገሮች አሉ፣ ግን ላንቺ ያለኝ ፍቅር ከሁሉም ይበልጣል። በህይወቴ ውስጥ ስላለሽ በየቀኑ እራሴን እንደ እድለኛ እቆጥረዋለሁ።"
            </p>
            <div class="mt-12 flex gap-6">
                <button onclick="goToStep(3)" class="bg-white text-black px-10 py-4 rounded-full font-bold hover:scale-105 transition-transform">
                    ቀጥይ...
                </button>
            </div>
        </section>

        <section id="step-3" class="step flex-col items-center w-full max-w-4xl">
            <div class="glass p-10 md:p-20 relative overflow-hidden w-full border-pink-500/20">
                <div class="absolute top-0 right-0 p-8 opacity-20">
                    <i data-lucide="bird" class="w-32 h-32 text-white"></i>
                </div>
                
                <h1 class="text-6xl md:text-9xl font-black mb-8 tracking-tighter">አፈቅርሻለሁ 🥰</h1>
                <p class="text-2xl text-pink-300 mb-12 font-medium">አንቺ የኔ አለም ነሽ!</p>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <div class="glass p-6 bg-white/5">
                        <h4 class="text-pink-400 font-bold mb-2">ልዩ ነሽ</h4>
                        <p class="text-sm opacity-70">ከውስጥም ከውጭም የምታበሪ ውድ ስጦታዬ።</p>
                    </div>
                    <div class="glass p-6 bg-white/5">
                        <h4 class="text-pink-400 font-bold mb-2">ምርጫዬ</h4>
                        <p class="text-sm opacity-70">ሁሌም ቢሆን ድጋሚ የምመርጥሽ አንቺኑ ነው።</p>
                    </div>
                    <div class="glass p-6 bg-white/5">
                        <h4 class="text-pink-400 font-bold mb-2">ነገዬ</h4>
                        <p class="text-sm opacity-70">የወደፊት ህይወቴን ካንቺ ውጪ ማሰብ አልችልም።</p>
                    </div>
                </div>

                <div class="mt-12 flex justify-center gap-4">
                     <div class="p-3 glass rounded-full animate-pulse"><i data-lucide="heart" class="text-pink-500"></i></div>
                     <div class="p-3 glass rounded-full animate-pulse" style="animation-delay: 0.2s"><i data-lucide="heart" class="text-pink-400"></i></div>
                     <div class="p-3 glass rounded-full animate-pulse" style="animation-delay: 0.4s"><i data-lucide="heart" class="text-pink-300"></i></div>
                </div>
            </div>
        </section>

    </main>

    <script>
        // Initialize Icons
        lucide.createIcons();

        // Navigation Control
        function goToStep(stepNumber) {
            document.querySelectorAll('.step').forEach(s => {
                s.classList.remove('active');
            });
            setTimeout(() => {
                document.getElementById(`step-${stepNumber}`).classList.add('active');
            }, 100);
        }

        // Particle Background Logic
        const canvas = document.getElementById('bg-canvas');
        const ctx = canvas.getContext('2d');
        let particles = [];

        function resize() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }

        window.addEventListener('resize', resize);
        resize();

        class Particle {
            constructor() {
                this.reset();
            }
            reset() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 3 + 1;
                this.speedX = Math.random() * 0.5 - 0.25;
                this.speedY = Math.random() * 0.5 - 0.25;
                this.opacity = Math.random() * 0.5;
            }
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                if(this.x < 0 || this.x > canvas.width) this.speedX *= -1;
                if(this.y < 0 || this.y > canvas.height) this.speedY *= -1;
            }
            draw() {
                ctx.fillStyle = `rgba(255, 77, 109, ${this.opacity})`;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function init() {
            for(let i = 0; i < 80; i++) particles.push(new Particle());
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach(p => {
                p.update();
                p.draw();
            });
            requestAnimationFrame(animate);
        }

        init();
        animate();
    </script>
</body>
</html>
