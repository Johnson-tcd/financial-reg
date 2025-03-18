<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Global Financial Regulations Hub</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <style>
        :root {
            --purple-dark: #4a1c61;
            --purple-medium: #6a2c91;
            --gold: #d4af37;
            --gold-light: #f1e5ac;
            --background: #f8f8f8;
            --text-dark: #333;
            --text-light: #f8f8f8;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--background);
            color: var(--text-dark);
        }
        
        header {
            background: linear-gradient(135deg, var(--purple-dark), var(--purple-medium));
            color: white;
            padding: 1rem;
            position: relative;
            box-shadow: 0 3px 10px rgba(0,0,0,0.2);
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin-left: 10px;
            color: var(--text-light);
        }
        
        .logo-icon {
            color: var(--gold);
            font-size: 2rem;
        }
        
        .login-btn {
            background-color: var(--gold);
            color: var(--purple-dark);
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .login-btn:hover {
            background-color: var(--gold-light);
            transform: translateY(-2px);
        }
        
        main {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }
        
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .hero h2 {
            font-size: 2.2rem;
            color: var(--purple-dark);
            margin-bottom: 1rem;
            border-bottom: 3px solid var(--gold);
            padding-bottom: 0.5rem;
        }
        
        .hero p {
            max-width: 800px;
            font-size: 1.1rem;
            line-height: 1.6;
            margin-bottom: 2rem;
        }
        
        .globe-container {
            width: 100%;
            height: 500px;
            position: relative;
            margin-bottom: 3rem;
            border: 2px solid var(--gold);
            border-radius: 5px;
            overflow: hidden;
            background-color: #0a0a2a;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        #globe-canvas {
            width: 100%;
            height: 100%;
        }
        
        .globe-overlay {
            position: absolute;
            top: 20px;
            left: 20px;
            background-color: rgba(74, 28, 97, 0.8);
            color: white;
            padding: 15px;
            border-radius: 5px;
            border: 1px solid var(--gold);
            max-width: 300px;
            z-index: 10;
        }
        
        .globe-overlay h3 {
            color: var(--gold);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }
        
        .globe-overlay p {
            font-size: 0.9rem;
            margin-bottom: 0;
        }
        
        .region-info {
            position: absolute;
            bottom: 20px;
            right: 20px;
            background-color: rgba(74, 28, 97, 0.9);
            color: white;
            padding: 15px;
            border-radius: 5px;
            border: 1px solid var(--gold);
            max-width: 300px;
            display: none;
            z-index: 10;
        }
        
        .region-info h4 {
            color: var(--gold);
            margin-bottom: 10px;
        }
        
        .region-info-btn {
            margin-top: 10px;
            background-color: var(--gold);
            color: var(--purple-dark);
            border: none;
            padding: 8px 12px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
        }
        
        .news-section {
            margin-top: 2rem;
        }
        
        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .section-header h3 {
            font-size: 1.8rem;
            color: var(--purple-dark);
            border-left: 5px solid var(--gold);
            padding-left: 10px;
        }
        
        .view-all {
            color: var(--purple-medium);
            text-decoration: none;
            font-weight: bold;
        }
        
        .view-all:hover {
            color: var(--gold);
        }
        
        .news-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 20px;
        }
        
        .news-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .news-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .news-header {
            background-color: var(--purple-medium);
            color: white;
            padding: 10px 15px;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .region-tag {
            background-color: var(--gold);
            color: var(--purple-dark);
            padding: 3px 8px;
            border-radius: 3px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        .news-body {
            padding: 15px;
        }
        
        .news-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--purple-dark);
        }
        
        .news-date {
            color: #777;
            font-size: 0.8rem;
            margin-bottom: 10px;
        }
        
        .news-summary {
            font-size: 0.95rem;
            line-height: 1.5;
            margin-bottom: 15px;
        }
        
        .news-link {
            color: var(--purple-medium);
            text-decoration: none;
            font-weight: bold;
            display: inline-block;
            margin-top: 10px;
        }
        
        .news-link:hover {
            color: var(--gold);
        }
        
        footer {
            background: linear-gradient(135deg, var(--purple-dark), var(--purple-medium));
            color: white;
            padding: 2rem 1rem;
            margin-top: 3rem;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
            margin-bottom: 1.5rem;
        }
        
        .footer-section h4 {
            color: var(--gold);
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 0.5rem;
        }
        
        .footer-section a {
            color: var(--text-light);
            text-decoration: none;
        }
        
        .footer-section a:hover {
            color: var(--gold-light);
        }
        
        .copyright {
            text-align: center;
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255,255,255,0.2);
            font-size: 0.9rem;
            color: var(--text-light);
        }
        
        @media (max-width: 768px) {
            .news-grid {
                grid-template-columns: 1fr;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .globe-container {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="logo">
                <span class="logo-icon">⚖️</span>
                <h1>Global Financial Regulations Hub</h1>
            </div>
            <button class="login-btn">Login / Register</button>
        </div>
    </header>
    
    <main>
        <section class="hero">
            <h2>Your Global Financial Regulation Center</h2>
            <p>Stay updated with the latest financial regulations and policy changes across major economic regions. Our interactive platform provides real-time updates and comprehensive analysis from regulatory experts worldwide.</p>
        </section>
        
        <div class="globe-container">
            <div id="globe-canvas"></div>
            <div class="globe-overlay">
                <h3>Interactive Financial Globe</h3>
                <p>Rotate the globe and click on a region to view detailed financial regulations and updates.</p>
            </div>
            <div class="region-info" id="region-info">
                <h4 id="region-title">Region Name</h4>
                <p id="region-description">Region description and key financial details will appear here.</p>
                <button class="region-info-btn" id="region-btn">View Details</button>
            </div>
        </div>
        
        <section class="news-section">
            <div class="section-header">
                <h3>Latest Regulation Updates</h3>
                <a href="#" class="view-all">View All Updates</a>
            </div>
            
            <div class="news-grid">
                <div class="news-card">
                    <div class="news-header">
                        <span>Regulatory Update</span>
                        <span class="region-tag">USA</span>
                    </div>
                    <div class="news-body">
                        <h4 class="news-title">SEC Finalizes New Climate Disclosure Rules</h4>
                        <p class="news-date">March 15, 2025</p>
                        <p class="news-summary">The Securities and Exchange Commission has approved new climate-related disclosure requirements for public companies, establishing standardized reporting on climate risks and greenhouse gas emissions.</p>
                        <a href="#" class="news-link">Read More →</a>
                    </div>
                </div>
                
                <div class="news-card">
                    <div class="news-header">
                        <span>Policy Change</span>
                        <span class="region-tag">EU</span>
                    </div>
                    <div class="news-body">
                        <h4 class="news-title">European Central Bank Updates Digital Euro Framework</h4>
                        <p class="news-date">March 12, 2025</p>
                        <p class="news-summary">The ECB has published its updated regulatory framework for the digital euro, outlining new compliance requirements for financial institutions and payment service providers.</p>
                        <a href="#" class="news-link">Read More →</a>
                    </div>
                </div>
                
                <div class="news-card">
                    <div class="news-header">
                        <span>Regulatory Update</span>
                        <span class="region-tag">UK</span>
                    </div>
                    <div class="news-body">
                        <h4 class="news-title">FCA Introduces Enhanced Consumer Protection Rules</h4>
                        <p class="news-date">March 10, 2025</p>
                        <p class="news-summary">The UK's Financial Conduct Authority has implemented new consumer duty regulations requiring financial firms to provide more transparent service and demonstrate better outcomes for retail customers.</p>
                        <a href="#" class="news-link">Read More →</a>
                    </div>
                </div>
                
                <div class="news-card">
                    <div class="news-header">
                        <span>Regulatory Update</span>
                        <span class="region-tag">China</span>
                    </div>
                    <div class="news-body">
                        <h4 class="news-title">PBOC Announces New Capital Requirements for Digital Banks</h4>
                        <p class="news-date">March 8, 2025</p>
                        <p class="news-summary">China's central bank has unveiled stricter capital adequacy requirements for digital banks and fintech platforms, aiming to strengthen financial stability in the growing digital finance sector.</p>
                        <a href="#" class="news-link">Read More →</a>
                    </div>
                </div>
                
                <div class="news-card">
                    <div class="news-header">
                        <span>Policy Change</span>
                        <span class="region-tag">Singapore</span>
                    </div>
                    <div class="news-body">
                        <h4 class="news-title">MAS Revises Digital Asset Licensing Framework</h4>
                        <p class="news-date">March 5, 2025</p>
                        <p class="news-summary">The Monetary Authority of Singapore has updated its licensing regime for digital asset service providers, introducing new requirements for customer protection and risk management.</p>
                        <a href="#" class="news-link">Read More →</a>
                    </div>
                </div>
                
                <div class="news-card">
                    <div class="news-header">
                        <span>Regulatory Update</span>
                        <span class="region-tag">Global</span>
                    </div>
                    <div class="news-body">
                        <h4 class="news-title">FATF Updates Anti-Money Laundering Guidelines</h4>
                        <p class="news-date">March 1, 2025</p>
                        <p class="news-summary">The Financial Action Task Force has published revised guidelines on anti-money laundering and counter-terrorist financing measures, with new requirements for virtual assets and cross-border transactions.</p>
                        <a href="#" class="news-link">Read More →</a>
                    </div>
                </div>
            </div>
        </section>
    </main>
    
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h4>Regional Hubs</h4>
                <ul>
                    <li><a href="#">North America</a></li>
                    <li><a href="#">European Union</a></li>
                    <li><a href="#">United Kingdom</a></li>
                    <li><a href="#">Asia Pacific</a></li>
                    <li><a href="#">Middle East</a></li>
                    <li><a href="#">Latin America</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>Key Regulators</h4>
                <ul>
                    <li><a href="#">SEC (USA)</a></li>
                    <li><a href="#">ECB (EU)</a></li>
                    <li><a href="#">FCA (UK)</a></li>
                    <li><a href="#">PBOC (China)</a></li>
                    <li><a href="#">MAS (Singapore)</a></li>
                    <li><a href="#">FATF (Global)</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>Resources</h4>
                <ul>
                    <li><a href="#">Regulation Database</a></li>
                    <li><a href="#">Policy Analyses</a></li>
                    <li><a href="#">Expert Opinions</a></li>
                    <li><a href="#">Compliance Tools</a></li>
                    <li><a href="#">Events & Webinars</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>About Us</h4>
                <ul>
                    <li><a href="#">Our Team</a></li>
                    <li><a href="#">Methodology</a></li>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">Careers</a></li>
                    <li><a href="#">Terms of Service</a></li>
                </ul>
            </div>
        </div>
        
        <div class="copyright">
            &copy; 2025 Global Financial Regulations Hub. All rights reserved.
        </div>
    </footer>

    <script>
        // Initialize the globe using Three.js
        let scene, camera, renderer, globe, raycaster, mouse;
        const regions = [
            { name: "North America", 
              color: "#3a7bd5", 
              position: { lat: 40, lng: -100 },
              description: "Home to major financial regulators including the SEC, Federal Reserve, and CFTC. Features some of the world's largest financial markets and institutions." },
            { name: "European Union", 
              color: "#00d2ff", 
              position: { lat: 50, lng: 10 },
              description: "Governed by the European Central Bank and European Banking Authority. Known for comprehensive financial regulations including MiFID II and GDPR." },
            { name: "United Kingdom", 
              color: "#0052cc", 
              position: { lat: 55, lng: -2 },
              description: "Regulated by the Financial Conduct Authority (FCA) and Bank of England. London remains one of the world's premier financial centers." },
            { name: "China", 
              color: "#d70000", 
              position: { lat: 35, lng: 105 },
              description: "Financial system overseen by the People's Bank of China (PBOC) and China Banking and Insurance Regulatory Commission (CBIRC)." },
            { name: "Japan", 
              color: "#ff6b6b", 
              position: { lat: 36, lng: 138 },
              description: "Financial markets regulated by the Financial Services Agency (FSA). Home to the Tokyo Stock Exchange, one of Asia's largest markets." },
            { name: "Singapore", 
              color: "#ff9e00", 
              position: { lat: 1.3, lng: 103.8 },
              description: "Regulated by the Monetary Authority of Singapore (MAS). A leading international financial center with strong regulatory framework." },
            { name: "Middle East", 
              color: "#ffd700", 
              position: { lat: 25, lng: 45 },
              description: "Emerging financial hubs include Dubai International Financial Centre (DIFC) and Abu Dhabi Global Market (ADGM)." },
            { name: "Australia", 
              color: "#2ecc71", 
              position: { lat: -25, lng: 135 },
              description: "Financial system regulated by the Australian Securities and Investments Commission (ASIC) and Reserve Bank of Australia." },
            { name: "Brazil", 
              color: "#27ae60", 
              position: { lat: -10, lng: -55 },
              description: "Largest financial market in Latin America, regulated by the Central Bank of Brazil and Securities and Exchange Commission (CVM)." }
        ];
        
        let regionMarkers = [];
        let selectedRegion = null;
        
        function init() {
            // Scene setup
            scene = new THREE.Scene();
            camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            camera.position.z = 2;
            
            // Renderer setup
            renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
            renderer.setSize(document.getElementById('globe-canvas').offsetWidth, document.getElementById('globe-canvas').offsetHeight);
            document.getElementById('globe-canvas').appendChild(renderer.domElement);
            
            // Setup for object selection
            raycaster = new THREE.Raycaster();
            mouse = new THREE.Vector2();
            
            // Create the globe
            const earthGeometry = new THREE.SphereGeometry(1, 32, 32);
            const earthMaterial = new THREE.MeshBasicMaterial({
                color: 0x1a1a2e,
                transparent: true,
                opacity: 0.8
            });
            
            // Create grid lines for the globe
            const gridMaterial = new THREE.LineBasicMaterial({ color: 0x334756, transparent: true, opacity: 0.5 });
            const gridGeometry = new THREE.SphereGeometry(1.01, 32, 32);
            const gridWireframe = new THREE.WireframeGeometry(gridGeometry);
            const gridLines = new THREE.LineSegments(gridWireframe, gridMaterial);
            
            globe = new THREE.Mesh(earthGeometry, earthMaterial);
            scene.add(globe);
            scene.add(gridLines);
            
            // Add ambient light
            const ambientLight = new THREE.AmbientLight(0xffffff, 0.5);
            scene.add(ambientLight);
            
            // Add point light
            const pointLight = new THREE.PointLight(0xffffff, 1);
            pointLight.position.set(5, 3, 5);
            scene.add(pointLight);
            
            // Add region markers
            addRegionMarkers();
            
            // Add event listeners
            window.addEventListener('resize', onWindowResize);
            renderer.domElement.addEventListener('mousemove', onMouseMove);
            renderer.domElement.addEventListener('click', onMouseClick);
            
            document.getElementById('region-btn').addEventListener('click', function() {
                if (selectedRegion) {
                    // Redirect to region page
                    alert(`Redirecting to ${selectedRegion.name} financial regulations page`);
                }
            });
            
            // Start animation
            animate();
        }
        
        function latLongToVector3(lat, lng, radius) {
            const phi = (90 - lat) * (Math.PI / 180);
            const theta = (lng + 180) * (Math.PI / 180);
            
            const x = -radius * Math.sin(phi) * Math.cos(theta);
            const y = radius * Math.cos(phi);
            const z = radius * Math.sin(phi) * Math.sin(theta);
            
            return new THREE.Vector3(x, y, z);
        }
        
        function addRegionMarkers() {
            regions.forEach(region => {
                const markerGeometry = new THREE.SphereGeometry(0.03, 16, 16);
                const markerMaterial = new THREE.MeshBasicMaterial({ color: region.color });
                const marker = new THREE.Mesh(markerGeometry, markerMaterial);
                
                // Position marker at region coordinates
                const position = latLongToVector3(region.position.lat, region.position.lng, 1.02);
                marker.position.copy(position);
                
                // Add region data to marker
                marker.userData = {
                    name: region.name,
                    description: region.description,
                    color: region.color
                };
                
                scene.add(marker);
                regionMarkers.push(marker);
            });
        }
        
        function onWindowResize() {
            camera.aspect = document.getElementById('globe-canvas').offsetWidth / document.getElementById('globe-canvas').offsetHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(document.getElementById('globe-canvas').offsetWidth, document.getElementById('globe-canvas').offsetHeight);
        }
        
        function onMouseMove(event) {
            // Calculate mouse position in normalized device coordinates
            const rect = renderer.domElement.getBoundingClientRect();
            mouse.x = ((event.clientX - rect.left) / rect.width) * 2 - 1;
            mouse.y = -((event.clientY - rect.top) / rect.height) * 2 + 1;
            
            // Update the cursor
            checkIntersection();
        }
        
        function onMouseClick(event) {
            // Calculate mouse position in normalized device coordinates
            const rect = renderer.domElement.getBoundingClientRect();
            mouse.x = ((event.clientX - rect.left) / rect.width) * 2 - 1;
            mouse.y = -((event.clientY - rect.top) / rect.height) * 2 + 1;
            
            // Check for intersections
            raycaster.setFromCamera(mouse, camera);
            const intersects = raycaster.intersectObjects(regionMarkers);
            
            if (intersects.length > 0) {
                const region = intersects[0].object.userData;
                selectedRegion = region;
                
                // Update region info panel
                document.getElementById('region-title').textContent = region.name;
                document.getElementById('region-description').textContent = region.description;
                document.getElementById('region-info').style.display = 'block';
                
                // Pulse animation for selected marker
                const selectedMarker = intersects[0].object;
                const originalScale = selectedMarker.scale.x;
                
                // Simple pulse animation
                const timeline = {
                    scale: originalScale * 1.5,
                    duration: 0.3,
                    ease: 'power2.out',
                    onComplete: () => {
                        selectedMarker.scale.set(originalScale, originalScale, originalScale);
                    }
                };
                
                // Apply animation manually since we're not using a animation library
                selectedMarker.scale.set(timeline.scale, timeline.scale, timeline.scale);
            }
        }
        
        function checkIntersection() {
            raycaster.setFromCamera(mouse, camera);
            const intersects = raycaster.intersectObjects(regionMarkers);
            
            if (intersects.length > 0) {
                document.body.style.cursor = 'pointer';
            } else {
                document.body.style.cursor = 'default';
            }
        }
        
        function animate() {
            requestAnimationFrame(animate);
            
            // Slowly rotate the globe
            globe.rotation.y += 0.001;
            
            // Update marker positions as globe rotates
            regionMarkers.forEach(marker => {
                // Calculate marker position relative to globe rotation
                const vec = marker.position.clone();
                vec.applyAxisAngle(new THREE.Vector3(0, 1, 0), 0.001);
                marker.position.copy(vec);
                
                // Make sure markers always face the camera (billboarding)
                marker.lookAt(camera.position);
            });
            
            renderer.render(scene, camera);
        }
        
        // Start the globe
        window.addEventListener('load', init);
    </script>
</body>
</html>  
