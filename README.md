<!--
███╗   ███╗██████╗     ███████╗ █████╗ ██████╗ ██╗ ██████╗ ██╗   ██╗███████╗
████╗ ████║██╔══██╗    ██╔════╝██╔══██╗██╔══██╗██║██╔═══██╗██║   ██║██╔════╝
██╔████╔██║██████╔╝    ███████╗███████║██║  ██║██║██║   ██║██║   ██║█████╗  
██║╚██╔╝██║██╔══██╗    ╚════██║██╔══██║██║  ██║██║██║▄▄ ██║██║   ██║██╔══╝  
██║ ╚═╝ ██║██████╔╝    ███████║██║  ██║██████╔╝██║╚██████╔╝╚██████╔╝███████╗
╚═╝     ╚═╝╚═════╝     ╚══════╝╚═╝  ╚═╝╚═════╝ ╚═╝ ╚══▀▀═╝  ╚═════╝ ╚══════╝
-->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>Md Sadique Amin – Full Stack AI Engineer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
    <script src="https://unpkg.com/typed.js@2.0.16/dist/typed.umd.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background: #0a192f;
            color: #e2e8f0;
            overflow-x: hidden;
        }
        .digital-font {
            font-family: 'Orbitron', monospace;
        }
        .gradient-text {
            background: linear-gradient(45deg, #22d3ee, #0ea5e9, #3b82f6, #8b5cf6);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 3s ease infinite;
        }
        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        .neon-card {
            background: rgba(15, 23, 42, 0.6);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(34, 211, 238, 0.2);
            border-radius: 1.5rem;
            transition: all 0.3s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .neon-card:hover {
            border-color: rgba(34, 211, 238, 0.7);
            box-shadow: 0 0 30px rgba(34, 211, 238, 0.3);
            transform: translateY(-6px);
        }
        .custom-cursor {
            width: 20px;
            height: 20px;
            border: 2px solid #22d3ee;
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            mix-blend-mode: difference;
        }
        .custom-cursor-dot {
            width: 4px;
            height: 4px;
            background: #22d3ee;
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 9999;
        }
        .scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            width: 0%;
            height: 3px;
            background: linear-gradient(90deg, #22d3ee, #8b5cf6);
            z-index: 10000;
        }
        .reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }
        .reveal.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .skill-ring svg {
            transform: rotate(-90deg);
        }
        .progress-ring {
            stroke-dasharray: 314;
            stroke-dashoffset: 314;
            transition: stroke-dashoffset 1.5s ease-out;
        }
        .project-filter.active {
            background: rgba(34, 211, 238, 0.3);
            border-color: rgba(34, 211, 238, 0.8);
        }
        #three-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            pointer-events: none;
        }
        .container {
            position: relative;
            z-index: 2;
        }
        .btn-magnetic {
            transition: transform 0.2s cubic-bezier(0.23, 1, 0.32, 1);
        }
    </style>
</head>
<body>
    <div class="scroll-progress"></div>
    <canvas id="three-canvas"></canvas>
    <div class="custom-cursor"></div>
    <div class="custom-cursor-dot"></div>

    <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-12">
        <!-- ================= HERO SECTION ================= -->
        <div class="min-h-screen flex flex-col justify-center items-center text-center relative z-10">
            <div class="mb-6 flex flex-wrap justify-center gap-3">
                <span class="px-4 py-2 rounded-full bg-cyan-900/40 border border-cyan-400 text-cyan-400 text-sm digital-font">🚀 FULL STACK DEV</span>
                <span class="px-4 py-2 rounded-full bg-purple-900/40 border border-purple-400 text-purple-400 text-sm digital-font">🤖 AI ENGINEER</span>
                <span class="px-4 py-2 rounded-full bg-green-900/40 border border-green-400 text-green-400 text-sm digital-font">📊 DATA SCIENTIST</span>
            </div>
            <h1 class="text-5xl md:text-7xl font-bold mb-4">
                <span class="gradient-text">Md Sadique</span><br>
                <span class="text-slate-300">Amin</span>
            </h1>
            <div class="text-2xl md:text-4xl font-bold mb-6 h-20">
                <span id="typed-text" class="gradient-text digital-font"></span>
                <span class="typing-cursor inline-block w-1 h-8 bg-cyan-400 ml-1 animate-pulse"></span>
            </div>
            <p class="text-lg text-slate-400 max-w-2xl mb-10">
                Crafting intelligent solutions with <span class="text-cyan-400 font-bold">Java</span>, <span class="text-cyan-400 font-bold">Spring Boot</span>, 
                <span class="text-cyan-400 font-bold">Python</span>, <span class="text-purple-400 font-bold">Machine Learning</span> & 
                <span class="text-green-400 font-bold">Data Science</span>.
            </p>
            <div class="flex flex-wrap gap-4 justify-center">
                <a href="#contact" class="btn-magnetic px-8 py-3 bg-gradient-to-r from-cyan-500 to-blue-600 rounded-lg font-semibold shadow-lg shadow-cyan-500/25 hover:scale-105 transition">📧 Hire Me</a>
                <a href="#projects" class="btn-magnetic px-8 py-3 border-2 border-cyan-400 text-cyan-400 rounded-lg font-semibold hover:bg-cyan-400/10 transition hover:scale-105">🔍 View Projects</a>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 mt-16 w-full max-w-3xl">
                <div class="text-center p-4 rounded-xl bg-slate-800/30 border border-slate-700">
                    <div class="text-3xl font-bold text-cyan-400 digital-font counter" data-target="20">0</div>
                    <div class="text-sm text-slate-400">Projects</div>
                </div>
                <div class="text-center p-4 rounded-xl bg-slate-800/30 border border-slate-700">
                    <div class="text-3xl font-bold text-purple-400 digital-font counter" data-target="6">0</div>
                    <div class="text-sm text-slate-400">AI Projects</div>
                </div>
                <div class="text-center p-4 rounded-xl bg-slate-800/30 border border-slate-700">
                    <div class="text-3xl font-bold text-cyan-400 digital-font counter" data-target="6">0</div>
                    <div class="text-sm text-slate-400">Months Exp</div>
                </div>
                <div class="text-center p-4 rounded-xl bg-slate-800/30 border border-slate-700">
                    <div class="text-3xl font-bold text-green-400 digital-font counter" data-target="25">0</div>
                    <div class="text-sm text-slate-400">Skills</div>
                </div>
            </div>
        </div>

        <!-- ================= ABOUT ================= -->
        <div class="py-20 reveal">
            <h2 class="text-4xl font-bold text-center mb-16"><span class="gradient-text digital-font">About Me</span></h2>
            <div class="grid md:grid-cols-2 gap-12">
                <div class="neon-card p-8">
                    <h3 class="text-2xl font-bold text-cyan-400 mb-6 flex items-center"><i class='bx bx-user-circle mr-3'></i> Profile</h3>
                    <div class="space-y-4">
                        <div class="flex items-center gap-4"><i class='bx bx-calendar text-cyan-400 text-xl'></i><span><strong>DOB:</strong> 05/03/2002</span></div>
                        <div class="flex items-center gap-4"><i class='bx bx-map text-cyan-400 text-xl'></i><span><strong>Location:</strong> Begusarai, Bihar, India</span></div>
                        <div class="flex items-center gap-4"><i class='bx bx-envelope text-cyan-400 text-xl'></i><span><strong>Email:</strong> mdsadiqueamin721786@gmail.com</span></div>
                        <div class="flex items-center gap-4"><i class='bx bx-phone text-cyan-400 text-xl'></i><span><strong>Phone:</strong> +91 9318302850</span></div>
                    </div>
                    <div class="mt-8 pt-6 border-t border-slate-700">
                        <h4 class="text-lg font-semibold text-cyan-400 mb-3">Objective</h4>
                        <p class="text-slate-300">Passionate Software Engineer with expertise in Full Stack Development, Artificial Intelligence, and Data Science. Seeking challenging opportunities to leverage my skills in building innovative, privacy-first solutions.</p>
                    </div>
                </div>
                <div class="neon-card p-8">
                    <h3 class="text-2xl font-bold text-cyan-400 mb-6 flex items-center"><i class='bx bx-bulb mr-3'></i> Expertise Areas</h3>
                    <div class="space-y-4">
                        <div><i class='bx bx-code-curly text-cyan-400 text-xl mr-3'></i> <strong>Full Stack Development</strong><br>Java, Spring Boot, Python, Django, React, MySQL</div>
                        <div><i class='bx bx-brain text-purple-400 text-xl mr-3'></i> <strong>AI/ML Engineering</strong><br>TensorFlow, PyTorch, NLP, Computer Vision</div>
                        <div><i class='bx bx-line-chart text-green-400 text-xl mr-3'></i> <strong>Data Science</strong><br>Pandas, NumPy, Tableau, Predictive Modeling</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ================= SKILLS ================= -->
        <div class="py-20 reveal">
            <h2 class="text-4xl font-bold text-center mb-16"><span class="gradient-text digital-font">Technical Skills</span></h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div class="neon-card p-6 text-center">
                    <div class="skill-ring mx-auto mb-4 w-32 h-32 relative">
                        <svg viewBox="0 0 120 120"><circle cx="60" cy="60" r="50" fill="none" stroke="#1e293b" stroke-width="8"/><circle class="progress-ring" cx="60" cy="60" r="50" fill="none" stroke="url(#g1)" stroke-width="8" data-percent="92"/></svg>
                        <div class="absolute inset-0 flex items-center justify-center"><i class='bx bx-layer text-4xl text-cyan-400'></i></div>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Full Stack</h3>
                    <div class="flex flex-wrap justify-center gap-2 mt-3"><span class="px-3 py-1 bg-cyan-900/30 rounded-full text-xs">Java</span><span class="px-3 py-1 bg-cyan-900/30 rounded-full text-xs">Spring Boot</span><span class="px-3 py-1 bg-cyan-900/30 rounded-full text-xs">React</span></div>
                </div>
                <div class="neon-card p-6 text-center">
                    <div class="skill-ring mx-auto mb-4 w-32 h-32 relative">
                        <svg viewBox="0 0 120 120"><circle cx="60" cy="60" r="50" fill="none" stroke="#1e293b" stroke-width="8"/><circle class="progress-ring" cx="60" cy="60" r="50" fill="none" stroke="url(#g2)" stroke-width="8" data-percent="88"/></svg>
                        <div class="absolute inset-0 flex items-center justify-center"><i class='bx bx-brain text-4xl text-purple-400'></i></div>
                    </div>
                    <h3 class="text-xl font-bold mb-2">AI/ML</h3>
                    <div class="flex flex-wrap justify-center gap-2 mt-3"><span class="px-3 py-1 bg-purple-900/30 rounded-full text-xs">TensorFlow</span><span class="px-3 py-1 bg-purple-900/30 rounded-full text-xs">PyTorch</span><span class="px-3 py-1 bg-purple-900/30 rounded-full text-xs">NLP</span></div>
                </div>
                <div class="neon-card p-6 text-center">
                    <div class="skill-ring mx-auto mb-4 w-32 h-32 relative">
                        <svg viewBox="0 0 120 120"><circle cx="60" cy="60" r="50" fill="none" stroke="#1e293b" stroke-width="8"/><circle class="progress-ring" cx="60" cy="60" r="50" fill="none" stroke="url(#g3)" stroke-width="8" data-percent="85"/></svg>
                        <div class="absolute inset-0 flex items-center justify-center"><i class='bx bx-line-chart text-4xl text-green-400'></i></div>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Data Science</h3>
                    <div class="flex flex-wrap justify-center gap-2 mt-3"><span class="px-3 py-1 bg-green-900/30 rounded-full text-xs">Pandas</span><span class="px-3 py-1 bg-green-900/30 rounded-full text-xs">NumPy</span><span class="px-3 py-1 bg-green-900/30 rounded-full text-xs">Tableau</span></div>
                </div>
                <div class="neon-card p-6 text-center">
                    <div class="skill-ring mx-auto mb-4 w-32 h-32 relative">
                        <svg viewBox="0 0 120 120"><circle cx="60" cy="60" r="50" fill="none" stroke="#1e293b" stroke-width="8"/><circle class="progress-ring" cx="60" cy="60" r="50" fill="none" stroke="url(#g4)" stroke-width="8" data-percent="80"/></svg>
                        <div class="absolute inset-0 flex items-center justify-center"><i class='bx bx-cog text-4xl text-yellow-400'></i></div>
                    </div>
                    <h3 class="text-xl font-bold mb-2">DevOps & Tools</h3>
                    <div class="flex flex-wrap justify-center gap-2 mt-3"><span class="px-3 py-1 bg-yellow-900/30 rounded-full text-xs">Docker</span><span class="px-3 py-1 bg-yellow-900/30 rounded-full text-xs">Git</span><span class="px-3 py-1 bg-yellow-900/30 rounded-full text-xs">AWS</span></div>
                </div>
            </div>
        </div>

        <!-- ================= PROJECTS ================= -->
        <div class="py-20 reveal">
            <h2 class="text-4xl font-bold text-center mb-16"><span class="gradient-text digital-font">Featured Projects</span></h2>
            <div class="flex flex-wrap justify-center gap-3 mb-12">
                <button class="project-filter active px-5 py-2 rounded-full bg-cyan-900/30 border border-cyan-400 text-cyan-400" data-filter="all">All</button>
                <button class="project-filter px-5 py-2 rounded-full bg-purple-900/30 border border-purple-400 text-purple-400" data-filter="ai">AI/ML</button>
                <button class="project-filter px-5 py-2 rounded-full bg-green-900/30 border border-green-400 text-green-400" data-filter="ds">Data Science</button>
                <button class="project-filter px-5 py-2 rounded-full bg-cyan-900/30 border border-cyan-400 text-cyan-400" data-filter="web">Web Dev</button>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="projects-grid">
                <!-- Projects will be populated by JS -->
            </div>
        </div>

        <!-- ================= AI AGENT MSA ================= -->
        <div class="py-20 reveal">
            <h2 class="text-4xl font-bold text-center mb-16"><span class="ai-gradient digital-font">🚀 MSA – Ultimate Offline AI Agent</span></h2>
            <div class="neon-card p-8 max-w-4xl mx-auto">
                <div class="flex flex-col md:flex-row gap-8 items-center">
                    <div class="flex-1">
                        <h3 class="text-2xl font-bold text-cyan-400 mb-3">⚡ Your Personal AI — Fully Offline, Private, Powerful</h3>
                        <p class="text-slate-300 mb-4">MSA is a next‑generation offline AI assistant that runs locally on your laptop and seamlessly controls your mobile device over Wi‑Fi. No cloud. No API. No tracking. Just pure private AI power.</p>
                        <ul class="space-y-2 text-sm">
                            <li>🎙️ <strong>Voice Intelligence</strong> – Offline speech recognition (Vosk/Whisper) + speaker verification</li>
                            <li>🧠 <strong>AI Brain</strong> – Local Llama 2 (GGUF) with smart decision‑making</li>
                            <li>📱 <strong>Multi‑Device Control</strong> – Control Android over Wi‑Fi (ADB)</li>
                            <li>👁️ <strong>Computer Vision</strong> – OpenCV, real‑time object detection</li>
                            <li>🔒 <strong>Privacy First</strong> – 100% offline, encrypted local storage</li>
                        </ul>
                        <div class="mt-6 flex gap-3">
                            <a href="https://github.com/Sadique721/AI-Agent-MSA" class="px-4 py-2 bg-cyan-600 rounded-lg text-sm font-semibold hover:bg-cyan-700 transition">🔗 Repository</a>
                            <a href="#" class="px-4 py-2 border border-cyan-400 rounded-lg text-sm font-semibold hover:bg-cyan-400/10 transition">📖 Documentation</a>
                        </div>
                    </div>
                    <div class="flex-1 text-center">
                        <i class='bx bx-chip text-8xl text-cyan-400'></i>
                        <p class="text-sm text-slate-500 mt-2">Offline AI – Your data stays with you.</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- ================= EXPERIENCE & EDUCATION ================= -->
        <div class="py-20 reveal">
            <h2 class="text-4xl font-bold text-center mb-16"><span class="gradient-text digital-font">Experience & Education</span></h2>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="neon-card p-8">
                    <h3 class="text-2xl font-bold text-cyan-400 mb-6">💼 Work Experience</h3>
                    <div class="mb-6">
                        <h4 class="text-xl font-semibold">Web Development Intern</h4>
                        <p class="text-cyan-300 text-sm">TechnoFly Solutions, Bengaluru | Sep 2022 – Jan 2023</p>
                        <ul class="list-disc list-inside text-slate-400 mt-2 text-sm">
                            <li>Developed 5+ dynamic client websites using Django and React.js</li>
                            <li>Optimized SQL queries, reducing page load times by 40%</li>
                            <li>Collaborated on responsive design and REST APIs</li>
                        </ul>
                    </div>
                    <div>
                        <h4 class="text-xl font-semibold">Industrial Trainee</h4>
                        <p class="text-cyan-300 text-sm">BSNL, Hyderabad | Jun 2022 – Jul 2022</p>
                        <ul class="list-disc list-inside text-slate-400 mt-2 text-sm">
                            <li>Exposure to telecom networks and cybersecurity protocols</li>
                            <li>Assisted in network troubleshooting and maintenance</li>
                        </ul>
                    </div>
                </div>
                <div class="neon-card p-8">
                    <h3 class="text-2xl font-bold text-cyan-400 mb-6">🎓 Education</h3>
                    <div class="space-y-4">
                        <div><span class="font-bold">B.E. Computer Science</span> – Government Engineering College, Patan (2023–2026) <br><span class="text-cyan-400">7.9 CGPA</span></div>
                        <div><span class="font-bold">Diploma in CS</span> – MANUU Polytechnic, Bangalore (2021–2023) <br><span class="text-cyan-400">87.3%</span></div>
                        <div><span class="font-bold">HSC (12th)</span> – G.D. College, Begusarai (2020) <br><span class="text-cyan-400">66%</span></div>
                        <div><span class="font-bold">SSC (10th)</span> – Nerly Inter College, Begusarai (2018) <br><span class="text-cyan-400">72.8%</span></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ================= GITHUB STATS ================= -->
        <div class="py-20 reveal">
            <h2 class="text-4xl font-bold text-center mb-16"><span class="gradient-text digital-font">GitHub Analytics</span></h2>
            <div class="flex flex-wrap justify-center gap-6">
                <img src="https://github-readme-stats.vercel.app/api?username=Sadique721&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0a192f&title_color=22d3ee&icon_color=8b5cf6" alt="GitHub Stats" class="rounded-xl shadow-lg">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sadique721&layout=compact&theme=tokyonight&hide_border=true&bg_color=0a192f&title_color=22d3ee" alt="Top Languages" class="rounded-xl shadow-lg">
            </div>
            <div class="mt-8 text-center">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=Sadique721&theme=tokyonight&hide_border=true&background=0a192f&stroke=22d3ee&ring=22d3ee&fire=8b5cf6" alt="GitHub Streak" class="mx-auto rounded-xl shadow-lg">
            </div>
            <div class="mt-8">
                <img src="https://github-readme-activity-graph.vercel.app/graph?username=Sadique721&theme=tokyo-night&hide_border=true&bg_color=0a192f&color=22d3ee&line=8b5cf6&point=ffffff&area=true" alt="Activity Graph" class="rounded-xl shadow-lg">
            </div>
        </div>

        <!-- ================= CONTACT ================= -->
        <div id="contact" class="py-20 reveal">
            <h2 class="text-4xl font-bold text-center mb-16"><span class="gradient-text digital-font">Get In Touch</span></h2>
            <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <div class="neon-card p-8">
                    <h3 class="text-2xl font-bold text-cyan-400 mb-6 flex items-center"><i class='bx bx-conversation mr-3'></i> Let's Connect</h3>
                    <div class="space-y-4">
                        <div class="flex items-center gap-4"><i class='bx bx-envelope text-2xl text-cyan-400'></i> mdsadiqueamin721786@gmail.com</div>
                        <div class="flex items-center gap-4"><i class='bx bx-phone text-2xl text-cyan-400'></i> +91 9318302850</div>
                        <div class="flex items-center gap-4"><i class='bx bx-map text-2xl text-cyan-400'></i> Begusarai, Bihar – 851126</div>
                    </div>
                    <div class="flex gap-4 mt-8">
                        <a href="https://github.com/Sadique721" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-slate-900 transition"><i class='bx bxl-github text-xl'></i></a>
                        <a href="https://www.linkedin.com/in/md-sadique-amin-b6a948198/" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-slate-900 transition"><i class='bx bxl-linkedin text-xl'></i></a>
                        <a href="https://www.youtube.com/@mdsadiqueamin721" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-slate-900 transition"><i class='bx bxl-youtube text-xl'></i></a>
                        <a href="https://www.instagram.com/mdsadiqueamin721/" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-cyan-400 hover:bg-cyan-400 hover:text-slate-900 transition"><i class='bx bxl-instagram text-xl'></i></a>
                    </div>
                </div>
                <div class="neon-card p-8">
                    <h3 class="text-2xl font-bold text-cyan-400 mb-6 flex items-center"><i class='bx bx-send mr-3'></i> Send Message</h3>
                    <form id="contact-form" class="space-y-4">
                        <input type="text" name="name" placeholder="Your Name" required class="w-full p-3 bg-slate-800 border border-slate-700 rounded-lg focus:outline-none focus:border-cyan-400">
                        <input type="email" name="email" placeholder="Your Email" required class="w-full p-3 bg-slate-800 border border-slate-700 rounded-lg focus:outline-none focus:border-cyan-400">
                        <input type="text" name="subject" placeholder="Subject" required class="w-full p-3 bg-slate-800 border border-slate-700 rounded-lg focus:outline-none focus:border-cyan-400">
                        <textarea name="message" rows="4" placeholder="Your Message" required class="w-full p-3 bg-slate-800 border border-slate-700 rounded-lg focus:outline-none focus:border-cyan-400"></textarea>
                        <button type="submit" class="w-full py-3 bg-gradient-to-r from-cyan-500 to-blue-600 rounded-lg font-semibold hover:scale-[1.02] transition">Send →</button>
                    </form>
                </div>
            </div>
        </div>

        <footer class="text-center py-8 border-t border-slate-800 text-slate-500 text-sm">
            © 2026 Md Sadique Amin. Built with ❤️ and 🚀 | Privacy-first philosophy
        </footer>
    </div>

    <svg width="0" height="0" style="position:absolute">
        <defs>
            <linearGradient id="g1" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" stop-color="#22d3ee"/><stop offset="100%" stop-color="#0ea5e9"/></linearGradient>
            <linearGradient id="g2" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" stop-color="#8b5cf6"/><stop offset="100%" stop-color="#a78bfa"/></linearGradient>
            <linearGradient id="g3" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" stop-color="#10b981"/><stop offset="100%" stop-color="#34d399"/></linearGradient>
            <linearGradient id="g4" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" stop-color="#f59e0b"/><stop offset="100%" stop-color="#fbbf24"/></linearGradient>
        </defs>
    </svg>

    <script>
        // ================= THREE.JS BACKGROUND =================
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({ canvas: document.getElementById('three-canvas'), alpha: true });
        renderer.setSize(window.innerWidth, window.innerHeight);
        renderer.setPixelRatio(window.devicePixelRatio);
        const geometry = new THREE.BufferGeometry();
        const count = 2000;
        const positions = new Float32Array(count * 3);
        for (let i = 0; i < count; i++) {
            positions[i*3] = (Math.random() - 0.5) * 100;
            positions[i*3+1] = (Math.random() - 0.5) * 60;
            positions[i*3+2] = (Math.random() - 0.5) * 50 - 20;
        }
        geometry.setAttribute('position', new THREE.BufferAttribute(positions, 3));
        const material = new THREE.PointsMaterial({ color: 0x22d3ee, size: 0.08, transparent: true, opacity: 0.6, blending: THREE.AdditiveBlending });
        const points = new THREE.Points(geometry, material);
        scene.add(points);
        camera.position.z = 30;
        let mouseX = 0, mouseY = 0;
        document.addEventListener('mousemove', (e) => {
            mouseX = (e.clientX / window.innerWidth) * 2 - 1;
            mouseY = (e.clientY / window.innerHeight) * 2 - 1;
        });
        function animate() {
            requestAnimationFrame(animate);
            points.rotation.y += 0.0005 + mouseX * 0.0002;
            points.rotation.x += 0.0003 + mouseY * 0.0002;
            renderer.render(scene, camera);
        }
        animate();
        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });

        // ================= TYPED.JS =================
        new Typed('#typed-text', {
            strings: ['Full Stack Developer','Java Developer','Python Developer','AI Engineer','Data Scientist','Spring Boot Expert'],
            typeSpeed: 50, backSpeed: 30, backDelay: 2000, loop: true, showCursor: false
        });

        // ================= SCROLL REVEAL =================
        const reveals = document.querySelectorAll('.reveal');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.classList.add('visible');
            });
        }, { threshold: 0.1 });
        reveals.forEach(r => observer.observe(r));

        // ================= COUNTER ANIMATION =================
        const counters = document.querySelectorAll('.counter');
        const counterObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const el = entry.target;
                    const target = parseInt(el.getAttribute('data-target'));
                    let current = 0;
                    const increment = target / 50;
                    const timer = setInterval(() => {
                        current += increment;
                        if (current >= target) {
                            el.textContent = target;
                            clearInterval(timer);
                        } else {
                            el.textContent = Math.floor(current);
                        }
                    }, 30);
                    counterObserver.unobserve(el);
                }
            });
        }, { threshold: 0.5 });
        counters.forEach(c => counterObserver.observe(c));

        // ================= SKILL RINGS =================
        const rings = document.querySelectorAll('.progress-ring');
        const ringObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const ring = entry.target;
                    const percent = parseFloat(ring.getAttribute('data-percent'));
                    const circumference = 314;
                    const offset = circumference - (percent / 100) * circumference;
                    ring.style.strokeDashoffset = offset;
                    ringObserver.unobserve(ring);
                }
            });
        }, { threshold: 0.5 });
        rings.forEach(r => ringObserver.observe(r));

        // ================= PROJECTS DATA =================
        const projects = [
            { name: 'Ethical Hacking Portal', desc: 'Cybersecurity learning platform with Django, role-based access', tech: 'Django, Python, SQL', type: 'web', link: 'https://github.com/Sadique721/ethical-hacking-portal', img: 'https://images.unsplash.com/photo-1550751827-4bd374c3f58b?w=400&q=80' },
            { name: 'Advanced Scientific Calculator', desc: 'Pure JS calculator with 15+ scientific functions', tech: 'HTML/CSS/JS', type: 'web', link: 'https://github.com/Sadique721/Advanced-Scientific-Calculator', img: 'https://images.unsplash.com/photo-1587145820266-a5951ee6f620?w=400&q=80' },
            { name: 'Interactive Digital Clock', desc: 'Auto day/night mode, custom sound effects', tech: 'JavaScript, Canvas', type: 'web', link: 'https://github.com/Sadique721/Interactive-Digital-Clock', img: 'https://images.unsplash.com/photo-1516035069371-29a1b244cc32?w=400&q=80' },
            { name: 'Recipe Finder Pro', desc: 'Dark mode UI, instant search, hover effects', tech: 'React, API', type: 'web', link: 'https://github.com/Sadique721/Recipe-finder-pro-', img: 'https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400&q=80' },
            { name: 'Modern Analog Clock', desc: 'Real-time, color-coded hands, CSS powered', tech: 'CSS, JS', type: 'web', link: 'https://github.com/Sadique721/Modern-Analog-Clock', img: 'https://images.unsplash.com/photo-1501139083538-0139583c060f?w=400&q=80' },
            { name: 'Entitykart E-commerce', desc: 'Spring Boot + React + JWT', tech: 'Spring Boot, React, MySQL', type: 'web', link: 'https://github.com/Sadique721/Entitykart', img: 'https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?w=400&q=80' },
            { name: 'Intelligent Image Recognition', desc: 'Deep learning with 95% accuracy', tech: 'TensorFlow, OpenCV', type: 'ai', link: '#', img: 'https://images.unsplash.com/photo-1677442135703-1787eea5ce01?w=400&q=80' },
            { name: 'Sentiment Analysis Chatbot', desc: 'BERT-based conversational AI', tech: 'PyTorch, Flask', type: 'ai', link: '#', img: 'https://images.unsplash.com/photo-1531746790731-6c087fecd65a?w=400&q=80' },
            { name: 'Predictive Analytics Dashboard', desc: 'ML forecasting & visualizations', tech: 'Pandas, Scikit-learn, Tableau', type: 'ds', link: '#', img: 'https://images.unsplash.com/photo-1460925895917-afdab827c52f?w=400&q=80' },
            { name: 'Real-time Data Streaming', desc: 'Kafka + Spark + AWS pipeline', tech: 'Apache Spark, Kafka', type: 'ds', link: '#', img: 'https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=400&q=80' }
        ];
        const grid = document.getElementById('projects-grid');
        function renderProjects(filter) {
            grid.innerHTML = '';
            projects.filter(p => filter === 'all' || p.type === filter).forEach(p => {
                const card = document.createElement('div');
                card.className = 'neon-card rounded-2xl overflow-hidden group';
                card.innerHTML = `
                    <div class="h-48 overflow-hidden"><img src="${p.img}" class="w-full h-full object-cover group-hover:scale-110 transition duration-500"></div>
                    <div class="p-6"><h3 class="text-xl font-bold text-cyan-400 mb-2">${p.name}</h3><p class="text-slate-400 text-sm mb-3">${p.desc}</p><div class="flex flex-wrap gap-2 mb-4">${p.tech.split(',').map(t => `<span class="px-2 py-1 bg-slate-800 rounded-full text-xs text-cyan-300">${t.trim()}</span>`).join('')}</div><a href="${p.link}" class="text-cyan-400 hover:underline text-sm">View Project →</a></div>
                `;
                grid.appendChild(card);
            });
        }
        renderProjects('all');
        document.querySelectorAll('.project-filter').forEach(btn => {
            btn.addEventListener('click', () => {
                document.querySelectorAll('.project-filter').forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                renderProjects(btn.dataset.filter);
            });
        });

        // ================= CUSTOM CURSOR =================
        const cursor = document.querySelector('.custom-cursor');
        const dot = document.querySelector('.custom-cursor-dot');
        document.addEventListener('mousemove', e => {
            gsap.to(cursor, { x: e.clientX, y: e.clientY, duration: 0.2 });
            gsap.to(dot, { x: e.clientX, y: e.clientY, duration: 0.05 });
        });
        document.querySelectorAll('a, button').forEach(el => {
            el.addEventListener('mouseenter', () => gsap.to(cursor, { scale: 2, duration: 0.3 }));
            el.addEventListener('mouseleave', () => gsap.to(cursor, { scale: 1, duration: 0.3 }));
        });

        // ================= MAGNETIC BUTTONS =================
        document.querySelectorAll('.btn-magnetic').forEach(btn => {
            btn.addEventListener('mousemove', e => {
                const rect = btn.getBoundingClientRect();
                gsap.to(btn, { x: (e.clientX - rect.left - rect.width/2) * 0.3, y: (e.clientY - rect.top - rect.height/2) * 0.3, duration: 0.3 });
            });
            btn.addEventListener('mouseleave', () => gsap.to(btn, { x: 0, y: 0, duration: 0.3 }));
        });

        // ================= SCROLL PROGRESS =================
        gsap.to('.scroll-progress', {
            width: '100%', ease: 'none',
            scrollTrigger: { trigger: 'body', start: 'top top', end: 'bottom bottom', scrub: 0.3 }
        });

        // ================= CONTACT FORM =================
        document.getElementById('contact-form').addEventListener('submit', (e) => {
            e.preventDefault();
            const form = e.target;
            const data = new FormData(form);
            const message = `Name: ${data.get('name')}%0AEmail: ${data.get('email')}%0ASubject: ${data.get('subject')}%0AMessage: ${data.get('message')}`;
            window.open(`https://wa.me/919318302850?text=${message}`, '_blank');
            form.reset();
        });
    </script>
</body>
</html>
<!-- Header -->
## Hi There <img src="https://raw.githubusercontent.com/ABSphreak/ABSphreak/master/gifs/Hi.gif" width="30px">

I'm **Md Sadique Amin**  
Software Engineer | Problem Solver | Web & Java Developer  
Currently pursuing B.E. in Computer Science & Engineering  

---

### 🚀 What I'm working on

- 🔭 I'm currently working on **MSA – Offline AI Agent** (local LLM + Android control)  
- 🌱 I'm currently learning **Advanced Spring Boot**, **Kotlin Multiplatform**, and **Big Data pipelines**  
- 👯 I'm looking to collaborate on **AI/ML projects** and **open‑source full‑stack applications**  
- 🤝 I'm looking for help with **real‑time data streaming** and **cloud‑native deployment**  
- 💬 Ask me about **Java, Spring Boot, Python, Machine Learning, Data Science**  
- 📫 How to reach me:  
  **Email**: mdsadiqueamin721786@gmail.com  
  **GitHub**: [Sadique721](https://github.com/Sadique721)  
  **LinkedIn**: [md-sadique-amin](https://www.linkedin.com/in/md-sadique-amin-b6a948198/)  
  **YouTube**: [@mdsadiqueamin721](http://www.youtube.com/@mdsadiqueamin721)  
- 😄 Pronouns: He/Him  

---

### 🧠 Tech Stack

| Category | Technologies |
|----------|--------------|
| **Languages** | Java, Python, JavaScript, C, SQL |
| **Backend** | Spring Boot, Django, REST APIs, JWT |
| **Frontend** | React.js, HTML5, CSS3, Tailwind |
| **Databases** | MySQL, MongoDB, PostgreSQL |
| **AI/ML** | TensorFlow, PyTorch, Scikit‑learn, OpenCV, NLTK |
| **Data Science** | Pandas, NumPy, Matplotlib, Tableau |
| **DevOps & Tools** | Git, GitHub, Docker, AWS (EC2/S3), Kafka, Spark |

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)

---

### 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Sadique721&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0a192f&title_color=22d3ee&icon_color=8b5cf6)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Sadique721&layout=compact&theme=tokyonight&hide_border=true&bg_color=0a192f&title_color=22d3ee)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=Sadique721&theme=tokyonight&hide_border=true&background=0a192f&stroke=22d3ee&ring=22d3ee&fire=8b5cf6)

![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Sadique721&theme=tokyo-night&hide_border=true&bg_color=0a192f&color=22d3ee&line=8b5cf6&point=ffffff&area=true)

---

### 🔥 Featured Projects

| Project | Description | Tech |
|---------|-------------|------|
| **[MSA – Offline AI Agent](https://github.com/Sadique721/AI-Agent-MSA)** | Local AI assistant (voice + LLM + Android control) | Python, Vosk, Llama2, ADB |
| **[Entitykart](https://github.com/Sadique721/Entitykart)** | Full‑featured e‑commerce platform | Spring Boot, React, JWT, MySQL |
| **[Ethical Hacking Portal](https://github.com/Sadique721/ethical-hacking-portal)** | Cybersecurity learning platform | Django, Python, SQLite |
| **[Recipe Finder Pro](https://github.com/Sadique721/Recipe-finder-pro-)** | Instant recipe search with dark mode | React.js, REST APIs |
| **[Advanced Scientific Calculator](https://github.com/Sadique721/Advanced-Scientific-Calculator)** | 15+ scientific functions | HTML/CSS/JS |
| **[Intelligent Image Recognition](https://github.com/Sadique721/)** | 95% accuracy real‑time object detection | TensorFlow, OpenCV |

> 📌 See all my repositories [here](https://github.com/Sadique721?tab=repositories)

---

### 💼 Experience & Education

**Experience**

- **Web Development Intern** @ TechnoFly Solutions, Bengaluru (Sep 2022 – Jan 2023)  
  → Developed 5+ websites using Django + React.js. Optimized SQL queries (40% faster).
- **Industrial Trainee** @ BSNL, Hyderabad (Jun 2022 – Jul 2022)  
  → Telecom networks & cybersecurity protocols.

**Education**

| Degree | Institution | Year | Score |
|--------|-------------|------|-------|
| B.E. (CSE) | Government Engineering College, Patan | 2023–26 | 7.9 CGPA |
| Diploma (CS) | MANUU Polytechnic, Bangalore | 2021–23 | 87.3% |
| HSC | G.D. College, Begusarai | 2020 | 66% |
| SSC | Nerly Inter College, Begusarai | 2018 | 72.8% |

---

### 📫 Connect with me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/md-sadique-amin-b6a948198/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sadique721)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](http://www.youtube.com/@mdsadiqueamin721)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/mdsadiqueamin721/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mdsadiqueamin721786@gmail.com)

---

*“Code. Create. Decentralize.”*
