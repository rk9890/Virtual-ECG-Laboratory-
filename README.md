<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Virtual ECG Laboratory</title>
  <!-- Include Tailwind CSS for styling -->
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Custom styles for animations/effects (approximated) */
    .glow-effect { box-shadow: 0 0 20px rgba(59, 130, 246, 0.5); }
    .float-animation { animation: float 3s ease-in-out infinite; }
    @keyframes float { 0%, 100% { transform: translateY(0px); } 50% { transform: translateY(-10px); } }
    .animate-pulse { animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite; }
    @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }
    .animate-gradient { animation: gradient 3s ease infinite; background-size: 200% 200%; }
    @keyframes gradient { 0%, 100% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } }
    .glass-panel { backdrop-filter: blur(10px); background: rgba(255, 255, 255, 0.1); }
  </style>
</head>
<body class="min-h-screen bg-gradient-to-br from-gray-50 via-blue-50 to-purple-50 relative overflow-hidden">
  <!-- Animated background elements -->
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <div class="absolute top-20 left-10 w-72 h-72 bg-blue-100 rounded-full blur-3xl animate-pulse"></div>
    <div class="absolute bottom-20 right-10 w-96 h-96 bg-purple-100 rounded-full blur-3xl animate-pulse delay-1000"></div>
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-gradient-to-r from-blue-50 to-purple-50 rounded-full blur-3xl"></div>
  </div>

  <!-- Hero Section -->
  <header class="container mx-auto px-4 pt-20 pb-16 relative z-10">
    <div class="flex flex-col items-center text-center space-y-8">
      <div class="relative">
        <div class="h-24 w-24 rounded-3xl bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center shadow-2xl glow-effect float-animation">
          <span class="text-white text-2xl">🧪</span> <!-- Replaced FlaskConical icon -->
        </div>
        <div class="absolute -inset-6 bg-gradient-to-r from-blue-200 to-purple-200 blur-3xl -z-10 animate-pulse"></div>
      </div>
      
      <div class="space-y-6 max-w-4xl">
        <div class="inline-block text-sm px-6 py-2 bg-gray-200 rounded-full shadow-lg">
          <span class="h-2 w-2 rounded-full bg-green-500 animate-pulse inline-block mr-2"></span>
          Experiment 3 - Bio-Medical Instrumentation
        </div>
        <h1 class="text-5xl md:text-7xl font-bold bg-gradient-to-r from-blue-500 via-purple-500 to-blue-500 bg-clip-text text-transparent animate-gradient">
          Virtual ECG Laboratory
        </h1>
        <p class="text-xl md:text-2xl text-gray-600 max-w-2xl mx-auto leading-relaxed">
          Master the art of Electrocardiogram monitoring for augmented leads through interactive simulation and real-time feedback
        </p>
      </div>

      <div class="flex flex-col sm:flex-row gap-4">
        <a href="#lab" class="inline-block">
          <button class="bg-gradient-to-r from-blue-500 to-purple-500 hover:shadow-2xl hover:scale-105 transition-all duration-300 text-lg px-10 py-7 shadow-xl glow-effect text-white rounded-lg">
            Start Lab Experience
            <span class="ml-2">→</span>
          </button>
        </a>
        <a href="#demo" class="inline-block">
          <button class="text-lg px-10 py-7 border-2 border-gray-300 hover:bg-blue-50 hover:border-blue-500 transition-all duration-300 rounded-lg">
            <span class="mr-2">▶</span>
            View Demo
          </button>
        </a>
      </div>
    </div>
  </header>

  <!-- Stats Section -->
  <section class="container mx-auto px-4 py-12 relative z-10">
    <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-300 hover:scale-105 hover:shadow-xl p-6 text-center space-y-3 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center mx-auto shadow-lg">
          <span class="text-white text-xl">📊</span> <!-- Activity icon -->
        </div>
        <div>
          <p class="text-3xl font-bold bg-gradient-to-r from-blue-500 to-purple-500 bg-clip-text text-transparent">3</p>
          <p class="text-sm text-gray-600 font-medium">ECG Leads</p>
        </div>
      </div>
      <!-- Repeat for other stats: Brain (🧠), Clock (⏰), Award (🏆) -->
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-300 hover:scale-105 hover:shadow-xl p-6 text-center space-y-3 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-purple-500 to-blue-500 flex items-center justify-center mx-auto shadow-lg">
          <span class="text-white text-xl">🧠</span>
        </div>
        <div>
          <p class="text-3xl font-bold bg-gradient-to-r from-purple-500 to-blue-500 bg-clip-text text-transparent">4</p>
          <p class="text-sm text-gray-600 font-medium">Learning Modules</p>
        </div>
      </div>
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-300 hover:scale-105 hover:shadow-xl p-6 text-center space-y-3 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center mx-auto shadow-lg">
          <span class="text-white text-xl">⏰</span>
        </div>
        <div>
          <p class="text-3xl font-bold bg-gradient-to-r from-blue-500 to-purple-500 bg-clip-text text-transparent">45m</p>
          <p class="text-sm text-gray-600 font-medium">Avg. Duration</p>
        </div>
      </div>
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-300 hover:scale-105 hover:shadow-xl p-6 text-center space-y-3 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-purple-500 to-blue-500 flex items-center justify-center mx-auto shadow-lg">
          <span class="text-white text-xl">🏆</span>
        </div>
        <div>
          <p class="text-3xl font-bold bg-gradient-to-r from-purple-500 to-blue-500 bg-clip-text text-transparent">98%</p>
          <p class="text-sm text-gray-600 font-medium">Success Rate</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Features Grid -->
  <section class="container mx-auto px-4 py-16 relative z-10">
    <div class="text-center mb-12 space-y-4">
      <div class="inline-block text-sm px-4 py-1 border border-gray-300 rounded-full">Key Features</div>
      <h2 class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-blue-500 to-purple-500 bg-clip-text text-transparent">
        Why Choose Our Virtual Lab?
      </h2>
      <p class="text-gray-600 text-lg max-w-2xl mx-auto">
        Experience cutting-edge simulation technology designed for medical students
      </p>
    </div>
    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6 mb-16">
      <!-- Feature 1: Target (🎯) -->
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-500 hover:scale-105 p-6 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center mb-4 shadow-lg">
          <span class="text-white text-xl">🎯</span>
        </div>
        <h3 class="text-xl font-semibold">Precision Simulation</h3>
        <p class="text-gray-600">Real-time ECG waveform generation with accurate augmented lead calculations</p>
      </div>
      <!-- Repeat for other features: Zap (⚡), BookOpen (📖), Users (👥) -->
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-500 hover:scale-105 p-6 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-purple-500 to-blue-500 flex items-center justify-center mb-4 shadow-lg">
          <span class="text-white text-xl">⚡</span>
        </div>
        <h3 class="text-xl font-semibold">Interactive Learning</h3>
        <p class="text-gray-600">Hands-on electrode placement with instant visual feedback</p>
      </div>
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-500 hover:scale-105 p-6 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center mb-4 shadow-lg">
          <span class="text-white text-xl">📖</span>
        </div>
        <h3 class="text-xl font-semibold">Comprehensive Theory</h3>
        <p class="text-gray-600">In-depth coverage of ECG principles and clinical applications</p>
      </div>
      <div class="glass-panel border-2 border-blue-200 hover:border-blue-400 transition-all duration-500 hover:scale-105 p-6 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-purple-500 to-blue-500 flex items-center justify-center mb-4 shadow-lg">
          <span class="text-white text-xl">👥</span>
        </div>
        <h3 class="text-xl font-semibold">Self-Paced</h3>
        <p class="text-gray-600">Learn at your own speed with unlimited practice sessions</p>
      </div>
    </div>
  </section>

  <!-- Main Content Cards -->
  <main class="container mx-auto px-4 pb-20 relative z-10">
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
      <!-- Experiment Overview -->
      <div class="glass-panel shadow-2xl border-2 border-blue-200 hover:border-blue-400 transition-all duration-500 hover:scale-105 p-6 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center mb-4 shadow-lg glow-effect">
          <span class="text-white text-xl">🧪</span>
        </div>
        <h3 class="text-2xl font-semibold">Experiment Overview</h3>
        <p class="text-gray-600">Learn about ECG monitoring and augmented leads</p>
        <div class="space-y-3 mt-4">
          <h4 class="font-semibold text-lg flex items-center gap-2">
            <span>⚡</span> What You'll Monitor
          </h4>
          <ul class="space-y-3 text-sm">
            <li class="flex items-start gap-3"><span class="px-3 py-1 bg-blue-100 text-blue-600 rounded-lg font-semibold">aVR</span> Right arm augmented lead</li>
            <li class="flex items-start gap-3"><span class="px-3 py-1 bg-purple-100 text-purple-600 rounded-lg font-semibold">aVL</span> Left arm augmented lead</li>
            <li class="flex items-start gap-3"><span class="px-3 py-1 bg-red-100 text-red-600 rounded-lg font-semibold">aVF</span> Left foot augmented lead</li>
          </ul>
        </div>
      </div>

      <!-- Learning Objectives -->
      <div class="glass-panel shadow-2xl border-2 border-blue-200 hover:border-blue-400 transition-all duration-500 hover:scale-105 p-6 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-purple-500 to-blue-500 flex items-center justify-center mb-4 shadow-lg glow-effect">
          <span class="text-white text-xl">🎯</span>
        </div>
        <h3 class="text-2xl font-semibold">Learning Objectives</h3>
        <p class="text-gray-600">Key skills you'll develop in this lab</p>
        <ul class="space-y-3 text-sm mt-4">
          <li class="flex items-start gap-3"><span class="text-green-500">✓</span> Understand the derivation of augmented leads from limb electrodes</li>
          <li class="flex items-start gap-3"><span class="text-green-500">✓</span> Master proper electrode placement techniques</li>
          <li class="flex items-start gap-3"><span class="text-green-500">✓</span> Recognize normal ECG patterns in each augmented lead</li>
          <li class="flex items-start gap-3"><span class="text-green-500">✓</span> Apply knowledge to clinical diagnostic scenarios</li>
        </ul>
      </div>

      <!-- Prerequisites -->
      <div class="glass-panel shadow-2xl border-2 border-blue-200 hover:border-blue-400 transition-all duration-500 hover:scale-105 p-6 rounded-lg">
        <div class="h-14 w-14 rounded-2xl bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center mb-4 shadow-lg glow-effect">
          <span class="text-white text-xl">📖</span>
        </div>
        <h3 class="text-2xl font-semibold">Prerequisites</h3>
        <p class="text-gray-600">What you should know before starting</p>
        <ul class="space-y-3 text-sm mt-4">
          <li class="flex items-start gap-3"><span class="w-2 h-2 bg-gradient-to-r from-blue-500 to-purple-500 rounded-full mt-2"></span> Basic understanding of cardiovascular anatomy</li>
          <li class="flex items-start gap-3"><span class="w-2 h-2 bg-gradient-to-r from-blue-500 to-purple-500 rounded-full mt-2"></span> Familiarity with electrical signals in the body</li>
          <li class="flex items-start gap-3"><span class="w-2 h-2 bg-gradient-to-r from-blue-500 to-purple-500 rounded-full mt-2"></span> Knowledge of standard ECG lead placement (recommended)</li>
          <li class="flex items-start gap-3"><span class="w-2 h-2 bg-gradient-to-r from-blue-500 to-purple-500 rounded-full mt-2"></span> Understanding of Einthoven's triangle concept</li>
        </ul>
      </div>
    </div>
  </main>

  <!-- CTA Section -->
  <section class="container mx-auto px-4 py-16 relative z-10">
    <div class="glass-panel shadow-2xl border-2 border-blue-300 p-16 text-center rounded-lg">
      <div class="max-w-2xl mx-auto space-y-6">
        <h2 class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-blue-500 via-purple-500 to-blue-500 bg-clip-text text-transparent animate-gradient">
          Ready to Begin?
        </h2>
        <p class="text-lg text-gray-600">
          Start your journey into ECG monitoring and master augmented lead analysis
        </p>
        <a href="#lab" class="inline-block">
          <button class="bg-gradient-to-r from-blue-500 to-purple-500 hover:shadow-2xl hover:scale-110 transition-all duration-300 text-lg px-12 py-7 shadow-xl glow-effect text-white rounded-lg">
            Launch Virtual Lab
            <span class="ml-2">→</span>
          </button>
        </a>
      </div>
    </div>
  </section>

  <!-- Demo Section (Static Placeholder for Videos) -->
  <section id="demo" class="container mx-auto px-4 py-16 relative z-10">
    <h2 class="text-3xl font-bold text-center mb-8">Demo Videos</h2>
    <p class="text-center text-gray-600 mb-8">Watch these instructional videos (embedded from YouTube).</p>
    <div class="space-y-8">
      <div class="border-2 border-blue-200 p-6 rounded-lg">
        <h3 class="text-xl font-semibold mb-4">How To Place Augmented Limb Leads In ECG</h3>
        <iframe width="100%" height="400" src="https://www.youtube.com/embed/sMaAxv5uy8A" frameborder="0" allowfullscreen></iframe>
      </div>
      <div class="border-2 border-blue-
