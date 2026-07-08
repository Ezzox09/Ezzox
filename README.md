# Ezzox
<!DOCTYPE html>
<html lang="fr">
<head>
    <base target="_self">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Boost Pro - Boost Brawl Stars, Fortnite, Valorant v6</title>
    <meta name="description" content="Boost Pro : commandez du boost pour Brawl Stars, Fortnite et Valorant. Chat en direct, offres détaillées avec TOUS les paliers. Valorant: Iron→Bronze 10€, Bronze→Silver 10€, Silver→Gold 10€, Gold→Plat 15€, Plat→Diamant 20€, Diamant→Ascendant 30€, Ascendant→Immo 80€, Immo→Radiant 400€.">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --chat-bg: #1e293b;
            --chat-msg-bot: #334155;
            --chat-msg-user: #3b82f6;
        }
        .chat-window {
            height: 300px;
            overflow-y: auto;
            scroll-behavior: smooth;
        }
        .chat-window::-webkit-scrollbar { width: 6px; }
        .chat-window::-webkit-scrollbar-thumb { background: #475569; border-radius: 3px; }
        .chat-message-user { background: var(--chat-msg-user); }
        .chat-message-bot { background: var(--chat-msg-bot); }
        .game-card:hover { transform: translateY(-4px); }
        .game-card { transition: transform 0.2s ease; }
        .offer-badge { background: #0f172a; border: 1px solid #334155; }
        .chat-message-bot, .chat-message-user { max-width: 85%; }
        .rank-progress { height: 6px; border-radius: 3px; }
    </style>
</head>
<body class="bg-slate-900 text-white font-sans">

    <header class="sticky top-0 z-50 bg-slate-800/90 backdrop-blur-md border-b border-slate-700">
        <nav class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
            <a href="#hero" class="text-2xl font-bold text-cyan-400"><i class="fas fa-bolt mr-2"></i>Boost Pro</a>
            <ul id="nav-list" class="hidden md:flex space-x-6 text-sm font-medium" role="menubar"></ul>
            <button id="mobile-menu-btn" class="md:hidden text-white text-xl" aria-label="Menu"><i class="fas fa-bars"></i></button>
        </nav>
        <div id="mobile-menu" class="hidden md:hidden bg-slate-800 px-4 pb-4 border-b border-slate-700">
            <ul id="mobile-nav-list" class="space-y-2"></ul>
        </div>
    </header>

    <main>
        <!-- Hero -->
        <section id="hero" class="relative overflow-hidden bg-gradient-to-br from-slate-800 via-slate-900 to-cyan-900 min-h-[70vh] flex items-center">
            <div class="absolute inset-0 opacity-20 bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-cyan-500 via-transparent to-transparent"></div>
            <div class="max-w-6xl mx-auto px-4 py-20 text-center relative z-10">
                <h1 class="text-4xl md:text-6xl font-extrabold mb-4 bg-gradient-to-r from-cyan-300 to-blue-500 bg-clip-text text-transparent">
                    Boostez votre rang compétitif
                </h1>
                <p class="text-lg md:text-xl text-slate-300 max-w-2xl mx-auto mb-8">
                    Services de boost professionnels pour Brawl Stars, Fortnite et Valorant. <strong>TOUS les paliers listés</strong>. Chat en direct, devis immédiat. Boost Valorant : Iron→Bronze 10€, Immortal→Radiant 400€.
                </p>
                <div class="flex flex-wrap justify-center gap-4">
                    <a href="#order" class="px-8 py-3 bg-cyan-500 hover:bg-cyan-400 text-slate-900 font-bold rounded-lg shadow-lg transition">Commander maintenant</a>
                    <a href="#chat" class="px-8 py-3 bg-transparent border border-cyan-400 text-cyan-300 hover:bg-cyan-800/30 rounded-lg transition"><i class="fas fa-comments mr-2"></i>Chat en direct</a>
                </div>
            </div>
        </section>

        <!-- Games -->
        <section id="games" class="max-w-6xl mx-auto px-4 py-16">
            <h2 class="text-3xl font-bold text-center mb-2 text-white">Nos jeux</h2>
            <p class="text-slate-400 text-center mb-10">Choisissez votre jeu et découvrez les offres disponibles avec TOUS les paliers</p>
            <div id="card-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6"></div>
        </section>

        <!-- Valorant Rank Progress -->
        <section id="valorant-ranks" class="bg-slate-800/50 py-12">
            <div class="max-w-4xl mx-auto px-4">
                <h2 class="text-2xl font-bold text-center mb-2">Progression des rangs Valorant</h2>
                <p class="text-slate-400 text-center mb-8">Parcourez chaque étape avec nos prix fixes. Exemple: <strong>Iron→Bronze 10€</strong>, <strong>Immo→Radiant 400€</strong>.</p>
                <div class="space-y-4">
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Iron → Bronze</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-red-700 to-yellow-700 w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">10€</span>
                    </div>
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Bronze → Silver</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-yellow-700 to-gray-300 w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">10€</span>
                    </div>
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Silver → Gold</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-gray-300 to-yellow-400 w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">10€</span>
                    </div>
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Gold → Platinum</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-yellow-400 to-cyan-300 w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">15€</span>
                    </div>
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Platinum → Diamond</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-cyan-300 to-purple-500 w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">20€</span>
                    </div>
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Diamond → Ascendant</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-purple-500 to-green-500 w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">30€</span>
                    </div>
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Ascendant → Immortal</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-green-500 to-red-500 w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">80€</span>
                    </div>
                    <div class="flex items-center justify-between">
                        <span class="text-slate-300 font-medium w-32">Immortal → Radiant</span>
                        <div class="flex-1 h-2 mx-4">
                            <div class="rank-progress bg-gradient-to-r from-red-500 to-gold w-full"></div>
                        </div>
                        <span class="text-green-400 font-bold text-right w-24">400€</span>
                    </div>
                </div>
                <p class="text-center text-slate-400 text-sm mt-6">Calcul automatique sur demande dans le chat.</p>
            </div>
        </section>

        <!-- Order -->
        <section id="order" class="bg-slate-800/30 py-16">
            <div class="max-w-3xl mx-auto px-4">
                <h2 class="text-3xl font-bold text-center mb-2">Passer une commande</h2>
                <p class="text-slate-400 text-center mb-8">Remplissez ce formulaire et un expert vous contactera dans le chat.</p>
                <form id="order-form" class="bg-slate-700/50 p-6 md:p-8 rounded-xl shadow-lg space-y-5">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label for="name" class="block text-sm font-medium mb-1">Votre pseudo</label>
                            <input type="text" id="name" required class="w-full px-4 py-2 bg-slate-600 border border-slate-500 rounded-lg focus:ring-2 focus:ring-cyan-500 text-white placeholder-slate-400" placeholder="Ex: DarkGamer">
                        </div>
                        <div>
                            <label for="game" class="block text-sm font-medium mb-1">Jeu</label>
                            <select id="game" required class="w-full px-4 py-2 bg-slate-600 border border-slate-500 rounded-lg focus:ring-2 focus:ring-cyan-500 text-white">
                                <option value="">Sélectionnez un jeu</option>
                                <option value="Brawl Stars">Brawl Stars</option>
                                <option value="Fortnite">Fortnite</option>
                                <option value="Valorant">Valorant</option>
                            </select>
                        </div>
                    </div>
                    <div>
                        <label for="message" class="block text-sm font-medium mb-1">Détails de la commande</label>
                        <textarea id="message" rows="3" required class="w-full px-4 py-2 bg-slate-600 border border-slate-500 rounded-lg focus:ring-2 focus:ring-cyan-500 text-white placeholder-slate-400" placeholder="Décrivez ce que vous voulez (offre choisie, rang de départ, rang cible, etc.)"></textarea>
                    </div>
                    <button type="submit" class="w-full py-3 bg-cyan-500 hover:bg-cyan-400 text-slate-900 font-bold rounded-lg transition">Envoyer la commande</button>
                </form>
                <p id="order-confirm" class="hidden text-green-400 text-center mt-4"><i class="fas fa-check-circle mr-2"></i>Commande envoyée ! Consultez le chat pour la réponse.</p>
            </div>
        </section>

        <!-- Chat -->
        <section id="chat" class="max-w-4xl mx-auto px-4 py-16">
            <h2 class="text-3xl font-bold text-center mb-2">Chat en direct</h2>
            <p class="text-slate-400 text-center mb-8">Discutez avec nos boosters et suivez vos commandes.</p>
            <div class="bg-slate-800 rounded-xl shadow-xl border border-slate-700 overflow-hidden">
                <div id="chat-messages" class="chat-window p-4 space-y-3 bg-[var(--chat-bg)]">
                    <!-- messages generated by JS -->
                </div>
                <div class="flex items-center border-t border-slate-700 p-3 bg-slate-850">
                    <input type="text" id="chat-input" placeholder="Écrivez votre message..." class="flex-1 px-4 py-2 bg-slate-700 border border-slate-600 rounded-full text-sm focus:ring-2 focus:ring-cyan-500 text-white placeholder-slate-400 outline-none">
                    <button id="chat-send" class="ml-3 bg-cyan-500 hover:bg-cyan-400 text-white w-10 h-10 rounded-full flex items-center justify-center transition" aria-label="Envoyer"><i class="fas fa-paper-plane"></i></button>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-slate-800 border-t border-slate-700 py-8 text-center text-sm text-slate-400">
        <div class="max-w-6xl mx-auto px-4">
            <p class="mb-2">&copy; 2025 Boost Pro. Tous droits réservés.</p>
            <p>Boost pour Brawl Stars, Fortnite et Valorant.</p>
        </div>
    </footer>

    <script>
        // ── DATA LAYER ──
        const navItems = [
            { label: "Accueil", href: "#hero" },
            { label: "Jeux", href: "#games" },
            { label: "Progression Valorant", href: "#valorant-ranks" },
            { label: "Commander", href: "#order" },
            { label: "Chat", href: "#chat" }
        ];

        const games = [
            {
                title: "Brawl Stars",
                desc: "Boostez votre compte Brawl Stars avec nos offres détaillées ci-dessous.",
                icon: "fa-star",
                color: "text-yellow-400",
                bgColor: "from-yellow-600/20 to-transparent",
                img: "https://picsum.photos/400/250?random=1",
                offers: [
                    { name: "L1 → Master", price: "20€" },
                    { name: "Mythique 1 → L1", price: "10€" },
                    { name: "Master → Master 2", price: "45€" },
                    { name: "Master → Master 3", price: "200€" },
                    { name: "Master → Pro", price: "400€" }
                ]
            },
            {
                title: "Fortnite",
                desc: "Boostez votre rang Fortnite de Bronze à Unreal. <strong>5€ par palier</strong> avant Diamant, <strong>10€ par palier</strong> après Diamant (Diamant 1 → Unreal).",
                icon: "fa-crown",
                color: "text-purple-400",
                bgColor: "from-purple-600/20 to-transparent",
                img: "https://picsum.photos/400/250?random=2",
                offers: [
                    { name: "Bronze 1 → Bronze 2", price: "5€" },
                    { name: "Bronze 2 → Bronze 3", price: "5€" },
                    { name: "Bronze 3 → Argent 1", price: "5€" },
                    { name: "Argent 1 → Argent 2", price: "5€" },
                    { name: "Argent 2 → Argent 3", price: "5€" },
                    { name: "Argent 3 → Or 1", price: "5€" },
                    { name: "Or 1 → Or 2", price: "5€" },
                    { name: "Or 2 → Or 3", price: "5€" },
                    { name: "Or 3 → Platine 1", price: "5€" },
                    { name: "Platine 1 → Platine 2", price: "5€" },
                    { name: "Platine 2 → Platine 3", price: "5€" },
                    { name: "Platine 3 → Diamant 1", price: "5€" },
                    { name: "Diamant 1 → Diamant 2", price: "10€" },
                    { name: "Diamant 2 → Diamant 3", price: "10€" },
                    { name: "Diamant 3 → Élite", price: "10€" },
                    { name: "Élite → Champion", price: "10€" },
                    { name: "Champion → Unreal", price: "10€" }
                ]
            },
            {
                title: "Valorant",
                desc: "Boost de rang complet : Iron→Bronze 10€, Bronze→Silver 10€, Silver→Gold 10€, Gold→Platinum 15€, Platinum→Diamond 20€, Diamond→Ascendant 30€, Ascendant→Immortal 80€, Immortal→Radiant 400€.",
                icon: "fa-crosshairs",
                color: "text-red-400",
                bgColor: "from-red-600/20 to-transparent",
                img: "https://picsum.photos/400/250?random=3",
                offers: [
                    { name: "Iron → Bronze", price: "10€" },
                    { name: "Bronze → Silver", price: "10€" },
                    { name: "Silver → Gold", price: "10€" },
                    { name: "Gold → Platinum", price: "15€" },
                    { name: "Platinum → Diamond", price: "20€" },
                    { name: "Diamond → Ascendant", price: "30€" },
                    { name: "Ascendant → Immortal", price: "80€" },
                    { name: "Immortal → Radiant", price: "400€" }
                ]
            }
        ];

        // ── RENDER FUNCTIONS ──
        function renderNav(items) {
            return items.map(i =>
                `<li role="menuitem"><a href="${i.href}" class="hover:text-cyan-300 transition">${i.label}</a></li>`
            ).join("");
        }

        function renderMobileNav(items) {
            return items.map(i =>
                `<li><a href="${i.href}" class="block py-2 hover:text-cyan-300 transition">${i.label}</a></li>`
            ).join("");
        }

        function renderOffers(offers) {
            if (!offers || offers.length === 0) return '<p class="text-slate-400 text-sm italic mt-3">Contactez-nous pour un devis personnalisé.</p>';
            return `
                <div class="mt-4 space-y-2">
                    <h4 class="text-sm font-semibold text-cyan-300 uppercase tracking-wide">Offres disponibles</h4>
                    ${offers.map(o => `
                        <div class="offer-badge flex justify-between items-center px-3 py-2 rounded-lg text-sm hover:bg-slate-700/30 transition-colors">
                            <span class="truncate mr-2">${o.name}</span>
                            <span class="font-bold text-green-400 whitespace-nowrap">${o.price}</span>
                        </div>
                    `).join('')}
                </div>
            `;
        }

        function renderCards(items) {
            return items.map((g, idx) => `
                <article class="game-card bg-slate-800 rounded-xl overflow-hidden shadow-xl border border-slate-700 hover:border-cyan-500/50">
                    <img src="${g.img}" alt="Illustration boost ${g.title}" loading="lazy" class="w-full h-48 object-cover">
                    <div class="p-5">
                        <div class="flex items-center mb-3">
                            <i class="fas ${g.icon} ${g.color} text-2xl mr-3"></i>
                            <h3 class="text-xl font-bold">${g.title}</h3>
                        </div>
                        <p class="text-slate-300 text-sm mb-2">${g.desc}</p>
                        ${renderOffers(g.offers)}
                        <a href="#order" class="inline-block mt-4 px-5 py-2 bg-cyan-500 hover:bg-cyan-400 text-slate-900 font-semibold rounded-lg transition text-sm">Commander</a>
                    </div>
                </article>
            `).join("");
        }

        // ── MOUNT ──
        document.getElementById("nav-list").innerHTML = renderNav(navItems);
        document.getElementById("mobile-nav-list").innerHTML = renderMobileNav(navItems);
        document.getElementById("card-grid").innerHTML = renderCards(games);

        // ── EVENT DELEGATION (navigation) ──
        document.addEventListener("click", function(e) {
            const link = e.target.closest("a[href^='#']");
            if (!link) return;
            e.preventDefault();
            const target = document.querySelector(link.getAttribute("href"));
            if (target) {
                target.scrollIntoView({ behavior: "smooth" });
                document.getElementById("mobile-menu").classList.add("hidden");
            }
        });

        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById("mobile-menu-btn");
        const mobileMenu = document.getElementById("mobile-menu");
        mobileMenuBtn.addEventListener("click", function() {
            mobileMenu.classList.toggle("hidden");
        });

        // ── ORDER FORM ──
        const orderForm = document.getElementById("order-form");
        const orderConfirm = document.getElementById("order-confirm");
        orderForm.addEventListener("submit", function(e) {
            e.preventDefault();
            const name = document.getElementById("name").value;
            const game = document.getElementById("game").value;
            const message = document.getElementById("message").value;
            orderConfirm.classList.remove("hidden");
            orderConfirm.innerHTML = `<i class="fas fa-check-circle mr-2"></i>Merci ${name} ! Votre commande pour ${game} a été envoyée. Un booster vous répondra dans le chat.`;
            orderForm.reset();
            setTimeout(() => { orderConfirm.classList.add("hidden"); }, 5000);
            addBotMessage(`✅ Nouvelle commande de <b>${name}</b> pour <b>${game}</b>. Détails : "${message}". Nous vous contacterons dans les 10 minutes.`);
        });

        // ── CHAT SYSTEM ──
        const chatMessages = document.getElementById("chat-messages");
        const chatInput = document.getElementById("chat-input");
        const chatSend = document.getElementById("chat-send");

        function addBotMessage(text) {
            const div = document.createElement("div");
            div.className = "chat-message-bot text-white text-sm p-3 rounded-lg self-start";
            div.innerHTML = `<i class="fas fa-robot mr-2 text-cyan-400"></i>${text}`;
            chatMessages.appendChild(div);
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }

        function addUserMessage(text) {
            const div = document.createElement("div");
            div.className = "chat-message-user text-white text-sm p-3 rounded-lg self-end ml-auto";
            div.textContent = text;
            chatMessages.appendChild(div);
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }

        function calculateValorantPrice(start, end) {
            const ranks = ["Iron", "Bronze", "Silver", "Gold", "Platinum", "Diamond", "Ascendant", "Immortal", "Radiant"];
            const prices = [0, 10, 10, 10, 15, 20, 30, 80, 400];
            const startIdx = ranks.indexOf(start);
            const endIdx = ranks.indexOf(end);
            if (startIdx === -1 || endIdx === -1 || startIdx >= endIdx) return null;
            let total = 0;
            for (let i = startIdx; i < endIdx; i++) {
                total += prices[i + 1];
            }
            return total;
        }

        function handleUserMessage(text) {
            const lower = text.toLowerCase();
            let reply = "";
            if (lower.includes("bonjour") || lower.includes("salut") || lower.includes("hello")) {
                reply = "Bonjour ! Comment puis-je vous aider ? Consultez les offres détaillées avec TOUS les paliers dans la section Jeux et la progression Valorant. Vous pouvez commander via le formulaire ou me poser une question.";
            } else if (lower.includes("fortnite") && (lower.includes("palier") || lower.includes("diamant") || lower.includes("5€"))) {
                reply = "<b>Fortnite – Tous les paliers 5€ (avant Diamant) / 10€ (après Diamant):</b><br>• Tous les paliers Bronze, Argent, Or, Platine : <strong>5€ par palier</strong> (ex: Bronze1→Bronze2 5€)<br>• Tous les paliers Diamant → Unreal : <strong>10€ par palier</strong> (ex: Diamant1→Diamant2 10€, Champion→Unreal 10€)<br>Total Bronze1→Unreal (15 paliers) : 80€";
            } else if (lower.includes("valorant") && (lower.includes("iron") || lower.includes("bronze") || lower.includes("10€") || lower.includes("20€") || lower.includes("30€") || lower.includes("80€") || lower.includes("400€"))) {
                reply = "<b>Valorant – Tous les paliers :</b><br>• Iron→Bronze: <strong>10€</strong><br>• Bronze→Silver: <strong>10€</strong><br>• Silver→Gold: <strong>10€</strong><br>• Gold→Platinum: <strong>15€</strong><br>• Platinum→Diamond: <strong>20€</strong><br>• Diamond→Ascendant: <strong>30€</strong><br>• Ascendant→Immortal: <strong>80€</strong><br>• Immortal→Radiant: <strong>400€</strong><br><br>Pour un calcul automatique, écrivez par exemple 'Valorant Gold→Diamond'.";
            } else if (lower.includes("valorant") && lower.includes("→")) {
                const match = text.match(/(Iron|Bronze|Silver|Gold|Platinum|Diamond|Ascendant|Immortal|Radiant)\s*→\s*(Iron|Bronze|Silver|Gold|Platinum|Diamond|Ascendant|Immortal|Radiant)/i);
                if (match) {
                    const start = match[1].charAt(0).toUpperCase() + match[1].slice(1).toLowerCase();
                    const end = match[2].charAt(0).toUpperCase() + match[2].slice(1).toLowerCase();
                    const total = calculateValorantPrice(start, end);
                    if (total !== null) {
                        reply = `Boost Valorant <b>${start} → ${end}</b> : <strong>${total}€</strong>. Précisez votre Riot ID pour la commande.`;
                    } else {
                        reply = "Je n'ai pas pu calculer ce trajet. Assurez-vous que le rang de départ est inférieur au rang cible.";
                    }
                } else {
                    reply = "Pour un devis Valorant, écrivez 'Valorant Gold→Diamond' ou consultez la section Progression Valorant.";
                }
            } else if (lower.includes("brawl stars")) {
                reply = "Boost Brawl Stars : L1→Master 20€, Mythique1→L1 10€, Master→Master2 45€, Master→Master3 200€, Master→Pro 400€. Indiquez votre ID de joueur et l'offre choisie.";
            } else if (lower.includes("merci") || lower.includes("thanks")) {
                reply = "Avec plaisir ! Si vous avez d'autres questions, n'hésitez pas. Bon jeu !";
            } else {
                reply = "Je suis un assistant automatique. Pour une aide personnalisée, veuillez passer commande via le formulaire ci-dessus ou reformuler votre question. Merci !";
            }
            addBotMessage(reply);
        }

        function sendMessage() {
            const text = chatInput.value.trim();
            if (!text) return;
            addUserMessage(text);
            chatInput.value = "";
            setTimeout(() => handleUserMessage(text), 500);
        }

        chatSend.addEventListener("click", sendMessage);
        chatInput.addEventListener("keydown", function(e) {
            if (e.key === "Enter") sendMessage();
        });

        // Initial bot welcome
        addBotMessage("Bienvenue sur Boost Pro ! <strong>Valorant : Iron→Bronze 10€, Bronze→Silver 10€, Silver→Gold 10€, Gold→Platinum 15€, Platinum→Diamond 20€, Diamond→Ascendant 30€, Ascendant→Immortal 80€, Immortal→Radiant 400€</strong>. Consultez les offres dans la section Jeux et la progression complète !");
    </script>
</body>
</html>
