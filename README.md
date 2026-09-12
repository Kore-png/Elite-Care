<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elite Care - Sports Rehabilitation & Therapy Center</title>
    <meta name="description" content="Professional sports rehabilitation, cupping therapy, and therapeutic massage services at our center or in the comfort of your home.">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=Cairo:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Poppins', 'Cairo', 'sans-serif'],
                    },
                    colors: {
                        primary: {
                            50: '#f0f9ff',
                            100: '#e0f2fe',
                            200: '#bae6fd',
                            300: '#7dd3fc',
                            400: '#38bdf8',
                            500: '#0ea5e9',
                            600: '#0284c7',
                            700: '#0369a1',
                            800: '#075985',
                            900: '#0c4a6e',
                            950: '#082f49',
                        },
                        secondary: {
                            50: '#f8fafc',
                            100: '#f1f5f9',
                            200: '#e2e8f0',
                            300: '#cbd5e1',
                            400: '#94a3b8',
                            500: '#64748b',
                            600: '#475569',
                            700: '#334155',
                            800: '#1e293b',
                            900: '#0f172a',
                            950: '#020617',
                        },
                        accent: {
                            400: '#34d399',
                            500: '#10b981',
                            600: '#059669',
                        }
                    }
                }
            }
        }
    </script>
    
    <style>
        /* Custom Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        @keyframes pulse-slow {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.8; }
        }
        
        .animate-fadeInUp {
            animation: fadeInUp 0.8s ease-out forwards;
        }
        
        .animate-float {
            animation: float 3s ease-in-out infinite;
        }
        
        .animate-pulse-slow {
            animation: pulse-slow 3s ease-in-out infinite;
        }
        
        /* Card Hover Effects */
        .member-card {
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .member-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
        
        .member-card:hover .member-image {
            transform: scale(1.05);
        }
        
        .member-image {
            transition: transform 0.6s ease;
        }
        
        /* Button Hover Effects */
        .contact-btn {
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .contact-btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }
        
        .contact-btn:hover::before {
            width: 300px;
            height: 300px;
        }
        
        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .contact-btn:active {
            transform: translateY(-1px);
        }
        
        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        
        ::-webkit-scrollbar-track {
            background: #f1f5f9;
        }
        
        ::-webkit-scrollbar-thumb {
            background: #0ea5e9;
            border-radius: 5px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: #0284c7;
        }
        
        /* Gradient Text */
        .gradient-text {
            background: linear-gradient(135deg, #0ea5e9 0%, #10b981 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        /* Glass Effect */
        .glass {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        /* Language Switcher */
        .lang-btn {
            transition: all 0.3s ease;
        }
        
        .lang-btn.active {
            background: linear-gradient(135deg, #0ea5e9 0%, #10b981 100%);
            color: white;
            box-shadow: 0 4px 15px rgba(14, 165, 233, 0.4);
        }
        
        .lang-btn:not(.active) {
            background: rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.8);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .lang-btn:not(.active):hover {
            background: rgba(255, 255, 255, 0.2);
            color: white;
        }
        
        /* Flag Icons */
        .flag-icon {
            width: 20px;
            height: 14px;
            border-radius: 2px;
            overflow: hidden;
            display: inline-flex;
            box-shadow: 0 1px 3px rgba(0,0,0,0.2);
        }
        
        /* RTL Support */
        [dir="rtl"] {
            font-family: 'Cairo', sans-serif;
        }
        
        [dir="rtl"] .fa-chevron-down {
            transform: rotate(180deg);
        }
        
        [dir="rtl"] .space-x-2 > :not([hidden]) ~ :not([hidden]) {
            --tw-space-x-reverse: 1;
        }
        
        [dir="rtl"] .space-x-3 > :not([hidden]) ~ :not([hidden]) {
            --tw-space-x-reverse: 1;
        }
        
        [dir="rtl"] .space-x-4 > :not([hidden]) ~ :not([hidden]) {
            --tw-space-x-reverse: 1;
        }
        
        [dir="rtl"] .space-x-8 > :not([hidden]) ~ :not([hidden]) {
            --tw-space-x-reverse: 1;
        }
        
        [dir="rtl"] .mr-2 {
            margin-left: 0.5rem;
            margin-right: 0;
        }
        
        [dir="rtl"] .mr-4 {
            margin-left: 1rem;
            margin-right: 0;
        }
        
        [dir="rtl"] .ml-2 {
            margin-right: 0.5rem;
            margin-left: 0;
        }
        
        [dir="rtl"] .text-left {
            text-align: right;
        }
        
        [dir="rtl"] .fa-arrow-right {
            transform: rotate(180deg);
        }
        
        [dir="rtl"] .fa-chevron-right {
            transform: rotate(180deg);
        }
    </style>
</head>
<body class="font-sans bg-secondary-50 text-secondary-800">

    <!-- Navigation Bar -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-md shadow-lg">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <div class="flex items-center space-x-3">
                    <div class="w-12 h-12 bg-gradient-to-br from-primary-500 to-accent-500 rounded-xl flex items-center justify-center text-white text-2xl font-bold shadow-lg">
                        <i class="fas fa-heartbeat"></i>
                    </div>
                    <div>
                        <h1 class="text-xl font-bold text-secondary-900" data-en="Elite Care" data-ar="الرعاية النخبوية">Elite Care</h1>
                        <p class="text-xs text-secondary-500" data-en="Rehabilitation Center" data-ar="مركز التأهيل">Rehabilitation Center</p>
                    </div>
                </div>
                
                <!-- Desktop Menu -->
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="text-secondary-600 hover:text-primary-600 font-medium transition-colors" data-en="Home" data-ar="الرئيسية">Home</a>
                    <a href="#team" class="text-secondary-600 hover:text-primary-600 font-medium transition-colors" data-en="Our Team" data-ar="فريقنا">Our Team</a>
                    <a href="#services" class="text-secondary-600 hover:text-primary-600 font-medium transition-colors" data-en="Services" data-ar="خدماتنا">Services</a>
                    
                    <!-- Language Switcher -->
                    <div class="flex items-center space-x-2 bg-secondary-100 rounded-full p-1">
                        <button onclick="switchLanguage('en')" id="btn-en" class="lang-btn active flex items-center space-x-2 px-4 py-2 rounded-full text-sm font-semibold">
                            <span class="flag-icon">
                                <svg viewBox="0 0 60 40" xmlns="http://www.w3.org/2000/svg">
                                    <clipPath id="s"><path d="M0,0 v40 h60 v-40 z"/></clipPath>
                                    <clipPath id="t"><path d="M30,20 h30 v20 z v20 h-30 z h-30 v-20 z v-20 h30 z"/></clipPath>
                                    <g clip-path="url(#s)">
                                        <path d="M0,0 v40 h60 v-40 z" fill="#012169"/>
                                        <path d="M0,0 L60,40 M60,0 L0,40" stroke="#fff" stroke-width="6"/>
                                        <path d="M0,0 L60,40 M60,0 L0,40" clip-path="url(#t)" stroke="#C8102E" stroke-width="4"/>
                                        <path d="M30,0 v40 M0,20 h60" stroke="#fff" stroke-width="10"/>
                                        <path d="M30,0 v40 M0,20 h60" stroke="#C8102E" stroke-width="6"/>
                                    </g>
                                </svg>
                            </span>
                            <span>EN</span>
                        </button>
                        <button onclick="switchLanguage('ar')" id="btn-ar" class="lang-btn flex items-center space-x-2 px-4 py-2 rounded-full text-sm font-semibold">
                            <span class="flag-icon">
                                <svg viewBox="0 0 60 40" xmlns="http://www.w3.org/2000/svg">
                                    <rect width="60" height="13.3" fill="#CE1126"/>
                                    <rect y="13.3" width="60" height="13.3" fill="#FFFFFF"/>
                                    <rect y="26.6" width="60" height="13.4" fill="#000000"/>
                                    <path d="M 22,16.5 L 25.5,16.5 L 26.8,13.5 L 28.1,16.5 L 31.6,16.5 L 28.8,18.5 L 30,21.5 L 26.8,19.6 L 23.6,21.5 L 24.8,18.5 Z" fill="#C09300" transform="translate(3,0)"/>
                                </svg>
                            </span>
                            <span>عربي</span>
                        </button>
                    </div>
                    
                    <a href="#contact" class="bg-gradient-to-r from-primary-600 to-accent-500 text-white px-6 py-2.5 rounded-full font-medium hover:shadow-lg transition-all transform hover:scale-105" data-en="Book Now" data-ar="احجز الآن">
                        Book Now
                    </a>
                </div>
                
                <!-- Mobile Menu Button -->
                <div class="flex items-center space-x-3 md:hidden">
                    <!-- Mobile Language Switcher -->
                    <div class="flex items-center space-x-1 bg-secondary-100 rounded-full p-1">
                        <button onclick="switchLanguage('en')" id="btn-en-mobile" class="lang-btn active flex items-center px-3 py-1.5 rounded-full text-xs font-semibold">
                            <span class="flag-icon" style="width:16px;height:11px;">
                                <svg viewBox="0 0 60 40" xmlns="http://www.w3.org/2000/svg">
                                    <clipPath id="s-m"><path d="M0,0 v40 h60 v-40 z"/></clipPath>
                                    <clipPath id="t-m"><path d="M30,20 h30 v20 z v20 h-30 z h-30 v-20 z v-20 h30 z"/></clipPath>
                                    <g clip-path="url(#s-m)">
                                        <path d="M0,0 v40 h60 v-40 z" fill="#012169"/>
                                        <path d="M0,0 L60,40 M60,0 L0,40" stroke="#fff" stroke-width="6"/>
                                        <path d="M0,0 L60,40 M60,0 L0,40" clip-path="url(#t-m)" stroke="#C8102E" stroke-width="4"/>
                                        <path d="M30,0 v40 M0,20 h60" stroke="#fff" stroke-width="10"/>
                                        <path d="M30,0 v40 M0,20 h60" stroke="#C8102E" stroke-width="6"/>
                                    </g>
                                </svg>
                            </span>
                        </button>
                        <button onclick="switchLanguage('ar')" id="btn-ar-mobile" class="lang-btn flex items-center px-3 py-1.5 rounded-full text-xs font-semibold">
                            <span class="flag-icon" style="width:16px;height:11px;">
                                <svg viewBox="0 0 60 40" xmlns="http://www.w3.org/2000/svg">
                                    <rect width="60" height="13.3" fill="#CE1126"/>
                                    <rect y="13.3" width="60" height="13.3" fill="#FFFFFF"/>
                                    <rect y="26.6" width="60" height="13.4" fill="#000000"/>
                                    <path d="M 22,16.5 L 25.5,16.5 L 26.8,13.5 L 28.1,16.5 L 31.6,16.5 L 28.8,18.5 L 30,21.5 L 26.8,19.6 L 23.6,21.5 L 24.8,18.5 Z" fill="#C09300" transform="translate(3,0)"/>
                                </svg>
                            </span>
                        </button>
                    </div>
                    
                    <button id="mobile-menu-btn" class="text-secondary-600 focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t">
            <div class="px-4 py-3 space-y-3">
                <a href="#home" class="block py-2 text-secondary-600 hover:text-primary-600 font-medium" data-en="Home" data-ar="الرئيسية">Home</a>
                <a href="#team" class="block py-2 text-secondary-600 hover:text-primary-600 font-medium" data-en="Our Team" data-ar="فريقنا">Our Team</a>
                <a href="#services" class="block py-2 text-secondary-600 hover:text-primary-600 font-medium" data-en="Services" data-ar="خدماتنا">Services</a>
                <a href="#contact" class="block py-3 text-center bg-gradient-to-r from-primary-600 to-accent-500 text-white rounded-full font-medium" data-en="Book Now" data-ar="احجز الآن">Book Now</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gradient-to-br from-secondary-900 via-primary-900 to-secondary-900 pt-20">
        <!-- Background Pattern -->
        <div class="absolute inset-0 opacity-10">
            <div class="absolute inset-0" style="background-image: url('data:image/svg+xml,%3Csvg width="60" height="60" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg"%3E%3Cg fill="none" fill-rule="evenodd"%3E%3Cg fill="%23ffffff" fill-opacity="1"%3E%3Cpath d="M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z"/%3E%3C/g%3E%3C/g%3E%3C/svg%3E');"></div>
        </div>
        
        <!-- Decorative Circles -->
        <div class="absolute top-20 right-10 w-72 h-72 bg-primary-500/20 rounded-full blur-3xl animate-pulse-slow"></div>
        <div class="absolute bottom-20 left-10 w-96 h-96 bg-accent-500/20 rounded-full blur-3xl animate-pulse-slow"></div>
        
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <div class="animate-fadeInUp">
                <!-- Badge -->
                <div class="inline-flex items-center space-x-2 bg-white/10 backdrop-blur-md rounded-full px-6 py-2 mb-8 border border-white/20">
                    <span class="w-2 h-2 bg-accent-400 rounded-full animate-pulse"></span>
                    <span class="text-white/90 text-sm font-medium" data-en="Trusted by 1000+ Patients" data-ar="موثوق من أكثر من 1000 مريض">Trusted by 1000+ Patients</span>
                </div>
                
                <!-- Main Title -->
                <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight">
                    <span data-en="Complete Recovery &" data-ar="التعافي الكامل و">Complete Recovery &</span><br>
                    <span class="gradient-text" data-en="Therapeutic Care" data-ar="الرعاية العلاجية">Therapeutic Care</span>
                </h1>
                
                <!-- Subtitle -->
                <p class="text-lg sm:text-xl text-white/80 max-w-3xl mx-auto mb-10 leading-relaxed" data-en="Our expert team of three specialists provides integrated sports rehabilitation, cupping therapy, and therapeutic massage — available at our center or in the comfort of your home." data-ar="فريقنا المتخصص من ثلاثة خبراء يقدم تأهيلاً رياضياً متكاملاً وعلاجاً بالحجامة ومساجاً علاجياً — متاح في مركزنا أو في راحة منزلك.">
                    Our expert team of three specialists provides integrated sports rehabilitation, 
                    cupping therapy, and therapeutic massage — available at our center or in the 
                    comfort of your home.
                </p>
                
                <!-- CTA Buttons -->
                <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-16">
                    <a href="#team" class="w-full sm:w-auto bg-gradient-to-r from-primary-500 to-accent-500 text-white px-8 py-4 rounded-full font-semibold text-lg hover:shadow-2xl transition-all transform hover:scale-105 flex items-center justify-center space-x-2">
                        <i class="fas fa-users"></i>
                        <span data-en="Meet Our Team" data-ar="تعرف على فريقنا">Meet Our Team</span>
                    </a>
                    <a href="#services" class="w-full sm:w-auto bg-white/10 backdrop-blur-md text-white px-8 py-4 rounded-full font-semibold text-lg border-2 border-white/30 hover:bg-white/20 transition-all flex items-center justify-center space-x-2">
                        <i class="fas fa-calendar-check"></i>
                        <span data-en="Our Services" data-ar="خدماتنا">Our Services</span>
                    </a>
                </div>
                
                <!-- Stats -->
                <div class="grid grid-cols-3 gap-4 max-w-2xl mx-auto">
                    <div class="glass rounded-2xl p-4">
                        <div class="text-3xl sm:text-4xl font-bold text-white">3+</div>
                        <div class="text-white/70 text-sm mt-1" data-en="Specialists" data-ar="متخصصين">Specialists</div>
                    </div>
                    <div class="glass rounded-2xl p-4">
                        <div class="text-3xl sm:text-4xl font-bold text-white">1000+</div>
                        <div class="text-white/70 text-sm mt-1" data-en="Happy Patients" data-ar="مريض سعيد">Happy Patients</div>
                    </div>
                    <div class="glass rounded-2xl p-4">
                        <div class="text-3xl sm:text-4xl font-bold text-white">5+</div>
                        <div class="text-white/70 text-sm mt-1" data-en="Years Experience" data-ar="سنوات خبرة">Years Experience</div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Scroll Indicator -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-float">
            <a href="#team" class="text-white/60 hover:text-white transition-colors">
                <i class="fas fa-chevron-down text-2xl"></i>
            </a>
        </div>
    </section>

    <!-- Team Section -->
    <section id="team" class="py-20 lg:py-32 bg-gradient-to-b from-secondary-50 to-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Section Header -->
            <div class="text-center mb-16">
                <span class="text-primary-600 font-semibold text-sm uppercase tracking-wider" data-en="Our Specialists" data-ar="متخصصونا">Our Specialists</span>
                <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-secondary-900 mt-4 mb-6" data-en="Meet Our Expert Team" data-ar="تعرف على فريقنا الخبير">
                    Meet Our Expert Team
                </h2>
                <p class="text-secondary-600 max-w-2xl mx-auto text-lg" data-en="Three dedicated professionals committed to your recovery and well-being, offering personalized treatment plans tailored to your needs." data-ar="ثلاثة محترفين مكرّسين لتعافيك ورفاهيتك، يقدمون خطط علاجية مخصصة تناسب احتياجاتك.">
                    Three dedicated professionals committed to your recovery and well-being, 
                    offering personalized treatment plans tailored to your needs.
                </p>
            </div>
            
            <!-- Team Cards Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 lg:gap-10">
                
                <!-- Member 1: Sports Rehabilitation Specialist -->
                <div class="member-card bg-white rounded-3xl overflow-hidden shadow-xl border border-secondary-100">
                    <!-- Image Container -->
                    <div class="relative h-80 bg-gradient-to-br from-primary-500 to-primary-700 overflow-hidden">
                        <!-- Placeholder for personal photo - Replace with actual image -->
                        <div class="absolute inset-0 flex items-center justify-center">
                            <div class="text-center text-white/50">
                                <i class="fas fa-user text-8xl mb-4"></i>
                                <p class="text-sm" data-en="Add Photo Here" data-ar="أضف الصورة هنا">Add Photo Here</p>
                            </div>
                        </div>
                        <!-- Uncomment and replace src with actual photo -->
                        <!-- <img src="photo1.jpg" alt="Dr. Ahmed Hassan" class="member-image w-full h-full object-cover"> -->
                        
                        <!-- Overlay Badge -->
                        <div class="absolute top-4 left-4">
                            <span class="bg-white/90 text-primary-700 px-4 py-1.5 rounded-full text-sm font-semibold" data-en="Sports Rehab" data-ar="التأهيل الرياضي">
                                Sports Rehab
                            </span>
                        </div>
                        
                        <!-- Availability Badge -->
                        <div class="absolute top-4 right-4">
                            <span class="bg-accent-500 text-white px-3 py-1.5 rounded-full text-xs font-semibold flex items-center">
                                <i class="fas fa-circle text-[8px] mr-1 animate-pulse"></i>
                                <span data-en="Available" data-ar="متاح">Available</span>
                            </span>
                        </div>
                    </div>
                    
                    <!-- Card Content -->
                    <div class="p-6 lg:p-8">
                        <h3 class="text-2xl font-bold text-secondary-900 mb-1" data-en="Dr. Ahmed Hassan" data-ar="د. أحمد حسن">Dr. Ahmed Hassan</h3>
                        <p class="text-primary-600 font-semibold mb-4" data-en="Sports Rehabilitation Specialist" data-ar="أخصائي التأهيل الرياضي">Sports Rehabilitation Specialist</p>
                        
                        <p class="text-secondary-600 text-sm leading-relaxed mb-6" data-en="Specialized in sports injury recovery, post-surgical rehabilitation, and athletic performance enhancement. Customized treatment plans to get you back in the game." data-ar="متخصص في تعافي الإصابات الرياضية، التأهيل بعد الجراحة، وتعزيز الأداء الرياضي. خطط علاجية مخصصة لإعادتك إلى الملعب.">
                            Specialized in sports injury recovery, post-surgical rehabilitation, and athletic 
                            performance enhancement. Customized treatment plans to get you back in the game.
                        </p>
                        
                        <!-- Service Location -->
                        <div class="flex items-center space-x-2 mb-6 text-sm">
                            <div class="flex items-center text-accent-600 bg-accent-50 px-3 py-1.5 rounded-full">
                                <i class="fas fa-hospital mr-1.5"></i>
                                <span data-en="At Center" data-ar="في المركز">At Center</span>
                            </div>
                            <div class="flex items-center text-primary-600 bg-primary-50 px-3 py-1.5 rounded-full">
                                <i class="fas fa-home mr-1.5"></i>
                                <span data-en="Home Visit" data-ar="زيارة منزلية">Home Visit</span>
                            </div>
                        </div>
                        
                        <!-- Contact Buttons -->
                        <div class="space-y-3">
                            <!-- WhatsApp/Phone -->
                            <a href="tel:+1234567890" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-green-500 to-green-600 text-white py-3.5 rounded-xl font-semibold">
                                <i class="fas fa-phone-alt relative z-10"></i>
                                <span class="relative z-10" data-en="Call / WhatsApp" data-ar="اتصال / واتساب">Call / WhatsApp</span>
                            </a>
                            
                            <!-- Facebook -->
                            <a href="https://facebook.com/drahmedhassan" target="_blank" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-3 rounded-xl font-semibold">
                                <i class="fab fa-facebook-f relative z-10"></i>
                                <span class="relative z-10">Facebook</span>
                            </a>
                            
                            <!-- TikTok -->
                            <a href="https://tiktok.com/@drahmedhassan" target="_blank" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-secondary-900 to-secondary-800 text-white py-3 rounded-xl font-semibold">
                                <i class="fab fa-tiktok relative z-10"></i>
                                <span class="relative z-10">TikTok</span>
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Member 2: Cupping Therapy Specialist -->
                <div class="member-card bg-white rounded-3xl overflow-hidden shadow-xl border border-secondary-100">
                    <!-- Image Container -->
                    <div class="relative h-80 bg-gradient-to-br from-accent-500 to-accent-600 overflow-hidden">
                        <!-- Placeholder for personal photo - Replace with actual image -->
                        <div class="absolute inset-0 flex items-center justify-center">
                            <div class="text-center text-white/50">
                                <i class="fas fa-user text-8xl mb-4"></i>
                                <p class="text-sm" data-en="Add Photo Here" data-ar="أضف الصورة هنا">Add Photo Here</p>
                            </div>
                        </div>
                        <!-- Uncomment and replace src with actual photo -->
                        <!-- <img src="photo2.jpg" alt="Mohamed Ali" class="member-image w-full h-full object-cover"> -->
                        
                        <!-- Overlay Badge -->
                        <div class="absolute top-4 left-4">
                            <span class="bg-white/90 text-accent-600 px-4 py-1.5 rounded-full text-sm font-semibold" data-en="Cupping Therapy" data-ar="الحجامة">
                                Cupping Therapy
                            </span>
                        </div>
                        
                        <!-- Availability Badge -->
                        <div class="absolute top-4 right-4">
                            <span class="bg-accent-500 text-white px-3 py-1.5 rounded-full text-xs font-semibold flex items-center">
                                <i class="fas fa-circle text-[8px] mr-1 animate-pulse"></i>
                                <span data-en="Available" data-ar="متاح">Available</span>
                            </span>
                        </div>
                    </div>
                    
                    <!-- Card Content -->
                    <div class="p-6 lg:p-8">
                        <h3 class="text-2xl font-bold text-secondary-900 mb-1" data-en="Mohamed Ali" data-ar="محمد علي">Mohamed Ali</h3>
                        <p class="text-accent-600 font-semibold mb-4" data-en="Cupping Therapy Specialist" data-ar="أخصائي الحجامة">Cupping Therapy Specialist</p>
                        
                        <p class="text-secondary-600 text-sm leading-relaxed mb-6" data-en="Certified hijama practitioner with expertise in traditional and modern cupping techniques. Helps relieve pain, improve circulation, and promote natural healing." data-ar="ممارس حجامة معتمد بخبرة في تقنيات الحجامة التقليدية والحديثة. يساعد في تخفيف الألم وتحسين الدورة الدموية وتعزيز الشفاء الطبيعي.">
                            Certified hijama practitioner with expertise in traditional and modern cupping 
                            techniques. Helps relieve pain, improve circulation, and promote natural healing.
                        </p>
                        
                        <!-- Service Location -->
                        <div class="flex items-center space-x-2 mb-6 text-sm">
                            <div class="flex items-center text-accent-600 bg-accent-50 px-3 py-1.5 rounded-full">
                                <i class="fas fa-hospital mr-1.5"></i>
                                <span data-en="At Center" data-ar="في المركز">At Center</span>
                            </div>
                            <div class="flex items-center text-primary-600 bg-primary-50 px-3 py-1.5 rounded-full">
                                <i class="fas fa-home mr-1.5"></i>
                                <span data-en="Home Visit" data-ar="زيارة منزلية">Home Visit</span>
                            </div>
                        </div>
                        
                        <!-- Contact Buttons -->
                        <div class="space-y-3">
                            <!-- WhatsApp/Phone -->
                            <a href="tel:+1234567891" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-green-500 to-green-600 text-white py-3.5 rounded-xl font-semibold">
                                <i class="fas fa-phone-alt relative z-10"></i>
                                <span class="relative z-10" data-en="Call / WhatsApp" data-ar="اتصال / واتساب">Call / WhatsApp</span>
                            </a>
                            
                            <!-- Facebook -->
                            <a href="https://facebook.com/mohamedali" target="_blank" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-3 rounded-xl font-semibold">
                                <i class="fab fa-facebook-f relative z-10"></i>
                                <span class="relative z-10">Facebook</span>
                            </a>
                            
                            <!-- TikTok -->
                            <a href="https://tiktok.com/@mohamedali" target="_blank" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-secondary-900 to-secondary-800 text-white py-3 rounded-xl font-semibold">
                                <i class="fab fa-tiktok relative z-10"></i>
                                <span class="relative z-10">TikTok</span>
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Member 3: Therapeutic Massage Specialist -->
                <div class="member-card bg-white rounded-3xl overflow-hidden shadow-xl border border-secondary-100 md:col-span-2 lg:col-span-1 md:max-w-md md:mx-auto lg:max-w-none">
                    <!-- Image Container -->
                    <div class="relative h-80 bg-gradient-to-br from-secondary-700 to-secondary-900 overflow-hidden">
                        <!-- Placeholder for personal photo - Replace with actual image -->
                        <div class="absolute inset-0 flex items-center justify-center">
                            <div class="text-center text-white/50">
                                <i class="fas fa-user text-8xl mb-4"></i>
                                <p class="text-sm" data-en="Add Photo Here" data-ar="أضف الصورة هنا">Add Photo Here</p>
                            </div>
                        </div>
                        <!-- Uncomment and replace src with actual photo -->
                        <!-- <img src="photo3.jpg" alt="Omar Khaled" class="member-image w-full h-full object-cover"> -->
                        
                        <!-- Overlay Badge -->
                        <div class="absolute top-4 left-4">
                            <span class="bg-white/90 text-secondary-700 px-4 py-1.5 rounded-full text-sm font-semibold" data-en="Massage Therapy" data-ar="المساج العلاجي">
                                Massage Therapy
                            </span>
                        </div>
                        
                        <!-- Availability Badge -->
                        <div class="absolute top-4 right-4">
                            <span class="bg-accent-500 text-white px-3 py-1.5 rounded-full text-xs font-semibold flex items-center">
                                <i class="fas fa-circle text-[8px] mr-1 animate-pulse"></i>
                                <span data-en="Available" data-ar="متاح">Available</span>
                            </span>
                        </div>
                    </div>
                    
                    <!-- Card Content -->
                    <div class="p-6 lg:p-8">
                        <h3 class="text-2xl font-bold text-secondary-900 mb-1" data-en="Omar Khaled" data-ar="عمر خالد">Omar Khaled</h3>
                        <p class="text-secondary-600 font-semibold mb-4" data-en="Therapeutic Massage Specialist" data-ar="أخصائي المساج العلاجي">Therapeutic Massage Specialist</p>
                        
                        <p class="text-secondary-600 text-sm leading-relaxed mb-6" data-en="Licensed massage therapist specializing in deep tissue, sports massage, and relaxation techniques. Relieves muscle tension and promotes overall wellness." data-ar="معالج مساج مرخص متخصص في الأنسجة العميقة والمساج الرياضي وتقنيات الاسترخاء. يخفف توتر العضلات ويعزز الصحة العامة.">
                            Licensed massage therapist specializing in deep tissue, sports massage, and 
                            relaxation techniques. Relieves muscle tension and promotes overall wellness.
                        </p>
                        
                        <!-- Service Location -->
                        <div class="flex items-center space-x-2 mb-6 text-sm">
                            <div class="flex items-center text-accent-600 bg-accent-50 px-3 py-1.5 rounded-full">
                                <i class="fas fa-hospital mr-1.5"></i>
                                <span data-en="At Center" data-ar="في المركز">At Center</span>
                            </div>
                            <div class="flex items-center text-primary-600 bg-primary-50 px-3 py-1.5 rounded-full">
                                <i class="fas fa-home mr-1.5"></i>
                                <span data-en="Home Visit" data-ar="زيارة منزلية">Home Visit</span>
                            </div>
                        </div>
                        
                        <!-- Contact Buttons -->
                        <div class="space-y-3">
                            <!-- WhatsApp/Phone -->
                            <a href="tel:+1234567892" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-green-500 to-green-600 text-white py-3.5 rounded-xl font-semibold">
                                <i class="fas fa-phone-alt relative z-10"></i>
                                <span class="relative z-10" data-en="Call / WhatsApp" data-ar="اتصال / واتساب">Call / WhatsApp</span>
                            </a>
                            
                            <!-- Facebook -->
                            <a href="https://facebook.com/omarkhaled" target="_blank" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-3 rounded-xl font-semibold">
                                <i class="fab fa-facebook-f relative z-10"></i>
                                <span class="relative z-10">Facebook</span>
                            </a>
                            
                            <!-- TikTok -->
                            <a href="https://tiktok.com/@omarkhaled" target="_blank" class="contact-btn flex items-center justify-center space-x-3 w-full bg-gradient-to-r from-secondary-900 to-secondary-800 text-white py-3 rounded-xl font-semibold">
                                <i class="fab fa-tiktok relative z-10"></i>
                                <span class="relative z-10">TikTok</span>
                            </a>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Services Overview Section -->
    <section id="services" class="py-20 lg:py-32 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Section Header -->
            <div class="text-center mb-16">
                <span class="text-primary-600 font-semibold text-sm uppercase tracking-wider" data-en="What We Offer" data-ar="ما نقدمه">What We Offer</span>
                <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-secondary-900 mt-4 mb-6" data-en="Our Services" data-ar="خدماتنا">
                    Our Services
                </h2>
                <p class="text-secondary-600 max-w-2xl mx-auto text-lg" data-en="Comprehensive therapeutic treatments designed to restore your health and enhance your quality of life." data-ar="علاجات علاجية شاملة مصممة لاستعادة صحتك وتعزيز جودة حياتك.">
                    Comprehensive therapeutic treatments designed to restore your health and enhance your quality of life.
                </p>
            </div>
            
            <!-- Services Grid -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="group bg-gradient-to-br from-primary-50 to-white rounded-3xl p-8 border-2 border-primary-100 hover:border-primary-300 transition-all hover:shadow-xl">
                    <div class="w-16 h-16 bg-gradient-to-br from-primary-500 to-primary-600 rounded-2xl flex items-center justify-center text-white text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fas fa-running"></i>
                    </div>
                    <h3 class="text-xl font-bold text-secondary-900 mb-3" data-en="Sports Rehabilitation" data-ar="التأهيل الرياضي">Sports Rehabilitation</h3>
                    <p class="text-secondary-600 leading-relaxed" data-en="Specialized programs for sports injuries, post-surgical recovery, and performance optimization. Get back to your peak condition with expert guidance." data-ar="برامج متخصصة للإصابات الرياضية والتعافي بعد الجراحة وتحسين الأداء. عد إلى ذروة لياقتك مع إرشاد الخبراء.">
                        Specialized programs for sports injuries, post-surgical recovery, and performance 
                        optimization. Get back to your peak condition with expert guidance.
                    </p>
                    <ul class="mt-4 space-y-2 text-sm text-secondary-600">
                        <li class="flex items-center"><i class="fas fa-check text-primary-500 mr-2"></i><span data-en="Injury assessment & treatment" data-ar="تقييم وعلاج الإصابات">Injury assessment & treatment</span></li>
                        <li class="flex items-center"><i class="fas fa-check text-primary-500 mr-2"></i><span data-en="Post-surgical rehab" data-ar="التأهيل بعد الجراحة">Post-surgical rehab</span></li>
                        <li class="flex items-center"><i class="fas fa-check text-primary-500 mr-2"></i><span data-en="Athletic conditioning" data-ar="الإعداد الرياضي">Athletic conditioning</span></li>
                    </ul>
                </div>
                
                <!-- Service 2 -->
                <div class="group bg-gradient-to-br from-accent-50 to-white rounded-3xl p-8 border-2 border-accent-100 hover:border-accent-300 transition-all hover:shadow-xl">
                    <div class="w-16 h-16 bg-gradient-to-br from-accent-500 to-accent-600 rounded-2xl flex items-center justify-center text-white text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fas fa-fire"></i>
                    </div>
                    <h3 class="text-xl font-bold text-secondary-900 mb-3" data-en="Cupping Therapy" data-ar="الحجامة">Cupping Therapy</h3>
                    <p class="text-secondary-600 leading-relaxed" data-en="Traditional and modern cupping techniques to relieve pain, improve blood circulation, and promote natural healing processes in the body." data-ar="تقنيات الحجامة التقليدية والحديثة لتخفيف الألم وتحسين الدورة الدموية وتعزيز عمليات الشفاء الطبيعية في الجسم.">
                        Traditional and modern cupping techniques to relieve pain, improve blood circulation, 
                        and promote natural healing processes in the body.
                    </p>
                    <ul class="mt-4 space-y-2 text-sm text-secondary-600">
                        <li class="flex items-center"><i class="fas fa-check text-accent-500 mr-2"></i><span data-en="Dry & wet cupping" data-ar="الحجامة الجافة والرطبة">Dry & wet cupping</span></li>
                        <li class="flex items-center"><i class="fas fa-check text-accent-500 mr-2"></i><span data-en="Pain relief" data-ar="تخفيف الألم">Pain relief</span></li>
                        <li class="flex items-center"><i class="fas fa-check text-accent-500 mr-2"></i><span data-en="Detoxification" data-ar="إزالة السموم">Detoxification</span></li>
                    </ul>
                </div>
                
                <!-- Service 3 -->
                <div class="group bg-gradient-to-br from-secondary-100 to-white rounded-3xl p-8 border-2 border-secondary-200 hover:border-secondary-400 transition-all hover:shadow-xl">
                    <div class="w-16 h-16 bg-gradient-to-br from-secondary-700 to-secondary-900 rounded-2xl flex items-center justify-center text-white text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fas fa-hands"></i>
                    </div>
                    <h3 class="text-xl font-bold text-secondary-900 mb-3" data-en="Therapeutic Massage" data-ar="المساج العلاجي">Therapeutic Massage</h3>
                    <p class="text-secondary-600 leading-relaxed" data-en="Professional massage therapy including deep tissue, sports massage, and relaxation techniques to relieve tension and restore balance." data-ar="علاج مساج احترافي يشمل الأنسجة العميقة والمساج الرياضي وتقنيات الاسترخاء لتخفيف التوتر واستعادة التوازن.">
                        Professional massage therapy including deep tissue, sports massage, and relaxation 
                        techniques to relieve tension and restore balance.
                    </p>
                    <ul class="mt-4 space-y-2 text-sm text-secondary-600">
                        <li class="flex items-center"><i class="fas fa-check text-secondary-600 mr-2"></i><span data-en="Deep tissue massage" data-ar="مساج الأنسجة العميقة">Deep tissue massage</span></li>
                        <li class="flex items-center"><i class="fas fa-check text-secondary-600 mr-2"></i><span data-en="Sports massage" data-ar="المساج الرياضي">Sports massage</span></li>
                        <li class="flex items-center"><i class="fas fa-check text-secondary-600 mr-2"></i><span data-en="Relaxation therapy" data-ar="علاج الاسترخاء">Relaxation therapy</span></li>
                    </ul>
                </div>
            </div>
            
            <!-- Home Visit Banner -->
            <div class="mt-16 bg-gradient-to-r from-primary-600 to-accent-500 rounded-3xl p-8 lg:p-12 text-center text-white">
                <div class="flex flex-col lg:flex-row items-center justify-between">
                    <div class="mb-6 lg:mb-0 lg:text-left">
                        <h3 class="text-2xl lg:text-3xl font-bold mb-2" data-en="We Come To You!" data-ar="نأتي إليك!">We Come To You!</h3>
                        <p class="text-white/90 text-lg" data-en="All services available at our center or in the comfort of your home." data-ar="جميع الخدمات متاحة في مركزنا أو في راحة منزلك.">All services available at our center or in the comfort of your home.</p>
                    </div>
                    <a href="#team" class="bg-white text-primary-600 px-8 py-4 rounded-full font-bold text-lg hover:shadow-2xl transition-all transform hover:scale-105 whitespace-nowrap">
                        <i class="fas fa-home mr-2"></i><span data-en="Book Home Visit" data-ar="احجز زيارة منزلية">Book Home Visit</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us Section -->
    <section class="py-20 bg-secondary-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <!-- Image Side -->
                <div class="relative">
                    <div class="bg-gradient-to-br from-primary-100 to-accent-100 rounded-3xl p-8 lg:p-12">
                        <div class="bg-white rounded-2xl shadow-xl p-8">
                            <div class="grid grid-cols-2 gap-4">
                                <div class="bg-primary-50 rounded-xl p-4 text-center">
                                    <i class="fas fa-certificate text-primary-600 text-3xl mb-2"></i>
                                    <p class="text-sm font-semibold text-secondary-700" data-en="Certified" data-ar="معتمد">Certified</p>
                                </div>
                                <div class="bg-accent-50 rounded-xl p-4 text-center">
                                    <i class="fas fa-award text-accent-600 text-3xl mb-2"></i>
                                    <p class="text-sm font-semibold text-secondary-700" data-en="Experienced" data-ar="ذو خبرة">Experienced</p>
                                </div>
                                <div class="bg-secondary-100 rounded-xl p-4 text-center">
                                    <i class="fas fa-hand-holding-heart text-secondary-600 text-3xl mb-2"></i>
                                    <p class="text-sm font-semibold text-secondary-700" data-en="Caring" data-ar="مهتم">Caring</p>
                                </div>
                                <div class="bg-primary-50 rounded-xl p-4 text-center">
                                    <i class="fas fa-clock text-primary-600 text-3xl mb-2"></i>
                                    <p class="text-sm font-semibold text-secondary-700" data-en="Flexible" data-ar="مرن">Flexible</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- Decorative Element -->
                    <div class="absolute -bottom-6 -right-6 w-32 h-32 bg-accent-500/20 rounded-full blur-2xl"></div>
                </div>
                
                <!-- Content Side -->
                <div>
                    <span class="text-primary-600 font-semibold text-sm uppercase tracking-wider" data-en="Why Choose Us" data-ar="لماذا تختارنا">Why Choose Us</span>
                    <h2 class="text-3xl sm:text-4xl font-bold text-secondary-900 mt-4 mb-6" data-en="Your Health Is Our Priority" data-ar="صحتك أولويتنا">
                        Your Health Is Our Priority
                    </h2>
                    <p class="text-secondary-600 text-lg mb-8" data-en="We combine expertise, compassion, and convenience to deliver the highest quality therapeutic care tailored to your individual needs." data-ar="نجمع بين الخبرة والتعاطف والراحة لتقديم أعلى جودة من الرعاية العلاجية المصممة خصيصاً لاحتياجاتك الفردية.">
                        We combine expertise, compassion, and convenience to deliver the highest quality 
                        therapeutic care tailored to your individual needs.
                    </p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <div class="w-12 h-12 bg-primary-100 rounded-xl flex items-center justify-center text-primary-600 text-xl mr-4 flex-shrink-0">
                                <i class="fas fa-user-md"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-secondary-900 mb-1" data-en="Expert Specialists" data-ar="متخصصون خبراء">Expert Specialists</h4>
                                <p class="text-secondary-600" data-en="Highly trained and certified professionals with years of experience." data-ar="محترفون مدربون ومعتمدون بسنوات من الخبرة.">Highly trained and certified professionals with years of experience.</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="w-12 h-12 bg-accent-100 rounded-xl flex items-center justify-center text-accent-600 text-xl mr-4 flex-shrink-0">
                                <i class="fas fa-home"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-secondary-900 mb-1" data-en="Home Visits Available" data-ar="الزيارات المنزلية متاحة">Home Visits Available</h4>
                                <p class="text-secondary-600" data-en="Receive treatment in the comfort and privacy of your own home." data-ar="احصل على العلاج في راحة وخصوصية منزلك.">Receive treatment in the comfort and privacy of your own home.</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="w-12 h-12 bg-secondary-200 rounded-xl flex items-center justify-center text-secondary-700 text-xl mr-4 flex-shrink-0">
                                <i class="fas fa-calendar-alt"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-secondary-900 mb-1" data-en="Flexible Scheduling" data-ar="جدولة مرنة">Flexible Scheduling</h4>
                                <p class="text-secondary-600" data-en="Appointments that fit your busy lifestyle, including weekends." data-ar="مواعيد تناسب نمط حياتك المزدحم، بما في ذلك عطلات نهاية الأسبوع.">Appointments that fit your busy lifestyle, including weekends.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 lg:py-32 bg-gradient-to-br from-secondary-900 to-primary-900 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <span class="text-accent-400 font-semibold text-sm uppercase tracking-wider" data-en="Get In Touch" data-ar="تواصل معنا">Get In Touch</span>
                <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold mt-4 mb-6" data-en="Ready To Start Your Recovery?" data-ar="مستعد لبدء رحلة التعافي؟">
                    Ready To Start Your Recovery?
                </h2>
                <p class="text-white/70 max-w-2xl mx-auto text-lg" data-en="Contact us today to schedule your appointment at our center or request a home visit." data-ar="اتصل بنا اليوم لحجز موعدك في مركزنا أو طلب زيارة منزلية.">
                    Contact us today to schedule your appointment at our center or request a home visit.
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-4xl mx-auto">
                <!-- Contact Card 1 -->
                <div class="glass rounded-2xl p-8 text-center hover:bg-white/20 transition-all">
                    <div class="w-16 h-16 bg-accent-500 rounded-full flex items-center justify-center text-2xl mx-auto mb-4">
                        <i class="fas fa-phone-alt"></i>
                    </div>
                    <h3 class="font-bold text-xl mb-2" data-en="Call Us" data-ar="اتصل بنا">Call Us</h3>
                    <p class="text-white/70 mb-4" data-en="Available for appointments" data-ar="متاح للحجوزات">Available for appointments</p>
                    <a href="tel:+1234567890" class="text-accent-400 font-semibold hover:text-accent-300 transition-colors">
                        +1 (234) 567-890
                    </a>
                </div>
                
                <!-- Contact Card 2 -->
                <div class="glass rounded-2xl p-8 text-center hover:bg-white/20 transition-all">
                    <div class="w-16 h-16 bg-primary-500 rounded-full flex items-center justify-center text-2xl mx-auto mb-4">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <h3 class="font-bold text-xl mb-2" data-en="Visit Us" data-ar="زورونا">Visit Us</h3>
                    <p class="text-white/70 mb-4" data-en="Our center location" data-ar="موقع مركزنا">Our center location</p>
                    <span class="text-primary-400 font-semibold" data-en="123 Health Street, City" data-ar="123 شارع الصحة، المدينة">
                        123 Health Street, City
                    </span>
                </div>
                
                <!-- Contact Card 3 -->
                <div class="glass rounded-2xl p-8 text-center hover:bg-white/20 transition-all">
                    <div class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center text-2xl mx-auto mb-4">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3 class="font-bold text-xl mb-2" data-en="Working Hours" data-ar="ساعات العمل">Working Hours</h3>
                    <p class="text-white/70 mb-4" data-en="We're here for you" data-ar="نحن هنا من أجلك">We're here for you</p>
                    <span class="text-blue-400 font-semibold" data-en="Sat-Thu: 9AM - 9PM" data-ar="السبت-الخميس: 9ص - 9م">
                        Sat-Thu: 9AM - 9PM
                    </span>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-secondary-950 text-white py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <!-- Brand -->
                <div class="md:col-span-2">
                    <div class="flex items-center space-x-3 mb-4">
                        <div class="w-12 h-12 bg-gradient-to-br from-primary-500 to-accent-500 rounded-xl flex items-center justify-center text-white text-2xl font-bold">
                            <i class="fas fa-heartbeat"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold" data-en="Elite Care" data-ar="الرعاية النخبوية">Elite Care</h3>
                            <p class="text-secondary-400 text-sm" data-en="Rehabilitation Center" data-ar="مركز التأهيل">Rehabilitation Center</p>
                        </div>
                    </div>
                    <p class="text-secondary-400 leading-relaxed max-w-md" data-en="Professional sports rehabilitation, cupping therapy, and therapeutic massage services. Your journey to wellness starts here." data-ar="خدمات احترافية للتأهيل الرياضي والحجامة والمساج العلاجي. رحلتك نحو العافية تبدأ هنا.">
                        Professional sports rehabilitation, cupping therapy, and therapeutic massage services. 
                        Your journey to wellness starts here.
                    </p>
                </div>
                
                <!-- Quick Links -->
                <div>
                    <h4 class="font-bold text-lg mb-4" data-en="Quick Links" data-ar="روابط سريعة">Quick Links</h4>
                    <ul class="space-y-2 text-secondary-400">
                        <li><a href="#home" class="hover:text-white transition-colors" data-en="Home" data-ar="الرئيسية">Home</a></li>
                        <li><a href="#team" class="hover:text-white transition-colors" data-en="Our Team" data-ar="فريقنا">Our Team</a></li>
                        <li><a href="#services" class="hover:text-white transition-colors" data-en="Services" data-ar="خدماتنا">Services</a></li>
                        <li><a href="#contact" class="hover:text-white transition-colors" data-en="Contact" data-ar="اتصل بنا">Contact</a></li>
                    </ul>
                </div>
                
                <!-- Services -->
                <div>
                    <h4 class="font-bold text-lg mb-4" data-en="Services" data-ar="خدماتنا">Services</h4>
                    <ul class="space-y-2 text-secondary-400">
                        <li data-en="Sports Rehabilitation" data-ar="التأهيل الرياضي">Sports Rehabilitation</li>
                        <li data-en="Cupping Therapy" data-ar="الحجامة">Cupping Therapy</li>
                        <li data-en="Therapeutic Massage" data-ar="المساج العلاجي">Therapeutic Massage</li>
                        <li data-en="Home Visits" data-ar="الزيارات المنزلية">Home Visits</li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-secondary-800 mt-12 pt-8 text-center text-secondary-500">
                <p data-en="© 2025 Elite Care Rehabilitation Center. All rights reserved." data-ar="© 2025 مركز الرعاية النخبوية للتأهيل. جميع الحقوق محفوظة.">&copy; 2025 Elite Care Rehabilitation Center. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button id="back-to-top" class="fixed bottom-6 right-6 w-12 h-12 bg-gradient-to-r from-primary-600 to-accent-500 text-white rounded-full shadow-lg flex items-center justify-center text-xl opacity-0 invisible transition-all hover:shadow-xl hover:scale-110 z-50">
        <i class="fas fa-arrow-up"></i>
    </button>

    <!-- JavaScript -->
    <script>
        // Language Switcher Function
        let currentLang = 'en';
        
        function switchLanguage(lang) {
            currentLang = lang;
            
            // Update HTML attributes
            document.documentElement.lang = lang;
            document.documentElement.dir = lang === 'ar' ? 'rtl' : 'ltr';
            
            // Update all translatable elements
            document.querySelectorAll('[data-en]').forEach(element => {
                const text = element.getAttribute(`data-${lang}`);
                if (text) {
                    element.textContent = text;
                }
            });
            
            // Update button states
            updateLanguageButtons();
            
            // Save preference
            localStorage.setItem('preferredLanguage', lang);
        }
        
        function updateLanguageButtons() {
            const btnEn = document.getElementById('btn-en');
            const btnAr = document.getElementById('btn-ar');
            const btnEnMobile = document.getElementById('btn-en-mobile');
            const btnArMobile = document.getElementById('btn-ar-mobile');
            
            if (currentLang === 'en') {
                btnEn.classList.add('active');
                btnAr.classList.remove('active');
                btnEnMobile.classList.add('active');
                btnArMobile.classList.remove('active');
            } else {
                btnEn.classList.remove('active');
                btnAr.classList.add('active');
                btnEnMobile.classList.remove('active');
                btnArMobile.classList.add('active');
            }
        }
        
        // Load saved language preference
        document.addEventListener('DOMContentLoaded', () => {
            const savedLang = localStorage.getItem('preferredLanguage');
            if (savedLang && savedLang !== currentLang) {
                switchLanguage(savedLang);
            }
        });
        
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
            const icon = mobileMenuBtn.querySelector('i');
            if (mobileMenu.classList.contains('hidden')) {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            } else {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            }
        });
        
        // Close mobile menu when clicking on a link
        const mobileLinks = mobileMenu.querySelectorAll('a');
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
                mobileMenuBtn.querySelector('i').classList.remove('fa-times');
                mobileMenuBtn.querySelector('i').classList.add('fa-bars');
            });
        });
        
        // Back to Top Button
        const backToTopBtn = document.getElementById('back-to-top');
        
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                backToTopBtn.classList.remove('opacity-0', 'invisible');
                backToTopBtn.classList.add('opacity-100', 'visible');
            } else {
                backToTopBtn.classList.add('opacity-0', 'invisible');
                backToTopBtn.classList.remove('opacity-100', 'visible');
            }
        });
        
        backToTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Smooth scroll for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    const offset = 80;
                    const targetPosition = target.getBoundingClientRect().top + window.pageYOffset - offset;
                    window.scrollTo({
                        top: targetPosition,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-fadeInUp');
                }
            });
        }, observerOptions);
        
        // Observe elements for animation
        document.querySelectorAll('.member-card, .group').forEach(el => {
            el.style.opacity = '0';
            observer.observe(el);
        });
    </script>
</body>
</html>
