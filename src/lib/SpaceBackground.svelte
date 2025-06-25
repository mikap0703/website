<!-- SpaceBackground.svelte -->
<div class="space-background">
	<!-- Stars -->
	<div class="star" style="width: 2px; height: 2px; top: 10%; left: 20%;"></div>
	<div class="star" style="width: 1px; height: 1px; top: 20%; left: 80%;"></div>
	<div class="star" style="width: 2px; height: 2px; top: 30%; left: 60%;"></div>
	<div class="star" style="width: 1px; height: 1px; top: 40%; left: 30%;"></div>
	<div class="star" style="width: 2px; height: 2px; top: 50%; left: 90%;"></div>
	<div class="star" style="width: 1px; height: 1px; top: 60%; left: 10%;"></div>
	<div class="star" style="width: 2px; height: 2px; top: 70%; left: 70%;"></div>
	<div class="star" style="width: 1px; height: 1px; top: 80%; left: 40%;"></div>
	<div class="star" style="width: 2px; height: 2px; top: 90%; left: 85%;"></div>
	<div class="star" style="width: 1px; height: 1px; top: 15%; left: 50%;"></div>
	<div class="star" style="width: 2px; height: 2px; top: 5%; left: 75%;"></div>
	<div class="star" style="width: 1px; height: 1px; top: 25%; left: 5%;"></div>
	<div class="star" style="width: 2px; height: 2px; top: 35%; left: 95%;"></div>
	<div class="star" style="width: 1px; height: 1px; top: 45%; left: 65%;"></div>
	<div class="star" style="width: 2px; height: 2px; top: 55%; left: 25%;"></div>

	<!-- Nebula Effects -->
	<div class="nebula"></div>
	<div class="nebula nebula-2"></div>

	<!-- Orbits -->
	<div class="orbit orbit-1">
		<div class="orbit-planet"></div>
	</div>
	<div class="orbit orbit-2">
		<div class="orbit-planet"></div>
	</div>
	<div class="orbit orbit-3">
		<div class="orbit-planet"></div>
	</div>

	<!-- Floating Planets -->
	<div class="planet planet-1"></div>
	<div class="planet planet-2"></div>
	<div class="planet planet-3"></div>
	<div class="planet planet-4"></div>

	<!-- Shooting Stars -->
	<div class="shooting-star shooting-star-1"></div>
	<div class="shooting-star shooting-star-2"></div>
</div>

<style>
    .space-background {
        position: fixed;
        inset: 0;
        z-index: -10;
        background: radial-gradient(ellipse at center, #0f0f23 0%, #000000 100%);
        overflow: hidden;
    }

    /* Stars */
    .star {
        position: absolute;
        background: white;
        border-radius: 50%;
        animation: twinkle 2s infinite alternate;
    }

    .star:nth-child(odd) {
        animation-delay: 1s;
    }

    @keyframes twinkle {
        0% { opacity: 0.3; transform: scale(1); }
        100% { opacity: 1; transform: scale(1.2); }
    }

    /* Planets */
    .planet {
        position: absolute;
        border-radius: 50%;
        animation: float 6s ease-in-out infinite;
    }

    .planet-1 {
        width: 60px;
        height: 60px;
        background: linear-gradient(135deg, #ff6b6b, #ff8e8e);
        top: 15%;
        left: 10%;
        animation-delay: 0s;
        box-shadow: 0 0 30px rgba(255, 107, 107, 0.3);
    }

    .planet-2 {
        width: 80px;
        height: 80px;
        background: linear-gradient(135deg, #4ecdc4, #44a08d);
        top: 60%;
        right: 15%;
        animation-delay: 2s;
        box-shadow: 0 0 40px rgba(78, 205, 196, 0.3);
    }

    .planet-3 {
        width: 40px;
        height: 40px;
        background: linear-gradient(135deg, #feca57, #ff9ff3);
        top: 30%;
        right: 30%;
        animation-delay: 4s;
        box-shadow: 0 0 25px rgba(254, 202, 87, 0.3);
    }

    .planet-4 {
        width: 100px;
        height: 100px;
        background: linear-gradient(135deg, #a8edea, #fed6e3);
        bottom: 20%;
        left: 20%;
        animation-delay: 1s;
        box-shadow: 0 0 50px rgba(168, 237, 234, 0.3);
    }

    @keyframes float {
        0%, 100% { transform: translateY(0px) rotate(0deg); }
        50% { transform: translateY(-20px) rotate(180deg); }
    }

    /* Orbits */
    .orbit {
        position: absolute;
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 50%;
        animation: rotate 20s linear infinite;
    }

    .orbit-1 {
        width: 300px;
        height: 300px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        animation-duration: 25s;
    }

    .orbit-2 {
        width: 500px;
        height: 500px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        animation-duration: 35s;
        animation-direction: reverse;
    }

    .orbit-3 {
        width: 200px;
        height: 200px;
        top: 20%;
        right: 10%;
        animation-duration: 15s;
        transform-origin: center;
    }

    @keyframes rotate {
        from { transform: translate(-50%, -50%) rotate(0deg); }
        to { transform: translate(-50%, -50%) rotate(360deg); }
    }

    .orbit-3 {
        animation-name: rotate-simple;
    }

    @keyframes rotate-simple {
        from { transform: rotate(0deg); }
        to { transform: rotate(360deg); }
    }

    /* Orbit planets */
    .orbit-planet {
        position: absolute;
        width: 12px;
        height: 12px;
        background: linear-gradient(45deg, #667eea, #764ba2);
        border-radius: 50%;
        top: -6px;
        left: 50%;
        transform: translateX(-50%);
        box-shadow: 0 0 15px rgba(102, 126, 234, 0.5);
    }

    /* Shooting stars */
    .shooting-star {
        position: absolute;
        width: 2px;
        height: 2px;
        background: white;
        border-radius: 50%;
        animation: shoot 3s linear infinite;
    }

    .shooting-star-1 {
        top: 20%;
        left: 80%;
        animation-delay: 0s;
    }

    .shooting-star-2 {
        top: 70%;
        left: 20%;
        animation-delay: 2s;
    }

    @keyframes shoot {
        0% {
            transform: translate(0, 0) scale(1);
            opacity: 1;
        }
        70% {
            transform: translate(-300px, 150px) scale(0);
            opacity: 0.5;
        }
        100% {
            transform: translate(-400px, 200px) scale(0);
            opacity: 0;
        }
    }

    /* Nebula effect */
    .nebula {
        position: absolute;
        width: 400px;
        height: 400px;
        background: radial-gradient(circle, rgba(138, 43, 226, 0.1) 0%, transparent 70%);
        border-radius: 50%;
        top: 10%;
        right: 20%;
        animation: pulse 8s ease-in-out infinite;
    }

    .nebula-2 {
        width: 600px;
        height: 600px;
        background: radial-gradient(circle, rgba(30, 144, 255, 0.08) 0%, transparent 70%);
        bottom: 10%;
        left: 10%;
        animation-delay: 4s;
    }

    @keyframes pulse {
        0%, 100% { transform: scale(1); opacity: 0.3; }
        50% { transform: scale(1.2); opacity: 0.6; }
    }
</style>