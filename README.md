<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YugNirmaan - India's First Freelancer-Style Construction Marketplace</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'gold': '#D4AF37',
                        'gold-light': '#F4E4BC',
                        'gold-dark': '#B8860B',
                        'charcoal': '#1a1a1a',
                        'charcoal-light': '#2d2d2d',
                        'charcoal-dark': '#0d0d0d'
                    },
                    fontFamily: {
                        'display': ['Playfair Display', 'serif'],
                        'body': ['Inter', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800;900&family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: #0d0d0d;
            color: white;
            overflow-x: hidden;
        }
        
        .premium-gradient {
            background: linear-gradient(135deg, #0d0d0d 0%, #1a1a1a 50%, #2d2d2d 100%);
        }
        
        .white-section {
            background: linear-gradient(135deg, #fafafa 0%, #ffffff 50%, #f5f5f5 100%);
            color: #2d2d2d;
        }
        
        .white-section h2, .white-section h3, .white-section h4 {
            color: #1a1a1a;
        }
        
        .white-section .text-gold-gradient {
            background: linear-gradient(135deg, #B8860B 0%, #D4AF37 50%, #F4E4BC 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .white-section .glass-card {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(212, 175, 55, 0.3);
            color: #2d2d2d;
            box-shadow: 
                0 8px 32px rgba(0, 0, 0, 0.1),
                inset 0 1px 0 rgba(212, 175, 55, 0.1);
        }
        
        .white-section .glass-card:hover {
            background: rgba(255, 255, 255, 0.9);
            border-color: rgba(212, 175, 55, 0.5);
            box-shadow: 
                0 20px 40px rgba(0, 0, 0, 0.15),
                0 0 30px rgba(212, 175, 55, 0.2),
                inset 0 1px 0 rgba(212, 175, 55, 0.15);
        }
        
        .white-section .text-gray-300 {
            color: #4a5568 !important;
        }
        
        .textured-bg {
            background-image: 
                radial-gradient(circle at 20% 80%, rgba(212, 175, 55, 0.12) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(212, 175, 55, 0.08) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(255, 255, 255, 0.04) 0%, transparent 50%),
                linear-gradient(135deg, #0d0d0d 0%, #1a1a1a 50%, #2d2d2d 100%);
            background-size: 800px 800px, 600px 600px, 400px 400px, 100% 100%;
            position: relative;
        }
        
        .textured-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: 
                repeating-linear-gradient(
                    45deg,
                    transparent,
                    transparent 2px,
                    rgba(212, 175, 55, 0.02) 2px,
                    rgba(212, 175, 55, 0.02) 4px
                );
            pointer-events: none;
        }
        
        .textured-bg-alt {
            background-image: 
                radial-gradient(circle at 70% 30%, rgba(212, 175, 55, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 30% 70%, rgba(212, 175, 55, 0.06) 0%, transparent 50%),
                radial-gradient(circle at 60% 60%, rgba(255, 255, 255, 0.03) 0%, transparent 50%),
                linear-gradient(225deg, #0d0d0d 0%, #1a1a1a 50%, #2d2d2d 100%);
            background-size: 700px 700px, 500px 500px, 300px 300px, 100% 100%;
            position: relative;
        }
        
        .textured-bg-alt::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: 
                repeating-linear-gradient(
                    -45deg,
                    transparent,
                    transparent 3px,
                    rgba(212, 175, 55, 0.015) 3px,
                    rgba(212, 175, 55, 0.015) 6px
                );
            pointer-events: none;
        }
        
        .white-textured-bg {
            background-image: 
                radial-gradient(circle at 20% 80%, rgba(212, 175, 55, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(212, 175, 55, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(0, 0, 0, 0.05) 0%, transparent 50%),
                linear-gradient(135deg, #ffffff 0%, #f8f9fa 50%, #e9ecef 100%);
            background-size: 800px 800px, 600px 600px, 400px 400px, 100% 100%;
            position: relative;
        }
        
        .white-textured-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: 
                repeating-linear-gradient(
                    45deg,
                    transparent,
                    transparent 2px,
                    rgba(212, 175, 55, 0.03) 2px,
                    rgba(212, 175, 55, 0.03) 4px
                );
            pointer-events: none;
        }
        
        .gold-gradient {
            background: linear-gradient(135deg, #D4AF37 0%, #F4E4BC 50%, #B8860B 100%);
        }
        
        .glass-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(212, 175, 55, 0.2);
            border-radius: 16px;
            box-shadow: 
                0 8px 32px rgba(0, 0, 0, 0.3),
                inset 0 1px 0 rgba(255, 255, 255, 0.1);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .glass-card:hover {
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(212, 175, 55, 0.4);
            transform: translateY(-8px);
            box-shadow: 
                0 20px 40px rgba(0, 0, 0, 0.4),
                0 0 30px rgba(212, 175, 55, 0.2),
                inset 0 1px 0 rgba(255, 255, 255, 0.15);
        }
        
        .premium-button {
            background: linear-gradient(135deg, #D4AF37 0%, #F4E4BC 50%, #B8860B 100%);
            color: #0d0d0d;
            font-weight: 700;
            padding: 16px 32px;
            border-radius: 12px;
            border: none;
            cursor: pointer;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 
                0 8px 25px rgba(212, 175, 55, 0.3),
                inset 0 1px 0 rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }
        
        .premium-button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.6s ease;
        }
        
        .premium-button:hover::before {
            left: 100%;
        }
        
        .premium-button:hover {
            transform: translateY(-4px) scale(1.05);
            box-shadow: 
                0 15px 35px rgba(212, 175, 55, 0.4),
                0 0 40px rgba(212, 175, 55, 0.2),
                inset 0 1px 0 rgba(255, 255, 255, 0.3);
        }
        
        .text-gold-gradient {
            background: linear-gradient(135deg, #D4AF37 0%, #F4E4BC 50%, #B8860B 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .hero-pattern {
            background-image: 
                radial-gradient(circle at 25% 25%, rgba(212, 175, 55, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 75% 75%, rgba(212, 175, 55, 0.05) 0%, transparent 50%),
                linear-gradient(135deg, #0d0d0d 0%, #1a1a1a 100%);
            background-size: 600px 600px, 400px 400px, 100% 100%;
            animation: heroFloat 20s ease-in-out infinite;
        }
        
        @keyframes heroFloat {
            0%, 100% { background-position: 0% 0%, 100% 100%, 0 0; }
            50% { background-position: 100% 100%, 0% 0%, 0 0; }
        }
        
        .fade-up {
            opacity: 0;
            transform: translateY(60px);
            transition: all 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .fade-up.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .stagger-1 { transition-delay: 0.1s; }
        .stagger-2 { transition-delay: 0.2s; }
        .stagger-3 { transition-delay: 0.3s; }
        .stagger-4 { transition-delay: 0.4s; }
        
        .nav-glass {
            background: rgba(13, 13, 13, 0.9);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .section-divider {
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(212, 175, 55, 0.3), transparent);
            margin: 80px 0;
        }
        
        .floating-element {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .pulse-gold {
            animation: pulseGold 2s ease-in-out infinite;
        }
        
        @keyframes pulseGold {
            0%, 100% { box-shadow: 0 0 20px rgba(212, 175, 55, 0.3); }
            50% { box-shadow: 0 0 40px rgba(212, 175, 55, 0.6); }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="fixed top-0 w-full nav-glass z-50 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 gold-gradient rounded-lg flex items-center justify-center">
                        <span class="text-2xl">🏗️</span>
                    </div>
                    <div>
                        <h1 class="text-2xl font-display font-bold text-gold-gradient">YugNirmaan</h1>
                        <p class="text-xs text-gray-400">Building Trust, Building India</p>
                    </div>
                </div>
                
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="text-white hover:text-gold transition-all duration-300 font-medium">Home</a>
                    <a href="#about" class="text-white hover:text-gold transition-all duration-300 font-medium">About</a>
                    <a href="#how-it-works" class="text-white hover:text-gold transition-all duration-300 font-medium">How It Works</a>
                    <a href="#benefits" class="text-white hover:text-gold transition-all duration-300 font-medium">Benefits</a>
                    <a href="mailto:yugnirmaan.india@gmail.com" class="premium-button text-sm">Contact Us</a>
                </div>
                
                <button class="md:hidden text-white">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen hero-pattern flex items-center relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-b from-transparent via-charcoal/20 to-charcoal/40"></div>
        
        <div class="max-w-7xl mx-auto px-6 lg:px-8 py-32 relative z-10">
            <div class="text-center">
                <div class="fade-up">
                    <h1 class="text-6xl md:text-8xl font-display font-bold mb-6">
                        <span class="text-gold-gradient">YugNirmaan</span>
                    </h1>
                    <p class="text-2xl md:text-3xl text-gold font-semibold mb-4">
                        India's First Freelancer-Style Construction Marketplace
                    </p>
                    <p class="text-xl text-gray-300 max-w-4xl mx-auto mb-12 leading-relaxed">
                        Building Trust, Building India
                    </p>
                </div>
                
                <div class="fade-up stagger-2">
                    <div class="flex flex-col sm:flex-row gap-6 justify-center items-center">
                        <a href="#register" class="premium-button text-lg px-8 py-4">
                            Get Started Today
                        </a>
                        <a href="#about" class="glass-card px-8 py-4 text-white font-semibold transition-all duration-300 hover:text-gold">
                            Learn More
                        </a>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 floating-element">
            <div class="w-6 h-10 border-2 border-gold rounded-full flex justify-center">
                <div class="w-1 h-3 bg-gold rounded-full mt-2 animate-bounce"></div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 premium-gradient textured-bg">
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 fade-up">
                <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
                    🌍 What is <span class="text-gold-gradient">YugNirmaan</span>?
                </h2>
                <p class="text-xl text-gray-300 max-w-4xl mx-auto">
                    YugNirmaan is a revolutionary platform designed to solve the biggest challenge in India's construction industry – trust and transparency.
                </p>
            </div>

            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="space-y-8 fade-up">
                    <div class="glass-card p-8 rounded-lg">
                        <h3 class="text-2xl font-display font-bold text-gold mb-6">For decades, customers have struggled with:</h3>
                        <ul class="space-y-4 text-gray-300">
                            <li class="flex items-center"><span class="text-gold mr-3">•</span> Delayed projects</li>
                            <li class="flex items-center"><span class="text-gold mr-3">•</span> Budget overruns</li>
                            <li class="flex items-center"><span class="text-gold mr-3">•</span> Contractors abandoning work after taking advance payments</li>
                        </ul>
                    </div>
                </div>

                <div class="space-y-8 fade-up stagger-1">
                    <div class="glass-card p-8 rounded-lg">
                        <h3 class="text-2xl font-display font-bold text-gold mb-6">On the other side, contractors face:</h3>
                        <ul class="space-y-4 text-gray-300">
                            <li class="flex items-center"><span class="text-gold mr-3">•</span> Difficulty finding genuine projects</li>
                            <li class="flex items-center"><span class="text-gold mr-3">•</span> Payment delays</li>
                            <li class="flex items-center"><span class="text-gold mr-3">•</span> Risk of fraud</li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="text-center mt-16 fade-up stagger-2">
                <div class="glass-card p-8 rounded-lg pulse-gold max-w-4xl mx-auto">
                    <h3 class="text-3xl font-display font-bold text-gold mb-4">Our Solution</h3>
                    <p class="text-xl text-gray-300">
                        YugNirmaan bridges this gap by creating a trusted digital ecosystem where customers and verified contractors connect securely with milestone-based payments.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider max-w-7xl mx-auto px-6 lg:px-8"></div>

    <!-- How It Works -->
    <section id="how-it-works" class="py-20 textured-bg">
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center mb-20 fade-up">
                <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
                    🔑 How <span class="text-gold-gradient">YugNirmaan</span> Works
                </h2>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="glass-card p-8 fade-up stagger-1">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 gold-gradient rounded-full flex items-center justify-center text-black font-bold text-xl mr-4">1</div>
                        <h3 class="text-xl font-display font-bold text-gold">Customer posts a project</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed">
                        Including location, budget, and requirements (home construction, renovation, or office setup).
                    </p>
                </div>
                
                <div class="glass-card p-8 fade-up stagger-2">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 gold-gradient rounded-full flex items-center justify-center text-black font-bold text-xl mr-4">2</div>
                        <h3 class="text-xl font-display font-bold text-gold">Verified contractors place bids</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed">
                        With their rates, timeline, and portfolio.
                    </p>
                </div>
                
                <div class="glass-card p-8 fade-up stagger-3">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 gold-gradient rounded-full flex items-center justify-center text-black font-bold text-xl mr-4">3</div>
                        <h3 class="text-xl font-display font-bold text-gold">Shortlist & selection</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed">
                        Customers receive a curated list and select the contractor.
                    </p>
                </div>
                
                <div class="glass-card p-8 fade-up stagger-1">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 gold-gradient rounded-full flex items-center justify-center text-black font-bold text-xl mr-4">4</div>
                        <h3 class="text-xl font-display font-bold text-gold">Escrow payment system</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed">
                        Customer deposits money into a secure YugNirmaan account.
                    </p>
                </div>
                
                <div class="glass-card p-8 fade-up stagger-2">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 gold-gradient rounded-full flex items-center justify-center text-black font-bold text-xl mr-4">5</div>
                        <h3 class="text-xl font-display font-bold text-gold">Milestone-based releases</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed">
                        Funds are released only when each project stage is completed and approved.
                    </p>
                </div>
                
                <div class="glass-card p-8 fade-up stagger-3">
                    <div class="flex items-center mb-6">
                        <div class="w-12 h-12 gold-gradient rounded-full flex items-center justify-center text-black font-bold text-xl mr-4">6</div>
                        <h3 class="text-xl font-display font-bold text-gold">Project completion</h3>
                    </div>
                    <p class="text-gray-300 leading-relaxed">
                        Customer pays safely, contractor earns without delays.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider max-w-7xl mx-auto px-6 lg:px-8"></div>

    <!-- Escrow System Section -->
    <section class="py-20 premium-gradient textured-bg-alt">
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 fade-up">
                <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
                    💰 Escrow System – <span class="text-gold-gradient">Why It Matters</span>
                </h2>
                <p class="text-xl text-gray-300 max-w-3xl mx-auto mb-12">
                    The escrow system ensures zero risk for both sides. This protects both dreams and money.
                </p>
            </div>

            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="glass-card p-8 rounded-lg fade-up">
                    <h3 class="text-2xl font-display font-bold text-gold mb-6">Payment Example:</h3>
                    <div class="space-y-4">
                        <div class="flex justify-between items-center p-4 bg-gradient-to-r from-gold/10 to-gold/5 rounded border border-gold/20">
                            <span class="text-gray-300">Foundation completion</span>
                            <span class="text-gold font-bold">20%</span>
                        </div>
                        <div class="flex justify-between items-center p-4 bg-gradient-to-r from-gold/10 to-gold/5 rounded border border-gold/20">
                            <span class="text-gray-300">Structure completion</span>
                            <span class="text-gold font-bold">30%</span>
                        </div>
                        <div class="flex justify-between items-center p-4 bg-gradient-to-r from-gold/10 to-gold/5 rounded border border-gold/20">
                            <span class="text-gray-300">Finishing</span>
                            <span class="text-gold font-bold">30%</span>
                        </div>
                        <div class="flex justify-between items-center p-4 bg-gradient-to-r from-gold/10 to-gold/5 rounded border border-gold/20">
                            <span class="text-gray-300">Final handover</span>
                            <span class="text-gold font-bold">20%</span>
                        </div>
                    </div>
                </div>

                <div class="space-y-6 fade-up stagger-1">
                    <div class="glass-card p-6 rounded-lg">
                        <h4 class="text-xl font-display font-bold text-gold mb-3">For Customers</h4>
                        <p class="text-gray-300">Money is safe until work is delivered</p>
                    </div>
                    <div class="glass-card p-6 rounded-lg">
                        <h4 class="text-xl font-display font-bold text-gold mb-3">For Contractors</h4>
                        <p class="text-gray-300">Payment is guaranteed once milestones are achieved</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider max-w-7xl mx-auto px-6 lg:px-8"></div>

    <!-- Benefits Section -->
    <section id="benefits" class="py-20 textured-bg">
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 fade-up">
                <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
                    🎯 Benefits of <span class="text-gold-gradient">YugNirmaan</span>
                </h2>
            </div>

            <div class="grid md:grid-cols-2 gap-12">
                <div class="glass-card p-8 rounded-lg fade-up">
                    <h3 class="text-3xl font-display font-bold text-gold mb-6">For Customers:</h3>
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">Access to verified and trustworthy contractors</span>
                        </div>
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">Best price through transparent bidding</span>
                        </div>
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">100% safe payments via escrow</span>
                        </div>
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">Regular project updates & milestone tracking</span>
                        </div>
                    </div>
                </div>

                <div class="glass-card p-8 rounded-lg fade-up stagger-1">
                    <h3 class="text-3xl font-display font-bold text-gold mb-6">For Contractors:</h3>
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">Verified and genuine projects</span>
                        </div>
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">Assured timely payments without delays</span>
                        </div>
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">Portfolio building with ratings & reviews</span>
                        </div>
                        <div class="flex items-start">
                            <span class="text-gold text-xl mr-3">✅</span>
                            <span class="text-gray-300">Repeat business opportunities</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider max-w-7xl mx-auto px-6 lg:px-8"></div>

    <!-- Vision Section -->
    <section class="py-20 premium-gradient textured-bg-alt">
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 fade-up">
                <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
                    🚀 Vision for the <span class="text-gold-gradient">Future</span>
                </h2>
            </div>

            <div class="grid md:grid-cols-3 gap-8">
                <div class="text-center glass-card p-8 rounded-lg fade-up">
                    <div class="text-4xl mb-4">🎯</div>
                    <h3 class="text-xl font-display font-bold text-gold mb-3">Mission</h3>
                    <p class="text-gray-300">YugNirmaan's mission is to become India's most trusted construction ecosystem.</p>
                </div>

                <div class="text-center glass-card p-8 rounded-lg fade-up stagger-1">
                    <div class="text-4xl mb-4">📍</div>
                    <h3 class="text-xl font-display font-bold text-gold mb-3">Expansion</h3>
                    <p class="text-gray-300">Starting from Indore, we aim to expand nationwide.</p>
                </div>

                <div class="text-center glass-card p-8 rounded-lg fade-up stagger-2">
                    <div class="text-4xl mb-4">🏢</div>
                    <h3 class="text-xl font-display font-bold text-gold mb-3">Complete Ecosystem</h3>
                    <p class="text-gray-300">YugNirmaan will also provide materials, loans, and real estate services, creating a complete digital ecosystem for construction.</p>
                </div>
            </div>

            <div class="text-center mt-16 fade-up stagger-3">
                <div class="glass-card p-8 rounded-lg pulse-gold max-w-4xl mx-auto">
                    <h3 class="text-3xl font-display font-bold text-gold mb-4">❤️ Social Responsibility</h3>
                    <p class="text-xl text-gray-300">
                        YugNirmaan will donate 5% of its profits to charity and community development projects – because true construction is not just about buildings, but also about building society.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider max-w-7xl mx-auto px-6 lg:px-8"></div>

    <!-- Registration Section -->
    <section id="register" class="py-20 textured-bg">
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 fade-up">
                <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
                    📝 How to <span class="text-gold-gradient">Register</span>
                </h2>
            </div>

            <div class="grid md:grid-cols-2 gap-12">
                <div class="glass-card p-10 fade-up">
                    <div class="text-center mb-8">
                        <div class="w-20 h-20 gold-gradient rounded-full flex items-center justify-center mx-auto mb-4">
                            <span class="text-3xl">👥</span>
                        </div>
                        <h3 class="text-3xl font-display font-bold text-gold mb-4">For Customers</h3>
                    </div>
                    
                    <div class="space-y-4 mb-8">
                        <div class="flex items-center space-x-3">
                            <div class="w-6 h-6 gold-gradient rounded-full flex items-center justify-center">
                                <span class="text-black text-xs font-bold">1</span>
                            </div>
                            <span class="text-gray-300">Visit our registration page</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="w-6 h-6 gold-gradient rounded-full flex items-center justify-center">
                                <span class="text-black text-xs font-bold">2</span>
                            </div>
                            <span class="text-gray-300">Enter your phone number, location, and project requirements</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="w-6 h-6 gold-gradient rounded-full flex items-center justify-center">
                                <span class="text-black text-xs font-bold">3</span>
                            </div>
                            <span class="text-gray-300">Post your project and start receiving contractor bids</span>
                        </div>
                    </div>
                    
                    <a href="https://forms.gle/9M3SV8DVA81u3nNi8" target="_blank" class="premium-button w-full">
                        Register as Customer
                    </a>
                </div>
                
                <div class="glass-card p-10 fade-up stagger-1">
                    <div class="text-center mb-8">
                        <div class="w-20 h-20 gold-gradient rounded-full flex items-center justify-center mx-auto mb-4">
                            <span class="text-3xl">🔨</span>
                        </div>
                        <h3 class="text-3xl font-display font-bold text-gold mb-4">For Contractors</h3>
                    </div>
                    
                    <div class="space-y-4 mb-8">
                        <div class="flex items-center space-x-3">
                            <div class="w-6 h-6 gold-gradient rounded-full flex items-center justify-center">
                                <span class="text-black text-xs font-bold">1</span>
                            </div>
                            <span class="text-gray-300">Register with Aadhaar, PAN, and portfolio details</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="w-6 h-6 gold-gradient rounded-full flex items-center justify-center">
                                <span class="text-black text-xs font-bold">2</span>
                            </div>
                            <span class="text-gray-300">Get verified by YugNirmaan's team</span>
                        </div>
                        <div class="flex items-center space-x-3">
                            <div class="w-6 h-6 gold-gradient rounded-full flex items-center justify-center">
                                <span class="text-black text-xs font-bold">3</span>
                            </div>
                            <span class="text-gray-300">Start bidding on genuine projects and grow your business</span>
                        </div>
                    </div>
                    
                    <a href="https://forms.gle/85vN9SHRRqP5K7Km7" target="_blank" class="premium-button w-full">
                        Register as Contractor
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="premium-gradient textured-bg py-16 border-t border-gold/20">
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center">
                <div class="flex items-center justify-center space-x-4 mb-8">
                    <div class="w-16 h-16 gold-gradient rounded-lg flex items-center justify-center">
                        <span class="text-3xl">🏗️</span>
                    </div>
                    <div>
                        <h3 class="text-3xl font-display font-bold text-gold-gradient">YugNirmaan</h3>
                        <p class="text-gray-400">Building Trust, Building India</p>
                    </div>
                </div>
                
                <div class="glass-card p-8 max-w-4xl mx-auto mb-12">
                    <h4 class="text-2xl font-display font-bold text-gold mb-4">✨ Our Promise</h4>
                    <p class="text-lg text-gray-300 leading-relaxed mb-4">
                        YugNirmaan is more than a company – it is a movement to rebuild trust in India's construction industry.
                    </p>
                    <p class="text-2xl font-display font-bold text-gold-gradient">
                        YugNirmaan – Building Trust, Building India.
                    </p>
                </div>
                
                <div class="flex flex-wrap justify-center gap-8 mb-8">
                    <a href="#home" class="text-gray-400 hover:text-gold transition-all duration-300">Home</a>
                    <a href="#about" class="text-gray-400 hover:text-gold transition-all duration-300">About</a>
                    <a href="#how-it-works" class="text-gray-400 hover:text-gold transition-all duration-300">How It Works</a>
                    <a href="#benefits" class="text-gray-400 hover:text-gold transition-all duration-300">Benefits</a>
                    <a href="mailto:yugnirmaan.india@gmail.com" class="text-gold hover:text-white transition-all duration-300 font-semibold">
                        📧 yugnirmaan.india@gmail.com
                    </a>
                </div>
                
                <div class="border-t border-gold/20 pt-8">
                    <p class="text-gray-400">
                        © 2024 YugNirmaan. All rights reserved. Building Trust, Building India.
                    </p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Enhanced scroll effects
        let ticking = false;
        
        function updateScrollEffects() {
            const nav = document.querySelector('nav');
            const scrolled = window.scrollY;
            
            if (scrolled > 50) {
                nav.style.background = 'rgba(13, 13, 13, 0.95)';
                nav.style.backdropFilter = 'blur(25px)';
            } else {
                nav.style.background = 'rgba(13, 13, 13, 0.9)';
                nav.style.backdropFilter = 'blur(20px)';
            }
            
            ticking = false;
        }
        
        window.addEventListener('scroll', function() {
            if (!ticking) {
                requestAnimationFrame(updateScrollEffects);
                ticking = true;
            }
        });

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-up').forEach(el => {
            observer.observe(el);
        });

        // Premium loading animation
        window.addEventListener('load', function() {
            document.body.style.opacity = '1';
            
            // Trigger hero animations
            setTimeout(() => {
                document.querySelectorAll('#home .fade-up').forEach((el, index) => {
                    setTimeout(() => {
                        el.classList.add('visible');
                    }, index * 200);
                });
            }, 300);
        });
        
        // Initial page setup
        document.addEventListener('DOMContentLoaded', function() {
            document.body.style.opacity = '0';
            document.body.style.transition = 'opacity 0.8s ease';
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9821ac6977ac9a7d',t:'MTc1ODM3NDk4NS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>