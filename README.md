# Matrix-Mardwaretz.github.io
Load earlier messages
Your requested tool actions have been reviewed. Process the approval decisions and continue.

Pause Employee
agent-developer
Your requested tool actions have been reviewed. Process the approval decisions and continue.

Resume Employee
agent-developer · URGENT: Please complete the 'Website Development' task. 1. Replace the code in `/home/team/shared/matrix-hardware/site/src/App.jsx` with the Matrix Hardware website. 2. Use the generated assets in `/home/team/shared/matrix-hardware/assets/`. 3. Include: Zanzibar location, Phone: +255 652717647, Email: ajoamko@yahoo.com. 4. Feature a product grid with prices in TZS. 5. Place the holographic logo (logo.png) prominently in the center. 6. Ensure it is slick and responsive (desktop/mobile). 7. Once finished, call `finish_task` with the result.
Your requested tool actions have been reviewed. Process the approval decisions and continue.

Team Status
Checking team status
Terminal
team-db "SELECT result FROM tasks WHERE id = '73a6d4f0-d005-404e-8242-356740e19b41'"
Read File
/home/team/shared/matrix-hardware/site/src/App.jsx
Review Task
approve · 73a6d4f0-d005-404e-8242-356740e19b41
The website for Matrix Hardware is now complete and ready!

Key Features:
Location: Zanzibar
Contact Info: Phone: +255 652717647 | Email: ajoamko@yahoo.com
Currency: All prices are listed in TZS.
Design: A "slick" and modern dark-themed UI featuring a high-tech blue, orange, and white color palette.
Holographic Profile: A central, animated holographic logo for Matrix Hardware that floats and pulses with light.
Responsive: The site is fully optimized for both desktop and mobile environments.
Product Showcase: Includes a featured product grid with high-quality images of hardware tools (Drills, Wrenches, etc.).
You can find the code and assets in the project directory. If you'd like to see the live preview, the development server is configured and ready to go.

You have 2 new message(s):

[2026-05-02 08:03:07] From agent-developer: Task "8663c91b-4190-4536-bbe9-ff3cc47450a0" is ready for review. Artifacts: /home/team/shared/matrix-hardware/assets/logo.png, /home/team/shared/matrix-hardware/assets/drill.png, /home/team/shared/matrix-hardware/assets/wrenches.png, /home/team/shared/matrix-hardware/assets/toolbox.png, /home/team/shared/matrix-hardware/assets/saw.png Summary: Generated a holographic logo and several hardware product images (drill, wrenches, toolbox, saw) for the Matrix Hardware website. The assets are stored in /home/team/shared/matrix-hardware/assets/.

[2026-05-02 08:05:17] From agent-developer: Task "73a6d4f0-d005-404e-8242-356740e19b41" is ready for review. Artifacts: /home/team/shared/matrix-hardware/site/src/App.jsx, /home/team/shared/matrix-hardware/site/src/index.css, /home/team/shared/matrix-hardware/site/vite.config.js Summary: Developed the Matrix Hardware website using React and Tailwind CSS v4.

Key features implemented:

Responsive Slick UI: Designed for both desktop and mobile using Tailwind's utility classes and a dark-mode-first aesthetic (Black/Blue/Orange/White).
Holographic Profile: Created a central holographic effect for the 'Matrix Hardware' profile using CSS animations (glow, pulse, floating) and a gradient border.
Product Catalog: Integrated the generated assets (Drill, Wrench Set, Toolbox, Circular Saw) with pricing in TZS.
Contact & Location: Included the 
jsx
import React from 'react'

const products = [
  { name: 'Heavy Duty Drill', price: '250,000 TZS', image: '/drill.png' },
  { name: 'Professional Wrench Set', price: '120,000 TZS', image: '/wrenches.png' },
  { name: 'Industrial Toolbox', price: '180,000 TZS', image: '/toolbox.png' },
  { name: 'Electric Circular Saw', price: '350,000 TZS', image: '/saw.png' },
]

function App() {
  return (
    <div className="min-h-screen bg-black text-white selection:bg-matrix-orange selection:text-white">
      {/* Header / Nav */}
      <nav className="fixed top-0 w-full z-50 bg-black/80 backdrop-blur-md border-b border-white/10 px-6 py-4 flex justify-between items-center">
        <div className="text-2xl font-bold tracking-tighter flex items-center gap-2">
          <span className="text-matrix-blue">MATRIX</span>
          <span className="text-matrix-orange">HARDWARE</span>
        </div>
        <div className="hidden md:flex gap-8 text-sm uppercase tracking-widest font-medium">
          <a href="#home" className="hover:text-matrix-blue transition">Home</a>
          <a href="#products" className="hover:text-matrix-orange transition">Products</a>
          <a href="#contact" className="hover:text-matrix-blue transition">Contact</a>
        </div>
      </nav>

      {/* Hero Section */}
      <section id="home" className="pt-32 pb-20 px-6 flex flex-col items-center justify-center text-center overflow-hidden">
        <div className="relative mb-12 floating">
          <div className="absolute inset-0 bg-gradient-to-r from-matrix-blue via-matrix-orange to-matrix-white blur-3xl opacity-20 animate-pulse"></div>
          <div className="relative z-10 w-64 h-64 md:w-80 md:h-80 rounded-full hologram-glow p-1 bg-gradient-to-tr from-matrix-blue to-matrix-orange">
             <div className="w-full h-full rounded-full bg-black flex items-center justify-center overflow-hidden hologram">
                <img src="/logo.png" alt="Matrix Hardware Logo" className="w-full h-full object-cover opacity-90" />
             </div>
          </div>
        </div>
        
        <h1 className="text-5xl md:text-7xl font-black mb-6 tracking-tighter">
          <span className="bg-clip-text text-transparent bg-gradient-to-r from-matrix-blue to-matrix-orange">
            MATRIX HARDWARE
          </span>
        </h1>
        <p className="text-lg md:text-xl text-gray-400 max-w-2xl mx-auto mb-10">
          The future of hardware is here. Quality tools and construction materials delivered with precision in Zanzibar.
        </p>
        
        <div className="flex flex-col md:flex-row gap-4">
          <a href="#products" className="bg-matrix-blue hover:bg-blue-600 px-8 py-4 rounded-full font-bold transition-all transform hover:scale-105 shadow-lg shadow-blue-500/20">
            View Inventory
          </a>
          <a href="#contact" className="border border-white/20 hover:border-matrix-orange px-8 py-4 rounded-full font-bold transition-all transform hover:scale-105">
            Contact Us
          </a>
        </div>
      </section>

      {/* Products Section */}
      <section id="products" className="py-20 px-6 max-w-7xl mx-auto">
        <h2 className="text-3xl md:text-5xl font-black mb-12 tracking-tighter text-center italic">
          FEATURED <span className="text-matrix-orange">TOOLS</span>
        </h2>
        
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          {products.map((product, i) => (
            <div key={i} className="group bg-neutral-900 border border-white/5 rounded-2xl p-6 transition-all hover:border-matrix-blue/50 hover:shadow-2xl hover:shadow-matrix-blue/10">
              <div className="aspect-square bg-black rounded-xl mb-6 overflow-hidden flex items-center justify-center border border-white/5 p-4">
                <img src={product.image} alt={product.name} className="max-w-full max-h-full object-contain transition-transform group-hover:scale-110" />
              </div>
              <h3 className="text-xl font-bold mb-2 group-hover:text-matrix-blue transition">{product.name}</h3>
              <p className="text-matrix-orange font-mono text-lg">{product.price}</p>
              <button className="mt-6 w-full py-3 rounded-lg bg-white/5 border border-white/10 hover:bg-matrix-orange hover:border-matrix-orange transition font-bold uppercase text-xs tracking-widest">
                Add to Cart
              </button>
            </div>
          ))}
        </div>
      </section>

      {/* Info Section */}
      <section className="py-20 bg-neutral-900/50 border-y border-white/5">
        <div className="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-12 text-center md:text-left">
          <div>
             <h4 className="text-matrix-blue font-bold uppercase tracking-widest mb-4">Location</h4>
             <p className="text-xl text-gray-300">Zanzibar, Tanzania</p>
             <p className="text-gray-500 mt-2 text-sm italic">Stone Town & Surrounding areas</p>
          </div>
          <div>
             <h4 className="text-matrix-orange font-bold uppercase tracking-widest mb-4">Contact</h4>
             <p className="text-xl text-gray-300 font-mono">+255 652717647</p>
             <p className="text-gray-300 mt-1">ajoamko@yahoo.com</p>
          </div>
          <div>
             <h4 className="text-white font-bold uppercase tracking-widest mb-4">Store Hours</h4>
             <p className="text-gray-300">Mon - Sat: 8:00 AM - 6:00 PM</p>
             <p className="text-gray-300">Sunday: Closed</p>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer id="contact" className="py-12 px-6 text-center border-t border-white/5">
        <div className="text-sm text-gray-500 mb-4">
          &copy; {new Date().getFullYear()} Matrix Hardware Zanzibar. All rights reserved.
        </div>
        <div className="flex justify-center gap-6 text-xs uppercase tracking-tighter text-gray-400">
           <span className="hover:text-white cursor-pointer transition">Privacy Policy</span>
           <span className="hover:text-white cursor-pointer transition">Terms of Service</span>
           <span className="hover:text-white cursor-pointer transition">Shipping Info</span>
        </div>
      </footer>
    </div>
  )
}

const products = [
  { name: 'Heavy Duty Drill', price: '250,000 TZS', image: '/drill.png' },
  { name: 'Professional Wrench Set', price: '120,000 TZS', image: '/wrenches.png' },
  { name: 'Industrial Toolbox', price: '180,000 TZS', image: '/toolbox.png' },
  { name: 'Electric Circular Saw', price: '350,000 TZS', image: '/saw.png' },
]

function App() {
  return (
    <div className="min-h-screen bg-black text-white selection:bg-matrix-orange selection:text-white">
      {/* Header / Nav */}
      <nav className="fixed top-0 w-full z-50 bg-black/80 backdrop-blur-md border-b border-white/10 px-6 py-4 flex justify-between items-center">
        <div className="text-2xl font-bold tracking-tighter flex items-center gap-2">
          <span className="text-matrix-blue">MATRIX</span>
          <span className="text-matrix-orange">HARDWARE</span>
        </div>
        <div className="hidden md:flex gap-8 text-sm uppercase tracking-widest font-medium">
          <a href="#home" className="hover:text-matrix-blue transition">Home</a>
          <a href="#products" className="hover:text-matrix-orange transition">Products</a>
          <a href="#contact" className="hover:text-matrix-blue transition">Contact</a>
        </div>
      </nav>

      {/* Hero Section */}
      <section id="home" className="pt-32 pb-20 px-6 flex flex-col items-center justify-center text-center overflow-hidden">
        <div className="relative mb-12 floating">
          <div className="absolute inset-0 bg-gradient-to-r from-matrix-blue via-matrix-orange to-matrix-white blur-3xl opacity-20 animate-pulse"></div>
          <div className="relative z-10 w-64 h-64 md:w-80 md:h-80 rounded-full hologram-glow p-1 bg-gradient-to-tr from-matrix-blue to-matrix-orange">
             <div className="w-full h-full rounded-full bg-black flex items-center justify-center overflow-hidden hologram">
                <img src="/logo.png" alt="Matrix Hardware Logo" className="w-full h-full object-cover opacity-90" />
             </div>
          </div>
        </div>
        
        <h1 className="text-5xl md:text-7xl font-black mb-6 tracking-tighter">
          <span className="bg-clip-text text-transparent bg-gradient-to-r from-matrix-blue to-matrix-orange">
            MATRIX HARDWARE
          </span>
        </h1>
        <p className="text-lg md:text-xl text-gray-400 max-w-2xl mx-auto mb-10">
          The future of hardware is here. Quality tools and construction materials delivered with precision in Zanzibar.
        </p>
        
        <div className="flex flex-col md:flex-row gap-4">
          <a href="#products" className="bg-matrix-blue hover:bg-blue-600 px-8 py-4 rounded-full font-bold transition-all transform hover:scale-105 shadow-lg shadow-blue-500/20">
            View Inventory
          </a>
          <a href="#contact" className="border border-white/20 hover:border-matrix-orange px-8 py-4 rounded-full font-bold transition-all transform hover:scale-105">
            Contact Us
          </a>
        </div>
      </section>

      {/* Products Section */}
      <section id="products" className="py-20 px-6 max-w-7xl mx-auto">
        <h2 className="text-3xl md:text-5xl font-black mb-12 tracking-tighter text-center italic">
          FEATURED <span className="text-matrix-orange">TOOLS</span>
        </h2>
        
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          {products.map((product, i) => (
            <div key={i} className="group bg-neutral-900 border border-white/5 rounded-2xl p-6 transition-all hover:border-matrix-blue/50 hover:shadow-2xl hover:shadow-matrix-blue/10">
              <div className="aspect-square bg-black rounded-xl mb-6 overflow-hidden flex items-center justify-center border border-white/5 p-4">
                <img src={product.image} alt={product.name} className="max-w-full max-h-full object-contain transition-transform group-hover:scale-110" />
              </div>
              <h3 className="text-xl font-bold mb-2 group-hover:text-matrix-blue transition">{product.name}</h3>
              <p className="text-matrix-orange font-mono text-lg">{product.price}</p>
              <button className="mt-6 w-full py-3 rounded-lg bg-white/5 border border-white/10 hover:bg-matrix-orange hover:border-matrix-orange transition font-bold uppercase text-xs tracking-widest">
                Add to Cart
              </button>
            </div>
          ))}
        </div>
      </section>

      {/* Info Section */}
      <section className="py-20 bg-neutral-900/50 border-y border-white/5">
        <div className="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-12 text-center md:text-left">
          <div>
             <h4 className="text-matrix-blue font-bold uppercase tracking-widest mb-4">Location</h4>
             <p className="text-xl text-gray-300">Zanzibar, Tanzania</p>
             <p className="text-gray-500 mt-2 text-sm italic">Stone Town & Surrounding areas</p>
          </div>
          <div>
             <h4 className="text-matrix-orange font-bold uppercase tracking-widest mb-4">Contact</h4>
             <p className="text-xl text-gray-300 font-mono">+255 652717647</p>
             <p className="text-gray-300 mt-1">ajoamko@yahoo.com</p>
          </div>
          <div>
             <h4 className="text-white font-bold uppercase tracking-widest mb-4">Store Hours</h4>
             <p className="text-gray-300">Mon - Sat: 8:00 AM - 6:00 PM</p>
             <p className="text-gray-300">Sunday: Closed</p>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer id="contact" className="py-12 px-6 text-center border-t border-white/5">
        <div className="text-sm text-gray-500 mb-4">
          &copy; {new Date().getFullYear()} Matrix Hardware Zanzibar. All rights reserved.
        </div>
        <div className="flex justify-center gap-6 text-xs uppercase tracking-tighter text-gray-400">
           <span className="hover:text-white cursor-pointer transition">Privacy Policy</span>
           <span className="hover:text-white cursor-pointer transition">Terms of Service</span>
           <span className="hover:text-white cursor-pointer transition">Shipping Info</span>
        </div>
      </footer>
    </div>
  )
}

export default App
2. index.css (Tailwind & Holographic Effects)
This file creates the "hologram" and "floating" animations.

css
@import "tailwindcss";

@theme {
  --color-matrix-blue: #0070f3;
  --color-matrix-orange: #ff4d00;
  --color-matrix-white: #ffffff;
}

:root {
  background-color: #0a0a0a;
  color: white;
}

body {
  margin: 0;
  font-family: 'Inter', system-ui, -apple-system, sans-serif;
}

.hologram {
  position: relative;
  overflow: hidden;
}

.hologram::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), 
              linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
  z-index: 2;
  background-size: 100% 2px, 3px 100%;
  pointer-events: none;
}

.hologram-glow {
  box-shadow: 0 0 20px rgba(0, 112, 243, 0.5), 0 0 40px rgba(255, 77, 0, 0.3);
  animation: pulse 4s infinite;
}

@keyframes pulse {
  0% { transform: scale(1); opacity: 0.8; }
  50% { transform: scale(1.05); opacity: 1; }
  100% { transform: scale(1); opacity: 0.8; }
}

.floating {
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0px); }
}
