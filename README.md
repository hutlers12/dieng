<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A.dieng Shop - Vente en ligne</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Animation pour les cartes de produits */
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        /* Animation pour le bouton */
        .btn-hover:hover {
            background-position: right center;
        }
        
        /* Gradient pour le bouton */
        .gradient-btn {
            background-size: 200% auto;
            background-image: linear-gradient(to right, #ff512f 0%, #dd2476 51%, #ff512f 100%);
            transition: 0.5s;
        }
    </style>
</head>
<body class="font-sans bg-gray-50">
    <!-- Barre de navigation -->
    <nav class="bg-white shadow-lg sticky top-0 z-50">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center py-4">
                <!-- Logo -->
                <div class="flex items-center space-x-2">
                    <i class="fas fa-shopping-bag text-2xl text-purple-600"></i>
                    <span class="font-bold text-xl text-gray-800"><A class="dieng"></A>A.dieng  shop</span>
                </div>
                
                <!-- Liens de navigation - Desktop -->
                <div class="hidden md:flex space-x-8">
                    <a href="#" class="text-gray-800 hover:text-purple-600 font-medium">Accueil</a>
                    <a href="#" class="text-gray-800 hover:text-purple-600 font-medium">Boutique</a>
                    <a href="#" class="text-gray-800 hover:text-purple-600 font-medium">Nouveautés</a>
                    <a href="#" class="text-gray-800 hover:text-purple-600 font-medium">Contact</a>
                </div>
                
                <!-- Icônes panier/compte -->
                <div class="flex items-center space-x-4">
                    <a href="#" class="text-gray-800 hover:text-purple-600">
                        <i class="fas fa-user text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-800 hover:text-purple-600 relative">
                        <i class="fas fa-shopping-cart text-xl"></i>
                        <span class="absolute -top-2 -right-2 bg-purple-600 text-white text-xs rounded-full h-5 w-5 flex items-center justify-center">3</span>
                    </a>
                    
                    <!-- Menu mobile -->
                    <button id="mobile-menu-button" class="md:hidden text-gray-800 focus:outline-none">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
            
            <!-- Menu mobile - caché par défaut -->
            <div id="mobile-menu" class="hidden md:hidden pb-4">
                <a href="#" class="block py-2 text-gray-800 hover:text-purple-600">Accueil</a>
                <a href="#" class="block py-2 text-gray-800 hover:text-purple-600">Boutique</a>
                <a href="#" class="block py-2 text-gray-800 hover:text-purple-600">Nouveautés</a>
                <a href="#" class="block py-2 text-gray-800 hover:text-purple-600">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Bannière principale -->
    <div class="relative bg-gradient-to-r from-purple-500 to-pink-500 text-white py-16 md:py-24">
        <div class="container mx-auto px-4 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-8 md:mb-0">
                <h1 class="text-4xl md:text-5xl font-bold mb-4">Découvrez nos nouveautés</h1>
                <p class="text-xl mb-6">Des produits de qualité à des prix imbattables. Livraison rapide et sécurisée.</p>
                <button class="gradient-btn btn-hover text-white font-bold py-3 px-8 rounded-full">
                    Acheter maintenant
                </button>
            </div>
            <div class="md:w-1/2 flex justify-center">
                <img src="https://via.placeholder.com/500x300" alt="Produit vedette" class="rounded-lg shadow-xl w-full max-w-md">
            </div>
        </div>
    </div>

    <!-- Catégories -->
    <div class="container mx-auto px-4 py-12">
        <h2 class="text-3xl font-bold text-center mb-12">Nos Catégories</h2>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
            <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow">
                <div class="h-40 bg-purple-100 flex items-center justify-center">
                    <i class="fas fa-tshirt text-5xl text-purple-600"></i>
                </div>
                <div class="p-4">
                    <h3 class="font-semibold text-lg mb-2">Vêtements</h3>
                    <p class="text-gray-600">Découvrez notre collection</p>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow">
                <div class="h-40 bg-blue-100 flex items-center justify-center">
                    <i class="fas fa-laptop text-5xl text-blue-600"></i>
                </div>
                <div class="p-4">
                    <h3 class="font-semibold text-lg mb-2">Électronique</h3>
                    <p class="text-gray-600">Les derniers gadgets</p>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow">
                <div class="h-40 bg-yellow-100 flex items-center justify-center">
                    <i class="fas fa-home text-5xl text-yellow-600"></i>
                </div>
                <div class="p-4">
                    <h3 class="font-semibold text-lg mb-2">Maison</h3>
                    <p class="text-gray-600">Pour votre intérieur</p>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow">
                <div class="h-40 bg-green-100 flex items-center justify-center">
                    <i class="fas fa-dumbbell text-5xl text-green-600"></i>
                </div>
                <div class="p-4">
                    <h3 class="font-semibold text-lg mb-2">Sport</h3>
                    <p class="text-gray-600">Équipements de qualité</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Produits vedettes -->
    <div class="bg-gray-100 py-12">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12">Produits Vedettes</h2>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Produit 1 -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card transition duration-300">
                    <div class="relative">
                        <img src="https://via.placeholder.com/300x200" alt="Produit 1" class="w-full h-48 object-cover">
                        <div class="absolute top-2 right-2 bg-red-500 text-white text-xs font-bold px-2 py-1 rounded-full">
                            -20%
                        </div>
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="font-semibold text-lg">Smartphone Premium</h3>
                            <div class="flex items-center">
                                <i class="fas fa-star text-yellow-400"></i>
                                <span class="ml-1 text-gray-600">4.8</span>
                            </div>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Le dernier modèle avec caméra haute résolution</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-gray-400 line-through text-sm">€899.99</span>
                                <span class="text-purple-600 font-bold ml-2">€719.99</span>
                            </div>
                            <button class="bg-purple-100 text-purple-600 p-2 rounded-full hover:bg-purple-200">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Produit 2 -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card transition duration-300">
                    <img src="https://via.placeholder.com/300x200" alt="Produit 2" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="font-semibold text-lg">Casque Audio</h3>
                            <div class="flex items-center">
                                <i class="fas fa-star text-yellow-400"></i>
                                <span class="ml-1 text-gray-600">4.5</span>
                            </div>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Réduction de bruit exceptionnelle</p>
                        <div class="flex justify-between items-center">
                            <span class="text-purple-600 font-bold">€149.99</span>
                            <button class="bg-purple-100 text-purple-600 p-2 rounded-full hover:bg-purple-200">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Produit 3 -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card transition duration-300">
                    <img src="https://via.placeholder.com/300x200" alt="Produit 3" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="font-semibold text-lg">Montre Connectée</h3>
                            <div class="flex items-center">
                                <i class="fas fa-star text-yellow-400"></i>
                                <span class="ml-1 text-gray-600">4.7</span>
                            </div>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Suivi santé et notifications</p>
                        <div class="flex justify-between items-center">
                            <span class="text-purple-600 font-bold">€199.99</span>
                            <button class="bg-purple-100 text-purple-600 p-2 rounded-full hover:bg-purple-200">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Produit 4 -->
                <div class="bg-white rounded-lg overflow-hidden shadow-md product-card transition duration-300">
                    <div class="relative">
                        <img src="https://via.placeholder.com/300x200" alt="Produit 4" class="w-full h-48 object-cover">
                        <div class="absolute top-2 right-2 bg-green-500 text-white text-xs font-bold px-2 py-1 rounded-full">
                            Nouveau
                        </div>
                    </div>
                    <div class="p-4">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="font-semibold text-lg">Sac à Dos</h3>
                            <div class="flex items-center">
                                <i class="fas fa-star text-yellow-400"></i>
                                <span class="ml-1 text-gray-600">4.9</span>
                            </div>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Design ergonomique et résistant</p>
                        <div class="flex justify-between items-center">
                            <span class="text-purple-600 font-bold">€79.99</span>
                            <button class="bg-purple-100 text-purple-600 p-2 rounded-full hover:bg-purple-200">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-10">
                <button class="gradient-btn btn-hover text-white font-bold py-3 px-8 rounded-full">
                    Voir tous les produits
                </button>
            </div>
        </div>
    </div>

    <!-- Avantages -->
    <div class="container mx-auto px-4 py-12">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="flex flex-col items-center text-center">
                <div class="bg-purple-100 p-4 rounded-full mb-4">
                    <i class="fas fa-truck text-3xl text-purple-600"></i>
                </div>
                <h3 class="font-bold text-xl mb-2">Livraison Rapide</h3>
                <p class="text-gray-600">Livraison en 24-48h partout au senegal</p>
            </div>
            
            <div class="flex flex-col items-center text-center">
                <div class="bg-blue-100 p-4 rounded-full mb-4">
                    <i class="fas fa-shield-alt text-3xl text-blue-600"></i>
                </div>
                <h3 class="font-bold text-xl mb-2">Paiement Sécurisé</h3>
                <p class="text-gray-600">Transactions 100% sécurisées</p>
            </div>
            
            <div class="flex flex-col items-center text-center">
                <div class="bg-green-100 p-4 rounded-full mb-4">
                    <i class="fas fa-undo text-3xl text-green-600"></i>
                </div>
                <h3 class="font-bold text-xl mb-2">Retour Facile</h3>
                <p class="text-gray-600">30 jours pour changer d'avis</p>
            </div>
        </div>
    </div>

    <!-- Newsletter -->
    <div class="bg-purple-600 text-white py-12">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-4">Abonnez-vous à notre newsletter</h2>
            <p class="mb-6 max-w-2xl mx-auto">Recevez nos offres exclusives et soyez le premier informé de nos nouveautés.</p>
            <div class="flex flex-col sm:flex-row max-w-md mx-auto sm:max-w-xl">
                <input type="email" placeholder="Votre email" class="flex-grow px-4 py-3 rounded-l sm:rounded-l-full sm:rounded-r-none mb-2 sm:mb-0 text-gray-800 focus:outline-none">
                <button class="bg-pink-500 hover:bg-pink-600 px-6 py-3 rounded-r sm:rounded-r-full sm:rounded-l-none font-medium transition">
                    S'abonner
                </button>
            </div>
        </div>
    </div>

    <!-- Pied de page -->
    <footer class="bg-gray-800 text-white pt-12 pb-6">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <h3 class="text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-shopping-bag mr-2"></i> A.dieng shop
                    </h3>
                    <p class="text-gray-400">Votre boutique en ligne préférée pour des produits de qualité à des prix imbattables.</p>
                    <div class="flex space-x-4 mt-4">
                        <a href="#" class="text-gray-400 hover:text-white"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-gray-400 hover:text-white"><i class="fab fa-pinterest"></i></a>
                    </div>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4">Liens rapides</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Accueil</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Boutique</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Nouveautés</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Promotions</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4">Catégories</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Vêtements</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Électronique</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Maison</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Sport</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Beauté</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4">Contact</h4>
                    <ul class="space-y-2 text-gray-400">
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt mt-1 mr-2"></i>
                            <span>123 Rue TAKHIKAO THIES</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone-alt mr-2"></i>
                            <span>782780836</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-2"></i>
                            <span>mouhameddieng330@gmail.com</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-700 pt-6 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">© 2025  mad shop. Tous droits réservés.</p>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white text-sm">Mentions légales</a>
                    <a href="#" class="text-gray-400 hover:text-white text-sm">Politique de confidentialité</a>
                    <a href="#" class="text-gray-400 hover:text-white text-sm">CGV</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Menu mobile
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // Animation pour le compteur de panier
        const cartCount = document.querySelector('.fa-shopping-cart').nextElementSibling;
        if (cartCount) {
            setInterval(() => {
                cartCount.classList.toggle('animate-ping');
            }, 3000);
        }

        // Simulation d'ajout au panier
        const addToCartButtons = document.querySelectorAll('.fa-shopping-cart');
        addToCartButtons.forEach(button => {
            button.addEventListener('click', function(e) {
                e.preventDefault();
                const currentCount = parseInt(cartCount.textContent);
                cartCount.textContent = currentCount + 1;
                
                // Animation de confirmation
                cartCount.classList.add('animate-bounce');
                setTimeout(() => {
                    cartCount.classList.remove('animate-bounce');
                }, 1000);
            });
        });
    </script>
</body>
</html>
