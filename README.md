
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Strapphone - Kelompok 8 (12 H)</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts: Fredoka (Friendly/Rounded) & Poppins -->
    <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@300;400;500;600&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

    <!-- Custom Config for Pastel Colors -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        'sans': ['Poppins', 'sans-serif'],
                        'display': ['Fredoka', 'sans-serif'],
                    },
                    colors: {
                        'pastel-red': '#FF8FAB', 
                        'pastel-red-dark': '#FB6F92',
                        'pastel-cream': '#FFF0F3',
                        'pastel-bg': '#FFC2D1',
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #FFF0F3;
        }
        .glass-effect {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        .hero-pattern {
            background-image: radial-gradient(#FF8FAB 1px, transparent 1px);
            background-size: 20px 20px;
        }
        .scroll-smooth {
            scroll-behavior: smooth;
        }
        /* Hide scrollbar for clean look */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #FFF0F3; 
        }
        ::-webkit-scrollbar-thumb {
            background: #FF8FAB; 
            border-radius: 4px;
        }
    </style>
</head>
<body class="text-gray-700 font-sans scroll-smooth relative">

    <!-- Navbar -->
    <nav class="fixed w-full z-50 glass-effect shadow-sm transition-all duration-300">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <div class="bg-pastel-red text-white p-2 rounded-full">
                    <i class="fa-solid fa-mobile-screen-button"></i>
                </div>
                <div>
                    <h1 class="font-display text-2xl font-bold text-pastel-red-dark leading-none">strapphone</h1>
                    <span class="text-xs text-gray-500 font-medium tracking-wider">12 H &bull; Kelompok 8</span>
                </div>
            </div>
            
            <div class="flex items-center gap-6">
                <div class="hidden md:flex gap-6 font-medium text-gray-600">
                    <a href="#home" class="hover:text-pastel-red-dark transition">Beranda</a>
                    <a href="#about" class="hover:text-pastel-red-dark transition">Tentang Kami</a>
                    <a href="#products" class="hover:text-pastel-red-dark transition">Produk</a>
                </div>
                
                <!-- Cart Icon -->
                <button onclick="toggleCart()" class="relative p-2 text-pastel-red-dark hover:scale-110 transition">
                    <i class="fa-solid fa-cart-shopping text-2xl"></i>
                    <span id="cart-count" class="absolute -top-1 -right-1 bg-red-500 text-white text-xs font-bold w-5 h-5 flex items-center justify-center rounded-full animate-bounce">0</span>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="pt-32 pb-20 px-4 hero-pattern min-h-screen flex items-center">
        <div class="container mx-auto flex flex-col-reverse md:flex-row items-center gap-10">
            <!-- Text Content -->
            <div class="flex-1 text-center md:text-left space-y-6">
                <span class="inline-block px-4 py-1 bg-white text-pastel-red-dark rounded-full text-sm font-bold shadow-sm mb-2">
                    ✨ Trendy & Affordable
                </span>
                <h2 class="font-display text-4xl md:text-6xl font-bold text-gray-800 leading-tight">
                    Hiasi Ponselmu dengan <span class="text-pastel-red-dark">Gaya Kekinian!</span>
                </h2>
                <p class="text-lg text-gray-600">
                    Koleksi strapphone estetik dengan harga mulai <strong>Rp 15.000</strong>. Cocok untuk mempercantik harimu!
                </p>
                
                <!-- Team Card -->
                <div class="bg-white p-4 rounded-xl shadow-md border-l-4 border-pastel-red inline-block text-left w-full md:w-auto">
                    <h3 class="font-bold text-gray-700 mb-2 border-b pb-1">Tim Kelompok 8:</h3>
                    <ul class="text-sm space-y-1 text-gray-600">
                        <li><i class="fa-solid fa-bullhorn text-pastel-red w-6"></i> <strong>Kiramil Bararah</strong> [Marketing]</li>
                        <li><i class="fa-solid fa-truck-fast text-pastel-red w-6"></i> <strong>Muhammad Bagus</strong> [Delivery]</li>
                        <li><i class="fa-solid fa-coins text-pastel-red w-6"></i> <strong>Rusty Meliala Tanjung</strong> [Moneter]</li>
                    </ul>
                </div>

                <div class="pt-4">
                    <a href="#products" class="bg-pastel-red-dark hover:bg-red-500 text-white font-bold py-3 px-8 rounded-full shadow-lg transition transform hover:-translate-y-1 inline-block">
                        Belanja Sekarang <i class="fa-solid fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </div>
            
            <!-- Hero Image -->
            <div class="flex-1 relative">
                <div class="relative z-10 w-full max-w-md mx-auto aspect-square bg-white rounded-3xl overflow-hidden shadow-2xl p-2 rotate-3 hover:rotate-0 transition duration-500">
                    <img src="https://images.unsplash.com/photo-1623998021446-45cd9b269056?q=80&w=1000&auto=format&fit=crop" alt="Strapphone Aesthetic" class="w-full h-full object-cover rounded-2xl">
                    <div class="absolute bottom-4 right-4 bg-white/90 backdrop-blur px-4 py-2 rounded-lg shadow font-bold text-pastel-red-dark">
                        Rp 15.000+
                    </div>
                </div>
                <!-- Decorative blobs -->
                <div class="absolute top-0 right-0 w-64 h-64 bg-pastel-bg rounded-full mix-blend-multiply filter blur-3xl opacity-70 animate-pulse"></div>
                <div class="absolute bottom-0 left-0 w-64 h-64 bg-yellow-200 rounded-full mix-blend-multiply filter blur-3xl opacity-70"></div>
            </div>
        </div>
    </section>

    <!-- About Us -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-4 text-center max-w-3xl">
            <h3 class="font-display text-3xl font-bold text-pastel-red-dark mb-6">Tentang Kami</h3>
            <p class="text-gray-600 leading-relaxed mb-8">
                Kami adalah <strong>Kelompok 8</strong> dari kelas 12 H, yang berdedikasi menyediakan aksesoris ponsel lucu dan terjangkau untuk semua kalangan, mulai dari anak sekolah hingga dewasa. Strapphone kami dibuat dengan cinta, desain yang penuh warna, dan kualitas yang tahan lama. Kami percaya bahwa aksesoris kecil bisa membawa kebahagiaan besar!
            </p>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="p-4 bg-pastel-cream rounded-xl">
                    <i class="fa-solid fa-heart text-3xl text-pastel-red mb-3"></i>
                    <h4 class="font-bold">Handmade</h4>
                    <p class="text-sm">Dibuat dengan teliti.</p>
                </div>
                <div class="p-4 bg-pastel-cream rounded-xl">
                    <i class="fa-solid fa-wallet text-3xl text-pastel-red mb-3"></i>
                    <h4 class="font-bold">Terjangkau</h4>
                    <p class="text-sm">Mulai Rp 15.000 saja.</p>
                </div>
                <div class="p-4 bg-pastel-cream rounded-xl">
                    <i class="fa-solid fa-star text-3xl text-pastel-red mb-3"></i>
                    <h4 class="font-bold">Kekinian</h4>
                    <p class="text-sm">Model selalu update.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="py-20 bg-pastel-cream/50">
        <div class="container mx-auto px-4">
            <h3 class="font-display text-3xl font-bold text-center text-pastel-red-dark mb-2">Koleksi Terlaris</h3>
            <p class="text-center text-gray-500 mb-12">Pilih favoritmu dan masukkan ke keranjang!</p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                
                <!-- Product 1 -->
                <div class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition transform hover:-translate-y-2 group">
                    <div class="relative h-64 bg-gray-100 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1611591437281-460bfbe1220a?q=80&w=800&auto=format&fit=crop" alt="Pastel Beads Strap" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                        <span class="absolute top-3 left-3 bg-yellow-400 text-white text-xs font-bold px-3 py-1 rounded-full">Best Seller</span>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h4 class="font-display text-xl font-bold text-gray-800">Pastel Candy Beads</h4>
                            <span class="font-bold text-pastel-red-dark text-lg">Rp 15.000</span>
                        </div>
                        <p class="text-gray-500 text-sm mb-4">Campuran manik-manik warna pastel yang manis seperti permen. Cocok untuk outfit cerah.</p>
                        <button onclick="addToCart(1, 'Pastel Candy Beads', 15000)" class="w-full bg-pastel-red text-white font-bold py-2 rounded-lg hover:bg-pastel-red-dark transition flex justify-center items-center gap-2">
                            <i class="fa-solid fa-plus"></i> Tambah Keranjang
                        </button>
                    </div>
                </div>

                <!-- Product 2 -->
                <div class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition transform hover:-translate-y-2 group">
                    <div class="relative h-64 bg-gray-100 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1616406432452-07bc5946552b?q=80&w=800&auto=format&fit=crop" alt="Crystal Elegance" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h4 class="font-display text-xl font-bold text-gray-800">Crystal Elegance</h4>
                            <span class="font-bold text-pastel-red-dark text-lg">Rp 15.000</span>
                        </div>
                        <p class="text-gray-500 text-sm mb-4">Kombinasi kristal bening dan mutiara imitasi. Memberikan kesan mewah dan elegan.</p>
                        <button onclick="addToCart(2, 'Crystal Elegance', 15000)" class="w-full bg-pastel-red text-white font-bold py-2 rounded-lg hover:bg-pastel-red-dark transition flex justify-center items-center gap-2">
                            <i class="fa-solid fa-plus"></i> Tambah Keranjang
                        </button>
                    </div>
                </div>

                <!-- Product 3 -->
                <div class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition transform hover:-translate-y-2 group">
                    <div class="relative h-64 bg-gray-100 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1596464716127-f2a82984de30?q=80&w=800&auto=format&fit=crop" alt="Gummy Bear Custom" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                        <span class="absolute top-3 left-3 bg-green-400 text-white text-xs font-bold px-3 py-1 rounded-full">New Arrival</span>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h4 class="font-display text-xl font-bold text-gray-800">Gummy Bear Pop</h4>
                            <span class="font-bold text-pastel-red-dark text-lg">Rp 15.000</span>
                        </div>
                        <p class="text-gray-500 text-sm mb-4">Strap lucu dengan bandul beruang gummy yang menggemaskan. Warna-warni ceria.</p>
                        <button onclick="addToCart(3, 'Gummy Bear Pop', 15000)" class="w-full bg-pastel-red text-white font-bold py-2 rounded-lg hover:bg-pastel-red-dark transition flex justify-center items-center gap-2">
                            <i class="fa-solid fa-plus"></i> Tambah Keranjang
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-pastel-red-dark text-white py-8">
        <div class="container mx-auto px-4 text-center">
            <h2 class="font-display text-2xl font-bold mb-2">strapphone</h2>
            <p class="text-sm opacity-90 mb-4">Kelompok 8 - 12 H &copy; 2025</p>
            <div class="flex justify-center gap-4 mb-4">
                <a href="#" class="w-10 h-10 rounded-full bg-white text-pastel-red-dark flex items-center justify-center hover:bg-gray-100 transition"><i class="fa-brands fa-whatsapp"></i></a>
                <a href="#" class="w-10 h-10 rounded-full bg-white text-pastel-red-dark flex items-center justify-center hover:bg-gray-100 transition"><i class="fa-brands fa-instagram"></i></a>
            </div>
            <p class="text-xs opacity-75">Dibuat dengan ❤️ di Indonesia</p>
        </div>
    </footer>

    <!-- CART MODAL & CHECKOUT FORM -->
    <div id="cart-modal" class="fixed inset-0 z-[60] hidden">
        <!-- Backdrop -->
        <div class="absolute inset-0 bg-black/40 backdrop-blur-sm" onclick="toggleCart()"></div>
        
        <!-- Modal Content -->
        <div class="absolute right-0 top-0 h-full w-full md:w-[450px] bg-white shadow-2xl flex flex-col transform transition-transform duration-300 translate-x-full" id="cart-panel">
            <!-- Header -->
            <div class="p-5 bg-pastel-cream border-b flex justify-between items-center">
                <h3 class="font-display text-xl font-bold text-gray-800"><i class="fa-solid fa-basket-shopping mr-2"></i> Keranjang Belanja</h3>
                <button onclick="toggleCart()" class="text-gray-500 hover:text-red-500">
                    <i class="fa-solid fa-xmark text-2xl"></i>
                </button>
            </div>

            <!-- Bulk Delete Action Bar (Hidden by default) -->
            <div id="bulk-action-bar" class="hidden bg-red-50 px-5 py-2 border-b border-red-100 flex justify-between items-center animate-pulse">
                <span class="text-sm text-red-600 font-bold" id="selected-count-text">0 item terpilih</span>
                <button onclick="deleteSelected()" class="text-xs bg-red-500 text-white px-3 py-1.5 rounded hover:bg-red-600 transition font-bold shadow-sm">
                    <i class="fa-solid fa-trash-can mr-1"></i> Hapus Pilihan
                </button>
            </div>

            <!-- Cart Items (Scrollable) -->
            <div id="cart-items-container" class="flex-1 overflow-y-auto p-5 space-y-4">
                <!-- Items will be injected here by JS -->
                <div class="text-center text-gray-400 mt-10">
                    <i class="fa-regular fa-face-sad-tear text-4xl mb-2"></i>
                    <p>Keranjangmu masih kosong.</p>
                </div>
            </div>

            <!-- Total & Checkout Form -->
            <div class="p-5 bg-gray-50 border-t">
                <div class="flex justify-between items-center mb-4">
                    <span class="font-bold text-gray-600">Total Pembayaran:</span>
                    <span id="cart-total" class="font-display text-2xl font-bold text-pastel-red-dark">Rp 0</span>
                </div>

                <form id="checkout-form" onsubmit="event.preventDefault(); processOrder();">
                    <div class="space-y-3 mb-4">
                        <input type="text" id="cust-name" placeholder="Nama Lengkap" required class="w-full px-4 py-2 rounded-lg border focus:outline-none focus:ring-2 focus:ring-pastel-red">
                        <textarea id="cust-address" placeholder="Alamat Lengkap Pengiriman" required rows="2" class="w-full px-4 py-2 rounded-lg border focus:outline-none focus:ring-2 focus:ring-pastel-red"></textarea>
                        <input type="tel" id="cust-phone" placeholder="Nomor WhatsApp" required class="w-full px-4 py-2 rounded-lg border focus:outline-none focus:ring-2 focus:ring-pastel-red">
                    </div>

                    <!-- Payment Options -->
                    <div class="mb-4">
                        <p class="text-sm font-bold text-gray-600 mb-2">Metode Pembayaran:</p>
                        <a href="https://link.dana.id/minta?full_url=https://qr.dana.id/v1/281012012025052927934766" target="_blank" class="block w-full text-center bg-blue-500 text-white font-bold py-2 rounded-lg mb-2 hover:bg-blue-600 transition items-center gap-2">
                            <i class="fa-solid fa-wallet"></i> Bayar via DANA
                        </a>
                        <p class="text-xs text-gray-500 text-center">Atau transfer manual ke DANA: <strong>0881012765828</strong></p>
                    </div>

                    <button type="submit" class="w-full bg-green-500 text-white font-bold py-3 rounded-lg hover:bg-green-600 transition shadow-lg flex justify-center items-center gap-2">
                        <i class="fa-brands fa-whatsapp text-xl"></i> Pesan via WhatsApp
                    </button>
                </form>
            </div>
        </div>
    </div>

    <!-- JavaScript Logic -->
    <script>
        // State
        let cart = [];
        const waNumber = "62881012765828"; // Formatted for API
        
        // DOM Elements
        const cartModal = document.getElementById('cart-modal');
        const cartPanel = document.getElementById('cart-panel');
        const cartCount = document.getElementById('cart-count');
        const cartContainer = document.getElementById('cart-items-container');
        const cartTotalEl = document.getElementById('cart-total');
        const bulkActionBar = document.getElementById('bulk-action-bar');
        const selectedCountText = document.getElementById('selected-count-text');

        // Functions
        function toggleCart() {
            const isHidden = cartModal.classList.contains('hidden');
            if (isHidden) {
                cartModal.classList.remove('hidden');
                // Small delay for animation
                setTimeout(() => {
                    cartPanel.classList.remove('translate-x-full');
                }, 10);
            } else {
                cartPanel.classList.add('translate-x-full');
                setTimeout(() => {
                    cartModal.classList.add('hidden');
                }, 300);
            }
        }

        function addToCart(id, name, price) {
            const existingItem = cart.find(item => item.id === id);
            
            if (existingItem) {
                existingItem.qty++;
            } else {
                // Initialize new item with selected: false
                cart.push({ id, name, price, qty: 1, selected: false });
            }
            
            updateCartUI();
            
            // Show feedback (could be toast, simple alert for now)
            toggleCart();
        }

        function removeFromCart(id) {
            cart = cart.filter(item => item.id !== id);
            updateCartUI();
        }

        // Toggle selection for a single item
        function toggleSelect(id) {
            const item = cart.find(item => item.id === id);
            if (item) {
                item.selected = !item.selected;
                updateCartUI();
            }
        }

        // Delete all selected items
        function deleteSelected() {
            if(confirm('Yakin ingin menghapus item yang dipilih?')) {
                cart = cart.filter(item => !item.selected);
                updateCartUI();
            }
        }

        function updateQty(id, change) {
            const item = cart.find(item => item.id === id);
            if (item) {
                item.qty += change;
                if (item.qty <= 0) {
                    removeFromCart(id);
                } else {
                    updateCartUI();
                }
            }
        }

        function formatRupiah(number) {
            return new Intl.NumberFormat('id-ID', { style: 'currency', currency: 'IDR', minimumFractionDigits: 0 }).format(number);
        }

        function updateCartUI() {
            // Update Badge
            const totalQty = cart.reduce((sum, item) => sum + item.qty, 0);
            cartCount.innerText = totalQty;
            cartCount.classList.remove('hidden');
            if(totalQty === 0) cartCount.classList.add('hidden');

            // Check if any items are selected
            const selectedItems = cart.filter(item => item.selected);
            if (selectedItems.length > 0) {
                bulkActionBar.classList.remove('hidden');
                bulkActionBar.classList.add('flex');
                selectedCountText.innerText = `${selectedItems.length} item dipilih`;
            } else {
                bulkActionBar.classList.add('hidden');
                bulkActionBar.classList.remove('flex');
            }

            // Update List
            cartContainer.innerHTML = '';
            let total = 0;

            if (cart.length === 0) {
                cartContainer.innerHTML = `
                    <div class="text-center text-gray-400 mt-10">
                        <i class="fa-solid fa-basket-shopping text-4xl mb-2 opacity-30"></i>
                        <p>Keranjangmu masih kosong.</p>
                        <button onclick="toggleCart()" class="text-pastel-red-dark underline text-sm mt-2">Belanja dulu yuk!</button>
                    </div>
                `;
                bulkActionBar.classList.add('hidden'); // Ensure hidden if empty
            } else {
                cart.forEach(item => {
                    const itemTotal = item.price * item.qty;
                    total += itemTotal;
                    
                    cartContainer.innerHTML += `
                        <div class="flex items-center gap-3 bg-white p-3 rounded-lg shadow-sm border ${item.selected ? 'border-red-300 bg-red-50' : 'border-gray-100'} transition-colors">
                            <!-- Checkbox for Selection -->
                            <input type="checkbox" onchange="toggleSelect(${item.id})" ${item.selected ? 'checked' : ''} class="w-5 h-5 text-pastel-red-dark focus:ring-pastel-red rounded border-gray-300 cursor-pointer">
                            
                            <div class="flex-1 flex justify-between items-center">
                                <div>
                                    <h4 class="font-bold text-gray-700 text-sm">${item.name}</h4>
                                    <p class="text-pastel-red-dark text-xs font-bold">${formatRupiah(item.price)}</p>
                                </div>
                                <div class="flex items-center gap-3">
                                    <button onclick="updateQty(${item.id}, -1)" class="w-6 h-6 bg-gray-200 rounded text-gray-600 hover:bg-gray-300">-</button>
                                    <span class="text-sm font-bold w-4 text-center">${item.qty}</span>
                                    <button onclick="updateQty(${item.id}, 1)" class="w-6 h-6 bg-pastel-red text-white rounded hover:bg-pastel-red-dark">+</button>
                                    
                                    <!-- Individual Delete (Optional now, but good to keep) -->
                                    <button onclick="removeFromCart(${item.id})" class="ml-2 text-gray-300 hover:text-red-500"><i class="fa-solid fa-trash-can"></i></button>
                                </div>
                            </div>
                        </div>
                    `;
                });
            }

            cartTotalEl.innerText = formatRupiah(total);
        }

        function processOrder() {
            if (cart.length === 0) {
                alert("Keranjang masih kosong!");
                return;
            }

            const name = document.getElementById('cust-name').value;
            const address = document.getElementById('cust-address').value;
            const phone = document.getElementById('cust-phone').value;

            if (!name || !address || !phone) {
                alert("Harap lengkapi formulir pemesanan.");
                return;
            }

            // Calculate Total
            const total = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);

            // Construct Message
            let message = `Halo Kak, saya mau pesan Strapphone di *Kelompok 8* dong!%0A%0A`;
            message += `*Data Pemesan:*%0A`;
            message += `Nama: ${name}%0A`;
            message += `No. HP: ${phone}%0A`;
            message += `Alamat: ${address}%0A%0A`;
            message += `*Detail Pesanan:*%0A`;
            
            cart.forEach(item => {
                message += `- ${item.name} (${item.qty}x) : ${formatRupiah(item.price * item.qty)}%0A`;
            });

            message += `%0A*Total Bayar: ${formatRupiah(total)}*%0A`;
            message += `---------------------------%0A`;
            message += `Mohon konfirmasi pesanan saya. Saya akan/sudah melakukan pembayaran ke DANA (0881012765828). Terima kasih!`;

            // Redirect to WhatsApp
            const waLink = `https://wa.me/${waNumber}?text=${message}`;
            window.open(waLink, '_blank');
        }
    </script>
</body>
</html>
