<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>รายงานผลการวินิจฉัย - AGZ Team</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Font Awesome for Icons (Unicode usage context) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Placeholder Comments -->
    <!-- Chosen Palette: Natural Earth & Leaf (Warm Neutrals, Emerald Green, Amber Warning) -->
    <!-- Application Structure Plan: 
         1. Header: Branding 'AGZ Team'.
         2. Hero Visual Section: Main scientific image + Real evidence thumbnail.
         3. Diagnosis Content: Explains Phomopsis sp.
         4. Visual Analysis (Chart): Radar chart.
         5. Investigation Checklist.
         6. Treatment Plan.
         7. Footer: UPDATED with actual Google Docs link. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <style>
        @import url('https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;600;700&display=swap');
        
        body {
            font-family: 'Sarabun', sans-serif;
            background-color: #f5f5f4; /* stone-100 */
        }

        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 400px;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        ::-webkit-scrollbar-thumb {
            background: #a8a29e;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #78716c;
        }
        
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="text-stone-800 antialiased">

    <!-- Navigation / Header -->
    <nav class="bg-emerald-800 text-white shadow-lg sticky top-0 z-50">
        <div class="max-w-5xl mx-auto px-4 py-4 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <div>
                    <h1 class="text-xl font-bold leading-none">AGZ Team</h1>
                    <p class="text-xs text-emerald-200 mt-1">ระบบวิเคราะห์สุขภาพทุเรียน</p>
                </div>
            </div>
        </div>
    </nav>

    <!-- Main Content Container -->
    <main class="max-w-5xl mx-auto px-4 py-8 space-y-8">

        <!-- Section 1: Hero Visual (Main Image) -->
        <section class="relative rounded-2xl overflow-hidden shadow-xl border border-stone-200 bg-stone-900 group fade-in">
            
            <!-- Large Research Image (User Provided) -->
            <div class="relative w-full h-[400px] md:h-[500px]">
                <img src="https://i.ibb.co/JW6SYtfb/Gemini-Generated-Image-d524ftd524ftd524.png" 
                     alt="Scientific illustration of Phomopsis sp." 
                     class="w-full h-full object-cover opacity-95 group-hover:opacity-100 transition duration-700"
                     onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1596726615553-6a56c0734d0b?q=80&w=2000&auto=format&fit=crop';">
                
                <!-- Gradient Overlay for Text Readability -->
                <div class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/20 to-black/30"></div>

                <!-- Label for Main Image -->
                <div class="absolute bottom-6 left-6 text-white max-w-lg z-10">
                    <div class="inline-block bg-emerald-600/90 text-xs font-bold px-3 py-1 rounded-full mb-2 backdrop-blur-sm border border-emerald-400/30">
                        ภาพจำลองเชิงวิจัย (Research Model)
                    </div>
                    <h2 class="text-2xl md:text-3xl font-bold mb-2 text-white shadow-black drop-shadow-md leading-tight">
                        อาการโรคใบจุดจากเชื้อรา <br><span class="text-amber-400 italic">Phomopsis</span> sp.
                    </h2>
                    <p class="text-stone-300 text-sm md:text-base opacity-90 font-light">
                        ลักษณะจุดแผลสีน้ำตาลไหม้ ขอบแผลมีวงสีเหลือง (Halo) ล้อมรอบบนผิวใบ
                    </p>
                </div>
            </div>

            <!-- Thumbnail: Real Image (Top Right Corner - Circle) -->
            <div class="absolute top-4 right-4 z-20 flex flex-col items-end">
                <div class="relative group/thumb cursor-pointer">
                    <!-- Circular Container -->
                    <div class="w-24 h-24 md:w-32 md:h-32 rounded-full border-[3px] border-white shadow-2xl overflow-hidden transform transition hover:scale-110 duration-300 bg-stone-800 ring-4 ring-black/20">
                        <img src="https://source.roboflow.com/kqgFp9sbvAa3VE7fOf3MkkXTpoj2/2VOKZY7pixbLWXGsyH3N/original.jpg" 
                             alt="ภาพหน้างานจริง" 
                             class="w-full h-full object-cover"
                             onerror="this.src='https://via.placeholder.com/150?text=No+Image';">
                    </div>
                    <!-- Badge/Label -->
                    <div class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 bg-amber-500 text-white text-[10px] md:text-xs font-bold px-3 py-1 rounded-full shadow-md whitespace-nowrap border border-white z-30">
                        <i class="fa-solid fa-camera mr-1"></i>ภาพจริง
                    </div>
                </div>
            </div>
        </section>

        <!-- Section 2: Diagnosis Details -->
        <section class="bg-white rounded-2xl shadow-sm border border-stone-200 overflow-hidden fade-in">
            <div class="bg-amber-50 border-b border-amber-100 px-6 py-4">
                <h2 class="text-lg font-semibold text-amber-800 flex items-center gap-2">
                    <i class="fa-solid fa-notes-medical"></i> รายละเอียดการวินิจฉัย
                </h2>
            </div>
            <div class="p-6 md:p-8">
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <div>
                        <div class="mb-4">
                            <span class="bg-red-100 text-red-800 text-xs font-bold px-3 py-1 rounded-full">ความเสี่ยงสูงในต้นเล็ก</span>
                            <span class="bg-stone-100 text-stone-600 text-xs font-bold px-3 py-1 rounded-full ml-2">Leaf Spot Disease</span>
                        </div>
                        <p class="text-stone-600 leading-relaxed mb-6">
                            จากลักษณะอาการใบจุด คาดว่าเกิดจากเชื้อราโฟมอปซิส (<em>Phomopsis</em> sp.) ซึ่งมักแสดงอาการรุนแรงในทุเรียนต้นเล็ก ส่วนในต้นใหญ่อาการมักจะไม่รุนแรงเท่า 
                            โดยมีสาเหตุโน้มนำจากต้นที่ไม่แข็งแรงและขาดธาตุอาหาร
                        </p>
                        
                        <div class="bg-stone-50 rounded-xl p-4 border border-stone-100">
                            <h4 class="font-bold text-stone-700 mb-2 text-sm uppercase tracking-wide">อาการเด่นชัด</h4>
                            <ul class="space-y-2 text-sm text-stone-600">
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-circle-check text-emerald-500 mt-1"></i>
                                    <span>ใบมีอาการซีด ไม่เขียวเข้ม (Chlorosis)</span>
                                </li>
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-circle-check text-emerald-500 mt-1"></i>
                                    <span>เกิดจุดแผลสีน้ำตาลกระจายทั่วไปบนใบ</span>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <!-- Interactive Stat Block -->
                    <div class="grid grid-cols-2 gap-4">
                        <div class="bg-emerald-50 p-4 rounded-xl text-center hover:bg-emerald-100 transition cursor-default">
                            <i class="fa-solid fa-tree text-3xl text-emerald-600 mb-2"></i>
                            <div class="text-sm text-stone-500">เป้าหมาย</div>
                            <div class="font-bold text-stone-800">ต้นเล็ก / อ่อนแอ</div>
                        </div>
                        <div class="bg-amber-50 p-4 rounded-xl text-center hover:bg-amber-100 transition cursor-default">
                            <i class="fa-solid fa-virus text-3xl text-amber-600 mb-2"></i>
                            <div class="text-sm text-stone-500">ปัจจัยโน้มนำ</div>
                            <div class="font-bold text-stone-800">ขาดธาตุอาหาร</div>
                        </div>
                        <div class="col-span-2 bg-stone-800 text-white p-6 rounded-xl text-center shadow-lg transform transition hover:scale-[1.02]">
                            <div class="text-emerald-400 font-bold uppercase text-xs mb-1">คำแนะนำหลัก</div>
                            <div class="text-lg font-semibold">"โฟกัสที่พื้นฐาน: ดิน น้ำ ธาตุอาหาร"</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Section 3: Visual Analysis (Radar Chart) -->
        <section class="grid md:grid-cols-3 gap-6 fade-in">
            <div class="md:col-span-1 bg-white p-6 rounded-2xl shadow-sm border border-stone-200">
                <h3 class="font-bold text-xl text-stone-800 mb-4">ทำไมต้นถึงป่วย?</h3>
                <p class="text-stone-600 text-sm mb-6">
                    กราฟแสดงระดับความสมบูรณ์ของปัจจัยต่างๆ จะเห็นว่าปัจจัยด้าน "ธาตุอาหาร" และ "ความสมบูรณ์ของราก" ต่ำกว่าเกณฑ์ ทำให้ภูมิต้านทานโรคลดลง
                </p>
                <div class="space-y-3">
                    <div class="flex items-center justify-between text-sm">
                        <span class="flex items-center gap-2"><div class="w-3 h-3 rounded-full bg-emerald-500"></div> ระดับที่เหมาะสม</span>
                        <span class="font-bold text-emerald-700">100%</span>
                    </div>
                    <div class="flex items-center justify-between text-sm">
                        <span class="flex items-center gap-2"><div class="w-3 h-3 rounded-full bg-amber-500"></div> สภาพต้นปัจจุบัน</span>
                        <span class="font-bold text-amber-700">ต่ำกว่าเกณฑ์</span>
                    </div>
                </div>
                <button onclick="updateChartData()" class="mt-6 w-full py-2 bg-stone-100 hover:bg-stone-200 text-stone-700 rounded-lg text-sm font-semibold transition">
                    <i class="fa-solid fa-sync"></i> จำลองภาพหลังฟื้นฟู
                </button>
            </div>
            
            <div class="md:col-span-2 bg-white p-6 rounded-2xl shadow-sm border border-stone-200 flex flex-col justify-center items-center">
                <div class="chart-container">
                    <canvas id="healthRadarChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Section 4: Investigation Checklist -->
        <section class="fade-in">
            <div class="flex items-center gap-3 mb-6">
                <div class="w-10 h-10 rounded-full bg-blue-100 flex items-center justify-center text-blue-600 font-bold">1</div>
                <h2 class="text-2xl font-bold text-stone-800">ขั้นตอนการสำรวจ (Investigation)</h2>
            </div>
            <p class="text-stone-600 mb-6 max-w-3xl">
                ก่อนเริ่มการรักษา กรุณาตรวจสอบ 3 จุดสำคัญที่มักเป็นต้นเหตุของความอ่อนแอ ตามคำแนะนำของนักวิจัย
            </p>

            <div class="grid md:grid-cols-3 gap-4" id="checklist-container">
                <!-- Items injected by JS -->
            </div>
        </section>

        <!-- Section 5: Treatment Action Plan -->
        <section class="bg-stone-800 text-white rounded-3xl p-8 md:p-10 shadow-xl overflow-hidden relative fade-in">
            <div class="absolute top-0 right-0 opacity-10 transform translate-x-10 -translate-y-10">
                <i class="fa-solid fa-leaf text-9xl"></i>
            </div>

            <div class="relative z-10">
                <div class="flex items-center gap-3 mb-8">
                    <div class="w-10 h-10 rounded-full bg-emerald-500 flex items-center justify-center text-white font-bold">2</div>
                    <h2 class="text-2xl font-bold">แผนการจัดการและรักษา</h2>
                </div>

                <div class="grid md:grid-cols-2 gap-12">
                    <!-- Phase 1: Basics -->
                    <div>
                        <h3 class="text-emerald-400 font-bold tracking-wider uppercase mb-4 text-sm">Phase 1: การฟื้นฟูพื้นฐาน (สำคัญที่สุด)</h3>
                        <div class="space-y-6 border-l-2 border-stone-600 pl-6">
                            <div class="relative">
                                <div class="absolute -left-[31px] top-0 w-4 h-4 rounded-full bg-emerald-500 border-4 border-stone-800"></div>
                                <h4 class="font-bold text-lg mb-1">ดินและน้ำ</h4>
                                <p class="text-stone-400 text-sm">ปรับสภาพดินให้ร่วนซุย ค่า pH เหมาะสม และให้น้ำอย่างสม่ำเสมอ</p>
                            </div>
                            <div class="relative">
                                <div class="absolute -left-[31px] top-0 w-4 h-4 rounded-full bg-emerald-500 border-4 border-stone-800"></div>
                                <h4 class="font-bold text-lg mb-1">ธาตุอาหารครบถ้วน</h4>
                                <p class="text-stone-400 text-sm">เติมปุ๋ยที่มีธาตุอาหารหลัก (N-P-K), ธาตุรอง และจุลธาตุ ให้เพียงพอ เพื่อแก้ใบซีด</p>
                            </div>
                        </div>
                    </div>

                    <!-- Phase 2: Chemicals -->
                    <div>
                        <h3 class="text-amber-400 font-bold tracking-wider uppercase mb-4 text-sm">Phase 2: เคมีภัณฑ์ (เมื่อจำเป็น)</h3>
                        <div class="bg-stone-700/50 p-6 rounded-xl border border-stone-600">
                            <p class="mb-4 text-sm text-stone-300">หากสังเกตเห็นอาการเร็ว การใช้ยาพ่นจะช่วยได้ แต่ถ้าร่วงหมดต้นจะแก้ยาก</p>
                            <div class="flex flex-col gap-3">
                                <div class="flex items-center gap-3 bg-stone-800 p-3 rounded-lg">
                                    <i class="fa-solid fa-spray-can text-amber-500"></i>
                                    <div>
                                        <div class="font-bold text-sm">แมนโคเซบ (Mancozeb)</div>
                                        <div class="text-xs text-stone-500">ยาป้องกันกำจัดเชื้อรา</div>
                                    </div>
                                </div>
                                <div class="flex items-center gap-3 bg-stone-800 p-3 rounded-lg">
                                    <i class="fa-solid fa-spray-can text-amber-500"></i>
                                    <div>
                                        <div class="font-bold text-sm">คาร์เบนดาซิม (Carbendazim)</div>
                                        <div class="text-xs text-stone-500">ยาดูดซึมกำจัดเชื้อรา</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer with Clickable Ref Link -->
        <footer class="text-center text-stone-400 text-sm py-8 border-t border-stone-200 mt-8">
            <div class="mb-4">
                <a href="https://docs.google.com/document/d/1-HErkM9I30Qza-38HEK2QxwuAo94aVO4a30arMtq3Uc/edit?usp=sharing" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 px-5 py-2.5 rounded-full bg-white border border-stone-200 text-stone-600 text-xs font-semibold shadow-sm hover:bg-blue-50 hover:text-blue-700 hover:border-blue-200 hover:shadow-md transition-all duration-200 group no-underline" title="คลิกเพื่ออ่านเอกสารอ้างอิง">
                    <i class="fa-solid fa-file-word text-blue-600 text-base group-hover:scale-110 transition-transform"></i>
                    <span>Ref. วิเคราะห์โรคทุเรียนจากนักวิจัย AGZ.doc</span>
                    <i class="fa-solid fa-external-link-alt text-stone-400 ml-2 text-xs group-hover:text-blue-500 opacity-0 group-hover:opacity-100 transition-opacity"></i>
                </a>
            </div>
            <p>&copy; 2025 AGZ Team. ข้อมูลอ้างอิงจากทีมวิจัย AGZ</p>
        </footer>

    </main>

    <script>
        // --- DATA STORE ---
        const checklistData = [
            {
                id: 'roots',
                icon: 'fa-network-wired',
                title: 'ขุดดูระบบราก',
                question: 'รากแตกดีไหม? มีรากฝอยเยอะไหม?',
                detail: 'หากรากฝอยน้อย หรือมีรากเน่าดำ แสดงว่าต้นหาอาหารไม่ได้ ทำให้ใบซีดและอ่อนแอ',
                color: 'text-amber-600',
                bg: 'bg-amber-50'
            },
            {
                id: 'soil',
                icon: 'fa-flask',
                title: 'วัดค่า pH ดิน',
                question: 'ดินเป็นกรดหรือไม่?',
                detail: 'ค่า pH ที่เป็นกรดจัดจะขัดขวางการดูดซึมธาตุอาหาร ต่อให้ใส่ปุ๋ย ต้นก็กินไม่ได้',
                color: 'text-blue-600',
                bg: 'bg-blue-50'
            },
            {
                id: 'nutrient',
                icon: 'fa-utensils',
                title: 'ธาตุอาหาร',
                question: 'ได้รับ หลัก-รอง-เสริม ครบไหม?',
                detail: 'อาการใบซีดและจุดรา บ่งบอกถึงต้นที่ไม่แข็งแรง ขาดสารอาหารสำคัญในการสร้างภูมิคุ้มกัน',
                color: 'text-emerald-600',
                bg: 'bg-emerald-50'
            }
        ];

        let isHealthySimulated = false;
        let healthChart;

        // --- INITIALIZATION ---
        document.addEventListener('DOMContentLoaded', () => {
            renderChecklist();
            initChart();
        });

        // --- FUNCTIONS ---

        // 1. Render Interactive Checklist
        function renderChecklist() {
            const container = document.getElementById('checklist-container');
            container.innerHTML = checklistData.map(item => `
                <div class="bg-white rounded-xl shadow-sm border border-stone-200 overflow-hidden hover:shadow-md transition cursor-pointer group" onclick="toggleDetail('${item.id}')">
                    <div class="p-5">
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 rounded-full ${item.bg} flex items-center justify-center flex-shrink-0 group-hover:scale-110 transition">
                                <i class="fa-solid ${item.icon} ${item.color} text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-stone-800 text-lg">${item.title}</h4>
                                <p class="text-stone-500 text-sm mt-1">${item.question}</p>
                            </div>
                        </div>
                    </div>
                    <div id="detail-${item.id}" class="hidden bg-stone-50 px-5 py-3 border-t border-stone-100 text-sm text-stone-600 animate-slideDown">
                        <i class="fa-solid fa-circle-info mr-2 ${item.color}"></i> ${item.detail}
                    </div>
                    <div class="bg-stone-50 px-5 py-2 border-t border-stone-100 text-center text-xs text-stone-400 group-hover:bg-stone-100 transition">
                        คลิกเพื่อดูรายละเอียด
                    </div>
                </div>
            `).join('');
        }

        function toggleDetail(id) {
            const el = document.getElementById(`detail-${id}`);
            if (el.classList.contains('hidden')) {
                el.classList.remove('hidden');
            } else {
                el.classList.add('hidden');
            }
        }

        // 2. Chart.js Implementation
        function initChart() {
            const ctx = document.getElementById('healthRadarChart').getContext('2d');
            
            const data = {
                labels: [
                    'ความสมบูรณ์ของราก (Root Health)',
                    'ค่า pH ดิน (Soil pH)',
                    'การจัดการน้ำ (Water)',
                    'ธาตุอาหาร (Nutrients)',
                    'ความต้านทานโรค (Immunity)'
                ],
                datasets: [{
                    label: 'สภาพต้นปัจจุบัน (ป่วย)',
                    data: [40, 50, 60, 30, 20], // Low values indicating poor health
                    fill: true,
                    backgroundColor: 'rgba(245, 158, 11, 0.2)', // Amber
                    borderColor: 'rgb(245, 158, 11)',
                    pointBackgroundColor: 'rgb(245, 158, 11)',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: 'rgb(245, 158, 11)'
                }, {
                    label: 'เกณฑ์ที่เหมาะสม (เป้าหมาย)',
                    data: [90, 85, 90, 95, 100], // High target values
                    fill: true,
                    backgroundColor: 'rgba(16, 185, 129, 0.1)', // Emerald
                    borderColor: 'rgba(16, 185, 129, 0.5)',
                    pointBackgroundColor: 'rgba(16, 185, 129, 1)',
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: 'rgb(16, 185, 129)',
                    hidden: false
                }]
            };

            const config = {
                type: 'radar',
                data: data,
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    elements: {
                        line: { borderWidth: 3 }
                    },
                    scales: {
                        r: {
                            angleLines: { display: true, color: '#e5e7eb' },
                            grid: { color: '#e5e7eb' },
                            pointLabels: {
                                font: { size: 11, family: 'Sarabun' },
                                color: '#44403c'
                            },
                            suggestedMin: 0,
                            suggestedMax: 100,
                            ticks: { display: false }
                        }
                    },
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: { font: { family: 'Sarabun' } }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return context.dataset.label + ': ' + context.raw + '%';
                                }
                            }
                        }
                    }
                }
            };

            healthChart = new Chart(ctx, config);
        }

        function updateChartData() {
            if (!healthChart) return;
            
            const btn = document.querySelector('button[onclick="updateChartData()"]');

            if (!isHealthySimulated) {
                // Simulate Recovery
                healthChart.data.datasets[0].data = [80, 85, 85, 90, 85]; // Improved values
                healthChart.data.datasets[0].label = 'คาดการณ์หลังฟื้นฟู (Recovered)';
                healthChart.data.datasets[0].backgroundColor = 'rgba(16, 185, 129, 0.4)';
                healthChart.data.datasets[0].borderColor = 'rgb(16, 185, 129)';
                healthChart.data.datasets[0].pointBackgroundColor = 'rgb(16, 185, 129)';
                
                btn.innerHTML = '<i class="fa-solid fa-undo"></i> ดูสภาพก่อนรักษา';
                isHealthySimulated = true;
            } else {
                // Revert to Sick
                healthChart.data.datasets[0].data = [40, 50, 60, 30, 20];
                healthChart.data.datasets[0].label = 'สภาพต้นปัจจุบัน (ป่วย)';
                healthChart.data.datasets[0].backgroundColor = 'rgba(245, 158, 11, 0.2)';
                healthChart.data.datasets[0].borderColor = 'rgb(245, 158, 11)';
                healthChart.data.datasets[0].pointBackgroundColor = 'rgb(245, 158, 11)';
                
                btn.innerHTML = '<i class="fa-solid fa-sync"></i> จำลองภาพหลังฟื้นฟู';
                isHealthySimulated = false;
            }
            healthChart.update();
        }

    </script>
</body>
</html>

