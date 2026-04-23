<!DOCTYPE html>
<html lang="sk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coburg Bistro | Banská Štiavnica</title>
    
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700;1,900&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS 4 (via CDN for standalone use) -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style type="text/tailwindcss">
        @theme {
            --font-sans: "Inter", sans-serif;
            --font-serif: "Playfair Display", serif;
            --color-bistro-dark: #121110;
            --color-bistro-darker: #1C1B19;
            --color-bistro-accent: #f59e0b;
            --color-bistro-cream: #EBE6E0;
        }

        body {
            @apply bg-bistro-dark text-bistro-cream font-sans antialiased;
        }

        .heading-massive {
            @apply font-serif uppercase leading-[0.85] tracking-tighter;
        }

        .label-micro {
            @apply text-[11px] uppercase tracking-[0.3em] font-medium opacity-60;
        }

        /* Custom scrollbar */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { @apply bg-bistro-dark; }
        ::-webkit-scrollbar-thumb { @apply bg-bistro-accent/30 rounded-full hover:bg-bistro-accent/50; }
    </style>
</head>
<body>

    <!-- NAVBAR -->
    <nav id="navbar" class="fixed top-0 left-0 w-full z-50 transition-all duration-500 py-8 bg-transparent">
        <div class="container mx-auto px-6 flex justify-between items-end">
            <a href="#" class="flex flex-col">
                <span class="font-serif text-4xl md:text-5xl tracking-tighter leading-none italic uppercase font-black text-white">Coburg</span>
                <span class="label-micro ml-1 mt-1">Banská Štiavnica • Bistro</span>
            </a>
            <div class="hidden md:flex items-center space-x-10 text-[11px] uppercase tracking-widest font-bold">
                <a href="#" class="text-white/60 hover:text-bistro-accent transition-colors">Domov</a>
                <a href="#o-nas" class="text-white/60 hover:text-bistro-accent transition-colors">O nás</a>
                <a href="#menu" class="text-white/60 hover:text-bistro-accent transition-colors">Menu</a>
                <a href="#kontakt" class="bg-bistro-cream text-bistro-dark hover:bg-bistro-accent hover:text-white px-8 py-3 transition-all duration-300 font-black">Rezervácia</a>
            </div>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="relative h-screen w-full flex items-center justify-center overflow-hidden">
        <div class="absolute inset-0 z-0">
            <img src="https://images.unsplash.com/photo-1550966841-3ee4ad6b1074?q=80&w=2070&auto=format&fit=crop" class="w-full h-full object-cover grayscale opacity-40" alt="Background">
            <div class="absolute inset-0 bg-gradient-to-t from-bistro-dark via-bistro-dark/60 to-transparent"></div>
        </div>

        <div class="container mx-auto px-6 relative z-10">
            <div class="max-w-6xl mx-auto lg:grid lg:grid-cols-12 lg:gap-12 items-center">
                <div class="lg:col-span-8">
                    <h1 class="text-[15vw] md:text-[110px] heading-massive mb-8 text-white">
                        Poctivé <span class="text-bistro-accent">Burgre</span>
                    </h1>
                    <p class="text-xl md:text-2xl text-white/90 max-w-xl font-light leading-relaxed mb-12">
                        Zakladáme si na jednoduchom menu, najvyššej kvalite surovín a priateľskom prístupe v srdci historickej Štiavnice.
                    </p>

                    <div class="flex flex-col md:flex-row items-center space-y-4 md:space-y-0 md:space-x-4">
                        <a href="#kontakt" class="w-full md:w-auto bg-bistro-cream text-bistro-dark px-12 py-4 text-xs uppercase tracking-widest font-black hover:bg-bistro-accent hover:text-white text-center transition-all">Rezervovať stôl</a>
                        <a href="#menu" class="w-full md:w-auto border border-bistro-cream/20 text-white px-12 py-4 text-xs uppercase tracking-widest font-black hover:bg-white/10 text-center transition-all">Menu Lístok</a>
                    </div>

                    <div class="mt-16 flex flex-wrap items-center gap-8">
                        <div class="flex items-center gap-2">
                            <span class="w-2 h-2 rounded-full bg-green-500"></span>
                            <span class="label-micro">Psy povolené</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="w-2 h-2 rounded-full bg-green-500"></span>
                            <span class="label-micro">Terasa otvorená</span>
                        </div>
                    </div>
                </div>

                <div class="hidden lg:block lg:col-span-4 relative">
                    <div class="aspect-square rounded-full overflow-hidden border-8 border-white/5 shadow-2xl">
                        <img src="https://images.unsplash.com/photo-1571091718767-18b5b1457add?q=80&w=2072&auto=format&fit=crop" class="w-full h-full object-cover" alt="Burger">
                    </div>
                    <div class="absolute -bottom-6 -right-6 bg-bistro-accent text-bistro-dark px-6 py-4 rounded-2xl font-black text-xs uppercase tracking-widest">
                        Kvalita bez kompromisov
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- MENU SECTION -->
    <section id="menu" class="py-32 bg-bistro-darker">
        <div class="container mx-auto px-6">
            <div class="mb-16">
                <h2 class="label-micro mb-4 text-bistro-accent">Naša ponuka</h2>
                <h3 class="text-4xl md:text-7xl font-serif italic">Zamerané na chuť</h3>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
                <div class="lg:col-span-8 bg-bistro-dark p-8 md:p-12 border-l-4 border-bistro-accent">
                    <h3 class="label-micro mb-10 text-bistro-accent opacity-100 font-black">Lístok</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-x-12 gap-y-8">
                        <div class="border-b border-white/5 pb-4">
                            <div class="flex justify-between items-end mb-2">
                                <h4 class="text-xl font-serif italic">Coburg Classic</h4>
                                <span class="text-sm font-mono opacity-80">12.50 €</span>
                            </div>
                            <p class="text-[10px] text-white/40 uppercase tracking-widest">Hovädzie, cheddar, slanina, majonéza</p>
                        </div>
                        <div class="border-b border-white/5 pb-4">
                            <div class="flex justify-between items-end mb-2">
                                <h4 class="text-xl font-serif italic">Halloumi Veggie</h4>
                                <span class="text-sm font-mono opacity-80">11.50 €</span>
                            </div>
                            <p class="text-[10px] text-white/40 uppercase tracking-widest">Grilovaný syr, pesto, rukola</p>
                        </div>
                        <div class="border-b border-white/5 pb-4">
                            <div class="flex justify-between items-end mb-2">
                                <h4 class="text-xl font-serif italic">Pikant Mexiko</h4>
                                <span class="text-sm font-mono opacity-80">13.50 €</span>
                            </div>
                            <p class="text-[10px] text-white/40 uppercase tracking-widest">Jalapeños, nachos, avokádo</p>
                        </div>
                        <div class="border-b border-white/5 pb-4">
                            <div class="flex justify-between items-end mb-2">
                                <h4 class="text-xl font-serif italic">Craft Beer Selection</h4>
                                <span class="text-sm font-mono opacity-80">4.20 €</span>
                            </div>
                            <p class="text-[10px] text-white/40 uppercase tracking-widest">Výber z lokálnych pivovarov</p>
                        </div>
                    </div>
                </div>

                <div class="lg:col-span-4 p-12 border border-white/10 flex flex-col justify-between">
                    <div>
                        <p class="label-micro mb-4">Cena na osobu</p>
                        <p class="text-5xl font-serif italic text-bistro-accent mb-6">15 – 20 €</p>
                        <p class="text-sm font-light opacity-60 leading-relaxed">Pomer kvality a zážitku v historickom centre Banskej Štiavnice.</p>
                    </div>
                    <div class="mt-8 pt-8 border-t border-white/10">
                        <p class="text-[10px] uppercase font-black tracking-widest">Otvorené denne</p>
                        <p class="text-sm mt-2">11:00 – 22:00</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer id="kontakt" class="py-24 bg-bistro-dark border-t border-white/5">
        <div class="container mx-auto px-6">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-end mb-20">
                <div class="lg:col-span-7">
                    <h2 class="label-micro text-bistro-accent mb-6">Kontakt</h2>
                    <h3 class="text-5xl md:text-8xl font-serif italic mb-12">Zastavte sa u nás.</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <div>
                            <p class="label-micro opacity-40 mb-2">Lokalita</p>
                            <p class="text-lg font-medium italic font-serif leading-snug">Radničné námestie 43/12,<br>Banská Štiavnica</p>
                        </div>
                        <div>
                            <p class="label-micro opacity-40 mb-2">Rezervácie</p>
                            <p class="text-lg font-medium italic font-serif">0948 500 713</p>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-5 grid grid-cols-2 gap-4">
                    <div class="p-8 border border-white/10 bg-bistro-darker/50 text-center">
                        <p class="label-micro mb-2">Instagram</p>
                        <p class="text-sm font-bold opacity-80">@coburgbistro</p>
                    </div>
                    <div class="p-8 border border-white/10 bg-bistro-darker/50 text-center">
                        <p class="label-micro mb-2">Atmosféra</p>
                        <p class="text-sm font-bold opacity-80">Since 2022</p>
                    </div>
                </div>
            </div>

            <div class="flex flex-col md:flex-row justify-between items-center text-[10px] uppercase tracking-[0.3em] font-black opacity-30 pt-12 border-t border-white/10">
                <span>Coburg Bistro • Banská Štiavnica</span>
                <span class="mt-4 md:mt-0">© 2026 Všetky práva vyhradené</span>
            </div>
        </div>
    </footer>

    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const nav = document.getElementById('navbar');
            if (window.scrollY > 50) {
                nav.classList.add('bg-bistro-dark/95', 'backdrop-blur-md', 'py-4', 'border-b', 'border-white/10');
                nav.classList.remove('py-8', 'bg-transparent');
            } else {
                nav.classList.remove('bg-bistro-dark/95', 'backdrop-blur-md', 'py-4', 'border-b', 'border-white/10');
                nav.classList.add('py-8', 'bg-transparent');
            }
        });

        // Lucide icons init
        lucide.createIcons();
    </script>
</body>
</html>
