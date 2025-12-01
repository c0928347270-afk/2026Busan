# 2026Busan[index.html](https://github.com/user-attachments/files/23845781/index.html)
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Busan Trip 💖</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
    <script src="https://unpkg.com/@phosphor-icons/web"></script>
    <link href="https://fonts.googleapis.com/css2?family=Kiwi+Maru:wght@300;500&family=Nunito:wght@400;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        macaron: {
                            pink: '#FFC8DD',
                            blue: '#A2D2FF',
                            yellow: '#FDFD96',
                            green: '#BDE0FE', // Using soft blue-ish green
                            mint: '#C1E1C1',
                            purple: '#CDB4DB',
                            dark: '#555555'
                        }
                    },
                    fontFamily: {
                        cute: ['"Kiwi Maru"', '"Nunito"', 'sans-serif']
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Kiwi Maru', 'Nunito', sans-serif;
            background-color: #FFF9FA; /* Very light pink bg */
            color: #555;
            -webkit-tap-highlight-color: transparent;
        }
        
        /* Macaron Card Style */
        .cute-card {
            background: #FFFFFF;
            border-radius: 24px;
            box-shadow: 4px 4px 0px rgba(0, 0, 0, 0.05);
            border: 2px solid #FFF0F5;
        }

        .cute-shadow {
            box-shadow: 3px 3px 0px rgba(0,0,0,0.1);
        }

        /* Hide Scrollbar */
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }

        /* Custom Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-5px); }
            100% { transform: translateY(0px); }
        }
        .animate-float { animation: float 3s ease-in-out infinite; }

        .tab-active {
            color: #FF6B6B;
            transform: scale(1.1);
        }
    </style>
</head>
<body class="h-screen flex flex-col overflow-hidden">

<div id="app" class="flex flex-col h-full">

    <header class="pt-10 pb-4 px-6 bg-macaron-pink rounded-b-[30px] shadow-sm z-10 flex justify-between items-center relative overflow-hidden">
        <div class="absolute -top-5 -left-5 w-20 h-20 bg-white opacity-20 rounded-full"></div>
        <div class="absolute top-10 right-10 w-10 h-10 bg-white opacity-20 rounded-full"></div>

        <div class="z-10">
            <h1 class="text-2xl font-bold text-gray-800 tracking-wide flex items-center gap-2">
                釜山行 <span class="text-xl">✈️</span>
            </h1>
            <p class="text-sm text-gray-700 font-medium mt-1 opacity-80">Jan 21 - Jan 25, 2025</p>
        </div>
        <button @click="resetData" class="z-10 bg-white/50 backdrop-blur text-xs font-bold text-gray-600 px-3 py-1.5 rounded-full border border-white hover:bg-white transition">重置</button>
    </header>

    <main class="flex-1 overflow-y-auto p-5 pb-28 space-y-5">
        
        <div v-if="currentTab === 'itinerary'" class="space-y-4">
            <div class="flex space-x-3 overflow-x-auto pb-2 no-scrollbar px-1">
                <button v-for="i in 5" :key="i" 
                    @click="activeDay = i"
                    :class="activeDay === i ? 'bg-macaron-blue text-white ring-2 ring-macaron-blue ring-offset-2' : 'bg-white text-gray-400 border border-gray-100'"
                    class="flex-shrink-0 w-14 h-14 rounded-2xl flex flex-col items-center justify-center shadow-sm transition-all duration-300">
                    <span class="text-[10px] uppercase font-bold">Day</span>
                    <span class="text-lg font-black leading-none">{{ i }}</span>
                </button>
            </div>

            <div class="space-y-4">
                <div v-if="filteredItinerary.length === 0" class="text-center py-12">
                    <div class="bg-white p-6 rounded-full inline-block mb-3 cute-shadow animate-float">
                        <span class="text-4xl">🏝️</span>
                    </div>
                    <p class="text-gray-400 font-medium">今天想去哪裡玩呢？</p>
                </div>

                <div v-for="item in filteredItinerary" :key="item.id" 
                    class="cute-card p-4 flex gap-4 transform transition-all hover:scale-[1.01]"
                    :class="{'bg-blue-50 border-blue-100': item.isFlight}">
                    
                    <div class="flex flex-col items-center">
                        <div class="bg-macaron-yellow px-2 py-1 rounded-lg text-xs font-bold text-gray-700 shadow-sm border border-yellow-100 whitespace-nowrap">
                            {{ item.time }}
                        </div>
                        <div class="h-full w-0.5 bg-gray-200 my-2 border-l-2 border-dotted"></div>
                    </div>

                    <div class="flex-1 pb-1">
                        <div class="flex justify-between items-start">
                            <h3 class="font-bold text-lg text-gray-800 leading-tight">{{ item.title }}</h3>
                            <button v-if="!item.isFlight" @click="deleteItem(item.id)" class="text-gray-300 hover:text-red-400"><i class="ph ph-trash"></i></button>
                        </div>
                        
                        <p v-if="item.desc" class="text-xs text-gray-500 mt-1.5 bg-gray-50 p-2 rounded-lg inline-block">
                           {{ item.desc }}
                        </p>

                        <div v-if="item.isFlight" class="mt-2 flex items-center gap-2 text-xs font-bold text-blue-500">
                            <i class="ph ph-airplane-tilt text-lg"></i> 航班資訊
                        </div>
                        <a v-else :href="getNaverMapLink(item.location)" target="_blank" 
                           class="mt-3 inline-flex items-center text-xs font-bold text-white bg-macaron-mint px-3 py-1.5 rounded-xl shadow-sm hover:bg-green-300 transition-colors text-gray-700">
                            <i class="ph ph-map-pin mr-1.5"></i> Naver Map
                        </a>
                    </div>
                </div>
            </div>
            
            <button @click="showAddModal = true" class="fixed bottom-24 right-5 bg-macaron-purple text-white w-14 h-14 rounded-2xl cute-shadow flex items-center justify-center text-2xl z-20 hover:scale-110 transition-transform border-2 border-white">
                <i class="ph ph-plus-circle font-bold"></i>
            </button>
        </div>

        <div v-if="currentTab === 'expense'" class="space-y-5">
            
            <div class="cute-card p-5 bg-gradient-to-br from-macaron-blue to-blue-200 border-none text-white relative overflow-hidden">
                <i class="ph ph-coins absolute -right-5 -bottom-5 text-9xl text-white opacity-20"></i>
                <p class="text-sm font-medium opacity-90">總支出 Total</p>
                <h2 class="text-4xl font-black mt-1 tracking-tight">₩{{ formatNumber(totalExpenseKRW) }}</h2>
                <p class="text-sm opacity-80 mt-1">≈ NT$ {{ formatNumber(totalExpenseTWD) }}</p>
                
                <div class="mt-4 pt-4 border-t border-white/30 flex justify-between items-end">
                    <div>
                        <p class="text-xs opacity-80 mb-1">分攤人數</p>
                        <div class="flex items-center bg-white/20 rounded-lg p-1 backdrop-blur-sm">
                            <button @click="peopleCount = Math.max(1, peopleCount - 1)" class="w-6 h-6 flex items-center justify-center">-</button>
                            <span class="w-6 text-center font-bold text-sm">{{ peopleCount }}</span>
                            <button @click="peopleCount++" class="w-6 h-6 flex items-center justify-center">+</button>
                        </div>
                    </div>
                    <div class="text-right">
                        <p class="text-xs opacity-80">每人應付 (TWD)</p>
                        <p class="text-xl font-bold">NT$ {{ formatNumber(Math.round(totalExpenseTWD / peopleCount)) }}</p>
                    </div>
                </div>
            </div>

            <div class="bg-white px-4 py-3 rounded-xl flex justify-between items-center shadow-sm border border-gray-100">
                <span class="text-xs font-bold text-gray-500">匯率設定 (1 TWD =)</span>
                <div class="flex items-center gap-2">
                    <span class="text-gray-400 text-xs">₩</span>
                    <input v-model.number="exchangeRate" type="number" class="w-16 bg-gray-100 rounded-lg px-2 py-1 text-center font-bold text-sm text-gray-700 outline-none focus:ring-2 focus:ring-macaron-blue">
                </div>
            </div>

            <div class="cute-card p-4 space-y-3">
                <h3 class="font-bold text-gray-700 flex items-center gap-2">
                    <i class="ph ph-receipt text-macaron-purple text-xl"></i> 記一筆
                </h3>
                <div class="flex gap-2">
                    <input v-model="newExpense.item" placeholder="品項 (e.g. 烤肉)" class="flex-1 bg-gray-50 px-4 py-3 rounded-xl text-sm outline-none border border-transparent focus:border-macaron-purple focus:bg-white transition-all">
                </div>
                <div class="flex gap-2 items-center">
                    <div class="relative flex-1">
                        <input v-model.number="newExpense.amount" type="number" placeholder="韓幣金額" class="w-full bg-gray-50 px-4 py-3 pl-8 rounded-xl text-sm outline-none border border-transparent focus:border-macaron-purple focus:bg-white transition-all">
                        <span class="absolute left-3 top-3.5 text-gray-400 text-xs">₩</span>
                    </div>
                    <div class="text-xs font-bold text-gray-400 whitespace-nowrap">
                        ≈ NT$ {{ formatNumber(Math.round((newExpense.amount || 0) / exchangeRate)) }}
                    </div>
                </div>
                <button @click="addExpense" class="w-full bg-macaron-purple text-white py-3 rounded-xl font-bold text-sm shadow-md active:scale-95 transition-transform">
                    加入清單
                </button>
            </div>

            <div class="space-y-3">
                <div v-for="(exp, index) in expenses" :key="index" class="bg-white p-4 rounded-xl shadow-sm border border-gray-50 flex justify-between items-center">
                    <div>
                        <p class="font-bold text-gray-800">{{ exp.item }}</p>
                        <p class="text-[10px] text-gray-400">{{ exp.date }}</p>
                    </div>
                    <div class="text-right">
                        <p class="font-bold text-gray-700">₩{{ formatNumber(exp.amount) }}</p>
                        <p class="text-xs text-macaron-purple font-medium">NT$ {{ formatNumber(Math.round(exp.amount / exchangeRate)) }}</p>
                    </div>
                    <button @click="removeExpense(index)" class="ml-2 text-gray-300 hover:text-red-400"><i class="ph ph-x-circle text-lg"></i></button>
                </div>
            </div>
        </div>

        <div v-if="currentTab === 'weather'" class="space-y-4">
            <a href="https://www.google.com/search?q=釜山天氣" target="_blank" class="cute-card p-3 flex items-center justify-center gap-2 text-sm font-bold text-blue-500 bg-blue-50 border-blue-100 hover:bg-blue-100 transition">
                <i class="ph ph-google-logo text-lg"></i> Google 天氣
            </a>

            <div class="cute-card p-6 text-center bg-gradient-to-b from-sky-100 to-white border-blue-50">
                <h2 class="text-lg font-bold text-gray-600 uppercase tracking-widest mb-2">Busan</h2>
                <div v-if="weatherLoading" class="py-8 text-gray-400 text-sm animate-pulse">☁️ 雲朵運送中...</div>
                <div v-else>
                    <div class="text-6xl my-2">{{ getWeatherIcon(currentWeather.code) }}</div>
                    <p class="text-5xl font-black text-gray-800 tracking-tight">{{ currentWeather.temp }}°</p>
                    <div class="mt-4 flex justify-center gap-4 text-xs font-bold text-gray-500">
                        <span class="bg-white px-3 py-1 rounded-full shadow-sm">降雨 {{ currentWeather.rain }}%</span>
                        <span class="bg-white px-3 py-1 rounded-full shadow-sm">{{ currentWeather.desc }}</span>
                    </div>
                </div>
            </div>
            
            <div class="bg-white rounded-2xl p-4 shadow-sm border border-gray-100">
                <h3 class="font-bold mb-4 text-xs text-gray-400 uppercase ml-1">接下來 5 天</h3>
                <div v-if="!weatherLoading">
                    <div v-for="(day, index) in forecast" :key="index" class="flex items-center justify-between py-3 border-b border-gray-50 last:border-0">
                        <span class="w-20 font-bold text-gray-600 text-sm">{{ day.dateStr }}</span>
                        <div class="flex-1 text-center text-xl">{{ getWeatherIcon(day.code) }}</div>
                        <div class="w-24 text-right flex gap-2 justify-end text-sm">
                            <span class="text-gray-400">{{ day.min }}°</span>
                            <div class="w-10 bg-gray-100 rounded-full h-1.5 self-center mx-1 relative">
                                <div class="absolute inset-y-0 left-0 bg-macaron-blue rounded-full" style="width: 60%"></div>
                            </div>
                            <span class="font-bold text-gray-800">{{ day.max }}°</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div v-if="currentTab === 'map'" class="h-full flex flex-col">
            <div class="bg-white p-3 rounded-2xl shadow-sm mb-4 border border-green-50">
                <div class="flex gap-2">
                    <input v-model="mapQuery" @keyup.enter="searchNaver" type="text" placeholder="韓文/英文地點搜尋" class="flex-1 bg-gray-50 px-4 py-2.5 rounded-xl text-sm outline-none focus:bg-white focus:ring-2 focus:ring-green-100 transition">
                    <button @click="searchNaver" class="bg-[#03C75A] text-white px-4 py-2 rounded-xl text-sm font-bold shadow-md hover:bg-[#02b351] transition">
                        Naver
                    </button>
                </div>
            </div>
            
            <div class="flex-1 rounded-3xl overflow-hidden shadow-sm border-4 border-white relative bg-gray-100">
                <iframe width="100%" height="100%" style="border:0" loading="lazy" src="http://googleusercontent.com/maps.google.com/6"></iframe>
            </div>
        </div>

    </main>

    <nav class="fixed bottom-0 w-full pb-safe pt-2 px-6 flex justify-between items-center bg-white/90 backdrop-blur-md rounded-t-[30px] shadow-[0_-5px_20px_rgba(0,0,0,0.03)] z-30 border-t border-white">
        <button @click="currentTab = 'itinerary'" :class="currentTab === 'itinerary' ? 'text-macaron-pink tab-active' : 'text-gray-300'" class="flex flex-col items-center p-3 w-16 transition-all duration-300">
            <i class="ph ph-notebook text-2xl" :weight="currentTab === 'itinerary' ? 'fill' : 'regular'"></i>
            <span class="text-[10px] font-bold mt-1">行程</span>
        </button>
        <button @click="currentTab = 'map'" :class="currentTab === 'map' ? 'text-macaron-mint tab-active' : 'text-gray-300'" class="flex flex-col items-center p-3 w-16 transition-all duration-300">
            <i class="ph ph-map-trifold text-2xl" :weight="currentTab === 'map' ? 'fill' : 'regular'"></i>
            <span class="text-[10px] font-bold mt-1">地圖</span>
        </button>
        <button @click="currentTab = 'expense'" :class="currentTab === 'expense' ? 'text-macaron-blue tab-active' : 'text-gray-300'" class="flex flex-col items-center p-3 w-16 transition-all duration-300">
            <i class="ph ph-calculator text-2xl" :weight="currentTab === 'expense' ? 'fill' : 'regular'"></i>
            <span class="text-[10px] font-bold mt-1">分帳</span>
        </button>
        <button @click="currentTab = 'weather'" :class="currentTab === 'weather' ? 'text-macaron-yellow text-yellow-400 tab-active' : 'text-gray-300'" class="flex flex-col items-center p-3 w-16 transition-all duration-300">
            <i class="ph ph-sun-horizon text-2xl" :weight="currentTab === 'weather' ? 'fill' : 'regular'"></i>
            <span class="text-[10px] font-bold mt-1">天氣</span>
        </button>
    </nav>

    <div v-if="showAddModal" class="fixed inset-0 bg-gray-900/30 backdrop-blur-sm z-50 flex items-center justify-center p-4">
        <div class="bg-white w-full max-w-sm rounded-3xl p-6 shadow-2xl scale-100 transition-transform">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-gray-700">新增行程 ✨</h3>
                <button @click="showAddModal = false" class="bg-gray-100 w-8 h-8 rounded-full text-gray-500 hover:bg-gray-200"><i class="ph ph-x"></i></button>
            </div>
            <div class="space-y-4">
                <div>
                    <label class="text-xs text-macaron-purple font-bold ml-1 mb-1 block">時間</label>
                    <input v-model="newItem.time" type="time" class="w-full bg-gray-50 p-3 rounded-xl outline-none border focus:border-macaron-purple">
                </div>
                <div>
                    <label class="text-xs text-macaron-purple font-bold ml-1 mb-1 block">行程名稱</label>
                    <input v-model="newItem.title" type="text" placeholder="去哪裡玩？" class="w-full bg-gray-50 p-3 rounded-xl outline-none border focus:border-macaron-purple">
                </div>
                <div>
                    <label class="text-xs text-macaron-purple font-bold ml-1 mb-1 block">地點 (Naver Map 搜尋用)</label>
                    <input v-model="newItem.location" type="text" placeholder="關鍵字 (韓文/英文)" class="w-full bg-gray-50 p-3 rounded-xl outline-none border focus:border-macaron-purple">
                </div>
            </div>
            <button @click="addItem" class="w-full mt-6 py-3 bg-macaron-purple text-white font-bold rounded-xl shadow-lg hover:bg-purple-300 transition-colors">確認新增</button>
        </div>
    </div>

</div>

<script>
    const { createApp, ref, computed, onMounted, watch } = Vue;

    createApp({
        setup() {
            // State
            const currentTab = ref('itinerary');
            const activeDay = ref(1);
            const showAddModal = ref(false);
            const mapQuery = ref('');
            const peopleCount = ref(2);
            
            // Exchange Rate (Default: 1 TWD = 41.5 KRW, user can edit)
            const exchangeRate = ref(41.5); 

            // Flight & Itinerary Data
            const defaultItinerary = [
                // Day 1
                { id: 100, day: 1, time: '14:25', title: '長榮航空 BR110', location: '', desc: '桃園 TPE 🛫 釜山 PUS', isFlight: true },
                { id: 101, day: 1, time: '17:40', title: '抵達金海機場', location: 'Gimhae International Airport', desc: '入境、領行李、換錢', isFlight: true },
                { id: 102, day: 1, time: '19:00', title: '飯店 Check-in', location: 'Hotel Aventree Busan', desc: '南浦洞亞雲樹飯店' },
                { id: 103, day: 1, time: '20:00', title: '扎嘎其市場 / BIFF廣場', location: 'Jagalchi Market', desc: '晚餐、逛夜市' },

                // Day 2
                { id: 201, day: 2, time: '09:00', title: '海雲台傳統市場', location: 'Haeundae Traditional Market', desc: '早餐' },
                { id: 202, day: 2, time: '10:20', title: '海東龍宮寺', location: 'Haedong Yonggungsa', desc: '海邊寺廟' },
                { id: 203, day: 2, time: '11:40', title: '樂天 Outlet', location: 'Lotte Premium Outlets Dongbusan', desc: '午餐 + 購物' },
                { id: 204, day: 2, time: '15:00', title: 'SPA LAND 汗蒸幕', location: 'Spa Land Centum City', desc: '新世界百貨' },

                // Day 3
                { id: 301, day: 3, time: '09:00', title: '釜山站集合 (一日遊)', location: 'Busan Station', desc: '前往慶州' },
                { id: 302, day: 3, time: '10:30', title: '天空膠囊列車', location: 'Haeundae Blueline Park', desc: '藍線公園' },
                { id: 303, day: 3, time: '15:00', title: '佛國寺', location: 'Bulguksa', desc: '慶州世界遺產' },
                { id: 304, day: 3, time: '19:00', title: '東宮與月池', location: 'Donggung Palace and Wolji Pond', desc: '夜景' },

                // Day 4
                { id: 401, day: 4, time: '09:30', title: '松島天空步道', location: 'Songdo Cloud Trails', desc: '海上步道' },
                { id: 402, day: 4, time: '10:20', title: '松島海上纜車', location: 'Songdo Marine Cable Car', desc: '水晶車廂' },
                { id: 403, day: 4, time: '14:00', title: '影島大橋開橋', location: 'Yeongdo Bridge', desc: '樂天百貨頂樓觀看' },
                { id: 404, day: 4, time: '15:00', title: '白淺灘文化村', location: 'Huinnyeoul Culture Village', desc: '網美照' },

                // Day 5
                { id: 501, day: 5, time: '09:00', title: '甘川洞文化村', location: 'Gamcheon Culture Village', desc: '集章、小王子' },
                { id: 502, day: 5, time: '11:30', title: '返回南浦洞', location: 'Nampo Station', desc: '最後採買' },
                { id: 503, day: 5, time: '13:30', title: '前往機場', location: 'Gimhae International Airport', desc: '退稅' },
                { id: 504, day: 5, time: '16:25', title: '長榮航空 BR109', location: '', desc: '釜山 PUS 🛫 桃園 TPE', isFlight: true },
            ];

            const itinerary = ref([]);
            const expenses = ref([]);
            const newItem = ref({ time: '12:00', title: '', location: '' });
            const newExpense = ref({ item: '', amount: '' });

            // Weather
            const weatherLoading = ref(true);
            const currentWeather = ref({ temp: '--', desc: '--', rain: 0, code: 0 });
            const forecast = ref([]);

            const fetchWeather = async () => {
                try {
                    const lat = 35.1796; const lon = 129.0756;
                    const res = await fetch(`https://api.open-meteo.com/v1/forecast?latitude=${lat}&longitude=${lon}&current=temperature_2m,weather_code,precipitation_probability&daily=weather_code,temperature_2m_max,temperature_2m_min&timezone=Asia%2FTokyo`);
                    const data = await res.json();
                    
                    currentWeather.value = {
                        temp: Math.round(data.current.temperature_2m),
                        desc: getWeatherDesc(data.current.weather_code),
                        rain: data.current.precipitation_probability || 0,
                        code: data.current.weather_code
                    };

                    forecast.value = data.daily.time.map((date, idx) => ({
                        dateStr: new Date(date).toLocaleDateString('en-US', { weekday: 'short', month: 'numeric', day: 'numeric' }),
                        code: data.daily.weather_code[idx],
                        max: Math.round(data.daily.temperature_2m_max[idx]),
                        min: Math.round(data.daily.temperature_2m_min[idx])
                    })).slice(0, 5);
                    weatherLoading.value = false;
                } catch (e) {
                    weatherLoading.value = false;
                }
            };

            const getWeatherDesc = (code) => {
                if (code === 0) return '晴朗';
                if (code <= 3) return '多雲';
                if (code <= 67) return '雨天';
                return '陰天';
            };
            
            const getWeatherIcon = (code) => {
                if (code === 0) return '☀️';
                if (code <= 3) return '☁️';
                if (code <= 67) return '🌧️';
                if (code <= 77) return '❄️';
                return '🌥️';
            };

            onMounted(() => {
                const savedItinerary = localStorage.getItem('busan_cute_itinerary');
                const savedExpenses = localStorage.getItem('busan_cute_expenses');
                const savedRate = localStorage.getItem('busan_rate');
                
                itinerary.value = savedItinerary ? JSON.parse(savedItinerary) : defaultItinerary;
                if (savedExpenses) expenses.value = JSON.parse(savedExpenses);
                if (savedRate) exchangeRate.value = parseFloat(savedRate);

                fetchWeather();
            });

            watch([itinerary, expenses, exchangeRate], () => {
                localStorage.setItem('busan_cute_itinerary', JSON.stringify(itinerary.value));
                localStorage.setItem('busan_cute_expenses', JSON.stringify(expenses.value));
                localStorage.setItem('busan_rate', exchangeRate.value);
            }, { deep: true });

            // Computed
            const filteredItinerary = computed(() => {
                return itinerary.value
                    .filter(item => item.day === activeDay.value)
                    .sort((a, b) => a.time.localeCompare(b.time));
            });

            const totalExpenseKRW = computed(() => expenses.value.reduce((sum, item) => sum + item.amount, 0));
            const totalExpenseTWD = computed(() => Math.round(totalExpenseKRW.value / exchangeRate.value));

            // Methods
            const addItem = () => {
                if (!newItem.value.title) return;
                itinerary.value.push({
                    id: Date.now(),
                    day: activeDay.value,
                    time: newItem.value.time,
                    title: newItem.value.title,
                    location: newItem.value.location || newItem.value.title,
                    desc: ''
                });
                showAddModal.value = false;
                newItem.value = { time: '12:00', title: '', location: '' };
            };

            const deleteItem = (id) => {
                if(confirm('要刪除這個行程嗎？🥺')) {
                    itinerary.value = itinerary.value.filter(item => item.id !== id);
                }
            };

            const addExpense = () => {
                if (!newExpense.value.item || !newExpense.value.amount) return;
                const d = new Date();
                expenses.value.unshift({
                    item: newExpense.value.item,
                    amount: newExpense.value.amount,
                    date: `${d.getMonth()+1}/${d.getDate()}`
                });
                newExpense.value = { item: '', amount: '' };
            };

            const removeExpense = (index) => expenses.value.splice(index, 1);

            const resetData = () => {
                if(confirm('要重新開始嗎？所有紀錄會消失喔！✨')) {
                    itinerary.value = [...defaultItinerary];
                    expenses.value = [];
                    localStorage.removeItem('busan_cute_itinerary');
                    localStorage.removeItem('busan_cute_expenses');
                }
            };

            const getNaverMapLink = (query) => `https://map.naver.com/p/search/${encodeURIComponent(query)}`;
            const searchNaver = () => mapQuery.value && window.open(getNaverMapLink(mapQuery.value), '_blank');
            const formatNumber = (num) => num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");

            return {
                currentTab, activeDay, showAddModal, peopleCount,
                itinerary, expenses, exchangeRate,
                filteredItinerary, totalExpenseKRW, totalExpenseTWD,
                newItem, newExpense, mapQuery,
                addItem, deleteItem, addExpense, removeExpense, resetData,
                weatherLoading, currentWeather, forecast, getWeatherIcon,
                formatNumber, searchNaver, getNaverMapLink
            };
        }
    }).mount('#app');
</script>
</body>
</html>
