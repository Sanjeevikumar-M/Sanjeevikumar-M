<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sanjeevikumar M | AI Engineer & Systems Builder</title>
    
    <!-- Meta tags for SEO -->
    <meta name="description" content="Portfolio of Sanjeevikumar M, AI Engineer, Full Stack Developer, and Systems Builder. Designing intelligent solutions bridging hardware and software.">
    <meta name="keywords" content="AI, Machine Learning, Computer Vision, IoT, Embedded Systems, FastAPI, React, ESP32, Portfolio, Sanjeevikumar M">
    <meta name="author" content="Sanjeevikumar M">
    
    <!-- Google Fonts: Space Grotesk (Sci-Fi/Tech Headings) and Inter (Modern Readable Body) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Space Grotesk', 'sans-serif'],
                    },
                    colors: {
                        dark: {
                            DEFAULT: '#050505',
                            card: 'rgba(10, 10, 10, 0.6)',
                            border: 'rgba(255, 255, 255, 0.05)',
                        },
                        accent: {
                            DEFAULT: '#ff003c',
                            glow: 'rgba(255, 0, 60, 0.15)',
                            border: 'rgba(255, 0, 60, 0.3)',
                        }
                    }
                }
            }
        }
    </script>
    
    <!-- Lucide Icons CDN -->
    <script src="https://unpkg.com/lucide@latest"></script>
    
    <!-- Advanced Custom CSS -->
    <style>
        /* Base styles */
        body {
            background-color: #050505;
            color: #f3f4f6;
            overflow-x: hidden;
        }

        /* Glassmorphism Styles */
        .glass-card {
            background: rgba(10, 10, 10, 0.55);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.5);
            transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .glass-card:hover {
            border-color: rgba(255, 0, 60, 0.3);
            box-shadow: 0 0 30px rgba(255, 0, 60, 0.15), inset 0 0 15px rgba(255, 0, 60, 0.05);
            transform: translateY(-4px);
        }

        .glass-nav {
            background: rgba(5, 5, 5, 0.75);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        /* Glow Text & Elements */
        .text-glow {
            text-shadow: 0 0 15px rgba(255, 0, 60, 0.6);
        }

        .box-glow {
            box-shadow: 0 0 25px rgba(255, 0, 60, 0.4);
        }

        .border-glow:hover {
            box-shadow: 0 0 20px rgba(255, 0, 60, 0.2);
            border-color: rgba(255, 0, 60, 0.5);
        }

        /* Ambient Lights (Decorative Blurred Background Circles) */
        .ambient-light-1 {
            position: absolute;
            top: 10%;
            left: -10%;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(255, 0, 60, 0.1) 0%, rgba(0, 0, 0, 0) 70%);
            filter: blur(80px);
            pointer-events: none;
            z-index: 0;
        }

        .ambient-light-2 {
            position: absolute;
            bottom: 20%;
            right: -10%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(255, 0, 60, 0.08) 0%, rgba(0, 0, 0, 0) 70%);
            filter: blur(90px);
            pointer-events: none;
            z-index: 0;
        }

        .ambient-light-3 {
            position: absolute;
            top: 45%;
            left: 35%;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(255, 0, 60, 0.05) 0%, rgba(0, 0, 0, 0) 70%);
            filter: blur(70px);
            pointer-events: none;
            z-index: 0;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #050505;
        }
        ::-webkit-scrollbar-thumb {
            background: #1f1f1f;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #ff003c;
        }

        /* Floating Animation for Technology Tags */
        @keyframes float-1 {
            0%, 100% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(8px, -12px) scale(1.03); }
        }
        @keyframes float-2 {
            0%, 100% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(-10px, 15px) scale(0.98); }
        }
        @keyframes float-3 {
            0%, 100% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(12px, 8px) scale(1.02); }
        }
        @keyframes float-4 {
            0%, 100% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(-8px, -10px) scale(1.01); }
        }

        .float-tag-1 { animation: float-1 6s ease-in-out infinite; }
        .float-tag-2 { animation: float-2 7s ease-in-out infinite 0.5s; }
        .float-tag-3 { animation: float-3 8s ease-in-out infinite 1s; }
        .float-tag-4 { animation: float-4 5s ease-in-out infinite 1.5s; }

        /* Scroll Reveal System */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Grid Background Pattern overlay */
        .grid-overlay {
            background-image: 
                linear-gradient(rgba(255, 255, 255, 0.007) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 255, 255, 0.007) 1px, transparent 1px);
            background-size: 50px 50px;
        }

        /* Timeline details */
        .timeline-line {
            background: linear-gradient(to bottom, #111, rgba(255, 0, 60, 0.5) 30%, rgba(255, 0, 60, 0.5) 70%, #111);
        }

        /* Custom glow buttons */
        .glow-btn {
            position: relative;
            z-index: 1;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        .glow-btn::before {
            content: '';
            position: absolute;
            top: 0; left: -100%; width: 100%; height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: all 0.5s ease;
            z-index: -1;
        }
        .glow-btn:hover::before {
            left: 100%;
        }

        /* Custom blinking cursor for typewriter */
        .cursor {
            display: inline-block;
            width: 2px;
            background-color: #ff003c;
            margin-left: 2px;
            animation: blink 0.8s infinite;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
    </style>
</head>
<body class="font-sans antialiased text-gray-200 min-h-screen relative">

    <!-- Interactive Particle Background Canvas -->
    <canvas id="particleCanvas" class="fixed top-0 left-0 w-full h-full pointer-events-auto z-0"></canvas>

    <!-- Grid Overlay for futuristic background alignment -->
    <div class="fixed inset-0 grid-overlay pointer-events-none z-0"></div>

    <!-- Decorative lights -->
    <div class="ambient-light-1"></div>
    <div class="ambient-light-2"></div>
    <div class="ambient-light-3"></div>

    <!-- STICKY GLASSMORPHIC HEADER -->
    <header class="fixed top-0 left-0 w-full glass-nav z-50 transition-all duration-300" id="mainHeader">
        <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
            <a href="#hero" class="font-display font-bold text-xl tracking-wider text-white flex items-center gap-2 group">
                <span class="w-2.5 h-2.5 rounded-full bg-accent animate-pulse"></span>
                <span>SANJEEVIKUMAR <span class="text-accent group-hover:text-white transition-colors duration-300">M.</span></span>
            </a>
            
            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center gap-8">
                <a href="#about" class="text-sm font-medium text-gray-400 hover:text-white hover:text-glow transition-all duration-300">About</a>
                <a href="#expertise" class="text-sm font-medium text-gray-400 hover:text-white hover:text-glow transition-all duration-300">Expertise</a>
                <a href="#projects" class="text-sm font-medium text-gray-400 hover:text-white hover:text-glow transition-all duration-300">Projects</a>
                <a href="#journey" class="text-sm font-medium text-gray-400 hover:text-white hover:text-glow transition-all duration-300">Journey</a>
                <a href="#tech" class="text-sm font-medium text-gray-400 hover:text-white hover:text-glow transition-all duration-300">Skills</a>
                <a href="#contact" class="px-4 py-2 text-xs font-semibold uppercase tracking-widest border border-accent text-white rounded-full bg-accent/10 hover:bg-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.5)] transition-all duration-300">Connect</a>
            </nav>

            <!-- Mobile Menu Toggle Button -->
            <button class="md:hidden text-gray-300 hover:text-white focus:outline-none" id="mobileMenuBtn">
                <i data-lucide="menu" class="w-6 h-6"></i>
            </button>
        </div>

        <!-- Mobile Drawer menu -->
        <div class="hidden md:hidden border-t border-white/5 bg-dark/95 backdrop-blur-lg px-6 py-4 flex flex-col gap-4 absolute top-20 left-0 w-full" id="mobileDrawer">
            <a href="#about" class="text-sm font-medium py-2 text-gray-300 hover:text-accent transition-colors" onclick="toggleDrawer()">About</a>
            <a href="#expertise" class="text-sm font-medium py-2 text-gray-300 hover:text-accent transition-colors" onclick="toggleDrawer()">Expertise</a>
            <a href="#projects" class="text-sm font-medium py-2 text-gray-300 hover:text-accent transition-colors" onclick="toggleDrawer()">Projects</a>
            <a href="#journey" class="text-sm font-medium py-2 text-gray-300 hover:text-accent transition-colors" onclick="toggleDrawer()">Journey</a>
            <a href="#tech" class="text-sm font-medium py-2 text-gray-300 hover:text-accent transition-colors" onclick="toggleDrawer()">Skills</a>
            <a href="#contact" class="text-sm font-medium py-2 text-accent flex items-center gap-1 font-semibold" onclick="toggleDrawer()">Connect <i data-lucide="arrow-up-right" class="w-4 h-4"></i></a>
        </div>
    </header>

    <!-- MAIN PAGE CONTAINER -->
    <main class="relative z-10 max-w-7xl mx-auto px-6 pt-32 pb-24 flex flex-col gap-32">

        <!-- 1. HERO SECTION -->
        <section id="hero" class="min-h-[85vh] flex flex-col justify-center relative py-12">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                <!-- Hero Core Information -->
                <div class="lg:col-span-8 flex flex-col gap-6 select-none">
                    <div class="inline-flex items-center gap-2 border border-white/10 px-3.5 py-1.5 rounded-full bg-white/5 w-fit reveal">
                        <span class="w-2 h-2 rounded-full bg-accent animate-ping"></span>
                        <span class="text-xs font-semibold uppercase tracking-wider text-gray-300">Portfolio Initiative v2.6</span>
                    </div>

                    <h1 class="reveal">
                        <div class="text-xs uppercase tracking-widest font-display text-accent mb-2 font-semibold text-glow">System Architect & Engineer</div>
                        <div class="text-5xl sm:text-7xl font-display font-extrabold text-white tracking-tight leading-none">
                            SANJEEVIKUMAR M
                        </div>
                    </h1>

                    <h2 class="text-xl sm:text-3xl font-display font-medium text-gray-300 reveal leading-tight">
                        Building Intelligent Systems <br class="hidden sm:inline">
                        with <span class="text-white border-b-2 border-accent pb-0.5">AI, IoT & Embedded Engineering</span>
                    </h2>

                    <!-- Typing Subheadline container -->
                    <div class="h-6 flex items-center font-mono text-xs sm:text-sm text-gray-400 tracking-wider uppercase reveal">
                        <span id="typed-text"></span><span class="cursor">|</span>
                    </div>

                    <p class="text-sm sm:text-base text-gray-400 max-w-xl leading-relaxed reveal">
                        I design and build intelligent systems that connect Artificial Intelligence, Embedded Hardware, IoT Devices, Cloud Infrastructure, and Modern Web Applications to solve real-world challenges.
                    </p>

                    <!-- Call To Action Actions -->
                    <div class="flex flex-wrap items-center gap-4 mt-4 reveal">
                        <a href="#projects" class="glow-btn px-6 py-3 bg-accent text-white font-medium text-sm rounded-full box-glow hover:bg-accent/80 transition-all flex items-center gap-2">
                            Explore Projects <i data-lucide="arrow-down" class="w-4 h-4"></i>
                        </a>
                        <a href="https://github.com/Sanjeevikumar-M" target="_blank" class="px-6 py-3 border border-white/10 hover:border-accent hover:text-accent rounded-full bg-white/5 hover:bg-accent/5 transition-all text-sm font-medium flex items-center gap-2">
                            <i data-lucide="github" class="w-4 h-4"></i> GitHub
                        </a>
                        <a href="https://linkedin.com" target="_blank" class="px-6 py-3 border border-white/10 hover:border-accent hover:text-accent rounded-full bg-white/5 hover:bg-accent/5 transition-all text-sm font-medium flex items-center gap-2">
                            <i data-lucide="linkedin" class="w-4 h-4"></i> LinkedIn
                        </a>
                        <a href="#" class="px-6 py-3 text-gray-400 hover:text-white transition-all text-sm font-medium flex items-center gap-2">
                            <i data-lucide="file-text" class="w-4 h-4"></i> Resume
                        </a>
                    </div>
                </div>

                <!-- Interactive Floating Tags Panel -->
                <div class="lg:col-span-4 flex flex-wrap justify-start lg:justify-center items-center gap-3 relative min-h-[300px] reveal">
                    <!-- Overlay Tech Circle elements -->
                    <div class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-20">
                        <div class="w-64 h-64 rounded-full border border-dashed border-accent animate-[spin_40s_linear_infinite]"></div>
                        <div class="w-48 h-48 rounded-full border border-dotted border-white/20 absolute animate-[spin_20s_linear_infinite_reverse]"></div>
                    </div>

                    <!-- Tags placed systematically with float delays -->
                    <span class="float-tag-1 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white border border-accent/25 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">Python</span>
                    <span class="float-tag-2 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white/90 border border-white/5 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">FastAPI</span>
                    <span class="float-tag-3 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white/90 border border-white/5 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">TensorFlow</span>
                    <span class="float-tag-4 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white border border-accent/25 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">ESP32</span>
                    <span class="float-tag-1 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white/90 border border-white/5 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">React</span>
                    <span class="float-tag-2 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white/90 border border-white/5 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">Machine Learning</span>
                    <span class="float-tag-3 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white border border-accent/25 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">Computer Vision</span>
                    <span class="float-tag-4 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white/90 border border-white/5 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">IoT</span>
                    <span class="float-tag-2 glass-card px-4 py-2 rounded-full text-xs font-semibold text-white border border-accent/25 hover:border-accent hover:shadow-[0_0_15px_rgba(255,0,60,0.3)] transition-all cursor-default select-none">Embedded Systems</span>
                </div>
            </div>
        </section>

        <!-- 2. ABOUT SECTION -->
        <section id="about" class="py-12 reveal scroll-mt-24">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
                <div class="lg:col-span-5 flex flex-col justify-center">
                    <div class="text-accent uppercase tracking-widest text-xs font-semibold mb-2">Architecting Solutions</div>
                    <h2 class="text-3xl sm:text-4xl font-display font-bold text-white tracking-tight mb-6">
                        Engineering the Future
                    </h2>
                    <p class="text-gray-300 text-sm sm:text-base leading-relaxed mb-6">
                        I am an AI & Data Science Engineer passionate about creating intelligent solutions that bridge the gap between software and hardware.
                    </p>
                    <div class="border-l-2 border-accent pl-4 py-1.5 text-xs text-gray-400 font-mono italic">
                        "Focus on innovation, scalability, and real-world impact."
                    </div>
                </div>
                
                <div class="lg:col-span-7 flex flex-col justify-center">
                    <h3 class="text-xs uppercase tracking-widest font-display text-gray-400 mb-4 font-semibold">Primary Engineering Sectors</h3>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div class="glass-card p-4 rounded-xl flex items-start gap-3.5">
                            <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent shrink-0">
                                <i data-lucide="brain" class="w-4 h-4"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-semibold text-white mb-0.5">Artificial Intelligence</h4>
                                <p class="text-xs text-gray-400">Deep learning, Neural networks, models</p>
                            </div>
                        </div>

                        <div class="glass-card p-4 rounded-xl flex items-start gap-3.5">
                            <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent shrink-0">
                                <i data-lucide="cpu" class="w-4 h-4"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-semibold text-white mb-0.5">Embedded Engineering</h4>
                                <p class="text-xs text-gray-400">Microcontrollers, ESP32, STM32</p>
                            </div>
                        </div>

                        <div class="glass-card p-4 rounded-xl flex items-start gap-3.5">
                            <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent shrink-0">
                                <i data-lucide="wifi" class="w-4 h-4"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-semibold text-white mb-0.5">IoT Systems</h4>
                                <p class="text-xs text-gray-400">Smart devices, sensor nodes, telemetry</p>
                            </div>
                        </div>

                        <div class="glass-card p-4 rounded-xl flex items-start gap-3.5">
                            <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent shrink-0">
                                <i data-lucide="globe" class="w-4 h-4"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-semibold text-white mb-0.5">Full Stack Development</h4>
                                <p class="text-xs text-gray-400">React, FastAPIs, databases</p>
                            </div>
                        </div>

                        <div class="glass-card p-4 rounded-xl flex items-start gap-3.5">
                            <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent shrink-0">
                                <i data-lucide="eye" class="w-4 h-4"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-semibold text-white mb-0.5">Computer Vision</h4>
                                <p class="text-xs text-gray-400">Object detection, visual processing</p>
                            </div>
                        </div>

                        <div class="glass-card p-4 rounded-xl flex items-start gap-3.5">
                            <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent shrink-0">
                                <i data-lucide="cloud" class="w-4 h-4"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-semibold text-white mb-0.5">Cloud Technologies</h4>
                                <p class="text-xs text-gray-400">GCP, cloud telemetry, pipelines</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 3. EXPERTISE SECTION -->
        <section id="expertise" class="py-12 reveal scroll-mt-24">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <div class="text-accent uppercase tracking-widest text-xs font-semibold mb-2">Core Capabilities</div>
                <h2 class="text-3xl sm:text-4xl font-display font-bold text-white tracking-tight">Areas of Expertise</h2>
                <div class="w-12 h-1 bg-accent mx-auto mt-4 rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Card 1: AI -->
                <div class="glass-card p-8 rounded-2xl flex flex-col justify-between group">
                    <div class="flex flex-col gap-4">
                        <div class="w-10 h-10 rounded-xl bg-accent/10 border border-accent/20 flex items-center justify-center text-accent group-hover:scale-110 transition-transform duration-300">
                            <i data-lucide="brain-circuit" class="w-5 h-5"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white font-display">Artificial Intelligence</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            Build predictive models, intelligent agents, and AI-powered applications.
                        </p>
                    </div>
                    <div class="mt-6 flex items-center text-xs font-semibold text-accent gap-1 group-hover:translate-x-1.5 transition-transform">
                        Explore core details <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
                    </div>
                </div>

                <!-- Card 2: ML -->
                <div class="glass-card p-8 rounded-2xl flex flex-col justify-between group">
                    <div class="flex flex-col gap-4">
                        <div class="w-10 h-10 rounded-xl bg-accent/10 border border-accent/20 flex items-center justify-center text-accent group-hover:scale-110 transition-transform duration-300">
                            <i data-lucide="network" class="w-5 h-5"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white font-display">Machine Learning</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            Data-driven systems that learn and adapt.
                        </p>
                    </div>
                    <div class="mt-6 flex items-center text-xs font-semibold text-accent gap-1 group-hover:translate-x-1.5 transition-transform">
                        Explore core details <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
                    </div>
                </div>

                <!-- Card 3: CV -->
                <div class="glass-card p-8 rounded-2xl flex flex-col justify-between group">
                    <div class="flex flex-col gap-4">
                        <div class="w-10 h-10 rounded-xl bg-accent/10 border border-accent/20 flex items-center justify-center text-accent group-hover:scale-110 transition-transform duration-300">
                            <i data-lucide="scan-eye" class="w-5 h-5"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white font-display">Computer Vision</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            Object detection, image understanding, and visual intelligence.
                        </p>
                    </div>
                    <div class="mt-6 flex items-center text-xs font-semibold text-accent gap-1 group-hover:translate-x-1.5 transition-transform">
                        Explore core details <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
                    </div>
                </div>

                <!-- Card 4: Full Stack -->
                <div class="glass-card p-8 rounded-2xl flex flex-col justify-between group">
                    <div class="flex flex-col gap-4">
                        <div class="w-10 h-10 rounded-xl bg-accent/10 border border-accent/20 flex items-center justify-center text-accent group-hover:scale-110 transition-transform duration-300">
                            <i data-lucide="terminal" class="w-5 h-5"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white font-display">Full Stack Development</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            Scalable web platforms using React, FastAPI, and modern technologies.
                        </p>
                    </div>
                    <div class="mt-6 flex items-center text-xs font-semibold text-accent gap-1 group-hover:translate-x-1.5 transition-transform">
                        Explore core details <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
                    </div>
                </div>

                <!-- Card 5: IoT -->
                <div class="glass-card p-8 rounded-2xl flex flex-col justify-between group">
                    <div class="flex flex-col gap-4">
                        <div class="w-10 h-10 rounded-xl bg-accent/10 border border-accent/20 flex items-center justify-center text-accent group-hover:scale-110 transition-transform duration-300">
                            <i data-lucide="radio-receiver" class="w-5 h-5"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white font-display">IoT Systems</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            Connected devices, sensors, and intelligent automation.
                        </p>
                    </div>
                    <div class="mt-6 flex items-center text-xs font-semibold text-accent gap-1 group-hover:translate-x-1.5 transition-transform">
                        Explore core details <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
                    </div>
                </div>

                <!-- Card 6: Embedded -->
                <div class="glass-card p-8 rounded-2xl flex flex-col justify-between group">
                    <div class="flex flex-col gap-4">
                        <div class="w-10 h-10 rounded-xl bg-accent/10 border border-accent/20 flex items-center justify-center text-accent group-hover:scale-110 transition-transform duration-300">
                            <i data-lucide="pocket" class="w-5 h-5"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white font-display">Embedded Engineering</h3>
                        <p class="text-sm text-gray-400 leading-relaxed">
                            ESP32, Raspberry Pi, STM32, and hardware-software integration.
                        </p>
                    </div>
                    <div class="mt-6 flex items-center text-xs font-semibold text-accent gap-1 group-hover:translate-x-1.5 transition-transform">
                        Explore core details <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
                    </div>
                </div>
            </div>
        </section>

        <!-- 4. FEATURED PROJECTS SECTION -->
        <section id="projects" class="py-12 reveal scroll-mt-24">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-16">
                <div>
                    <div class="text-accent uppercase tracking-widest text-xs font-semibold mb-2">Realized Hardware & Software</div>
                    <h2 class="text-3xl sm:text-4xl font-display font-bold text-white tracking-tight">Featured Projects</h2>
                </div>
                <p class="text-gray-400 text-sm max-w-sm mt-4 md:mt-0">
                    A curated selection of hardware architectures and AI-driven cloud projects developed to solve complex challenges.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <!-- Project 1 -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between group relative overflow-hidden">
                    <div class="absolute -right-16 -top-16 w-32 h-32 bg-accent/5 rounded-full filter blur-xl group-hover:bg-accent/15 transition-all"></div>
                    
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-widest">Environmental Intelligence</span>
                            <a href="https://github.com/Sanjeevikumar-M" target="_blank" class="text-gray-400 hover:text-white transition-colors">
                                <i data-lucide="external-link" class="w-4 h-4"></i>
                            </a>
                        </div>
                        <h3 class="text-xl font-bold font-display text-white mb-3 group-hover:text-glow transition-all">Methane Shadow Hunter</h3>
                        <p class="text-sm text-gray-400 leading-relaxed mb-6">
                            An AI-powered environmental intelligence platform that detects methane super-emitters from satellite imagery, estimates emissions, and generates compliance reports.
                        </p>
                    </div>

                    <div>
                        <div class="flex flex-wrap gap-2">
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">FastAPI</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">React</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">Google Earth Engine</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-accent/10 border border-accent/20 text-accent">Machine Learning</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">GIS</span>
                        </div>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between group relative overflow-hidden">
                    <div class="absolute -right-16 -top-16 w-32 h-32 bg-accent/5 rounded-full filter blur-xl group-hover:bg-accent/15 transition-all"></div>

                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-widest">Smart Infrastructure</span>
                            <a href="https://github.com/Sanjeevikumar-M" target="_blank" class="text-gray-400 hover:text-white transition-colors">
                                <i data-lucide="external-link" class="w-4 h-4"></i>
                            </a>
                        </div>
                        <h3 class="text-xl font-bold font-display text-white mb-3 group-hover:text-glow transition-all">Smart Waste Management System</h3>
                        <p class="text-sm text-gray-400 leading-relaxed mb-6">
                            IoT-enabled smart city solution for real-time waste monitoring, predictive collection scheduling, and route optimization.
                        </p>
                    </div>

                    <div>
                        <div class="flex flex-wrap gap-2">
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-accent/10 border border-accent/20 text-accent">ESP32</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-accent/10 border border-accent/20 text-accent">IoT</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">Flask</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">MySQL</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">Analytics</span>
                        </div>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between group relative overflow-hidden">
                    <div class="absolute -right-16 -top-16 w-32 h-32 bg-accent/5 rounded-full filter blur-xl group-hover:bg-accent/15 transition-all"></div>

                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-widest">AgriTech & Supply Chain</span>
                            <a href="https://github.com/Sanjeevikumar-M" target="_blank" class="text-gray-400 hover:text-white transition-colors">
                                <i data-lucide="external-link" class="w-4 h-4"></i>
                            </a>
                        </div>
                        <h3 class="text-xl font-bold font-display text-white mb-3 group-hover:text-glow transition-all">AgroLink</h3>
                        <p class="text-sm text-gray-400 leading-relaxed mb-6">
                            AI-powered farmer-to-consumer marketplace improving agricultural supply chain efficiency.
                        </p>
                    </div>

                    <div>
                        <div class="flex flex-wrap gap-2">
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-accent/10 border border-accent/20 text-accent">AI</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">Web Development</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">Database Systems</span>
                        </div>
                    </div>
                </div>

                <!-- Project 4 -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between group relative overflow-hidden">
                    <div class="absolute -right-16 -top-16 w-32 h-32 bg-accent/5 rounded-full filter blur-xl group-hover:bg-accent/15 transition-all"></div>

                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-widest">Micro-Telemetry Station</span>
                            <a href="https://github.com/Sanjeevikumar-M" target="_blank" class="text-gray-400 hover:text-white transition-colors">
                                <i data-lucide="external-link" class="w-4 h-4"></i>
                            </a>
                        </div>
                        <h3 class="text-xl font-bold font-display text-white mb-3 group-hover:text-glow transition-all">IoT Weather Monitoring Station</h3>
                        <p class="text-sm text-gray-400 leading-relaxed mb-6">
                            Real-time environmental monitoring platform using sensor networks and cloud dashboards.
                        </p>
                    </div>

                    <div>
                        <div class="flex flex-wrap gap-2">
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-accent/10 border border-accent/20 text-accent">ESP8266</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-accent/10 border border-accent/20 text-accent">IoT</span>
                            <span class="text-[11px] font-mono px-2.5 py-1 rounded-md bg-white/5 border border-white/5 text-gray-300">Cloud Integration</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 5. JOURNEY TIMELINE SECTION -->
        <section id="journey" class="py-12 reveal scroll-mt-24">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <div class="text-accent uppercase tracking-widest text-xs font-semibold mb-2">Development Timeline</div>
                <h2 class="text-3xl sm:text-4xl font-display font-bold text-white tracking-tight">Professional Journey</h2>
                <div class="w-12 h-1 bg-accent mx-auto mt-4 rounded-full"></div>
            </div>

            <div class="relative max-w-3xl mx-auto">
                <!-- Vertical Center Line -->
                <div class="absolute left-4 sm:left-1/2 top-0 h-full w-[2px] timeline-line transform sm:-translate-x-1/2"></div>

                <!-- Timeline Nodes -->
                <div class="flex flex-col gap-12">
                    <!-- Node 1 -->
                    <div class="relative flex flex-col sm:flex-row items-start sm:items-center justify-between">
                        <div class="absolute left-4 sm:left-1/2 w-4 h-4 rounded-full bg-dark border-2 border-accent transform -translate-x-1/2 flex items-center justify-center">
                            <span class="w-1.5 h-1.5 rounded-full bg-accent"></span>
                        </div>
                        <div class="w-full sm:w-[45%] pl-12 sm:pl-0 sm:text-right">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-wider">Phase I</span>
                            <h3 class="text-lg font-bold text-white font-display mt-0.5">Student Engineer</h3>
                            <p class="text-xs text-gray-400 mt-1 max-w-sm sm:ml-auto">Developing core fundamentals in computer science, coding structures, logic development, and engineering principles.</p>
                        </div>
                        <div class="hidden sm:block w-[45%]"></div>
                    </div>

                    <!-- Node 2 -->
                    <div class="relative flex flex-col sm:flex-row items-start sm:items-center justify-between">
                        <div class="absolute left-4 sm:left-1/2 w-4 h-4 rounded-full bg-dark border-2 border-accent transform -translate-x-1/2 flex items-center justify-center">
                            <span class="w-1.5 h-1.5 rounded-full bg-accent animate-ping"></span>
                        </div>
                        <div class="hidden sm:block w-[45%]"></div>
                        <div class="w-full sm:w-[45%] pl-12">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-wider">Phase II</span>
                            <h3 class="text-lg font-bold text-white font-display mt-0.5">AI & Data Science Learner</h3>
                            <p class="text-xs text-gray-400 mt-1 max-w-sm">Deepening skills in analytics, data preparation pipelines, statistical learning algorithms, and deep neural models.</p>
                        </div>
                    </div>

                    <!-- Node 3 -->
                    <div class="relative flex flex-col sm:flex-row items-start sm:items-center justify-between">
                        <div class="absolute left-4 sm:left-1/2 w-4 h-4 rounded-full bg-dark border-2 border-accent transform -translate-x-1/2 flex items-center justify-center">
                            <span class="w-1.5 h-1.5 rounded-full bg-accent"></span>
                        </div>
                        <div class="w-full sm:w-[45%] pl-12 sm:pl-0 sm:text-right">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-wider">Phase III</span>
                            <h3 class="text-lg font-bold text-white font-display mt-0.5">Hackathon Competitor</h3>
                            <p class="text-xs text-gray-400 mt-1 max-w-sm sm:ml-auto">Competing in international summits, brainstorming smart-city IoT solutions, and deploying under pressure.</p>
                        </div>
                        <div class="hidden sm:block w-[45%]"></div>
                    </div>

                    <!-- Node 4 -->
                    <div class="relative flex flex-col sm:flex-row items-start sm:items-center justify-between">
                        <div class="absolute left-4 sm:left-1/2 w-4 h-4 rounded-full bg-dark border-2 border-accent transform -translate-x-1/2 flex items-center justify-center">
                            <span class="w-1.5 h-1.5 rounded-full bg-accent animate-ping"></span>
                        </div>
                        <div class="hidden sm:block w-[45%]"></div>
                        <div class="w-full sm:w-[45%] pl-12">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-wider">Phase IV</span>
                            <h3 class="text-lg font-bold text-white font-display mt-0.5">Systems Builder</h3>
                            <p class="text-xs text-gray-400 mt-1 max-w-sm">Synthesizing backend web architecture with embedded telemetry nodes, hardware sensors, and cloud pipelines.</p>
                        </div>
                    </div>

                    <!-- Node 5 -->
                    <div class="relative flex flex-col sm:flex-row items-start sm:items-center justify-between">
                        <div class="absolute left-4 sm:left-1/2 w-4 h-4 rounded-full bg-dark border-2 border-accent transform -translate-x-1/2 flex items-center justify-center">
                            <span class="w-1.5 h-1.5 rounded-full bg-accent"></span>
                        </div>
                        <div class="w-full sm:w-[45%] pl-12 sm:pl-0 sm:text-right">
                            <span class="text-xs font-semibold font-mono text-accent uppercase tracking-wider">Phase V</span>
                            <h3 class="text-lg font-bold text-white font-display mt-0.5 text-glow">AI Engineer</h3>
                            <p class="text-xs text-gray-400 mt-1 max-w-sm sm:ml-auto">Architecting end-to-end intelligent systems, machine learning pipelines, and responsive software solutions.</p>
                        </div>
                        <div class="hidden sm:block w-[45%]"></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 6. ACHIEVEMENTS SECTION -->
        <section id="achievements" class="py-12 reveal">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <div class="text-accent uppercase tracking-widest text-xs font-semibold mb-2">Track Record</div>
                <h2 class="text-3xl sm:text-4xl font-display font-bold text-white tracking-tight">Key Achievements</h2>
                <div class="w-12 h-1 bg-accent mx-auto mt-4 rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Achievement 1 -->
                <div class="glass-card p-6 rounded-2xl border-l-2 border-l-accent hover:border-l-accent transition-all duration-300 flex flex-col justify-between">
                    <div>
                        <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent mb-4">
                            <i data-lucide="trophy" class="w-4.5 h-4.5"></i>
                        </div>
                        <h3 class="text-sm font-semibold font-display text-white uppercase tracking-wider">TEXPERIA Hackathon</h3>
                        <p class="text-xs text-gray-400 mt-1 leading-relaxed">
                            2nd Prize Winner in the flagship technology challenge.
                        </p>
                    </div>
                    <span class="text-[10px] font-mono text-accent/80 font-bold uppercase tracking-widest mt-6 block">Silver Laureate</span>
                </div>

                <!-- Achievement 2 -->
                <div class="glass-card p-6 rounded-2xl border-l-2 border-l-accent hover:border-l-accent transition-all duration-300 flex flex-col justify-between">
                    <div>
                        <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent mb-4">
                            <i data-lucide="globe" class="w-4.5 h-4.5"></i>
                        </div>
                        <h3 class="text-sm font-semibold font-display text-white uppercase tracking-wider">ZYPH Global Summit</h3>
                        <p class="text-xs text-gray-400 mt-1 leading-relaxed">
                            Top 10 Finalist in the global hackathon competition.
                        </p>
                    </div>
                    <span class="text-[10px] font-mono text-accent/80 font-bold uppercase tracking-widest mt-6 block">Global Top 10</span>
                </div>

                <!-- Achievement 3 -->
                <div class="glass-card p-6 rounded-2xl border-l-2 border-l-accent hover:border-l-accent transition-all duration-300 flex flex-col justify-between">
                    <div>
                        <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent mb-4">
                            <i data-lucide="briefcase" class="w-4.5 h-4.5"></i>
                        </div>
                        <h3 class="text-sm font-semibold font-display text-white uppercase tracking-wider">AI Internships</h3>
                        <p class="text-xs text-gray-400 mt-1 leading-relaxed">
                            Completed multiple internships focused on AI and Full Stack developer environments.
                        </p>
                    </div>
                    <span class="text-[10px] font-mono text-accent/80 font-bold uppercase tracking-widest mt-6 block">Industry Applied</span>
                </div>

                <!-- Achievement 4 -->
                <div class="glass-card p-6 rounded-2xl border-l-2 border-l-accent hover:border-l-accent transition-all duration-300 flex flex-col justify-between">
                    <div>
                        <div class="w-8 h-8 rounded-lg bg-accent/10 border border-accent/20 flex items-center justify-center text-accent mb-4">
                            <i data-lucide="git-branch" class="w-4.5 h-4.5"></i>
                        </div>
                        <h3 class="text-sm font-semibold font-display text-white uppercase tracking-wider">Open Source</h3>
                        <p class="text-xs text-gray-400 mt-1 leading-relaxed">
                            Active contributor to AI libraries, IoT scripts, and public repositories.
                        </p>
                    </div>
                    <span class="text-[10px] font-mono text-accent/80 font-bold uppercase tracking-widest mt-6 block">Active Contributor</span>
                </div>
            </div>
        </section>

        <!-- 7. TECH STACK SECTION -->
        <section id="tech" class="py-12 reveal scroll-mt-24">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <div class="text-accent uppercase tracking-widest text-xs font-semibold mb-2">Systems Stack</div>
                <h2 class="text-3xl sm:text-4xl font-display font-bold text-white tracking-tight">Technologies I Master</h2>
                <div class="w-12 h-1 bg-accent mx-auto mt-4 rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
                <!-- Languages -->
                <div class="glass-card p-6 rounded-2xl">
                    <h3 class="text-sm font-bold font-display text-white mb-4 flex items-center gap-2 border-b border-white/5 pb-2">
                        <i data-lucide="code-2" class="w-4 h-4 text-accent"></i> Languages
                    </h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Python</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Java</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">JavaScript</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">C</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">C++</span>
                    </div>
                </div>

                <!-- AI -->
                <div class="glass-card p-6 rounded-2xl">
                    <h3 class="text-sm font-bold font-display text-white mb-4 flex items-center gap-2 border-b border-white/5 pb-2">
                        <i data-lucide="brain-circuit" class="w-4 h-4 text-accent"></i> AI & ML
                    </h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">TensorFlow</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Scikit-Learn</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Pandas</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">NumPy</span>
                    </div>
                </div>

                <!-- Backend -->
                <div class="glass-card p-6 rounded-2xl">
                    <h3 class="text-sm font-bold font-display text-white mb-4 flex items-center gap-2 border-b border-white/5 pb-2">
                        <i data-lucide="server" class="w-4 h-4 text-accent"></i> Backend
                    </h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">FastAPI</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Flask</span>
                    </div>
                </div>

                <!-- Frontend -->
                <div class="glass-card p-6 rounded-2xl">
                    <h3 class="text-sm font-bold font-display text-white mb-4 flex items-center gap-2 border-b border-white/5 pb-2">
                        <i data-lucide="layout" class="w-4 h-4 text-accent"></i> Frontend
                    </h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">React</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">HTML</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">CSS</span>
                    </div>
                </div>

                <!-- Databases -->
                <div class="glass-card p-6 rounded-2xl">
                    <h3 class="text-sm font-bold font-display text-white mb-4 flex items-center gap-2 border-b border-white/5 pb-2">
                        <i data-lucide="database" class="w-4 h-4 text-accent"></i> Database
                    </h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">MySQL</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">MongoDB</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Supabase</span>
                    </div>
                </div>

                <!-- Embedded -->
                <div class="glass-card p-6 rounded-2xl md:col-span-2 lg:col-span-1">
                    <h3 class="text-sm font-bold font-display text-white mb-4 flex items-center gap-2 border-b border-white/5 pb-2">
                        <i data-lucide="cpu" class="w-4 h-4 text-accent"></i> Embedded
                    </h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">ESP32</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">ESP8266</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">STM32</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Arduino</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Raspberry Pi</span>
                    </div>
                </div>

                <!-- Tools -->
                <div class="glass-card p-6 rounded-2xl md:col-span-2">
                    <h3 class="text-sm font-bold font-display text-white mb-4 flex items-center gap-2 border-b border-white/5 pb-2">
                        <i data-lucide="settings" class="w-4 h-4 text-accent"></i> Tools & OS
                    </h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Git</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">GitHub</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Linux</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">Docker</span>
                        <span class="text-[11px] font-mono px-2.5 py-1 rounded bg-white/5 hover:bg-accent/10 hover:text-accent transition-colors border border-white/5 cursor-default">VS Code</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- 8. VISION SECTION -->
        <section id="vision" class="py-12 reveal">
            <div class="glass-card p-8 sm:p-12 rounded-3xl relative overflow-hidden flex flex-col items-center text-center max-w-4xl mx-auto border border-accent/20">
                <div class="absolute -right-24 -bottom-24 w-48 h-48 bg-accent/5 rounded-full filter blur-2xl"></div>
                <div class="absolute -left-24 -top-24 w-48 h-48 bg-accent/5 rounded-full filter blur-2xl"></div>

                <div class="w-12 h-12 rounded-2xl bg-accent/10 border border-accent/20 flex items-center justify-center text-accent mb-6">
                    <i data-lucide="eye" class="w-6 h-6 text-glow"></i>
                </div>
                
                <h2 class="text-2xl sm:text-3xl font-display font-bold text-white tracking-tight mb-4">My Vision</h2>
                
                <p class="text-base sm:text-xl font-display text-gray-300 leading-relaxed max-w-2xl italic">
                    "To build intelligent technologies that make industries smarter, cities more sustainable, and everyday life more connected through the power of Artificial Intelligence and Embedded Systems."
                </p>
                
                <div class="w-12 h-0.5 bg-accent/30 mt-6"></div>
            </div>
        </section>

        <!-- 9. CONTACT SECTION -->
        <section id="contact" class="py-12 reveal scroll-mt-24">
            <div class="glass-card p-8 sm:p-16 rounded-3xl relative overflow-hidden flex flex-col items-center text-center max-w-4xl mx-auto border border-white/5">
                <div class="absolute top-0 right-0 w-24 h-24 bg-accent/5 rounded-full filter blur-xl"></div>

                <div class="text-accent uppercase tracking-widest text-xs font-semibold mb-2">Initiate Collaboration</div>
                <h2 class="text-3xl sm:text-5xl font-display font-bold text-white tracking-tight mb-6">
                    Let's Build Something <br>Intelligent Together
                </h2>
                <p class="text-sm sm:text-base text-gray-400 max-w-lg mb-8 leading-relaxed">
                    Have an interesting project, automation challenge, or machine learning application? Reach out, and let's structure the logic.
                </p>

                <!-- Social Connect Buttons -->
                <div class="flex flex-wrap justify-center items-center gap-4">
                    <a href="https://github.com/Sanjeevikumar-M" target="_blank" class="px-6 py-3.5 border border-white/10 hover:border-accent hover:text-accent rounded-full bg-white/5 hover:bg-accent/5 transition-all text-sm font-semibold flex items-center gap-2.5">
                        <i data-lucide="github" class="w-4 h-4"></i> GitHub
                    </a>
                    <a href="https://linkedin.com" target="_blank" class="px-6 py-3.5 border border-white/10 hover:border-accent hover:text-accent rounded-full bg-white/5 hover:bg-accent/5 transition-all text-sm font-semibold flex items-center gap-2.5">
                        <i data-lucide="linkedin" class="w-4 h-4"></i> LinkedIn
                    </a>
                    <a href="mailto:sanjeevi.embedded.ai@gmail.com" class="glow-btn px-6 py-3.5 bg-accent hover:bg-accent/90 text-white rounded-full text-sm font-semibold box-glow flex items-center gap-2.5 transition-all">
                        <i data-lucide="mail" class="w-4 h-4"></i> Email Me
                    </a>
                </div>
            </div>
        </section>

    </main>

    <!-- FOOTER -->
    <footer class="border-t border-white/5 py-12 relative z-10 bg-dark">
        <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-6 text-center md:text-left">
            <div>
                <div class="font-display font-bold text-lg tracking-wider text-white">
                    SANJEEVIKUMAR M.
                </div>
                <p class="text-xs text-gray-500 mt-1">
                    Building the future through AI, Engineering, and Innovation.
                </p>
            </div>
            
            <div class="flex flex-col items-center md:items-end gap-2">
                <span class="text-xs text-gray-500">© 2026 Sanjeevikumar M. All rights reserved.</span>
                <span class="text-[10px] font-mono text-gray-600">Built with pure HTML/CSS/JS telemetry layout.</span>
            </div>
        </div>
    </footer>

    <!-- INTERACTIVE JAVASCRIPT SYSTEM -->
    <script>
        // Init Lucide Vector Icons
        lucide.createIcons();

        // 1. Mobile Menu drawer toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileDrawer = document.getElementById('mobileDrawer');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileDrawer.classList.toggle('hidden');
        });

        function toggleDrawer() {
            mobileDrawer.classList.add('hidden');
        }

        // 2. Sticky Navbar Blur adjustment on Scroll
        const mainHeader = document.getElementById('mainHeader');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                mainHeader.classList.add('py-1');
                mainHeader.classList.remove('py-4');
                mainHeader.style.background = 'rgba(5, 5, 5, 0.85)';
            } else {
                mainHeader.classList.remove('py-1');
                mainHeader.classList.add('py-4');
                mainHeader.style.background = 'rgba(5, 5, 5, 0.75)';
            }
        });

        // 3. Typewriter Effect for the Subheadlines
        const words = [
            "AI Engineer",
            "Full Stack Developer",
            "Systems Builder"
        ];
        let wordIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typedTextEl = document.getElementById('typed-text');
        const typeSpeed = 100;
        const eraseSpeed = 60;
        const delayBetweenWords = 2000;

        function type() {
            const currentWord = words[wordIndex];
            
            if (isDeleting) {
                typedTextEl.textContent = currentWord.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typedTextEl.textContent = currentWord.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentWord.length) {
                isDeleting = true;
                setTimeout(type, delayBetweenWords);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                wordIndex = (wordIndex + 1) % words.length;
                setTimeout(type, 500);
            } else {
                setTimeout(type, isDeleting ? eraseSpeed : typeSpeed);
            }
        }
        
        // Start typewriter
        document.addEventListener('DOMContentLoaded', () => {
            setTimeout(type, 1000);
        });

        // 4. Custom high-performance Scroll-Reveal System using IntersectionObserver
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };

        const revealObserver = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                    // Once animated, no need to watch again
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        const elementsToReveal = document.querySelectorAll('.reveal');
        elementsToReveal.forEach((el, index) => {
            // Stagger animation timing slightly for adjacent elements
            el.style.transitionDelay = `${(index % 3) * 0.1}s`;
            revealObserver.observe(el);
        });

        // 5. Canvas Neural Network Particle System
        const canvas = document.getElementById('particleCanvas');
        const ctx = canvas.getContext('2d');
        
        let width = canvas.width = window.innerWidth;
        let height = canvas.height = window.innerHeight;

        const particles = [];
        const maxParticles = Math.min(100, Math.floor((width * height) / 15000)); // Dynamic particle count based on resolution
        const connectionDistance = 120;
        
        // Track Cursor
        const mouse = {
            x: null,
            y: null,
            radius: 180
        };

        window.addEventListener('mousemove', (e) => {
            mouse.x = e.clientX;
            mouse.y = e.clientY;
        });

        window.addEventListener('mouseleave', () => {
            mouse.x = null;
            mouse.y = null;
        });

        window.addEventListener('resize', () => {
            width = canvas.width = window.innerWidth;
            height = canvas.height = window.innerHeight;
        });

        // Particle Class
        class Particle {
            constructor() {
                this.x = Math.random() * width;
                this.y = Math.random() * height;
                this.vx = (Math.random() - 0.5) * 0.4;
                this.vy = (Math.random() - 0.5) * 0.4;
                this.radius = Math.random() * 1.5 + 1;
            }

            update() {
                this.x += this.vx;
                this.y += this.vy;

                // Wall bounces
                if (this.x < 0 || this.x > width) this.vx *= -1;
                if (this.y < 0 || this.y > height) this.vy *= -1;

                // Mouse interaction / push away slightly
                if (mouse.x !== null && mouse.y !== null) {
                    const dx = mouse.x - this.x;
                    const dy = mouse.y - this.y;
                    const dist = Math.hypot(dx, dy);
                    if (dist < mouse.radius) {
                        const force = (mouse.radius - dist) / mouse.radius;
                        const angle = Math.atan2(dy, dx);
                        // Shift away
                        this.x -= Math.cos(angle) * force * 0.6;
                        this.y -= Math.sin(angle) * force * 0.6;
                    }
                }
            }

            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(255, 0, 60, 0.4)'; // Subtle deep red nodes
                ctx.fill();
            }
        }

        // Initialize Particles
        for (let i = 0; i < maxParticles; i++) {
            particles.push(new Particle());
        }

        // Draw connections
        function drawLines() {
            for (let i = 0; i < particles.length; i++) {
                for (let j = i + 1; j < particles.length; j++) {
                    const p1 = particles[i];
                    const p2 = particles[j];
                    const dx = p1.x - p2.x;
                    const dy = p1.y - p2.y;
                    const dist = Math.hypot(dx, dy);

                    if (dist < connectionDistance) {
                        const alpha = (1 - dist / connectionDistance) * 0.08;
                        ctx.strokeStyle = `rgba(255, 0, 60, ${alpha})`;
                        ctx.lineWidth = 0.8;
                        ctx.beginPath();
                        ctx.moveTo(p1.x, p1.y);
                        ctx.lineTo(p2.x, p2.y);
                        ctx.stroke();
                    }
                }

                // Interactive Cursor Lines
                if (mouse.x !== null && mouse.y !== null) {
                    const p = particles[i];
                    const dx = mouse.x - p.x;
                    const dy = mouse.y - p.y;
                    const dist = Math.hypot(dx, dy);

                    if (dist < mouse.radius) {
                        const alpha = (1 - dist / mouse.radius) * 0.15;
                        ctx.strokeStyle = `rgba(255, 0, 60, ${alpha})`;
                        ctx.lineWidth = 1.0;
                        ctx.beginPath();
                        ctx.moveTo(p.x, p.y);
                        ctx.lineTo(mouse.x, mouse.y);
                        ctx.stroke();
                    }
                }
            }
        }

        // Animation Loop
        function animate() {
            ctx.clearRect(0, 0, width, height);
            
            particles.forEach(p => {
                p.update();
                p.draw();
            });

            drawLines();
            requestAnimationFrame(animate);
        }

        // Run Background canvas engine
        animate();
    </script>
</body>
</html>
