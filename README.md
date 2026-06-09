<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Özgür Nefes | Sigara Bırakma Sayacı</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#10b981', // Emerald 500
                        primaryDark: '#059669', // Emerald 600
                        dark: '#0f172a',
                    },
                    fontFamily: {
                        sans: ['Inter', 'ui-sans-serif', 'system-ui', '-apple-system', 'BlinkMacSystemFont', 'Segoe UI', 'Roboto', 'Helvetica Neue', 'Arial', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        /* Özelleştirilmiş scrollbar ve animasyonlar */
        body { font-family: 'Inter', sans-serif; }
        .glass-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(226, 232, 240, 0.8);
        }
        .progress-bar-animated {
            transition: width 1s ease-in-out;
        }
        @keyframes pulse-soft {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.8; transform: scale(1.05); }
        }
        .pulse-icon { animation: pulse-soft 2s infinite; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 min-h-screen flex flex-col">

    <!-- Navbar -->
    <nav class="bg-white shadow-sm p-4 sticky top-0 z-10">
        <div class="max-w-4xl mx-auto flex items-center justify-center space-x-2">
            <svg class="w-8 h-8 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
            </svg>
            <h1 class="text-2xl font-bold text-dark">Özgür Nefes</h1>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="flex-grow flex items-center justify-center p-4 sm:p-6 w-full max-w-4xl mx-auto">
        
        <!-- SETUP SCREEN -->
        <div id="setup-screen" class="w-full max-w-md glass-card rounded-2xl shadow-xl p-6 sm:p-8 w-full transition-all duration-300">
            <h2 class="text-xl sm:text-2xl font-bold text-center mb-6 text-slate-800">Yeni Bir Başlangıç</h2>
            <p class="text-slate-500 text-center mb-8 text-sm sm:text-base">Sigarayı bıraktığınız zamanı ve bilgileri girerek özgürlüğünüzü kutlamaya başlayın.</p>
            
            <form id="setup-form" class="space-y-5">
                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Bırakma Tarihi ve Saati</label>
                    <input type="datetime-local" id="input-date" required
                        class="w-full p-3 border border-slate-300 rounded-xl focus:ring-2 focus:ring-primary focus:border-primary outline-none transition-all text-slate-700">
                </div>
                
                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Günde İçilen Sigara Adedi</label>
                    <input type="number" id="input-cigs" min="1" max="150" placeholder="Örn: 20" required
                        class="w-full p-3 border border-slate-300 rounded-xl focus:ring-2 focus:ring-primary focus:border-primary outline-none transition-all text-slate-700">
                </div>
                
                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Bir Paket Sigaranın Fiyatı (₺)</label>
                    <input type="number" id="input-price" min="1" step="0.5" placeholder="Örn: 60" required
                        class="w-full p-3 border border-slate-300 rounded-xl focus:ring-2 focus:ring-primary focus:border-primary outline-none transition-all text-slate-700">
                    <p class="text-xs text-slate-400 mt-1">*Hesaplama pakette 20 sigara olduğu varsayılarak yapılır.</p>
                </div>

                <button type="submit" 
                    class="w-full bg-primary hover:bg-primaryDark text-white font-bold py-3.5 px-4 rounded-xl transition-colors duration-200 transform active:scale-95 shadow-lg flex justify-center items-center space-x-2">
                    <span>Yolculuğa Başla</span>
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                </button>
            </form>
        </div>

        <!-- DASHBOARD SCREEN (Initially Hidden) -->
        <div id="dashboard-screen" class="hidden w-full space-y-6 sm:space-y-8 animate-fade-in">
            
            <!-- Welcome back & Edit Button -->
            <div class="flex justify-between items-center bg-white p-4 rounded-2xl shadow-sm border border-slate-100">
                <div>
                    <h2 class="text-lg font-bold text-slate-800">Tebrikler! 🎉</h2>
                    <p class="text-sm text-slate-500">Kararlılığınızı sürdürün.</p>
                </div>
                <button id="btn-edit" class="text-primary hover:bg-emerald-50 p-2 rounded-lg text-sm font-medium transition-colors flex items-center space-x-1">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z"></path></svg>
                    <span class="hidden sm:inline">Bilgileri Düzenle</span>
                </button>
            </div>

            <!-- Main Timer Banner -->
            <div class="glass-card rounded-3xl p-6 sm:p-10 shadow-lg text-center relative overflow-hidden bg-gradient-to-br from-emerald-500 to-teal-600 text-white border-none">
                <div class="absolute -top-10 -right-10 opacity-10">
                    <svg class="w-48 h-48 pulse-icon" fill="currentColor" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
                </div>
                
                <h3 class="text-emerald-100 font-medium mb-4 text-sm sm:text-base uppercase tracking-wider">Sigarasız Geçen Süre</h3>
                <div class="grid grid-cols-4 gap-2 sm:gap-4 max-w-2xl mx-auto relative z-10">
                    <div class="flex flex-col items-center">
                        <div id="val-days" class="text-3xl sm:text-5xl font-bold font-mono">0</div>
                        <div class="text-xs sm:text-sm text-emerald-100 mt-1">Gün</div>
                    </div>
                    <div class="flex flex-col items-center">
                        <div id="val-hours" class="text-3xl sm:text-5xl font-bold font-mono">0</div>
                        <div class="text-xs sm:text-sm text-emerald-100 mt-1">Saat</div>
                    </div>
                    <div class="flex flex-col items-center">
                        <div id="val-mins" class="text-3xl sm:text-5xl font-bold font-mono">0</div>
                        <div class="text-xs sm:text-sm text-emerald-100 mt-1">Dakika</div>
                    </div>
                    <div class="flex flex-col items-center">
                        <div id="val-secs" class="text-3xl sm:text-5xl font-bold font-mono">0</div>
                        <div class="text-xs sm:text-sm text-emerald-100 mt-1">Saniye</div>
                    </div>
                </div>
            </div>

            <!-- Stats Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 sm:gap-6">
                <!-- Money Saved -->
                <div class="glass-card rounded-2xl p-6 shadow-sm flex items-center space-x-5">
                    <div class="bg-green-100 p-4 rounded-full text-green-600">
                        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                    </div>
                    <div>
                        <p class="text-sm text-slate-500 font-medium">Tasarruf Edilen</p>
                        <div class="text-2xl sm:text-3xl font-bold text-slate-800 font-mono mt-1"><span id="val-money">0.00</span> ₺</div>
                    </div>
                </div>

                <!-- Cigs Avoided -->
                <div class="glass-card rounded-2xl p-6 shadow-sm flex items-center space-x-5">
                    <div class="bg-blue-100 p-4 rounded-full text-blue-600">
                        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 18.364A9 9 0 005.636 5.636m12.728 12.728A9 9 0 015.636 5.636m12.728 12.728L5.636 5.636"></path></svg>
                    </div>
                    <div>
                        <p class="text-sm text-slate-500 font-medium">İçilmeyen Sigara</p>
                        <div class="text-2xl sm:text-3xl font-bold text-slate-800 font-mono mt-1" id="val-cigs">0</div>
                    </div>
                </div>
            </div>

            <!-- Health Progress Section -->
            <div class="glass-card rounded-2xl p-6 sm:p-8 shadow-sm">
                <div class="flex items-center space-x-2 mb-6">
                    <svg class="w-6 h-6 text-red-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path></svg>
                    <h3 class="text-xl font-bold text-slate-800">Sağlık İyileşmeleri</h3>
                </div>
                
                <div class="space-y-6" id="health-milestones-container">
                    <!-- Milestones will be injected here by JS -->
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="text-center py-6 text-slate-400 text-sm mt-auto">
        <p>Sağlıklı bir gelecek için atılan adıma tebrikler.</p>
    </footer>

    <!-- JavaScript Logic -->
    <script>
        // DOM Elements
        const setupScreen = document.getElementById('setup-screen');
        const dashboardScreen = document.getElementById('dashboard-screen');
        const setupForm = document.getElementById('setup-form');
        const btnEdit = document.getElementById('btn-edit');
        const milestonesContainer = document.getElementById('health-milestones-container');

        // State Variables
        let quitDate = null;
        let cigsPerDay = 0;
        let pricePerPack = 0;
        let timerInterval = null;

        // Health Milestones (in seconds)
        const milestones = [
            { id: 1, label: "Nabız ve tansiyon normale dönmeye başlar.", seconds: 20 * 60 },
            { id: 2, label: "Kandaki oksijen seviyesi normale döner.", seconds: 8 * 3600 },
            { id: 3, label: "Karbonmonoksit vücuttan atılır.", seconds: 24 * 3600 },
            { id: 4, label: "Tat ve koku alma duyusu keskinleşir.", seconds: 48 * 3600 },
            { id: 5, label: "Bronşlar gevşer, nefes almak kolaylaşır.", seconds: 72 * 3600 },
            { id: 6, label: "Kan dolaşımı ve akciğer fonksiyonu artar.", seconds: 14 * 24 * 3600 }, // 2 Hafta
            { id: 7, label: "Kalp krizi riski yarı yarıya azalır.", seconds: 365 * 24 * 3600 } // 1 Yıl
        ];

        // Initialize App
        function init() {
            // Set default date to now to make it easier for user
            const now = new Date();
            now.setMinutes(now.getMinutes() - now.getTimezoneOffset());
            document.getElementById('input-date').value = now.toISOString().slice(0, 16);
        }

        // Handle Form Submit
        setupForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const dateInput = document.getElementById('input-date').value;
            quitDate = new Date(dateInput);
            cigsPerDay = parseFloat(document.getElementById('input-cigs').value);
            pricePerPack = parseFloat(document.getElementById('input-price').value);

            if (quitDate > new Date()) {
                alert("Bırakma tarihi gelecekteki bir zaman olamaz!");
                return;
            }

            startTracking();
        });

        // Handle Edit Button
        btnEdit.addEventListener('click', () => {
            clearInterval(timerInterval);
            dashboardScreen.classList.add('hidden');
            setupScreen.classList.remove('hidden');
        });

        function startTracking() {
            // Switch Screens
            setupScreen.classList.add('hidden');
            dashboardScreen.classList.remove('hidden');

            // Render milestones UI first time
            renderMilestones();

            // Initial Update
            updateDashboard();

            // Start Loop
            timerInterval = setInterval(updateDashboard, 1000);
        }

        function updateDashboard() {
            const now = new Date();
            let secondsElapsed = Math.floor((now - quitDate) / 1000);

            if (secondsElapsed < 0) secondsElapsed = 0;

            // 1. Update Timer
            const d = Math.floor(secondsElapsed / (3600 * 24));
            const h = Math.floor((secondsElapsed % (3600 * 24)) / 3600);
            const m = Math.floor((secondsElapsed % 3600) / 60);
            const s = Math.floor(secondsElapsed % 60);

            document.getElementById('val-days').innerText = d;
            document.getElementById('val-hours').innerText = h.toString().padStart(2, '0');
            document.getElementById('val-mins').innerText = m.toString().padStart(2, '0');
            document.getElementById('val-secs').innerText = s.toString().padStart(2, '0');

            // 2. Calculate Stats
            // Assuming 20 cigs in a pack. 
            // seconds in a day = 86400
            const cigsPerSecond = cigsPerDay / 86400;
            const cigsAvoided = cigsPerSecond * secondsElapsed;
            
            const pricePerCig = pricePerPack / 20;
            const moneySaved = cigsAvoided * pricePerCig;

            document.getElementById('val-cigs').innerText = Math.floor(cigsAvoided);
            document.getElementById('val-money').innerText = moneySaved.toFixed(2);

            // 3. Update Milestones Progress
            updateMilestones(secondsElapsed);
        }

        function renderMilestones() {
            milestonesContainer.innerHTML = '';
            
            milestones.forEach((m, index) => {
                const html = `
                    <div class="relative" id="milestone-${m.id}">
                        <div class="flex justify-between text-sm mb-1">
                            <span class="font-medium text-slate-700">${m.label}</span>
                            <span class="text-slate-500 text-xs" id="ms-text-${m.id}">%0</span>
                        </div>
                        <div class="w-full bg-slate-100 rounded-full h-2.5 overflow-hidden">
                            <div id="ms-bar-${m.id}" class="bg-slate-300 h-2.5 rounded-full progress-bar-animated" style="width: 0%"></div>
                        </div>
                    </div>
                `;
                milestonesContainer.innerHTML += html;
            });
        }

        function updateMilestones(secondsElapsed) {
            milestones.forEach(m => {
                const bar = document.getElementById(`ms-bar-${m.id}`);
                const text = document.getElementById(`ms-text-${m.id}`);
                
                if (!bar || !text) return;

                let percentage = (secondsElapsed / m.seconds) * 100;
                
                if (percentage >= 100) {
                    percentage = 100;
                    bar.style.width = '100%';
                    bar.classList.replace('bg-slate-300', 'bg-primary');
                    text.innerText = "Tamamlandı! ✓";
                    text.classList.add('text-primary', 'font-bold');
                } else {
                    bar.style.width = `${percentage}%`;
                    bar.classList.replace('bg-primary', 'bg-blue-500'); // In progress color
                    text.innerText = `%${percentage.toFixed(1)}`;
                }
            });
        }

        // Run Init
        init();
    </script>
</body>
</html>
