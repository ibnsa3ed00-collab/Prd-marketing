<!DOCTYPE html>
<html lang="ku" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سیستەمی بەڕێوەبردنی کڕیارەکان | Prd.cc VIP</title>
    <!-- بەکارهێنانی فۆنتی مۆدێرن و ڕاقی بۆ کوردی -->
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary: #1e293b;
            --secondary: #3b82f6;
            --accent: #10b981;
            --bg-color: #f1f5f9;
            --card-bg: #ffffff;
            --text-dark: #0f172a;
            --text-light: #64748b;
            --border-color: #e2e8f0;
            --gold: #d97706;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Vazirmatn', sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-dark);
            line-height: 1.7;
        }

        /* Navbar - Glassmorphism Effect */
        nav {
            background: rgba(30, 41, 59, 0.95);
            backdrop-filter: blur(10px);
            color: white;
            padding: 1rem 3rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
        }

        .logo {
            font-size: 1.6rem;
            font-weight: 800;
            letter-spacing: 0.5px;
            color: white;
            text-decoration: none;
        }
        
        .logo span {
            color: var(--secondary);
        }

        .nav-links button {
            background: transparent;
            border: none;
            color: rgba(255,255,255,0.7);
            cursor: pointer;
            font-size: 1rem;
            margin-right: 2rem;
            font-weight: 600;
            padding-bottom: 0.5rem;
            transition: all 0.3s ease;
        }

        .nav-links button:hover, .nav-links button.active {
            color: white;
            border-bottom: 3px solid var(--secondary);
        }

        /* Main Container */
        .container {
            max-width: 1100px;
            margin: 3rem auto;
            padding: 0 1.5rem;
        }

        .section {
            display: none;
            animation: fadeUp 0.5s ease forwards;
            opacity: 0;
            transform: translateY(20px);
        }

        .section.active {
            display: block;
        }

        @keyframes fadeUp {
            to { opacity: 1; transform: translateY(0); }
        }

        /* Dashboard Header */
        .dashboard-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2.5rem;
        }

        .dashboard-header h2 {
            font-size: 1.8rem;
            font-weight: 700;
        }

        .btn-primary {
            background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
            color: white;
            border: none;
            padding: 0.8rem 1.8rem;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            font-size: 1rem;
            box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(59, 130, 246, 0.4);
        }

        /* VIP Cards Grid */
        .clients-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
            gap: 2rem;
        }

        .client-card {
            background: var(--card-bg);
            border-radius: 16px;
            padding: 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.04);
            border: 1px solid rgba(0,0,0,0.02);
            transition: transform 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .client-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.08);
        }

        .client-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--gold), #fbbf24);
        }

        .client-header {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .avatar {
            width: 55px;
            height: 55px;
            border-radius: 14px;
            background: #f8fafc;
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            font-weight: 800;
            margin-left: 1rem;
            border: 1px solid var(--border-color);
        }

        .client-info h3 {
            font-size: 1.3rem;
            color: var(--primary);
            font-weight: 700;
        }

        .client-info p {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-top: 0.2rem;
        }

        .package-badge {
            display: inline-block;
            background-color: #fffbeb;
            color: var(--gold);
            padding: 0.4rem 1rem;
            border-radius: 8px;
            font-size: 0.9rem;
            font-weight: 700;
            border: 1px solid #fef3c7;
            margin-bottom: 1.5rem;
        }

        /* Progress Bar */
        .progress-header {
            display: flex;
            justify-content: space-between;
            font-size: 0.95rem;
            margin-bottom: 0.8rem;
            font-weight: 600;
        }

        .progress-track {
            height: 8px;
            background-color: #f1f5f9;
            border-radius: 10px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--accent), #34d399);
            border-radius: 10px;
            transition: width 1s cubic-bezier(0.4, 0, 0.2, 1);
        }

        /* Actions */
        .card-actions {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            border-top: 1px solid var(--border-color);
            padding-top: 1.5rem;
        }
        
        .card-actions button {
            flex: 1;
            padding: 0.7rem;
            border: 1px solid var(--border-color);
            background: transparent;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            color: var(--text-dark);
            transition: all 0.2s;
        }
        
        .card-actions button:hover {
            background: var(--bg-color);
            border-color: #cbd5e1;
        }

        /* Forms & Modals */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(15, 23, 42, 0.6);
            backdrop-filter: blur(4px);
            align-items: center;
            justify-content: center;
            z-index: 1000;
        }

        .modal.active { display: flex; }

        .modal-content {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            width: 100%;
            max-width: 550px;
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
        }

        .close-btn {
            background: #f1f5f9;
            border: none;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            font-size: 1.2rem;
            cursor: pointer;
            color: var(--text-dark);
            transition: background 0.2s;
        }

        .close-btn:hover { background: #e2e8f0; }

        .form-group { margin-bottom: 1.5rem; }
        
        .form-group label {
            display: block;
            margin-bottom: 0.6rem;
            font-weight: 600;
            color: var(--text-dark);
        }
        
        .form-group input, .form-group select {
            width: 100%;
            padding: 0.9rem;
            border: 1.5px solid var(--border-color);
            border-radius: 10px;
            font-family: inherit;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        .form-group input:focus, .form-group select:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.1);
        }

        /* Client Demo VIP Portal */
        .portal-card {
            background: white;
            border-radius: 24px;
            padding: 3.5rem;
            box-shadow: 0 20px 40px rgba(0,0,0,0.06);
            max-width: 900px;
            margin: 0 auto;
            border-top: 6px solid var(--gold);
        }
        
        .task-list {
            list-style: none;
            margin-top: 1.5rem;
        }

        .task-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem;
            border: 1px solid var(--border-color);
            border-radius: 12px;
            margin-bottom: 1rem;
            background: #fafafa;
            transition: background 0.2s;
        }
        
        .task-item:hover { background: white; box-shadow: 0 4px 12px rgba(0,0,0,0.03); }
        
        .task-status {
            font-size: 0.85rem;
            padding: 0.4rem 0.8rem;
            border-radius: 6px;
            font-weight: 600;
        }
        
        .status-done { background: #dcfce7; color: #166534; }
        .status-wait { background: #fef3c7; color: #92400e; }
        .status-action { background: #dbeafe; color: #1e40af; }

        .btn-whatsapp {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background: #25D366;
            color: white;
            padding: 1rem 2.5rem;
            border-radius: 12px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            box-shadow: 0 10px 25px rgba(37, 211, 102, 0.3);
            transition: all 0.3s ease;
        }

        .btn-whatsapp:hover { transform: translateY(-3px); box-shadow: 0 15px 30px rgba(37, 211, 102, 0.4); }

    </style>
</head>
<body>

    <nav>
        <a href="#" class="logo">Prd<span>.cc</span></a>
        <div class="nav-links">
            <button class="active" onclick="switchTab('admin')">داشبۆردی سەرەکی</button>
            <button onclick="switchTab('client-demo')">نموونەی دەروازەی پزیشک</button>
        </div>
    </nav>

    <div class="container">
        
        <!-- Admin Dashboard Section -->
        <div id="admin-section" class="section active">
            <div class="dashboard-header">
                <div>
                    <h2>بەڕێوەبردنی کڕیارەکان</h2>
                    <p style="color: var(--text-light); margin-top: 5px;">چاودێری پرۆژەکان و ئۆفەرەکان بکە بە شێوازێکی پرۆفێشناڵ</p>
                </div>
                <button class="btn-primary" onclick="openModal()">+ کڕیاری نوێ</button>
            </div>

            <div class="clients-grid">
                <!-- Example Client 1 -->
                <div class="client-card">
                    <div class="client-header">
                        <div class="avatar">د</div>
                        <div class="client-info">
                            <h3>د. نەوزاد - نەشتەرگەری</h3>
                            <p>ئاب</p>
                        </div>
                    </div>
                    
                    <div class="package-badge">👑 ئۆفەری پێشکەوتوو</div>
                    
                    <div style="margin: 1.5rem 0;">
                        <div class="progress-header">
                            <span>پێشکەوتنی کارەکان</span>
                            <span style="color: var(--accent);">٨٠٪</span>
                        </div>
                        <div class="progress-track">
                            <div class="progress-fill" style="width: 80%;"></div>
                        </div>
                    </div>

                    <div class="card-actions">
                        <button onclick="copyClientLink('dr-nawzad')">🔗 کۆپی لینک</button>
                        <button style="color: var(--secondary);">✏️ نوێکردنەوە</button>
                    </div>
                </div>

                <!-- Example Client 2 -->
                <div class="client-card">
                    <div class="client-header">
                        <div class="avatar">ک</div>
                        <div class="client-info">
                            <h3>کلینیکی ئاسودە</h3>
                            <p>ئەیلول</p>
                        </div>
                    </div>
                    
                    <div class="package-badge" style="color: #0369a1; background: #e0f2fe; border-color: #bae6fd;">🚀 ئۆفەری گەشەسەندوو</div>
                    
                    <div style="margin: 1.5rem 0;">
                        <div class="progress-header">
                            <span>پێشکەوتنی کارەکان</span>
                            <span style="color: #0ea5e9;">٤٥٪</span>
                        </div>
                        <div class="progress-track">
                            <div class="progress-fill" style="width: 45%; background: linear-gradient(90deg, #3b82f6, #60a5fa);"></div>
                        </div>
                    </div>

                    <div class="card-actions">
                        <button onclick="copyClientLink('asuda-clinic')">🔗 کۆپی لینک</button>
                        <button style="color: var(--secondary);">✏️ نوێکردنەوە</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Client VIP Portal Demo -->
        <div id="client-demo-section" class="section">
            <div style="text-align: center; margin-bottom: 3rem;">
                <h1 style="font-size: 2.2rem; color: var(--primary); font-weight: 800;">بەخێربێیت، د. نەوزاد</h1>
                <p style="color: var(--text-light); font-size: 1.1rem; margin-top: 0.5rem;">ڕاپۆرتی مانگانەی کارەکانت لەلایەن ئاژانسی Prd.cc</p>
            </div>

            <div class="portal-card">
                <div style="display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid var(--border-color); padding-bottom: 2rem; margin-bottom: 2rem;">
                    <div>
                        <h2 style="color: var(--primary); font-size: 1.6rem;">ئاماری ئەم مانگە</h2>
                        <span class="package-badge" style="margin-top: 15px; display: inline-block;">👑 پاکێجی هەڵبژێردراو: ئۆفەری پێشکەوتوو</span>
                    </div>
                    <div class="avatar" style="width: 90px; height: 90px; font-size: 3rem;">د</div>
                </div>

                <div style="margin-bottom: 3rem;">
                    <div class="progress-header" style="font-size: 1.2rem;">
                        <span>ڕێژەی تەواوبوونی کارەکان</span>
                        <span style="color: var(--accent); font-size: 1.8rem; font-weight: 800;">٨٠٪</span>
                    </div>
                    <div class="progress-track" style="height: 18px;">
                        <div class="progress-fill" style="width: 80%;"></div>
                    </div>
                </div>

                <h3 style="font-size: 1.4rem; color: var(--primary); margin-bottom: 1.5rem;">وردەکاری کارەکان (Tasks)</h3>
                
                <ul class="task-list">
                    <li class="task-item">
                        <strong style="font-size: 1.1rem;">پێنج ڤیدیۆ تۆمارکردن + ڕێکخستنی ڕوناکی</strong>
                        <span class="task-status status-done">✅ تەواوبوو</span>
                    </li>
                    <li class="task-item">
                        <strong style="font-size: 1.1rem;">هاوبەشی پۆست لەگەڵ پەیجی mr nurse</strong>
                        <span class="task-status status-done">✅ ئامادەی بڵاوکردنەوەیە</span>
                    </li>
                    <li class="task-item">
                        <strong style="font-size: 1.1rem;">ڤیدیۆ لە ژووری نەشتەرگەری و کەیسی دەگمەن</strong>
                        <span class="task-status status-wait">⏳ چاوەڕێی کاتی نەشتەرگەری</span>
                    </li>
                    <li class="task-item">
                        <strong style="font-size: 1.1rem;">ئیدیتکردن + مۆشن گرافیک</strong>
                        <span class="task-status status-action">✂️ لە مۆنتاژدایە</span>
                    </li>
                    <li class="task-item">
                        <strong style="font-size: 1.1rem;">دیزاینی پێنج پۆست + عەرەبی لەگەڵ براندینگی تایبەت</strong>
                        <span class="task-status status-done">✅ تەواوبوو</span>
                    </li>
                    <li class="task-item">
                        <strong style="font-size: 1.1rem;">نووسینی کاپشن، هەڵبژاردنی ناوەڕۆک و سەرپەرشتی سپۆنسەر</strong>
                        <span class="task-status status-done">✅ جێبەجێ کراوە</span>
                    </li>
                </ul>
                
                <div style="text-align: center; margin-top: 4rem; padding-top: 2rem; border-top: 1px solid var(--border-color);">
                    <p style="color: var(--text-light); margin-bottom: 1.5rem; font-size: 1.1rem;">پێویستت بە گۆڕانکاری یان ڕاوێژ هەیە؟</p>
                    <a href="https://wa.me/9647729628611" target="_blank" class="btn-whatsapp">
                        پەیوەندی بە واتسئاپ 💬
                    </a>
                </div>
            </div>
        </div>

    </div>

    <!-- Add Client Modal -->
    <div class="modal" id="addModal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 style="font-size: 1.5rem; font-weight: 700;">+ زیادکردنی کڕیاری نوێ</h3>
                <button class="close-btn" onclick="closeModal()">&times;</button>
            </div>
            
            <form id="addClientForm" onsubmit="event.preventDefault(); alert('داتا خەزن کرا.'); closeModal();">
                <div class="form-group">
                    <label>ناوی پزیشک / سەنتەر</label>
                    <input type="text" placeholder="نموونە: د. نەوزاد" required>
                </div>
                
                <div class="form-group">
                    <label>مانگ</label>
                    <select required>
                        <option value="کانوونی دووەم">کانوونی دووەم (١)</option>
                        <option value="شوبات">شوبات (٢)</option>
                        <option value="ئازار">ئازار (٣)</option>
                        <option value="نیسان">نیسان (٤)</option>
                        <option value="ئایار">ئایار (٥)</option>
                        <option value="حوزەیران">حوزەیران (٦)</option>
                        <option value="تەممووز">تەممووز (٧)</option>
                        <option value="ئاب">ئاب (٨)</option>
                        <option value="ئەیلول">ئەیلول (٩)</option>
                        <option value="تشرینی یەکەم">تشرینی یەکەم (١٠)</option>
                        <option value="تشرینی دووەم">تشرینی دووەم (١١)</option>
                        <option value="کانوونی یەکەم">کانوونی یەکەم (١2)</option>
                    </select>
                </div>

                <div class="form-group">
                    <label>هەڵبژاردنی ئۆفەر</label>
                    <select required style="font-weight: 600;">
                        <option value="ئۆفەری سەرەتایی">🌱 ئۆفەری سەرەتایی (٣ ڤیدیۆ + ٣ دیزاین)</option>
                        <option value="ئۆفەری گەشەسەندوو">🚀 ئۆفەری گەشەسەندوو (٤ ڤیدیۆ + ٤ دیزاین)</option>
                        <option value="ئۆفەری پێشکەوتوو">👑 ئۆفەری پێشکەوتوو (٥ ڤیدیۆ + mr nurse)</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label>ڕێژەی تەواوبوونی سەرەتایی (%)</label>
                    <input type="number" min="0" max="100" value="0" required>
                </div>

                <button type="submit" class="btn-primary" style="width: 100%; margin-top: 1.5rem; padding: 1rem; font-size: 1.1rem;">پاشەکەوتکردن</button>
            </form>
        </div>
    </div>

    <script>
        function switchTab(tabId) {
            document.querySelectorAll('.nav-links button').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            
            document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
            if(tabId === 'admin') {
                document.getElementById('admin-section').classList.add('active');
            } else {
                document.getElementById('client-demo-section').classList.add('active');
            }
        }

        function openModal() { document.getElementById('addModal').classList.add('active'); }
        function closeModal() { document.getElementById('addModal').classList.remove('active'); }

        function copyClientLink(clientId) {
            const link = `https://prd.cc/portal/${clientId}`;
            navigator.clipboard.writeText(link);
            alert(`لینکەکە کۆپی کرا بۆ کڕیار:\n${link}`);
        }
        
        window.onclick = function(event) {
            const modal = document.getElementById('addModal');
            if (event.target == modal) { closeModal(); }
        }
    </script>
</body>
</html>
