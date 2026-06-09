<!DOCTYPE html>
<html lang="tr" class="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Özgür Nefes | Premium Sigara Bırakma Takipçisi</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Outfit:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: {
                            50: '#f0fdf4',
                            100: '#dcfce7',
                            200: '#bbf7d0',
                            500: '#10b981',
                            600: '#059669',
                            700: '#047857',
                        },
                        dark: {
                            900: '#0b0f19',
                            800: '#111827',
                            700: '#1f2937',
                            600: '#374151',
                            500: '#4b5563',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'ui-sans-serif', 'system-ui'],
                        display: ['Outfit', 'sans-serif']
                    }
                }
            }
        }
    </script>
    
    <style>
        :root {
            --font-primary: 'Inter', sans-serif;
            --font-display: 'Outfit', sans-serif;
        }

        body {
            font-family: var(--font-primary);
            overflow-x: hidden;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        h1, h2, h3, h4, .font-display {
            font-family: var(--font-display);
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.4);
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.04);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .dark .glass-card {
            background: rgba(17, 24, 39, 0.8);
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.2);
        }

        .glass-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 40px 0 rgba(31, 38, 135, 0.07);
        }

        .dark .glass-card:hover {
            box-shadow: 0 12px 40px 0 rgba(0, 0, 0, 0.3);
        }

        .blob {
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            z-index: 0;
            pointer-events: none;
            opacity: 0.35;
            animation: blob-float 12s infinite alternate ease-in-out;
        }

        .dark .blob {
            opacity: 0.15;
        }

        @keyframes blob-float {
            0% { transform: translate(0px, 0px) scale(1); }
            50% { transform: translate(30px, -50px) scale(1.1); }
            100% { transform: translate(-20px, 20px) scale(0.9); }
        }

        .tab-content {
            animation: fadeIn 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .circle-progress-bg {
            fill: none;
            stroke: #e2e8f0;
        }

        .dark .circle-progress-bg {
            stroke: #374151;
        }

        .circle-progress-bar {
            fill: none;
            stroke-linecap: round;
            transition: stroke-dashoffset 0.8s ease-in-out;
        }

        .bottom-nav-item {
            position: relative;
        }

        .bottom-nav-item.active {
            color: #10b981;
        }

        .bottom-nav-item::after {
            content: '';
            position: absolute;
            bottom: -6px;
            left: 50%;
            transform: translateX(-50%) scaleX(0);
            width: 16px;
            height: 3px;
            background-color: #10b981;
            border-radius: 2px;
            transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .bottom-nav-item.active::after {
            transform: translateX(-50%) scaleX(1);
        }

        @keyframes pulse-ring {
            0% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(16, 185, 129, 0.5); }
            70% { transform: scale(1); box-shadow: 0 0 0 10px rgba(16, 185, 129, 0); }
            100% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(16, 185, 129, 0); }
        }

        .pulse-btn {
            animation: pulse-ring 2s infinite;
        }

        ::-webkit-scrollbar { width: 8px; height: 8px; }
        ::-webkit-scrollbar-track { background: transparent; }
        ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 9999px; border: 2px solid transparent; background-clip: padding-box; }
        .dark ::-webkit-scrollbar-thumb { background: #4b5563; border: 2px solid transparent; background-clip: padding-box; }
        ::-webkit-scrollbar-thumb:hover { background-color: #94a3b8; }
        .dark ::-webkit-scrollbar-thumb:hover { background-color: #6b7280; }

        input:focus, select:focus { box-shadow: 0 0 0 3px rgba(16, 185, 129, 0.15); }
        .dark input[type="datetime-local"]::-webkit-calendar-picker-indicator { filter: invert(1); }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-dark-900 dark:text-slate-100 min-h-screen flex flex-col relative">
    
    <div class="blob bg-primary-200 dark:bg-primary-700/20 w-72 h-72 top-10 left-10"></div>
    <div class="blob bg-teal-200 dark:bg-teal-700/20 w-80 h-80 bottom-20 right-10"></div>

    <header class="bg-white/80 dark:bg-dark-800/80 backdrop-blur-md border-b border-slate-100 dark:border-dark-700 p-4 sticky top-0 z-40 transition-colors">
        <div class="max-w-4xl mx-auto flex items-center justify-between">
            <div class="flex items-center space-x-2.5">
                <div class="p-2 bg-primary-100 dark:bg-primary-950 text-primary-600 dark:text-primary-455 rounded-xl">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                </div>
                <div>
                    <h1 class="text-xl font-extrabold font-display bg-gradient-to-r from-primary-600 to-teal-500 bg-clip-text text-transparent">Özgür Nefes</h1>
                    <p class="text-[10px] text-slate-400 dark:text-slate-550 tracking-wider uppercase font-semibold">Sigarasız Yaşam Sayacı</p>
                </div>
            </div>
            
            <nav class="hidden md:flex items-center space-x-1">
                <button data-tab="dashboard" class="bottom-nav-item active px-4 py-2 rounded-xl text-sm font-medium hover:bg-slate-100 dark:hover:bg-dark-700 transition-colors">Gösterge Paneli</button>
                <button data-tab="health" class="bottom-nav-item px-4 py-2 rounded-xl text-sm font-medium hover:bg-slate-100 dark:hover:bg-dark-700 transition-colors">Sağlık</button>
                <button data-tab="achievements" class="bottom-nav-item px-4 py-2 rounded-xl text-sm font-medium hover:bg-slate-100 dark:hover:bg-dark-700 transition-colors">Başarılar</button>
                <button data-tab="settings" class="bottom-nav-item px-4 py-2 rounded-xl text-sm font-medium hover:bg-slate-100 dark:hover:bg-dark-700 transition-colors">Ayarlar</button>
            </nav>
        </div>
    </header>

    <main class="flex-grow flex items-center justify-center p-4 sm:p-6 w-full max-w-4xl mx-auto z-10">
        
        <!-- SETUP EKRANI -->
        <div id="setup-screen" class="w-full max-w-md glass-card rounded-3xl p-6 sm:p-8 transition-all duration-300">
            <div class="text-center mb-6">
                <h2 class="text-2xl font-extrabold text-slate-800 dark:text-slate-100 mb-2">Yeni Bir Başlangıç</h2>
                <p class="text-slate-500 dark:text-slate-400 text-sm">Sigarayı bıraktığınız anı girerek özgürlüğünüze ve sağlığınıza adım atın.</p>
            </div>
            
            <form id="setup-form" class="space-y-5">
                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-1.5">Bırakma Tarihi ve Saati</label>
                    <input type="datetime-local" id="input-date" required
                        class="w-full p-3.5 border border-slate-200 dark:border-dark-600 rounded-2xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-200 outline-none transition-all">
                </div>
                
                <div class="grid grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-1.5">Günlük Sigara (Adet)</label>
                        <input type="number" id="input-cigs" min="1" max="150" placeholder="Örn: 20" required
                            class="w-full p-3.5 border border-slate-200 dark:border-dark-600 rounded-2xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-200 outline-none transition-all">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-1.5">Paket Fiyatı (₺)</label>
                        <input type="number" id="input-price" min="1" step="0.5" placeholder="Örn: 120" required
                            class="w-full p-3.5 border border-slate-200 dark:border-dark-600 rounded-2xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-200 outline-none transition-all">
                    </div>
                </div>
                
                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-1.5">Bir Paketteki Sigara Sayısı</label>
                    <input type="number" id="input-pack-size" min="1" max="100" value="20" required
                        class="w-full p-3.5 border border-slate-200 dark:border-dark-600 rounded-2xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-200 outline-none transition-all">
                    <p class="text-[10px] text-slate-450 dark:text-slate-500 mt-1">*Standart paketlerde genellikle 20 adet bulunur.</p>
                </div>

                <button type="submit" 
                    class="w-full bg-gradient-to-r from-primary-500 to-teal-500 hover:from-primary-600 hover:to-teal-600 text-white font-bold py-4 px-4 rounded-2xl transition-all duration-200 transform active:scale-95 shadow-lg shadow-primary-500/20 flex justify-center items-center space-x-2">
                    <span class="font-display">Yolculuğa Başla</span>
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                </button>
            </form>
        </div>

        <!-- APP EKRANI -->
        <div id="app-screen" class="hidden w-full space-y-6 sm:space-y-8">
            
            <!-- GÖSTERGE PANELİ -->
            <div id="dashboard-section" class="tab-section space-y-6 sm:space-y-8 tab-content">
                
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                    <div class="lg:col-span-2 glass-card rounded-3xl p-6 sm:p-8 shadow-md relative overflow-hidden bg-gradient-to-br from-primary-500 to-teal-600 text-white border-none flex flex-col justify-between">
                        <div class="absolute -top-10 -right-10 opacity-10">
                            <svg class="w-48 h-48" fill="currentColor" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
                        </div>
                        
                        <div class="relative z-10 mb-6">
                            <span class="text-xs font-bold uppercase tracking-widest text-primary-100 bg-primary-600/30 px-3 py-1 rounded-full">Yolculuk Devam Ediyor</span>
                            <h3 class="text-primary-50 font-display font-medium mt-4 text-base uppercase tracking-wider">Sigarasız Geçen Süre</h3>
                        </div>

                        <div class="grid grid-cols-4 gap-2 sm:gap-4 max-w-xl relative z-10">
                            <div class="bg-white/10 backdrop-blur-sm rounded-2xl p-3 text-center border border-white/5">
                                <div id="val-days" class="text-3xl sm:text-5xl font-extrabold font-display tracking-tight">0</div>
                                <div class="text-[10px] sm:text-xs text-primary-100 mt-1 uppercase font-semibold">Gün</div>
                            </div>
                            <div class="bg-white/10 backdrop-blur-sm rounded-2xl p-3 text-center border border-white/5">
                                <div id="val-hours" class="text-3xl sm:text-5xl font-extrabold font-display tracking-tight">00</div>
                                <div class="text-[10px] sm:text-xs text-primary-100 mt-1 uppercase font-semibold">Saat</div>
                            </div>
                            <div class="bg-white/10 backdrop-blur-sm rounded-2xl p-3 text-center border border-white/5">
                                <div id="val-mins" class="text-3xl sm:text-5xl font-extrabold font-display tracking-tight">00</div>
                                <div class="text-[10px] sm:text-xs text-primary-100 mt-1 uppercase font-semibold">Dakika</div>
                            </div>
                            <div class="bg-white/10 backdrop-blur-sm rounded-2xl p-3 text-center border border-white/5">
                                <div id="val-secs" class="text-3xl sm:text-5xl font-extrabold font-display tracking-tight">00</div>
                                <div class="text-[10px] sm:text-xs text-primary-100 mt-1 uppercase font-semibold">Saniye</div>
                            </div>
                        </div>
                    </div>

                    <div class="glass-card rounded-3xl p-6 shadow-md flex flex-col items-center justify-center text-center">
                        <div class="relative flex items-center justify-center mb-3">
                            <svg class="w-32 h-32 transform -rotate-90">
                                <circle class="circle-progress-bg" cx="60" cy="60" r="54" stroke-width="8"></circle>
                                <circle id="circle-progress" class="circle-progress-bar text-primary-500" cx="60" cy="60" r="54" stroke-width="8" stroke-dasharray="339.29" stroke-dashoffset="339.29" stroke="currentColor"></circle>
                            </svg>
                            <div class="absolute flex flex-col items-center">
                                <span id="circle-percentage" class="text-2xl font-extrabold text-slate-800 dark:text-slate-100 font-display">%0</span>
                                <span class="text-[10px] uppercase font-bold text-slate-400">İyileşme</span>
                            </div>
                        </div>
                        <h4 class="font-bold text-slate-800 dark:text-slate-100 font-display">Ortalama Sağlık Skoru</h4>
                        <p class="text-xs text-slate-500 dark:text-slate-400 mt-1 max-w-[200px]">İlk 9 kritik aşamanın iyileşme yüzdesi.</p>
                    </div>
                </div>

                <div class="glass-card rounded-3xl p-6 shadow-md flex flex-col sm:flex-row items-center justify-between gap-4">
                    <div class="text-center sm:text-left">
                        <h4 class="font-extrabold text-slate-850 dark:text-slate-100 text-lg font-display">Canınız Sigara mı İstiyor?</h4>
                        <p class="text-sm text-slate-500 dark:text-slate-400 mt-1">İradenize sarılın, krizler geçicidir. Aşağıdaki butona basarak bu krizi yendiğinizi kaydedin!</p>
                    </div>
                    <button id="btn-craving" class="pulse-btn bg-primary-500 hover:bg-primary-600 text-white font-bold px-6 py-4 rounded-2xl flex items-center space-x-2 transition-all shadow-lg shadow-primary-500/25 active:scale-95 shrink-0">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                        <span>Krizi Savuşturdum!</span>
                    </button>
                </div>

                <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                    <div class="glass-card rounded-2xl p-5 shadow-sm border border-slate-100/50 flex flex-col justify-between">
                        <div class="flex items-center justify-between mb-3">
                            <span class="text-xs font-semibold text-slate-400 uppercase">Tasarruf Edilen</span>
                            <div class="bg-emerald-100 dark:bg-emerald-950/50 p-2 rounded-xl text-emerald-600 dark:text-emerald-450">
                                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                            </div>
                        </div>
                        <div>
                            <div class="text-xl sm:text-2xl font-extrabold text-slate-800 dark:text-slate-100 font-display"><span id="val-money">0.00</span> ₺</div>
                            <p class="text-[10px] text-slate-400 mt-1">Cebinizde kalan para</p>
                        </div>
                    </div>

                    <div class="glass-card rounded-2xl p-5 shadow-sm border border-slate-100/50 flex flex-col justify-between">
                        <div class="flex items-center justify-between mb-3">
                            <span class="text-xs font-semibold text-slate-400 uppercase">İçilmeyen Sigara</span>
                            <div class="bg-blue-100 dark:bg-blue-950/50 p-2 rounded-xl text-blue-600 dark:text-blue-400">
                                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 18.364A9 9 0 005.636 5.636m12.728 12.728A9 9 0 015.636 5.636m12.728 12.728L5.636 5.636"></path></svg>
                            </div>
                        </div>
                        <div>
                            <div class="text-xl sm:text-2xl font-extrabold text-slate-800 dark:text-slate-100 font-display" id="val-cigs">0.00</div>
                            <p class="text-[10px] text-slate-400 mt-1">Vücuda sokulmayan adet</p>
                        </div>
                    </div>

                    <div class="glass-card rounded-2xl p-5 shadow-sm border border-slate-100/50 flex flex-col justify-between">
                        <div class="flex items-center justify-between mb-3">
                            <span class="text-xs font-semibold text-slate-400 uppercase">Yenilen Aşermeler</span>
                            <div class="bg-violet-100 dark:bg-violet-950/50 p-2 rounded-xl text-violet-600 dark:text-violet-400">
                                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                            </div>
                        </div>
                        <div>
                            <div class="text-xl sm:text-2xl font-extrabold text-slate-800 dark:text-slate-100 font-display" id="val-cravings-count">0</div>
                            <p class="text-[10px] text-slate-400 mt-1">İrade savaşı galibiyeti</p>
                        </div>
                    </div>

                    <div class="glass-card rounded-2xl p-5 shadow-sm border border-slate-100/50 flex flex-col justify-between">
                        <div class="flex items-center justify-between mb-3">
                            <span class="text-xs font-semibold text-slate-400 uppercase">Yaşam Kazanımı</span>
                            <div class="bg-rose-100 dark:bg-rose-950/50 p-2 rounded-xl text-rose-600 dark:text-rose-450">
                                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path></svg>
                            </div>
                        </div>
                        <div>
                            <div class="text-sm sm:text-base font-extrabold text-slate-800 dark:text-slate-100 font-display leading-tight" id="val-life-saved">0 Dakika</div>
                            <p class="text-[10px] text-slate-400 mt-1">Kazanılan tahmini süre</p>
                        </div>
                    </div>
                </div>

                <div class="glass-card rounded-3xl p-6 shadow-sm border border-slate-150/40 relative overflow-hidden">
                    <div class="flex items-start justify-between">
                        <div class="space-y-2 max-w-[85%]">
                            <span class="text-[10px] font-bold uppercase tracking-wider text-slate-400">Günün Motivasyonu</span>
                            <p id="quote-text" class="text-base font-medium text-slate-700 dark:text-slate-200 italic leading-relaxed transition-opacity duration-300">"Küçük adımlar zamanla büyük dağlar aşar."</p>
                            <p id="quote-author" class="text-xs text-slate-500 dark:text-slate-400 transition-opacity duration-300">- Anonim</p>
                        </div>
                        <button id="btn-refresh-quote" class="p-2 rounded-xl bg-slate-100 hover:bg-slate-200 dark:bg-dark-750 dark:hover:bg-dark-700 text-slate-500 dark:text-slate-400 transition-colors shrink-0">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 1121.21 8.89M9 11l3 3L22 4"></path></svg>
                        </button>
                    </div>
                </div>
            </div>

            <!-- SAĞLIK -->
            <div id="health-section" class="tab-section hidden space-y-6 tab-content">
                <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4">
                    <div>
                        <h3 class="text-2xl font-extrabold text-slate-850 dark:text-slate-100 font-display">Sağlık İyileşmeleri</h3>
                        <p class="text-sm text-slate-500 dark:text-slate-400 mt-0.5">Vücudunuzun sigarayı bıraktığınız andan itibaren geçirdiği biyolojik değişimler.</p>
                    </div>
                    
                    <div class="flex flex-wrap gap-1.5 bg-slate-100/60 dark:bg-dark-800/60 p-1 rounded-2xl border border-slate-200/40 dark:border-dark-700 shrink-0 self-start sm:self-center">
                        <button data-filter="all" class="milestone-filter-btn px-3 py-1.5 text-xs font-semibold rounded-xl bg-primary-500 text-white dark:bg-primary-600 transition-all">Hepsi</button>
                        <button data-filter="Kısa Vade" class="milestone-filter-btn px-3 py-1.5 text-xs font-semibold rounded-xl bg-slate-100 text-slate-600 dark:bg-dark-700 dark:text-slate-300 hover:bg-slate-200 transition-all">Kısa Vade</button>
                        <button data-filter="Orta Vade" class="milestone-filter-btn px-3 py-1.5 text-xs font-semibold rounded-xl bg-slate-100 text-slate-600 dark:bg-dark-700 dark:text-slate-300 hover:bg-slate-200 transition-all">Orta Vade</button>
                        <button data-filter="Uzun Vade" class="milestone-filter-btn px-3 py-1.5 text-xs font-semibold rounded-xl bg-slate-100 text-slate-600 dark:bg-dark-700 dark:text-slate-300 hover:bg-slate-200 transition-all">Uzun Vade</button>
                    </div>
                </div>

                <div id="health-container" class="grid grid-cols-1 md:grid-cols-2 gap-4"></div>
            </div>

            <!-- BAŞARILAR -->
            <div id="achievements-section" class="tab-section hidden space-y-6 tab-content">
                <div class="glass-card rounded-3xl p-6 shadow-sm border border-slate-150/40">
                    <h3 class="text-xl font-extrabold text-slate-800 dark:text-slate-100 font-display">Başarılar ve Rozetler</h3>
                    <p class="text-sm text-slate-500 dark:text-slate-400 mt-1 mb-4">Mücadelenizi taçlandırın. Rozetlerinizi kilitlerini açarak sergileyin.</p>
                    
                    <div class="relative pt-1">
                        <div class="flex mb-2 items-center justify-between">
                            <span id="achievements-progress-text" class="text-xs font-bold text-slate-600 dark:text-slate-350 uppercase">0 / 0 Rozet Açıldı</span>
                        </div>
                        <div class="overflow-hidden h-2 flex rounded-full bg-slate-100 dark:bg-dark-700">
                            <div id="achievements-progress-bar" style="width:0%" class="shadow-none flex flex-col text-center whitespace-nowrap text-white justify-center bg-gradient-to-r from-primary-500 to-teal-500 transition-all duration-500"></div>
                        </div>
                    </div>
                </div>

                <div id="achievements-container" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4"></div>
            </div>

            <!-- AYARLAR -->
            <div id="settings-section" class="tab-section hidden space-y-6 tab-content">
                <div>
                    <h3 class="text-2xl font-extrabold text-slate-850 dark:text-slate-100 font-display">Ayarlar</h3>
                    <p class="text-sm text-slate-500 dark:text-slate-400 mt-0.5">Bırakma tarihi ve sigara alışkanlık verilerinizi güncelleyin veya uygulamanızı sıfırlayın.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="md:col-span-2 glass-card rounded-3xl p-6 shadow-sm space-y-5">
                        <h4 class="font-bold text-slate-800 dark:text-slate-100 font-display">Verileri Düzenle</h4>
                        
                        <form id="edit-form" class="space-y-4">
                            <div>
                                <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-1.5">Bırakma Tarihi ve Saati</label>
                                <input type="datetime-local" id="edit-date" required
                                    class="w-full p-3 border border-slate-200 dark:border-dark-600 rounded-xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-250 outline-none transition-all">
                            </div>
                            
                            <div class="grid grid-cols-2 gap-4">
                                <div>
                                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-1.5">Günde İçilen (Adet)</label>
                                    <input type="number" id="edit-cigs" min="1" max="150" required
                                        class="w-full p-3 border border-slate-200 dark:border-dark-600 rounded-xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-250 outline-none transition-all">
                                </div>
                                <div>
                                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-1.5">Paket Fiyatı (₺)</label>
                                    <input type="number" id="edit-price" min="1" step="0.5" required
                                        class="w-full p-3 border border-slate-200 dark:border-dark-600 rounded-xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-250 outline-none transition-all">
                                </div>
                            </div>
                            
                            <div>
                                <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-1.5">Paket İçi Sigara Adedi</label>
                                <input type="number" id="edit-pack-size" min="1" max="100" required
                                    class="w-full p-3 border border-slate-200 dark:border-dark-600 rounded-xl bg-white dark:bg-dark-800 text-slate-700 dark:text-slate-250 outline-none transition-all">
                            </div>

                            <button type="submit" 
                                class="w-full bg-primary-500 hover:bg-primary-600 text-white font-bold py-3.5 px-4 rounded-xl transition-all shadow-md active:scale-98 flex justify-center items-center space-x-2">
                                <span>Değişiklikleri Kaydet</span>
                            </button>
                        </form>
                    </div>

                    <div class="space-y-6">
                        <div class="glass-card rounded-3xl p-6 shadow-sm space-y-4">
                            <h4 class="font-bold text-slate-800 dark:text-slate-100 font-display">Görünüm Teması</h4>
                            <div class="flex flex-col gap-2">
                                <button id="theme-light" class="w-full flex items-center justify-between p-3 rounded-xl bg-slate-100 dark:bg-dark-700 text-slate-750 dark:text-slate-350 text-sm font-semibold transition-colors">
                                    <span class="flex items-center space-x-2">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 9H3m15.364-6.364l-.707.707M6.343 17.657l-.707.707m2.828 0l-.707-.707m12.02-12.02l-.707-.707M12 8a4 4 0 100 8 4 4 0 000-8z"></path></svg>
                                        <span>Açık Tema</span>
                                    </span>
                                </button>
                                <button id="theme-dark" class="w-full flex items-center justify-between p-3 rounded-xl bg-slate-100 dark:bg-dark-700 text-slate-750 dark:text-slate-350 text-sm font-semibold transition-colors">
                                    <span class="flex items-center space-x-2">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"></path></svg>
                                        <span>Karanlık Tema</span>
                                    </span>
                                </button>
                                <button id="theme-system" class="w-full flex items-center justify-between p-3 rounded-xl bg-slate-100 dark:bg-dark-700 text-slate-750 dark:text-slate-350 text-sm font-semibold transition-colors">
                                    <span class="flex items-center space-x-2">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                                        <span>Sistem Varsayılanı</span>
                                    </span>
                                </button>
                            </div>
                        </div>

                        <div class="glass-card rounded-3xl p-6 shadow-sm border border-red-150/40 dark:border-red-950/20 space-y-4">
                            <h4 class="font-bold text-red-500 font-display">Tehlikeli Bölge</h4>
                            <p class="text-[11px] text-slate-400">Verileri sıfırlayarak uygulamayı baştan kurabilirsiniz.</p>
                            <button id="btn-reset" class="w-full bg-red-100 hover:bg-red-200 dark:bg-red-950/40 dark:hover:bg-red-950 text-red-600 dark:text-red-400 font-bold py-3 px-4 rounded-xl text-sm transition-colors active:scale-98">
                                Tüm Verileri Sıfırla
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <footer class="text-center py-6 text-slate-400 dark:text-slate-550 text-xs mt-auto z-10 transition-colors">
        <p>Sağlıklı bir gelecek için kararlılıkla attığınız adıma tebrikler. ✨</p>
    </footer>

    <!-- Mobil Navigasyon -->
    <div class="md:hidden fixed bottom-0 left-0 right-0 bg-white/85 dark:bg-dark-800/85 backdrop-blur-lg border-t border-slate-100 dark:border-dark-700 py-3 px-6 z-40 transition-colors flex items-center justify-between">
        <button data-tab="dashboard" class="bottom-nav-item active flex flex-col items-center justify-center text-slate-500 dark:text-slate-400 space-y-1">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6a2 2 0 012-2h2a2 2 0 012 2v4a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v4a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v4a2 2 0 01-2 2H6a2 2 0 01-2-2v-4zM14 16a2 2 0 012-2h2a2 2 0 012 2v4a2 2 0 01-2 2h-2a2 2 0 01-2-2v-4z"></path></svg>
            <span class="text-[10px] font-medium">Gösterge</span>
        </button>
        <button data-tab="health" class="bottom-nav-item flex flex-col items-center justify-center text-slate-500 dark:text-slate-400 space-y-1">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[10px] font-medium">Sağlık</span>
        </button>
        <button data-tab="achievements" class="bottom-nav-item flex flex-col items-center justify-center text-slate-500 dark:text-slate-400 space-y-1">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v13m0-13V6a2 2 0 112 2h-2zm0 0V5a2 2 0 10-2 2h2zm0 0h4l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4h4z"></path></svg>
            <span class="text-[10px] font-medium">Başarılar</span>
        </button>
        <button data-tab="settings" class="bottom-nav-item flex flex-col items-center justify-center text-slate-500 dark:text-slate-400 space-y-1">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
            <span class="text-[10px] font-medium">Ayarlar</span>
        </button>
    </div>

    <script>
        // --- VERİ TANIMLAMALARI ---
        const milestones = [
            { id: 1, label: "Kalp Atış Hızı", detail: "Kan basıncı ve nabız hızı normale döner. El ve ayaklar ısınmaya başlar.", seconds: 20 * 60, icon: "pulse", category: "Kısa Vade" },
            { id: 2, label: "Oksijen Seviyesi", detail: "Kandaki karbonmonoksit seviyesi yarıya iner. Oksijen seviyesi normale döner.", seconds: 8 * 3600, icon: "wind", category: "Kısa Vade" },
            { id: 3, label: "Karbonmonoksit Temizliği", detail: "Vücuttaki tüm karbonmonoksit temizlenir. Akciğerler mukus ve döküntüleri dışarı atmaya başlar.", seconds: 24 * 3600, icon: "trash", category: "Kısa Vade" },
            { id: 4, label: "Duyuların Canlanması", detail: "Nikotin vücuttan tamamen atılır. Tat ve koku alma duyularınız belirgin şekilde keskinleşir.", seconds: 48 * 3600, icon: "sparkles", category: "Kısa Vade" },
            { id: 5, label: "Rahat Nefes", detail: "Bronşiyoller gevşer ve nefes alıp vermek kolaylaşır. Akciğer kapasitesi artmaya başlar.", seconds: 72 * 3600, icon: "cloud-upload", category: "Kısa Vade" },
            { id: 6, label: "Kritik Eşik", detail: "Fiziksel yoksunluk semptomlarının en zorlu dönemi başarıyla geride kalmıştır.", seconds: 7 * 24 * 3600, icon: "check-circle", category: "Orta Vade" },
            { id: 7, label: "Dolaşım İyileşmesi", detail: "Vücuttaki kan dolaşımı önemli ölçüde düzelir. Yürüme ve koşma gibi fiziksel aktiviteler kolaylaşır.", seconds: 14 * 24 * 3600, icon: "trending-up", category: "Orta Vade" },
            { id: 8, label: "Öksürük Azalması", detail: "Akciğerlerdeki siller (tüysü yapılar) temizlenir. Tıkanıklık, hırıltı ve nefes darlığı azalır.", seconds: 30 * 24 * 3600, icon: "activity", category: "Orta Vade" },
            { id: 9, label: "Akciğer Yenilenmesi", detail: "Akciğer fonksiyonlarında %30'a varan artış görülür. Enfeksiyonlara karşı koruma artar.", seconds: 90 * 24 * 3600, icon: "shield", category: "Orta Vade" },
            { id: 10, label: "Kalp Krizi Riski", detail: "Koroner kalp hastalığı ve kalp krizi geçirme riskiniz aktif bir içiciye göre yarı yarıya azalır.", seconds: 365 * 24 * 3600, icon: "heart", category: "Uzun Vade" },
            { id: 11, label: "Felç Riski", detail: "Felç (inme) geçirme riskiniz, hiç sigara içmemiş bir insanınkiyle aynı seviyeye geriler.", seconds: 5 * 365 * 24 * 3600, icon: "zap", category: "Uzun Vade" },
            { id: 12, label: "Kanser Koruma", detail: "Akciğer kanserinden ölüm riski yarıya iner. Ağız, gırtlak, yemek borusu ve böbrek kanseri riski azalır.", seconds: 10 * 365 * 24 * 3600, icon: "shield-alert", category: "Uzun Vade" },
            { id: 13, label: "Tam İyileşme", detail: "Kalp ve damar hastalıkları riskiniz, hiç sigara içmemiş birinin seviyesine kadar düşer.", seconds: 15 * 365 * 24 * 3600, icon: "award", category: "Uzun Vade" }
        ];

        const achievements = [
            { id: "time-1h", title: "İlk Kıvılcım", description: "Sigarasız geçen ilk 1 saat.", condition: (time, money, cravings) => time >= 3600, icon: "🔥", category: "time" },
            { id: "time-12h", title: "Yarım Gün Zaferi", description: "12 saattir zehirden uzaksınız.", condition: (time, money, cravings) => time >= 12 * 3600, icon: "☀️", category: "time" },
            { id: "time-24h", title: "Tam Bir Gün", description: "İlk 24 saati başarıyla devirdiniz.", condition: (time, money, cravings) => time >= 24 * 3600, icon: "⭐", category: "time" },
            { id: "time-3d", title: "Demir İrade", description: "En kritik ilk 3 günü (72 saat) atlattınız.", condition: (time, money, cravings) => time >= 3 * 24 * 3600, icon: "🛡️", category: "time" },
            { id: "time-1w", title: "İlk Hafta", description: "1 hafta boyunca sigaraya meydan okudunuz.", condition: (time, money, cravings) => time >= 7 * 24 * 3600, icon: "👑", category: "time" },
            { id: "time-1m", title: "Bir Aylık Mucize", description: "Dile kolay, tam 1 aydır tertemizsiniz.", condition: (time, money, cravings) => time >= 30 * 24 * 3600, icon: "🚀", category: "time" },
            { id: "time-6m", title: "Yarım Yıl Devrimi", description: "6 aydır kendinize sağlıklı bir hayat sunuyorsunuz.", condition: (time, money, cravings) => time >= 182 * 24 * 3600, icon: "🌈", category: "time" },
            { id: "time-1y", title: "Dumansız Yıl", description: "Tam 1 yıldır kendinizin kahramanısınız.", condition: (time, money, cravings) => time >= 365 * 24 * 3600, icon: "🏆", category: "time" },
            { id: "money-100", title: "Kumbarada İlk Para", description: "Sigaraya vermeyip kurtardığınız 100 ₺.", condition: (time, money, cravings) => money >= 100, icon: "🪙", category: "money" },
            { id: "money-500", title: "Akıllı Yatırım", description: "Tasarruf edilen toplam tutar 500 ₺'ye ulaştı.", condition: (time, money, cravings) => money >= 500, icon: "💵", category: "money" },
            { id: "money-2000", title: "Harcakazan", description: "Kurtarılan 2,000 ₺ ile kendinize bir hediye alın.", condition: (time, money, cravings) => money >= 2000, icon: "🛒", category: "money" },
            { id: "money-10000", title: "Büyük Tasarrufçu", description: "Cebinizde kalan tam 10,000 ₺!", condition: (time, money, cravings) => money >= 10000, icon: "💰", category: "money" },
            { id: "cravings-1", title: "İlk Dalga Aşıldı", description: "İlk aşermeyi başarıyla geçiştirdiniz.", condition: (time, money, cravings) => cravings >= 1, icon: "🧠", category: "craving" },
            { id: "cravings-10", title: "Kriz Savar", description: "10 aşerme atağını sakin kalarak yendiniz.", condition: (time, money, cravings) => cravings >= 10, icon: "🥋", category: "craving" },
            { id: "cravings-50", title: "Zihinsel Özgürlük", description: "50 kez canınız sigara istediğinde 'Hayır' dediniz.", condition: (time, money, cravings) => cravings >= 50, icon: "🕊️", category: "craving" }
        ];

        const quotes = [
            { quote: "Geleceğiniz, bugün ne yaptığınıza bağlıdır.", author: "Mahatma Gandhi" },
            { quote: "Zorluklar, iradenizi test eden ve sizi güçlendiren fırsatlardır.", author: "Anonim" },
            { quote: "Sigarayı bırakmak hayatınızı geri almaktır, daha azı değil.", author: "Özgür Nefes" },
            { quote: "Her içmediğin sigara, ciğerlerine ve sevdiklerine verilmiş sessiz bir 'Seni Seviyorum' mesajıdır.", author: "Anonim" },
            { quote: "Küçük adımlar zamanla büyük dağlar aşar. Kararlılığını koru.", author: "Anonim" },
            { quote: "Temiz hava en büyük şifadır. Akciğerlerine özgürlük hediye et.", author: "Anonim" },
            { quote: "Bağımlılığın zincirleri, önce hissedilmeyecek kadar hafif, sonra kırılamayacak kadar ağır olur.", author: "Warren Buffett" },
            { quote: "Sadece bugün içmemeyi seçerek başla. Günler birbirini kovalayacaktır.", author: "Anonim" },
            { quote: "Vücudun senin tek evindir. Oraya iyi bakmak zorundasın.", author: "Jim Rohn" },
            { quote: "Bırakmak zor gelebilir ama dumansız bir hayatın getirdiği hafiflik paha biçilemez.", author: "Anonim" },
            { quote: "Bugün gösterdiğin irade, yarınki sağlığının teminatıdır.", author: "Anonim" },
            { quote: "Sigara dumanıyla uçup giden sadece paran değil, gelecekteki mutlu günlerindir.", author: "Anonim" }
        ];

        // --- UYGULAMA DURUMU ---
        let appState = {
            quitDate: null,
            cigsPerDay: 0,
            pricePerPack: 0,
            packSize: 20,
            cravingsBeaten: 0,
            theme: 'light',
            unlockedAchievements: []
        };

        let timerInterval = null;
        let currentQuoteIndex = -1;

        const docHtml = document.documentElement;
        const setupScreen = document.getElementById('setup-screen');
        const appScreen = document.getElementById('app-screen');
        const setupForm = document.getElementById('setup-form');
        const resetBtn = document.getElementById('btn-reset');
        const cravingsBtn = document.getElementById('btn-craving');
        const editForm = document.getElementById('edit-form');
        const quoteText = document.getElementById('quote-text');
        const quoteAuthor = document.getElementById('quote-author');
        const quoteRefreshBtn = document.getElementById('btn-refresh-quote');

        const navItems = document.querySelectorAll('.bottom-nav-item');
        const tabSections = document.querySelectorAll('.tab-section');

        const themeLightBtn = document.getElementById('theme-light');
        const themeDarkBtn = document.getElementById('theme-dark');
        const themeSystemBtn = document.getElementById('theme-system');

        // --- TARİH PARSER (iOS Safari uyumlu) ---
        function parseDateSafely(dateStr) {
            if (!dateStr) return null;

            // ISO string (Z ile biten)
            if (typeof dateStr === 'string' && dateStr.endsWith('Z')) {
                const d = new Date(dateStr);
                return isNaN(d.getTime()) ? null : d;
            }

            // datetime-local formatı: YYYY-MM-DDTHH:MM veya YYYY-MM-DDTHH:MM:SS
            const match = String(dateStr).match(/^(\d{4})-(\d{2})-(\d{2})T(\d{2}):(\d{2})(?::(\d{2}))?/);
            if (match) {
                const d = new Date(
                    parseInt(match[1], 10),
                    parseInt(match[2], 10) - 1,
                    parseInt(match[3], 10),
                    parseInt(match[4], 10),
                    parseInt(match[5], 10),
                    match[6] ? parseInt(match[6], 10) : 0
                );
                return isNaN(d.getTime()) ? null : d;
            }

            const fallback = new Date(dateStr);
            return isNaN(fallback.getTime()) ? null : fallback;
        }

        // --- BAŞLANGIÇ ---
        document.addEventListener('DOMContentLoaded', () => {
            loadState();
            applyTheme(appState.theme);
            setupEventListeners();

            if (appState.quitDate && !isNaN(appState.quitDate.getTime())) {
                showAppScreen();
                startTracking();
            } else {
                showSetupScreen();
            }
        });

        function loadState() {
            try {
                const saved = localStorage.getItem('ozgur_nefes_state');
                if (!saved) return;
                const parsed = JSON.parse(saved);
                appState.quitDate = parsed.quitDate ? parseDateSafely(parsed.quitDate) : null;
                appState.cigsPerDay = parseFloat(parsed.cigsPerDay) || 0;
                appState.pricePerPack = parseFloat(parsed.pricePerPack) || 0;
                appState.packSize = parseFloat(parsed.packSize) || 20;
                appState.cravingsBeaten = parseInt(parsed.cravingsBeaten) || 0;
                appState.theme = parsed.theme || 'light';
                appState.unlockedAchievements = Array.isArray(parsed.unlockedAchievements) ? parsed.unlockedAchievements : [];
            } catch (e) {
                console.error('State yüklenemedi:', e);
            }
        }

        function saveState() {
            localStorage.setItem('ozgur_nefes_state', JSON.stringify({
                ...appState,
                quitDate: appState.quitDate ? appState.quitDate.toISOString() : null
            }));
        }

        // --- EKRAN GEÇİŞLERİ ---
        function showSetupScreen() {
            setupScreen.classList.remove('hidden');
            appScreen.classList.add('hidden');
            initSetupForm();
        }

        function showAppScreen() {
            setupScreen.classList.add('hidden');
            appScreen.classList.remove('hidden');
            fillEditForm();
            switchTab('dashboard');
        }

        function initSetupForm() {
            const now = new Date();
            const pad = n => String(n).padStart(2, '0');
            const dateInput = document.getElementById('input-date');
            if (dateInput) {
                dateInput.value = `${now.getFullYear()}-${pad(now.getMonth()+1)}-${pad(now.getDate())}T${pad(now.getHours())}:${pad(now.getMinutes())}`;
            }
        }

        function fillEditForm() {
            if (!appState.quitDate || isNaN(appState.quitDate.getTime())) return;
            const d = appState.quitDate;
            const pad = n => String(n).padStart(2, '0');
            const editDateInput = document.getElementById('edit-date');
            if (editDateInput) editDateInput.value = `${d.getFullYear()}-${pad(d.getMonth()+1)}-${pad(d.getDate())}T${pad(d.getHours())}:${pad(d.getMinutes())}`;
            const editCigs = document.getElementById('edit-cigs');
            const editPrice = document.getElementById('edit-price');
            const editPack = document.getElementById('edit-pack-size');
            if (editCigs) editCigs.value = appState.cigsPerDay;
            if (editPrice) editPrice.value = appState.pricePerPack;
            if (editPack) editPack.value = appState.packSize;
        }

        // --- SEKME GEÇİŞİ ---
        function switchTab(tabId) {
            // Nav aktif durumu
            navItems.forEach(item => {
                item.getAttribute('data-tab') === tabId
                    ? item.classList.add('active')
                    : item.classList.remove('active');
            });

            // Seksiyon görünürlüğü
            tabSections.forEach(section => {
                if (section.id === `${tabId}-section`) {
                    section.classList.remove('hidden');
                    // Animasyonu yeniden tetikle
                    section.classList.remove('tab-content');
                    void section.offsetWidth;
                    section.classList.add('tab-content');
                } else {
                    section.classList.add('hidden');
                }
            });

            if (tabId === 'dashboard') {
                displayRandomQuote();
                updateDashboard();
            } else if (tabId === 'health') {
                renderMilestones('all');
            } else if (tabId === 'achievements') {
                renderAchievements();
            }
        }

        // --- EVENT LISTENERS ---
        function setupEventListeners() {
            // Setup formu
            if (setupForm) {
                setupForm.addEventListener('submit', e => {
                    e.preventDefault();
                    const dateVal = document.getElementById('input-date').value;
                    const cigsVal = parseFloat(document.getElementById('input-cigs').value);
                    const priceVal = parseFloat(document.getElementById('input-price').value);
                    const packSizeVal = parseFloat(document.getElementById('input-pack-size').value) || 20;

                    const selectedDate = parseDateSafely(dateVal);
                    if (!selectedDate || isNaN(selectedDate.getTime())) {
                        alert("Geçersiz tarih! Lütfen tekrar girin.");
                        return;
                    }
                    if (selectedDate.getTime() > Date.now()) {
                        alert("Bırakma tarihi gelecekte olamaz!");
                        return;
                    }

                    appState.quitDate = selectedDate;
                    appState.cigsPerDay = cigsVal;
                    appState.pricePerPack = priceVal;
                    appState.packSize = packSizeVal;
                    appState.cravingsBeaten = 0;
                    appState.unlockedAchievements = [];
                    saveState();
                    showAppScreen();
                    startTracking();
                });
            }

            // Edit formu
            if (editForm) {
                editForm.addEventListener('submit', e => {
                    e.preventDefault();
                    const dateVal = document.getElementById('edit-date').value;
                    const cigsVal = parseFloat(document.getElementById('edit-cigs').value);
                    const priceVal = parseFloat(document.getElementById('edit-price').value);
                    const packSizeVal = parseFloat(document.getElementById('edit-pack-size').value) || 20;

                    const selectedDate = parseDateSafely(dateVal);
                    if (!selectedDate || isNaN(selectedDate.getTime())) {
                        alert("Geçersiz tarih!");
                        return;
                    }
                    if (selectedDate.getTime() > Date.now()) {
                        alert("Bırakma tarihi gelecekte olamaz!");
                        return;
                    }

                    appState.quitDate = selectedDate;
                    appState.cigsPerDay = cigsVal;
                    appState.pricePerPack = priceVal;
                    appState.packSize = packSizeVal;
                    saveState();
                    fillEditForm();
                    startTracking();
                    showNotification("Bilgileriniz başarıyla güncellendi.");
                });
            }

            // Sıfırla
            if (resetBtn) {
                resetBtn.addEventListener('click', () => {
                    if (confirm("Tüm bilgilerinizi ve istatistiklerinizi sıfırlamak istediğinizden emin misiniz? Bu işlem geri alınamaz.")) {
                        if (timerInterval) clearInterval(timerInterval);
                        timerInterval = null;
                        localStorage.removeItem('ozgur_nefes_state');
                        appState = { quitDate: null, cigsPerDay: 0, pricePerPack: 0, packSize: 20, cravingsBeaten: 0, theme: 'light', unlockedAchievements: [] };
                        showSetupScreen();
                    }
                });
            }

            // Aşerme butonu
            if (cravingsBtn) {
                cravingsBtn.addEventListener('click', () => {
                    appState.cravingsBeaten++;
                    saveState();
                    updateDashboard();
                    checkAchievements();
                    showNotification("Tebrikler! Bir kriz daha iradeyle aşıldı. 🌟");
                });
            }

            // Navigasyon
            navItems.forEach(item => {
                item.addEventListener('click', e => {
                    e.preventDefault();
                    const tab = item.getAttribute('data-tab');
                    if (appScreen.classList.contains('hidden')) return;
                    switchTab(tab);
                });
            });

            // Tema
            if (themeLightBtn) themeLightBtn.addEventListener('click', () => setTheme('light'));
            if (themeDarkBtn) themeDarkBtn.addEventListener('click', () => setTheme('dark'));
            if (themeSystemBtn) themeSystemBtn.addEventListener('click', () => setTheme('system'));

            // Alıntı yenile
            if (quoteRefreshBtn) quoteRefreshBtn.addEventListener('click', displayRandomQuote);

            // Sağlık filtreleri
            document.querySelectorAll('.milestone-filter-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    document.querySelectorAll('.milestone-filter-btn').forEach(b => {
                        b.classList.remove('bg-primary-500', 'text-white', 'dark:bg-primary-600');
                        b.classList.add('bg-slate-100', 'text-slate-600', 'dark:bg-dark-700', 'dark:text-slate-300');
                    });
                    btn.classList.add('bg-primary-500', 'text-white', 'dark:bg-primary-600');
                    btn.classList.remove('bg-slate-100', 'text-slate-600', 'dark:bg-dark-700', 'dark:text-slate-300');
                    renderMilestones(btn.getAttribute('data-filter'));
                });
            });
        }

        // --- TAKİP BAŞLAT ---
        function startTracking() {
            if (!appState.quitDate || isNaN(appState.quitDate.getTime())) {
                console.error('Geçersiz quitDate, takip başlatılamadı.');
                return;
            }
            if (timerInterval) clearInterval(timerInterval);
            updateDashboard();
            timerInterval = setInterval(updateDashboard, 1000);
        }

        // --- GÖSTERGE PANELİ GÜNCELLE ---
        function updateDashboard() {
            if (!appState.quitDate || isNaN(appState.quitDate.getTime())) return;

            const secondsElapsed = Math.max(0, Math.floor((Date.now() - appState.quitDate.getTime()) / 1000));

            const days    = Math.floor(secondsElapsed / 86400);
            const hours   = Math.floor((secondsElapsed % 86400) / 3600);
            const minutes = Math.floor((secondsElapsed % 3600) / 60);
            const seconds = secondsElapsed % 60;

            setElText('val-days', days);
            setElText('val-hours', String(hours).padStart(2, '0'));
            setElText('val-mins', String(minutes).padStart(2, '0'));
            setElText('val-secs', String(seconds).padStart(2, '0'));

            const cigsPerSecond = appState.cigsPerDay / 86400;
            const cigsAvoided   = cigsPerSecond * secondsElapsed;
            const pricePerCig   = appState.pricePerPack / appState.packSize;
            const moneySaved    = cigsAvoided * pricePerCig;
            const minsGained    = cigsAvoided * 11;

            setElText('val-cigs', cigsAvoided.toFixed(2));
            setElText('val-money', moneySaved.toFixed(2));
            setElText('val-cravings-count', appState.cravingsBeaten);

            let lifeText = '';
            if (minsGained < 60) {
                lifeText = `${Math.floor(minsGained)} Dakika`;
            } else if (minsGained < 1440) {
                lifeText = `${Math.floor(minsGained / 60)} Saat, ${Math.floor(minsGained % 60)} Dakika`;
            } else {
                lifeText = `${Math.floor(minsGained / 1440)} Gün, ${Math.floor((minsGained % 1440) / 60)} Saat`;
            }
            setElText('val-life-saved', lifeText);

            updateCircularHealthScore(secondsElapsed);
            checkAchievements(secondsElapsed, moneySaved);
        }

        function setElText(id, val) {
            const el = document.getElementById(id);
            if (el) el.textContent = val;
        }

        // --- DAİRESEL SAĞLIK SKORU ---
        function updateCircularHealthScore(secondsElapsed) {
            const circle = document.getElementById('circle-progress');
            const label  = document.getElementById('circle-percentage');
            if (!circle || !label) return;

            const targetMilestones = milestones.slice(0, 9);
            let total = 0;
            targetMilestones.forEach(m => {
                total += Math.min(100, (secondsElapsed / m.seconds) * 100);
            });
            const avg = total / targetMilestones.length;
            const circumference = 339.29;
            circle.style.strokeDashoffset = circumference - (avg / 100) * circumference;
            label.textContent = `%${Math.floor(avg)}`;
        }

        // --- SAĞLIK MİLESTONE'LARI ---
        function renderMilestones(categoryFilter = 'all') {
            const container = document.getElementById('health-container');
            if (!container) return;
            container.innerHTML = '';

            if (!appState.quitDate || isNaN(appState.quitDate.getTime())) return;
            const secondsElapsed = Math.floor((Date.now() - appState.quitDate.getTime()) / 1000);
            const filtered = milestones.filter(m => categoryFilter === 'all' || m.category === categoryFilter);

            filtered.forEach(m => {
                const rawPct = (secondsElapsed / m.seconds) * 100;
                const isDone = rawPct >= 100;
                const pct    = isDone ? 100 : rawPct;

                let timeRemainingText = '';
                if (!isDone) {
                    const rem = m.seconds - secondsElapsed;
                    if (rem > 86400) timeRemainingText = `Kalan: ${Math.ceil(rem / 86400)} gün`;
                    else if (rem > 3600) timeRemainingText = `Kalan: ${Math.ceil(rem / 3600)} saat`;
                    else timeRemainingText = `Kalan: ${Math.ceil(rem / 60)} dakika`;
                }

                const iconSvg = m.icon === 'heart'
                    ? '<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path></svg>'
                    : (m.icon === 'wind' || m.icon === 'cloud-upload')
                    ? '<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z"></path></svg>'
                    : '<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>';

                const card = document.createElement('div');
                card.className = `glass-card rounded-2xl p-5 border relative overflow-hidden transition-all duration-300 ${isDone ? 'border-primary-100 dark:border-primary-900 bg-gradient-to-br from-white to-primary-50/20 dark:from-dark-800 dark:to-primary-950/10' : ''}`;
                card.innerHTML = `
                    <div class="flex items-start space-x-4">
                        <div class="p-3 rounded-xl shrink-0 ${isDone ? 'bg-primary-100 text-primary-600 dark:bg-primary-950 dark:text-primary-400' : 'bg-slate-100 text-slate-500 dark:bg-dark-700 dark:text-slate-400'}">
                            ${iconSvg}
                        </div>
                        <div class="flex-1 min-w-0">
                            <div class="flex justify-between items-center mb-1 gap-2">
                                <h4 class="font-bold text-slate-800 dark:text-slate-100 text-base truncate">${m.label}</h4>
                                <span class="text-xs font-semibold px-2 py-0.5 rounded-full shrink-0 ${isDone ? 'bg-primary-100 text-primary-700 dark:bg-primary-950 dark:text-primary-400' : 'bg-slate-100 text-slate-600 dark:bg-dark-700 dark:text-slate-300'}">${m.category}</span>
                            </div>
                            <p class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed mb-3">${m.detail}</p>
                            <div class="relative pt-1">
                                <div class="flex mb-2 items-center justify-between">
                                    <span class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full ${isDone ? 'text-primary-600 bg-primary-100 dark:bg-primary-950/40' : 'text-blue-600 bg-blue-100 dark:text-blue-400 dark:bg-blue-950/40'}">${isDone ? 'Tamamlandı ✓' : 'İlerliyor'}</span>
                                    <span class="text-xs font-semibold ${isDone ? 'text-primary-600 dark:text-primary-400' : 'text-slate-500 dark:text-slate-400'}">${pct.toFixed(1)}%</span>
                                </div>
                                <div class="overflow-hidden h-2.5 flex rounded-full bg-slate-150 dark:bg-dark-700">
                                    <div style="width:${pct}%" class="${isDone ? 'bg-primary-500' : 'bg-blue-500'} transition-all duration-1000 rounded-full"></div>
                                </div>
                                ${!isDone ? `<p class="text-xs text-slate-400 mt-2 text-right">${timeRemainingText}</p>` : ''}
                            </div>
                        </div>
                    </div>
                `;
                container.appendChild(card);
            });
        }

        // --- BAŞARIMLAR ---
        function checkAchievements(secondsElapsed, moneySaved) {
            if (!appState.quitDate || isNaN(appState.quitDate.getTime())) return;

            if (secondsElapsed === undefined) {
                secondsElapsed = Math.floor((Date.now() - appState.quitDate.getTime()) / 1000);
            }
            if (moneySaved === undefined) {
                moneySaved = ((appState.cigsPerDay / 86400) * secondsElapsed) * (appState.pricePerPack / appState.packSize);
            }

            let changed = false;
            achievements.forEach(ach => {
                if (!appState.unlockedAchievements.includes(ach.id)) {
                    if (ach.condition(secondsElapsed, moneySaved, appState.cravingsBeaten)) {
                        appState.unlockedAchievements.push(ach.id);
                        changed = true;
                        showNotification(`🏆 Başarım Açıldı: ${ach.title}`);
                    }
                }
            });

            if (changed) {
                saveState();
                renderAchievements();
            }
        }

        function renderAchievements() {
            const container     = document.getElementById('achievements-container');
            const progressText  = document.getElementById('achievements-progress-text');
            const progressBar   = document.getElementById('achievements-progress-bar');
            if (!container) return;
            container.innerHTML = '';

            const total    = achievements.length;
            const unlocked = appState.unlockedAchievements.length;

            if (progressText) progressText.textContent = `${unlocked} / ${total} Başarım Kilidi Açıldı`;
            if (progressBar) progressBar.style.width = `${(unlocked / total) * 100}%`;

            achievements.forEach(ach => {
                const isUnlocked = appState.unlockedAchievements.includes(ach.id);
                const card = document.createElement('div');
                card.className = `glass-card rounded-2xl p-5 border text-center flex flex-col items-center justify-between transition-all duration-300 ${isUnlocked ? 'border-emerald-250 dark:border-emerald-950 bg-gradient-to-br from-white to-emerald-50/20 dark:from-dark-800 dark:to-emerald-950/10' : 'opacity-60 grayscale'}`;
                card.innerHTML = `
                    <div class="text-4xl mb-3">${ach.icon}</div>
                    <div>
                        <h4 class="font-bold text-slate-800 dark:text-slate-100 text-sm mb-1">${ach.title}</h4>
                        <p class="text-xs text-slate-500 dark:text-slate-400 leading-relaxed">${ach.description}</p>
                    </div>
                    <div class="mt-4 w-full">
                        <span class="text-[10px] font-bold px-2.5 py-1 rounded-full ${isUnlocked ? 'bg-emerald-100 text-emerald-800 dark:bg-emerald-950 dark:text-emerald-450' : 'bg-slate-100 text-slate-500 dark:bg-dark-700 dark:text-slate-400'}">${isUnlocked ? 'Açıldı ✓' : 'Kilitli'}</span>
                    </div>
                `;
                container.appendChild(card);
            });
        }

        // --- ALINTI ---
        function displayRandomQuote() {
            if (!quoteText || !quoteAuthor || quotes.length === 0) return;
            let idx = currentQuoteIndex;
            while (idx === currentQuoteIndex && quotes.length > 1) {
                idx = Math.floor(Math.random() * quotes.length);
            }
            currentQuoteIndex = idx;
            const q = quotes[idx];

            quoteText.style.opacity = '0';
            quoteAuthor.style.opacity = '0';
            setTimeout(() => {
                quoteText.textContent = `"${q.quote}"`;
                quoteAuthor.textContent = `- ${q.author}`;
                quoteText.style.opacity = '1';
                quoteAuthor.style.opacity = '1';
            }, 250);
        }

        // --- TEMA ---
        function applyTheme(theme) {
            if (theme === 'dark') {
                docHtml.classList.add('dark');
            } else if (theme === 'light') {
                docHtml.classList.remove('dark');
            } else {
                window.matchMedia('(prefers-color-scheme: dark)').matches
                    ? docHtml.classList.add('dark')
                    : docHtml.classList.remove('dark');
            }

            [
                { btn: themeLightBtn,  key: 'light' },
                { btn: themeDarkBtn,   key: 'dark' },
                { btn: themeSystemBtn, key: 'system' }
            ].forEach(({ btn, key }) => {
                if (!btn) return;
                if (key === theme) {
                    btn.classList.add('bg-primary-500', 'text-white', 'dark:bg-primary-600');
                    btn.classList.remove('bg-slate-100', 'text-slate-600', 'dark:bg-dark-700', 'dark:text-slate-300');
                } else {
                    btn.classList.remove('bg-primary-500', 'text-white', 'dark:bg-primary-600');
                    btn.classList.add('bg-slate-100', 'text-slate-600', 'dark:bg-dark-700', 'dark:text-slate-300');
                }
            });
        }

        function setTheme(theme) {
            appState.theme = theme;
            saveState();
            applyTheme(theme);
            const labels = { light: 'Açık', dark: 'Karanlık', system: 'Sistem Varsayılanı' };
            showNotification(`Tema "${labels[theme]}" olarak ayarlandı.`);
        }

        // --- BİLDİRİM TOAST ---
        function showNotification(message) {
            let container = document.getElementById('toast-container');
            if (!container) {
                container = document.createElement('div');
                container.id = 'toast-container';
                container.className = 'fixed bottom-20 sm:bottom-6 right-6 z-50 flex flex-col gap-2 max-w-sm w-full pointer-events-none';
                document.body.appendChild(container);
            }

            const toast = document.createElement('div');
            toast.className = 'glass-card bg-white/95 dark:bg-dark-800/95 border border-slate-100 dark:border-dark-700 text-slate-800 dark:text-slate-100 p-4 rounded-xl shadow-lg flex items-center space-x-3 pointer-events-auto transform translate-y-2 opacity-0 transition-all duration-300';
            toast.innerHTML = `
                <div class="p-1.5 rounded-lg bg-primary-100 dark:bg-primary-950 text-primary-600 shrink-0">
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                </div>
                <p class="text-sm font-semibold flex-1">${message}</p>
            `;
            container.appendChild(toast);

            requestAnimationFrame(() => {
                requestAnimationFrame(() => {
                    toast.classList.remove('translate-y-2', 'opacity-0');
                });
            });

            setTimeout(() => {
                toast.classList.add('translate-y-2', 'opacity-0');
                setTimeout(() => toast.remove(), 300);
            }, 3500);
        }
    </script>
</body>
</html>
