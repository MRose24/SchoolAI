<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI-Powered Empathy & Gratitude Journal (EGJ) Prototype</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* กำหนดรูปแบบฟอนต์ให้รองรับภาษาไทย */
        body {
            font-family: 'Tahoma', 'Avenir Next', sans-serif;
            background-color: #f7f9fc;
        }
    </style>
</head>
<body class="p-4 md:p-8">

    <header class="text-center mb-8">
        <h1 class="text-4xl font-bold text-indigo-700">Concept Navigator</h1>
        <h2 class="text-xl text-gray-600">AI-Powered Empathy & Gratitude Journal (EGJ)</h2>
        <p class="text-sm text-gray-500 mt-1">Prototype สำหรับโครงการ: การส่งเสริมพฤติกรรมเชิงบวกของนักเรียน</p>
    </header>

    <main class="max-w-4xl mx-auto space-y-8">

        <section class="bg-white p-6 rounded-xl shadow-lg border-t-4 border-indigo-500">
            <h3 class="text-2xl font-semibold text-gray-800 mb-4">บันทึก Journal ประจำวันของคุณ</h3>
            <p class="text-sm text-gray-500 mb-3">คุณสามารถเขียนถึงสิ่งที่เกิดขึ้นในวันนี้ ทั้งความรู้สึกดี ๆ หรือความท้าทายที่คุณพบเจอ</p>
            
            <textarea id="daily-entry" rows="6" 
                      class="w-full p-3 border border-gray-300 rounded-lg focus:ring-indigo-500 focus:border-indigo-500 transition duration-150 ease-in-out" 
                      placeholder="วันนี้... ฉันรู้สึกขอบคุณ/เห็นอกเห็นใจ/ท้าทายในเรื่อง..."></textarea>
            
            <button id="submit-journal" 
                    class="mt-4 w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 rounded-lg transition duration-200 shadow-md">
                ส่งบันทึกและรับ Feedback จาก AI (จำลอง)
            </button>
            <p class="text-xs text-center text-gray-400 mt-2">
                *ในแอปจริง ปุ่มนี้จะเชื่อมต่อกับ API ของ AI เพื่อวิเคราะห์ข้อความ
            </p>
        </section>

        <section id="ai-feedback" class="bg-yellow-50 p-6 rounded-xl shadow-lg border-l-4 border-yellow-400">
            <h3 class="text-2xl font-semibold text-gray-800 mb-4 flex items-center">
                <span class="mr-2 text-yellow-600">💡</span> AI Reflection Coach
            </h3>
            
            <div id="gratitude-score" class="mb-4 p-4 bg-white border border-yellow-200 rounded-lg">
                <p class="font-medium text-lg text-green-600">Gratitude Scanner Result (จำลอง):</p>
                <p class="text-gray-700">AI พบประโยคแสดงความขอบคุณ **3** ประโยค! <span class="font-bold">ระดับความขอบคุณวันนี้: 85%</span> (ดีมาก!)</p>
            </div>
            
            <div id="empathy-prompt" class="p-4 bg-white border border-yellow-200 rounded-lg">
                <p class="font-medium text-lg text-red-500">Empathy Reflection Prompt (AI-Generated Prompt):</p>
                <p class="text-gray-700 italic">
                    "จากที่คุณเล่าถึงความขัดแย้งกับเพื่อนเรื่องการทำโปรเจกต์ ลองใช้เวลา 1 นาที คิดดูว่า: **ถ้าคุณเป็นเพื่อนคนนั้น** ที่ทำงานหนักแต่ผลลัพธ์ยังไม่ดีพอ **คุณจะรู้สึกท้อแท้หรือผิดหวังในตัวเองอย่างไร?** การเข้าใจความรู้สึกนี้จะช่วยให้คุณสื่อสารกับเขาได้อย่างไรในวันพรุ่งนี้"
                </p>
            </div>
            
        </section>

        <section id="trend-report" class="bg-white p-6 rounded-xl shadow-lg border-t-4 border-green-500">
            <h3 class="text-2xl font-semibold text-gray-800 mb-4 flex items-center">
                <span class="mr-2 text-green-600">📈</span> Positive Trend Report (รายงานแนวโน้มเชิงบวก)
            </h3>
            <p class="text-gray-600 mb-4">สรุปแนวโน้มทางอารมณ์ของคุณในสัปดาห์ที่ผ่านมา:</p>
            
            <div class="bg-gray-100 p-4 rounded-lg border border-gray-300">
                <p class="text-sm font-semibold text-green-700">กราฟความสม่ำเสมอในการใช้คำเชิงบวก (จำลอง):</p>
                <div class="h-16 flex items-end justify-around mt-2">
                    <div class="w-1/6 bg-blue-400" style="height: 40%;" title="จันทร์"></div>
                    <div class="w-1/6 bg-blue-500" style="height: 70%;" title="อังคาร"></div>
                    <div class="w-1/6 bg-blue-300" style="height: 30%;" title="พุธ"></div>
                    <div class="w-1/6 bg-blue-600" style="height: 90%;" title="พฤหัส"></div>
                    <div class="w-1/6 bg-blue-500" style="height: 60%;" title="ศุกร์"></div>
                </div>
                <div class="flex justify-around text-xs mt-1 text-gray-500">
                    <span>จ</span><span>อ</span><span>พ</span><span>พฤ</span><span>ศ</span>
                </div>
            </div>
            
            <p class="mt-4 text-sm text-gray-700">
                <span class="font-semibold text-indigo-600">Insight จาก AI:</span> แนวโน้มของคุณชี้ให้เห็นว่าคุณมีการใช้คำศัพท์เชิงบวกเพิ่มขึ้น **15%** ในสัปดาห์นี้ จุดแข็งของคุณคือความสามารถในการค้นหาสิ่งที่น่าขอบคุณ แม้ในวันที่เครียด
            </p>
        </section>

    </main>

    <footer class="text-center mt-10 text-xs text-gray-400">
        <p>© 2025 Educational Innovation Project. Developed using No-Code/Low-Code Concept.</p>
    </footer>

</body>
</html>
