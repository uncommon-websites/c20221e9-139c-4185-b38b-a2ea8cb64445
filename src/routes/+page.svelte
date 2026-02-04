<script lang="ts">
  // Icons
  import { Play, Mic, FileText, Clock, Search, CheckCircle, Users, ArrowRight, Plus, Shield, Zap, Database, Settings } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "How accurate is Alago's AI transcription for construction terminology?",
    "Can I use Alago for different types of construction meetings?",
    "How does Alago ensure data security and GDPR compliance?",
    "Which languages does Alago support?",
    "Can I integrate Alago with my existing project management tools?",
    "How long does it take to generate a protocol?",
    "Can multiple team members collaborate on the same protocol?",
    "What happens to my audio recordings after transcription?",
    "Can I customize protocol templates for my company?",
    "Does Alago work offline on construction sites?"
  ];

  function toggleFaq(index: number) {
    openFaq = openFaq === index ? -1 : index;
  }


<main class="w-full overflow-hidden">
  <!-- Hero Section - ALREADY CUSTOMIZED, DO NOT MODIFY -->
  <section class="pt-16 md:pt-24 pb-0">
    <div class="max-w-[1600px] mx-auto px-6 md:px-10">
      
      <!-- Hero Text Content -->
      <div class="flex flex-col lg:flex-row lg:justify-between lg:items-end gap-10 mb-20">
        <!-- Left: Headline & CTA -->
        <div class="max-w-3xl">
          <h1 class="text-5xl md:text-[5.5rem] leading-[1.05] font-medium tracking-tight text-black mb-10">
            Turn construction site notes into protocols 50% faster
          </h1>
          <a href="#" class="inline-block bg-black text-white text-lg font-medium px-8 py-3.5 rounded-full hover:bg-gray-800 transition-colors">
            Get your first protocol
          </a>
        </div>

        <!-- Right: Description -->
        <div class="max-w-[500px] lg:mb-6">
          <p class="text-lg md:text-[1.15rem] leading-relaxed text-gray-800">
            Built for construction project managers. Alago transforms site recordings into structured protocols using specialized AI transcription tailored for the German building industry.
          </p>
        </div>
      </div>

    </div>

    <!-- Hero Visual / UI Mockup -->
    <div class="mx-4 md:mx-6 mt-8 rounded-t-[2.5rem] bg-gradient-to-br from-[#9baaf5] via-[#8e9bf0] to-[#9c78a8] pt-12 px-4 md:px-16 pb-0 overflow-hidden relative min-h-[600px]">
      
      <!-- The "Browser Window" / UI Container -->
      <div class="bg-white rounded-t-2xl shadow-2xl w-full h-full min-h-[800px] flex flex-col">
        
        <!-- UI Header -->
        <div class="flex items-center justify-between px-6 py-4 border-b border-gray-100">
          <div class="flex items-center gap-6">
            <span class="font-medium text-gray-900">Alago Protocol Builder</span>
            <div class="flex items-center gap-4 text-gray-400">
              <!-- Undo Icon -->
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 7v6h6"/><path d="M21 17a9 9 0 0 0-9-9 9 9 0 0 0-6 2.3L3 13"/></svg>
              <!-- Redo Icon -->
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 7v6h-6"/><path d="M3 17a9 9 0 0 1 9-9 9 9 0 0 1 6 2.3l3 3.7"/></svg>
            </div>
          </div>
          <div class="flex items-center gap-4">
            <span class="text-sm font-medium text-gray-500 cursor-pointer">Share</span>
            <button class="bg-black text-white text-sm font-medium px-4 py-1.5 rounded-md">Download PDF</button>
          </div>
        </div>

        <!-- UI Body -->
        <div class="flex flex-col md:flex-row flex-1">
          
          <!-- Left Panel: Text Editor -->
          <div class="w-full md:w-1/2 p-8 md:p-12 border-r border-gray-100 relative">
            <!-- Sidebar Icons (simulated) -->
            <div class="absolute right-4 top-12 flex flex-col gap-6 text-gray-400">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="5"/><path d="M12 1v2"/><path d="M12 21v2"/><path d="M4.22 4.22l1.42 1.42"/><path d="M18.36 18.36l1.42 1.42"/><path d="M1 12h2"/><path d="M21 12h2"/><path d="M4.22 19.78l1.42-1.42"/><path d="M18.36 5.64l1.42-1.42"/></svg>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"/></svg>
            </div>

            <div class="flex gap-4 mb-6">
              <!-- Blue Dot Indicator -->
              <div class="mt-1.5">
                <div class="w-4 h-4 rounded-full bg-gradient-to-br from-blue-400 to-[#3b82f6] shadow-sm"></div>
              </div>
              <!-- Active Line -->
              <div class="border-l-2 border-gray-800 pl-4 py-1">
                <p class="font-medium text-gray-900 text-lg">Project: Alago Tower Construction - Site Meeting #14</p>
              </div>
            </div>

            <div class="flex gap-4 mb-6 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Transcription processing. Mapping technical architectural terms and structural requirements from audio.</p>
              </div>
            </div>

            <div class="flex gap-4 mb-6 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Draft protocol ready: 8 safety observations, 5 contractor assignments, and 3 material delivery schedule updates detected.</p>
              </div>
            </div>

            <div class="flex gap-4 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Finalizing protocol for structural approval and distribution to site stakeholders.</p>
              </div>
            </div>
          </div>

          <!-- Right Panel: Image -->
          <div class="w-full md:w-1/2 p-8 flex items-center justify-center bg-gray-50">
            <div class="w-full h-full max-h-[500px] rounded-lg overflow-hidden shadow-lg relative">
              <!-- Construction site image -->
              <img src="/generated/image-modern-construction-site-with-steel-fram-1770243344759-3.webp" alt="Construction Site" class="w-full h-full object-cover" />
              <!-- Overlay gradient -->
              <div class="absolute inset-0 bg-gradient-to-t from-orange-500/40 to-transparent mix-blend-overlay"></div>
            </div>
          </div>
        </div>
      </div>

      <!-- Floating Voice Chat Widget -->
      <div class="absolute bottom-8 right-8 md:bottom-12 md:right-12 bg-white rounded-full p-1.5 pr-4 shadow-[0_8px_30px_rgb(0,0,0,0.12)] flex items-center gap-3 z-20">
        <!-- Orb Icon -->
        <div class="w-10 h-10 rounded-full bg-gradient-to-br from-primary-400 to-primary-600 flex items-center justify-center">
          <Mic class="w-5 h-5 text-white" />
        </div>
        
        <!-- Button -->
        <button class="bg-black text-white text-xs font-bold px-4 py-2 rounded-full tracking-wide">RECORD MEETING</button>
        
        <!-- Language Selector -->
        <div class="flex items-center gap-1 pl-1 cursor-pointer">
          <span class="text-lg">🇩🇪</span>
          <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-gray-500"><path d="m6 9 6 6 6-6"/></svg>
        </div>
      </div>

      <!-- Powered by text -->
      <div class="absolute bottom-4 right-1/2 translate-x-1/2 text-[10px] text-gray-500 opacity-50">
        Powered by Construction AI
      </div>

    </div>
  </section>

  <!-- Intro Section -->
  <section class="max-w-[1000px] mx-auto px-6 py-24 text-center">
    <span class="text-sm font-medium text-gray-500 mb-4 block">#AufKIGebaut 🌊</span>
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 leading-tight">
      End protocol chaos with AI-powered construction documentation. From site meeting to structured protocol in minutes, not hours.
    </h2>
    
    <div class="flex flex-wrap justify-center gap-x-6 gap-y-3 text-sm text-gray-600 mb-10">
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Mic size={14} /> AI Transcription</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><FileText size={14} /> Protocol Designer</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Search size={14} /> Smart Search</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Clock size={14} /> Project Logbook</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Users size={14} /> Real-time Collaboration</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Shield size={14} /> GDPR Compliant</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Database size={14} /> Integrations</span>
    </div>

    <button class="inline-flex items-center gap-2 bg-black text-white pl-3 pr-5 py-2 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
      <div class="w-6 h-6 bg-white rounded-full flex items-center justify-center">
        <Play size={10} class="fill-black text-black ml-0.5" />
      </div>
      Watch demo
    </button>
  </section>

  <!-- Features List Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-12 relative">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-24">
        
        <!-- Feature 1 -->
        <div class="flex flex-col justify-center order-1 md:order-1">
            <h3 class="text-3xl font-medium mb-4">AI transcription built for construction</h3>
            <p class="text-gray-600 leading-relaxed mb-6">
                Record site meetings and let our specialized AI transcribe technical terminology, contractor names, and building codes with precision. Trained specifically for German construction language.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 order-2 md:order-2 min-h-[400px]">
            <div class="text-xs text-gray-400 mb-4 font-medium uppercase tracking-wide">Construction Terms Detected</div>
            <div class="space-y-3">
                {#each [
                    {term: "Stahlbetondecke", type: "Structural Element", confidence: "98%"},
                    {term: "DIN 18065", type: "Building Code", confidence: "99%"},
                    {term: "Wärmedämmverbundsystem", type: "Technical Term", confidence: "97%"},
                    {term: "Baustellenverordnung", type: "Safety Regulation", confidence: "96%"},
                    {term: "Estricharbeiten", type: "Trade Work", confidence: "98%"},
                    {term: "KfW-55 Standard", type: "Energy Standard", confidence: "99%"},
                ] as item}
                <div class="flex items-center gap-3 p-3 bg-white rounded-lg border border-gray-100">
                    <div class="w-2 h-2 rounded-full bg-primary-500"></div>
                    <div class="flex-1">
                        <div class="text-sm font-medium text-gray-900">{item.term}</div>
                        <div class="text-xs text-gray-500">{item.type}</div>
                    </div>
                    <div class="text-xs font-medium text-primary-600">{item.confidence}</div>
                </div>
                {/each}
            </div>
        </div>

        <!-- Feature 2 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[400px] flex items-center justify-center order-4 md:order-3 relative overflow-hidden">
             <div class="w-full max-w-md bg-white rounded-xl shadow-lg p-6 border border-gray-100">
                 <div class="flex items-center justify-between mb-4">
                     <h4 class="font-medium text-gray-900">Protocol Template</h4>
                     <Settings size={16} class="text-gray-400" />
                 </div>
                 <div class="space-y-3">
                     <div class="flex items-center gap-2">
                         <CheckCircle size={16} class="text-primary-500" />
                         <span class="text-sm text-gray-600">Meeting details</span>
                     </div>
                     <div class="flex items-center gap-2">
                         <CheckCircle size={16} class="text-primary-500" />
                         <span class="text-sm text-gray-600">Participants</span>
                     </div>
                     <div class="flex items-center gap-2">
                         <CheckCircle size={16} class="text-primary-500" />
                         <span class="text-sm text-gray-600">Agenda items</span>
                     </div>
                     <div class="flex items-center gap-2">
                         <CheckCircle size={16} class="text-primary-500" />
                         <span class="text-sm text-gray-600">Decisions & tasks</span>
                     </div>
                     <div class="flex items-center gap-2">
                         <CheckCircle size={16} class="text-primary-500" />
                         <span class="text-sm text-gray-600">Safety observations</span>
                     </div>
                     <div class="flex items-center gap-2">
                         <CheckCircle size={16} class="text-primary-500" />
                         <span class="text-sm text-gray-600">Material updates</span>
                     </div>
                 </div>
             </div>
        </div>
        <div class="flex flex-col justify-center order-3 md:order-4">
            <h3 class="text-3xl font-medium mb-4">Structured protocols in your format</h3>
            <p class="text-gray-600 leading-relaxed">
                Automatically organize meeting notes into professional protocols following your company's templates. Every section properly formatted, every detail captured.
            </p>
        </div>

        <!-- Feature 3 -->
        <div class="flex flex-col justify-center order-5 md:order-5">
            <h3 class="text-3xl font-medium mb-4">Smart project logbook with timeline</h3>
            <p class="text-gray-600 leading-relaxed">
                Track all decisions, changes, and trade activities in a chronological logbook. Never lose track of who said what, when, and why during your construction project.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-6 md:order-6">
             <div class="w-full max-w-xs bg-white rounded-xl shadow-sm p-4 border border-gray-100">
                 <div class="space-y-4">
                     <div class="flex gap-3">
                         <div class="flex flex-col items-center">
                             <div class="w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center text-primary-600 text-xs font-bold">14</div>
                             <div class="w-0.5 h-8 bg-gray-200"></div>
                         </div>
                         <div class="flex-1 pt-1">
                             <div class="text-xs text-gray-500">Today</div>
                             <div class="text-sm font-medium">Safety inspection</div>
                         </div>
                     </div>
                     <div class="flex gap-3">
                         <div class="flex flex-col items-center">
                             <div class="w-8 h-8 rounded-full bg-gray-100 flex items-center justify-center text-gray-600 text-xs font-bold">13</div>
                             <div class="w-0.5 h-8 bg-gray-200"></div>
                         </div>
                         <div class="flex-1 pt-1">
                             <div class="text-xs text-gray-500">Yesterday</div>
                             <div class="text-sm font-medium">Material delivery</div>
                         </div>
                     </div>
                     <div class="flex gap-3">
                         <div class="flex flex-col items-center">
                             <div class="w-8 h-8 rounded-full bg-gray-100 flex items-center justify-center text-gray-600 text-xs font-bold">12</div>
                         </div>
                         <div class="flex-1 pt-1">
                             <div class="text-xs text-gray-500">3 days ago</div>
                             <div class="text-sm font-medium">Design change</div>
                         </div>
                     </div>
                 </div>
             </div>
        </div>

        <!-- Feature 4 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-8 md:order-7">
            <div class="relative w-full max-w-md bg-white rounded-xl shadow-sm p-6 border border-gray-100">
                <div class="flex items-center gap-2 mb-4">
                    <Search size={20} class="text-primary-500" />
                    <input type="text" placeholder="Search all protocols..." class="flex-1 outline-none text-sm" value="Estrich delay" />
                </div>
                <div class="space-y-2">
                    <div class="p-2 bg-primary-50 rounded border border-primary-100">
                        <div class="text-xs text-primary-600 font-medium">Meeting #12 - 08.01.2025</div>
                        <div class="text-sm text-gray-700 mt-1">...discussed <span class="bg-primary-200 px-1">Estrich delay</span> due to weather...</div>
                    </div>
                    <div class="p-2 bg-gray-50 rounded border border-gray-100">
                        <div class="text-xs text-gray-500 font-medium">Meeting #09 - 18.12.2024</div>
                        <div class="text-sm text-gray-600 mt-1">...original <span class="bg-primary-200 px-1">Estrich</span> schedule confirmed...</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex flex-col justify-center order-7 md:order-8">
            <h3 class="text-3xl font-medium mb-4">AI-powered search across all protocols</h3>
            <p class="text-gray-600 leading-relaxed">
                Find any decision, task, or discussion instantly. Our AI chatbot understands construction context and retrieves exactly what you need from thousands of pages.
            </p>
        </div>

        <!-- Feature 5 -->
        <div class="flex flex-col justify-center order-9 md:order-9">
            <h3 class="text-3xl font-medium mb-4">Real-time collaboration for your team</h3>
            <p class="text-gray-600 leading-relaxed">
                Multiple team members can edit protocols simultaneously. Share access with subcontractors and partners with one click. Everyone stays on the same page.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-10 md:order-10">
             <div class="w-full max-w-sm bg-white rounded-xl shadow-sm p-4 border border-gray-100">
                 <div class="flex items-center justify-between mb-4">
                     <span class="text-sm font-medium">Active collaborators</span>
                     <span class="text-xs text-gray-500">3 online</span>
                 </div>
                 <div class="space-y-2">
                     <div class="flex items-center gap-3 p-2 bg-primary-50 rounded-lg">
                         <div class="w-8 h-8 rounded-full bg-primary-500 flex items-center justify-center text-white text-xs font-bold">MK</div>
                         <div class="flex-1">
                             <div class="text-sm font-medium">Martin Klein</div>
                             <div class="text-xs text-gray-500">Editing section 3</div>
                         </div>
                         <div class="w-2 h-2 rounded-full bg-green-500"></div>
                     </div>
                     <div class="flex items-center gap-3 p-2 rounded-lg">
                         <div class="w-8 h-8 rounded-full bg-gray-300 flex items-center justify-center text-white text-xs font-bold">SB</div>
                         <div class="flex-1">
                             <div class="text-sm font-medium">Sarah Bauer</div>
                             <div class="text-xs text-gray-500">Viewing</div>
                         </div>
                         <div class="w-2 h-2 rounded-full bg-green-500"></div>
                     </div>
                     <div class="flex items-center gap-3 p-2 rounded-lg">
                         <div class="w-8 h-8 rounded-full bg-gray-300 flex items-center justify-center text-white text-xs font-bold">TM</div>
                         <div class="flex-1">
                             <div class="text-sm font-medium">Thomas Müller</div>
                             <div class="text-xs text-gray-500">Adding comments</div>
                         </div>
                         <div class="w-2 h-2 rounded-full bg-green-500"></div>
                     </div>
                 </div>
             </div>
        </div>
    </div>
  </section>
  
  <!-- Floating Action Bar (Stickyish) -->
  <div class="sticky bottom-6 z-40 flex justify-center pointer-events-none">
      <div class="bg-white/80 backdrop-blur-md border border-gray-200 shadow-lg rounded-full py-3 px-6 flex items-center gap-6 pointer-events-auto">
          <span class="text-sm font-medium text-gray-900 hidden sm:block">50% faster construction documentation with AI</span>
          <button class="bg-black text-white text-xs font-bold px-4 py-2 rounded-full hover:bg-gray-800 transition-colors">
              Start free trial
          </button>
      </div>
  </div>

  <!-- Complete Platform Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Everything you need for construction documentation</h2>
        <p class="text-gray-600">From meeting recording to protocol distribution, Alago provides a complete platform for managing construction project documentation efficiently.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <!-- Card 1: Integrations (Wide) -->
        <div class="md:col-span-2 bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10 max-w-md">
                <h3 class="text-xl font-medium mb-2">Seamless integrations</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Connect with PlanRadar, Capmo, and other construction management tools. Sync protocols with your existing CDE systems automatically.</p>
            </div>
            <div class="absolute right-8 bottom-8 flex flex-wrap gap-4 max-w-xs">
                 <div class="w-16 h-16 bg-white rounded-xl shadow-md border border-gray-100 flex items-center justify-center">
                     <Database size={24} class="text-gray-400" />
                 </div>
                 <div class="w-16 h-16 bg-white rounded-xl shadow-md border border-gray-100 flex items-center justify-center">
                     <Settings size={24} class="text-gray-400" />
                 </div>
                 <div class="w-16 h-16 bg-white rounded-xl shadow-md border border-gray-100 flex items-center justify-center">
                     <FileText size={24} class="text-gray-400" />
                 </div>
                 <div class="w-16 h-16 bg-white rounded-xl shadow-md border border-gray-100 flex items-center justify-center">
                     <Zap size={24} class="text-primary-500" />
                 </div>
            </div>
        </div>

        <!-- Card 2: Security -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
             <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Enterprise security</h3>
                <p class="text-sm text-gray-600 leading-relaxed">AES-256 encryption, GDPR compliant, hosted in Germany. Your construction data stays secure and private.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6">
                <div class="bg-white rounded-xl p-4 shadow-md border border-gray-100">
                    <Shield size={32} class="text-primary-500 mb-2" />
                    <div class="text-xs text-gray-500 space-y-1">
                        <div class="flex items-center gap-2">
                            <CheckCircle size={12} class="text-green-500" />
                            <span>GDPR Compliant</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <CheckCircle size={12} class="text-green-500" />
                            <span>AES-256 Encryption</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <CheckCircle size={12} class="text-green-500" />
                            <span>German Hosting</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Card 3: Automated Reports -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Automated alerts</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Get notified about delays, cost overruns, and safety concerns automatically detected in meeting content.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 space-y-2">
                <div class="bg-red-50 border border-red-200 text-red-700 p-2 rounded-lg text-xs">
                    ⚠️ Delay detected: Estrich
                </div>
                <div class="bg-orange-50 border border-orange-200 text-orange-700 p-2 rounded-lg text-xs">
                    💰 Budget concern mentioned
                </div>
                <div class="bg-yellow-50 border border-yellow-200 text-yellow-700 p-2 rounded-lg text-xs">
                    🔧 Material shortage flagged
                </div>
            </div>
        </div>

        <!-- Card 4: External Sharing -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">One-click sharing</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Share protocols with subcontractors and external partners instantly. Control access levels and track who viewed what.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 bg-white rounded-xl border border-gray-100 p-3 shadow-md">
                <div class="flex items-center gap-3">
                    <Users size={20} class="text-primary-500" />
                    <div class="flex-1">
                        <div class="text-xs font-medium">Shared with 5 partners</div>
                        <div class="text-[10px] text-gray-500">Last viewed 2 hours ago</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Card 5: Mobile App -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Mobile ready</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Record meetings directly from your phone on the construction site. Access protocols offline when needed.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 flex justify-center">
                <div class="w-32 h-48 bg-white rounded-2xl shadow-lg border-4 border-gray-800 p-2">
                    <div class="w-full h-full bg-gradient-to-br from-primary-100 to-primary-200 rounded-lg flex items-center justify-center">
                        <Mic size={32} class="text-primary-600" />
                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>

  <!-- Built for Construction Professionals -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Built for construction professionals</h2>
        <p class="text-gray-600">From project managers to site supervisors and general contractors, Alago adapts to your workflow — saving hours on documentation while ensuring nothing gets missed.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Professional 1 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-construction-project-manager-reviewing-b-1770243337555-0.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Project Manager" />
                <div class="absolute inset-0 bg-gradient-to-t from-primary-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-primary-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Project Managers</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Spend less time writing protocols and more time managing projects. Track all decisions, changes, and commitments automatically across multiple construction sites.</p>
        </div>

        <!-- Professional 2 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-construction-site-supervisor-with-tablet-1770243340184-1.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Site Supervisor" />
                <div class="absolute inset-0 bg-gradient-to-t from-orange-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-orange-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Site Supervisors</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Capture safety observations, material issues, and trade coordination on-site. Generate professional protocols instantly without leaving the construction site.</p>
        </div>

        <!-- Professional 3 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="/generated/image-general-contractor-in-business-attire-re-1770243342741-2.webp" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="General Contractor" />
                <div class="absolute inset-0 bg-gradient-to-t from-gray-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-gray-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">General Contractors</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Maintain clear documentation across all subcontractors. Search through years of protocols instantly to resolve disputes and track project history.</p>
        </div>
    </div>
  </section>

  <!-- Social Proof / Stats Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Trusted by construction teams across Germany</h2>
        <p class="text-gray-600">Join hundreds of construction professionals who have already eliminated protocol chaos and saved thousands of hours.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
        <div class="text-center p-8 bg-gray-50 rounded-2xl border border-gray-100">
            <div class="text-4xl font-bold text-primary-600 mb-2">50%</div>
            <div class="text-sm text-gray-600">Faster protocol creation</div>
        </div>
        <div class="text-center p-8 bg-gray-50 rounded-2xl border border-gray-100">
            <div class="text-4xl font-bold text-primary-600 mb-2">10K+</div>
            <div class="text-sm text-gray-600">Target projects by 2027</div>
        </div>
        <div class="text-center p-8 bg-gray-50 rounded-2xl border border-gray-100">
            <div class="text-4xl font-bold text-primary-600 mb-2">€50B</div>
            <div class="text-sm text-gray-600">Construction documentation market</div>
        </div>
    </div>

    <div class="max-w-4xl mx-auto">
        <div class="bg-gradient-to-br from-primary-50 to-primary-100 rounded-2xl p-8 md:p-12 border border-primary-200">
            <div class="flex flex-col md:flex-row gap-8 items-center">
                <div class="flex-1">
                    <div class="text-2xl font-medium text-gray-900 mb-4">
                        "Alago has transformed how we document our construction meetings. What used to take 2-3 hours now takes 30 minutes."
                    </div>
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-full bg-primary-500 flex items-center justify-center text-white font-bold">
                            PM
                        </div>
                        <div>
                            <div class="font-medium text-gray-900">Project Manager</div>
                            <div class="text-sm text-gray-600">Mid-sized Construction Firm</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>

  <!-- FAQ Section -->
  <section class="max-w-[1000px] mx-auto px-6 py-24">
      <h2 class="text-3xl font-medium mb-12">Frequently asked questions</h2>
      
      <div class="divide-y divide-gray-100">
          {#each faqs as question, i}
            <div class="py-4">
                <button class="w-full flex items-center justify-between text-left group" on:click={() => toggleFaq(i)}>
                    <span class="text-sm md:text-base text-gray-700 group-hover:text-black transition-colors">{question}</span>
                    <span class="text-gray-400">
                        <Plus size={16} class="transition-transform duration-200 {openFaq === i ? 'rotate-45' : ''}" />
                    </span>
                </button>
                {#if openFaq === i}
                    <div class="mt-4 text-sm text-gray-500 leading-relaxed pb-2">
                        {#if i === 0}
                            Alago's AI is specifically trained on German construction terminology, building codes (like DIN standards), and industry-specific language. Our models achieve over 95% accuracy on technical terms that generic transcription services often miss.
                        {:else if i === 1}
                            Yes! Alago works for all types of construction meetings: site coordination meetings, safety briefings, client meetings, subcontractor coordination, and planning discussions. The AI adapts to different meeting formats automatically.
                        {:else if i === 2}
                            We take data security seriously. All data is encrypted with AES-256 at rest and TLS 1.3 in transit. We're fully GDPR compliant, host all data in Germany, and use AI models that never retrain on your data. Row-level access control ensures only authorized team members see specific protocols.
                        {:else if i === 3}
                            Currently, Alago is optimized for German construction language. We're planning to expand to other languages based on customer demand. Contact us if you're interested in other language support.
                        {:else if i === 4}
                            Yes! Alago integrates with popular construction management tools like PlanRadar, Capmo, and standard CDE (Common Data Environment) systems. We can sync protocols automatically with your existing workflow.
                        {:else if i === 5}
                            Most protocols are ready within 5-10 minutes after your meeting ends. The AI transcription happens in real-time, and the structuring takes just a few minutes depending on meeting length.
                        {:else if i === 6}
                            Absolutely! Alago is built on a real-time database that enables simultaneous editing. Multiple team members can work on the same protocol at once, and changes sync instantly for everyone.
                        {:else if i === 7}
                            Audio recordings are stored securely and encrypted. You control retention policies - you can delete recordings immediately after transcription or keep them for your records. We never use your audio to train AI models.
                        {:else if i === 8}
                            Yes! You can create custom protocol templates that match your company's format and requirements. All protocols will automatically follow your template structure.
                        {:else if i === 9}
                            The mobile app can record meetings offline, but you'll need an internet connection to process the transcription and generate the protocol. We're working on enhanced offline capabilities for future releases.
                        {/if}
                    </div>
                {/if}
            </div>
          {/each}
      </div>
  </section>

  <!-- Bottom CTA -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 flex flex-col items-center text-center border-t border-gray-100">
      <div class="mb-4">
          <span class="text-4xl">🌊</span>
      </div>
      <h2 class="text-4xl font-medium tracking-tight mb-4">Ready to end protocol chaos?</h2>
      <p class="text-gray-600 mb-8 max-w-2xl">Join construction teams across Germany who are saving hours every week with AI-powered documentation.</p>
      <div class="flex flex-col sm:flex-row items-center gap-4">
          <button class="bg-black text-white px-8 py-3 rounded-full font-medium hover:bg-gray-800 transition-colors text-sm">
              Start free trial
          </button>
          <button class="bg-white text-black border border-gray-200 px-8 py-3 rounded-full font-medium hover:bg-gray-50 transition-colors text-sm">
              Book a demo
          </button>
      </div>
      <p class="text-xs text-gray-400 mt-6">No credit card required • 14-day free trial • Cancel anytime</p>
  </section>
</main>

<style>
    /* Custom scrollbar hide for clean look in some areas if needed */
    .no-scrollbar::-webkit-scrollbar {
        display: none;
    }
    .no-scrollbar {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
</style>

