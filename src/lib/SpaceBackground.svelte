<!-- SpaceBackground.svelte -->
<div class="space-background">
	<!-- Low Poly Stars -->
	<div class="poly-star" style="top: 10%; left: 20%; transform: rotate(45deg);"></div>
	<div class="poly-star small" style="top: 20%; left: 80%; transform: rotate(12deg);"></div>
	<div class="poly-star" style="top: 30%; left: 60%; transform: rotate(78deg);"></div>
	<div class="poly-star small" style="top: 40%; left: 30%; transform: rotate(156deg);"></div>
	<div class="poly-star" style="top: 50%; left: 90%; transform: rotate(234deg);"></div>
	<div class="poly-star small" style="top: 60%; left: 10%; transform: rotate(89deg);"></div>
	<div class="poly-star" style="top: 70%; left: 70%; transform: rotate(167deg);"></div>
	<div class="poly-star small" style="top: 80%; left: 40%; transform: rotate(201deg);"></div>
	<div class="poly-star" style="top: 90%; left: 85%; transform: rotate(312deg);"></div>
	<div class="poly-star small" style="top: 15%; left: 50%; transform: rotate(45deg);"></div>
	<div class="poly-star" style="top: 5%; left: 75%; transform: rotate(134deg);"></div>
	<div class="poly-star small" style="top: 25%; left: 5%; transform: rotate(289deg);"></div>

	<!-- Low Poly Geometric Shapes -->
	<div class="poly-shape triangle-1"></div>
	<div class="poly-shape triangle-2"></div>
	<div class="poly-shape triangle-3"></div>
	<div class="poly-shape hexagon-1"></div>
	<div class="poly-shape hexagon-2"></div>

	<!-- Low Poly Planets -->
	<div class="poly-planet planet-1">
		<div class="poly-facet facet-1"></div>
		<div class="poly-facet facet-2"></div>
		<div class="poly-facet facet-3"></div>
		<div class="poly-facet facet-4"></div>
	</div>
	<div class="poly-planet planet-2">
		<div class="poly-facet facet-1"></div>
		<div class="poly-facet facet-2"></div>
		<div class="poly-facet facet-3"></div>
		<div class="poly-facet facet-4"></div>
		<div class="poly-facet facet-5"></div>
		<div class="poly-facet facet-6"></div>
	</div>
	<div class="poly-planet planet-3">
		<div class="poly-facet facet-1"></div>
		<div class="poly-facet facet-2"></div>
		<div class="poly-facet facet-3"></div>
	</div>

	<!-- Low Poly Orbits -->
	<div class="poly-orbit orbit-1">
		<div class="poly-orbit-object"></div>
	</div>
	<div class="poly-orbit orbit-2">
		<div class="poly-orbit-object"></div>
	</div>

	<!-- Geometric Meteor -->
	<div class="poly-meteor"></div>

	<!-- Low Poly Constellation Lines -->
	<svg class="constellation" viewBox="0 0 100 100">
		<line x1="20" y1="30" x2="40" y2="15" stroke="rgba(255,255,255,0.3)" stroke-width="0.5"/>
		<line x1="40" y1="15" x2="60" y2="25" stroke="rgba(255,255,255,0.3)" stroke-width="0.5"/>
		<line x1="60" y1="25" x2="80" y2="10" stroke="rgba(255,255,255,0.3)" stroke-width="0.5"/>
		<line x1="80" y1="10" x2="70" y2="35" stroke="rgba(255,255,255,0.3)" stroke-width="0.5"/>
	</svg>

	<svg class="constellation constellation-2" viewBox="0 0 100 100">
		<line x1="10" y1="70" x2="30" y2="80" stroke="rgba(255,255,255,0.2)" stroke-width="0.5"/>
		<line x1="30" y1="80" x2="50" y2="65" stroke="rgba(255,255,255,0.2)" stroke-width="0.5"/>
		<line x1="50" y1="65" x2="25" y2="55" stroke="rgba(255,255,255,0.2)" stroke-width="0.5"/>
	</svg>
</div>

<style>
    .space-background {
        position: fixed;
        inset: 0;
        z-index: -10;
        background: linear-gradient(135deg, #0a0a1a 0%, #1a0a2e 30%, #16213e 70%, #000000 100%);
        overflow: hidden;
    }

    /* Low Poly Stars */
    .poly-star {
        position: absolute;
        width: 12px;
        height: 12px;
        background: white;
        clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
        animation: polyTwinkle 3s infinite alternate;
        filter: drop-shadow(0 0 6px rgba(255, 255, 255, 0.6));
    }

    .poly-star.small {
        width: 8px;
        height: 8px;
        animation-delay: 1.5s;
    }

    @keyframes polyTwinkle {
        0% { opacity: 0.4; transform: rotate(0deg) scale(1); }
        100% { opacity: 1; transform: rotate(45deg) scale(1.3); }
    }

    /* Geometric Shapes */
    .poly-shape {
        position: absolute;
        animation: geometricFloat 8s ease-in-out infinite;
    }

    .triangle-1 {
        width: 0;
        height: 0;
        border-left: 25px solid transparent;
        border-right: 25px solid transparent;
        border-bottom: 43px solid rgba(102, 126, 234, 0.3);
        top: 20%;
        right: 10%;
        animation-delay: 0s;
        filter: drop-shadow(0 0 15px rgba(102, 126, 234, 0.4));
    }

    .triangle-2 {
        width: 0;
        height: 0;
        border-left: 15px solid transparent;
        border-right: 15px solid transparent;
        border-bottom: 26px solid rgba(255, 107, 107, 0.4);
        bottom: 30%;
        left: 15%;
        animation-delay: 3s;
        filter: drop-shadow(0 0 10px rgba(255, 107, 107, 0.5));
    }

    .triangle-3 {
        width: 0;
        height: 0;
        border-left: 20px solid transparent;
        border-right: 20px solid transparent;
        border-bottom: 35px solid rgba(78, 205, 196, 0.3);
        top: 60%;
        right: 25%;
        animation-delay: 5s;
        filter: drop-shadow(0 0 12px rgba(78, 205, 196, 0.4));
    }

    .hexagon-1 {
        width: 40px;
        height: 35px;
        background: rgba(254, 202, 87, 0.3);
        clip-path: polygon(30% 0%, 70% 0%, 100% 50%, 70% 100%, 30% 100%, 0% 50%);
        top: 15%;
        left: 70%;
        animation-delay: 2s;
        filter: drop-shadow(0 0 15px rgba(254, 202, 87, 0.4));
    }

    .hexagon-2 {
        width: 30px;
        height: 26px;
        background: rgba(168, 237, 234, 0.4);
        clip-path: polygon(30% 0%, 70% 0%, 100% 50%, 70% 100%, 30% 100%, 0% 50%);
        bottom: 15%;
        right: 40%;
        animation-delay: 4s;
        filter: drop-shadow(0 0 12px rgba(168, 237, 234, 0.5));
    }

    @keyframes geometricFloat {
        0%, 100% { transform: translateY(0px) rotate(0deg); }
        33% { transform: translateY(-15px) rotate(120deg); }
        66% { transform: translateY(-8px) rotate(240deg); }
    }

    /* Low Poly Planets */
    .poly-planet {
        position: absolute;
        border-radius: 50%;
        animation: polyPlanetFloat 10s ease-in-out infinite;
        overflow: hidden;
    }

    .planet-1 {
        width: 80px;
        height: 80px;
        top: 25%;
        left: 8%;
        animation-delay: 0s;
        background: linear-gradient(135deg, #ff6b6b, #ff8e8e);
        filter: drop-shadow(0 0 25px rgba(255, 107, 107, 0.4));
    }

    .planet-2 {
        width: 100px;
        height: 100px;
        top: 50%;
        right: 10%;
        animation-delay: 3s;
        background: linear-gradient(135deg, #4ecdc4, #44a08d);
        filter: drop-shadow(0 0 30px rgba(78, 205, 196, 0.4));
    }

    .planet-3 {
        width: 60px;
        height: 60px;
        bottom: 25%;
        left: 25%;
        animation-delay: 6s;
        background: linear-gradient(135deg, #feca57, #ff9ff3);
        filter: drop-shadow(0 0 20px rgba(254, 202, 87, 0.4));
    }

    .poly-facet {
        position: absolute;
        background: rgba(255, 255, 255, 0.1);
        clip-path: polygon(0% 0%, 100% 0%, 50% 100%);
    }

    .planet-1 .facet-1 {
        width: 40px;
        height: 30px;
        top: 10px;
        left: 10px;
        background: rgba(255, 255, 255, 0.15);
    }

    .planet-1 .facet-2 {
        width: 30px;
        height: 25px;
        top: 20px;
        right: 15px;
        background: rgba(0, 0, 0, 0.1);
        clip-path: polygon(0% 100%, 100% 100%, 50% 0%);
    }

    .planet-1 .facet-3 {
        width: 35px;
        height: 20px;
        bottom: 15px;
        left: 20px;
        background: rgba(255, 255, 255, 0.08);
    }

    .planet-1 .facet-4 {
        width: 25px;
        height: 25px;
        bottom: 10px;
        right: 10px;
        background: rgba(0, 0, 0, 0.05);
        clip-path: polygon(0% 100%, 100% 100%, 50% 0%);
    }

    .planet-2 .facet-1 {
        width: 45px;
        height: 35px;
        top: 5px;
        left: 15px;
        background: rgba(255, 255, 255, 0.12);
    }

    .planet-2 .facet-2 {
        width: 35px;
        height: 30px;
        top: 15px;
        right: 10px;
        background: rgba(0, 0, 0, 0.08);
        clip-path: polygon(0% 100%, 100% 100%, 50% 0%);
    }

    .planet-2 .facet-3 {
        width: 40px;
        height: 25px;
        bottom: 20px;
        left: 10px;
        background: rgba(255, 255, 255, 0.1);
    }

    .planet-2 .facet-4 {
        width: 30px;
        height: 30px;
        bottom: 5px;
        right: 20px;
        background: rgba(0, 0, 0, 0.06);
        clip-path: polygon(0% 100%, 100% 100%, 50% 0%);
    }

    .planet-2 .facet-5 {
        width: 25px;
        height: 20px;
        top: 40px;
        left: 5px;
        background: rgba(255, 255, 255, 0.07);
    }

    .planet-2 .facet-6 {
        width: 20px;
        height: 20px;
        top: 35px;
        right: 35px;
        background: rgba(0, 0, 0, 0.04);
    }

    .planet-3 .facet-1 {
        width: 30px;
        height: 25px;
        top: 8px;
        left: 10px;
        background: rgba(255, 255, 255, 0.13);
    }

    .planet-3 .facet-2 {
        width: 25px;
        height: 20px;
        top: 20px;
        right: 8px;
        background: rgba(0, 0, 0, 0.07);
        clip-path: polygon(0% 100%, 100% 100%, 50% 0%);
    }

    .planet-3 .facet-3 {
        width: 28px;
        height: 18px;
        bottom: 12px;
        left: 15px;
        background: rgba(255, 255, 255, 0.09);
    }

    @keyframes polyPlanetFloat {
        0%, 100% { transform: translateY(0px) rotate(0deg); }
        50% { transform: translateY(-25px) rotate(180deg); }
    }

    /* Low Poly Orbits */
    .poly-orbit {
        position: absolute;
        border: 2px solid transparent;
        border-image: linear-gradient(45deg, rgba(255,255,255,0.1), transparent, rgba(255,255,255,0.1)) 1;
        clip-path: polygon(0% 0%, 20% 0%, 25% 5%, 75% 5%, 80% 0%, 100% 0%, 100% 20%, 95% 25%, 95% 75%, 100% 80%, 100% 100%, 80% 100%, 75% 95%, 25% 95%, 20% 100%, 0% 100%, 0% 80%, 5% 75%, 5% 25%, 0% 20%);
        animation: polyOrbitRotate 20s linear infinite;
    }

    .orbit-1 {
        width: 250px;
        height: 250px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        animation-duration: 25s;
    }

    .orbit-2 {
        width: 180px;
        height: 180px;
        top: 30%;
        right: 20%;
        animation-duration: 15s;
        animation-direction: reverse;
    }

    .poly-orbit-object {
        position: absolute;
        width: 8px;
        height: 8px;
        background: linear-gradient(45deg, #667eea, #764ba2);
        clip-path: polygon(30% 0%, 70% 0%, 100% 50%, 70% 100%, 30% 100%, 0% 50%);
        top: -4px;
        left: 50%;
        transform: translateX(-50%);
        filter: drop-shadow(0 0 8px rgba(102, 126, 234, 0.6));
    }

    @keyframes polyOrbitRotate {
        from { transform: translate(-50%, -50%) rotate(0deg); }
        to { transform: translate(-50%, -50%) rotate(360deg); }
    }

    .orbit-2 {
        animation-name: polyOrbitRotateSimple;
    }

    @keyframes polyOrbitRotateSimple {
        from { transform: rotate(0deg); }
        to { transform: rotate(360deg); }
    }

    /* Geometric Meteor */
    .poly-meteor {
        position: absolute;
        width: 0;
        height: 0;
        border-left: 8px solid transparent;
        border-right: 8px solid transparent;
        border-bottom: 14px solid rgba(255, 255, 255, 0.8);
        top: 10%;
        left: 80%;
        animation: polyMeteorShoot 4s linear infinite;
        filter: drop-shadow(0 0 10px rgba(255, 255, 255, 0.6));
    }

    @keyframes polyMeteorShoot {
        0% {
            transform: translate(0, 0) rotate(45deg) scale(1);
            opacity: 1;
        }
        70% {
            transform: translate(-400px, 200px) rotate(45deg) scale(0.3);
            opacity: 0.3;
        }
        100% {
            transform: translate(-500px, 250px) rotate(45deg) scale(0);
            opacity: 0;
        }
    }

    /* Constellation Lines */
    .constellation {
        position: absolute;
        width: 300px;
        height: 200px;
        top: 20%;
        left: 30%;
        opacity: 0.6;
        animation: constellationPulse 6s ease-in-out infinite;
    }

    .constellation-2 {
        width: 250px;
        height: 150px;
        bottom: 30%;
        right: 30%;
        animation-delay: 3s;
    }

    @keyframes constellationPulse {
        0%, 100% { opacity: 0.3; }
        50% { opacity: 0.7; }
    }
</style>