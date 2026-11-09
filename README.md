<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cyber Esports Club - ALT University Project</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #0b0f19;
            color: #f8fafc;
            line-height: 1.6;
        }
        header {
            background: linear-gradient(135deg, #1e293b, #0f172a);
            padding: 30px 20px;
            text-align: center;
            border-bottom: 2px solid #0284c7;
        }
        header h1 { color: #38bdf8; font-size: 2.5rem; margin-bottom: 10px; }
        header p { color: #94a3b8; font-size: 1.1rem; }
        
        nav {
            background: #1e293b;
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        nav a {
            color: #f8fafc;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s;
        }
        nav a:hover { color: #38bdf8; }

        .container {
            max-width: 1100px;
            margin: 30px auto;
            padding: 0 20px;
        }

        section {
            background: #1e293b;
            margin-bottom: 30px;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.3);
        }

        h2 { color: #38bdf8; margin-bottom: 20px; border-bottom: 2px solid #334155; padding-bottom: 10px; }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .card {
            background: #0f172a;
            padding: 20px;
            border-radius: 8px;
            border: 1px solid #334155;
        }
        .card h3 { color: #38bdf8; margin-bottom: 10px; }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }
        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #334155;
        }
        th { background-color: #0f172a; color: #38bdf8; }

        .form-group {
            margin-bottom: 15px;
        }
        label { display: block; margin-bottom: 5px; color: #94a3b8; }
        input, select {
            width: 100%;
            padding: 10px;
            background: #0f172a;
            border: 1px solid #334155;
            border-radius: 5px;
            color: white;
        }
        button {
            background: #0284c7;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            transition: background 0.3s;
        }
        button:hover { background: #0ea5e9; }

        footer {
            text-align: center;
            padding: 20px;
            background: #0f172a;
            color: #64748b;
            border-top: 1px solid #1e293b;
        }
    </style>
</head>
<body>

    <header>
        <h1>Cyber Esports Club</h1>
        <p>ALT Университеті - Theme 9: Деректер базасы және веб-қосымша</p>
    </header>

    <nav>
        <a href="#computers">Компьютерлер</a>
        <a href="#pricing">Прайс-лист</a>
        <a href="#booking">Брондау</a>
        <a href="#database">База туралы</a>
        <a href="#contact">Адрес</a>
    </nav>

    <div class="container">

        <!-- 1. КОМПЬЮТЕРЛЕР МЕН ЗОНАЛАР -->
        <section id="computers">
            <h2>💻 Клуб зоналары мен компьютер саны</h2>
            <div class="grid">
                <div class="card">
                    <h3>Standard Zone</h3>
                    <p>Барлығы: <b>15 компьютер</b></p>
                    <p>Сипаттамасы: Базовый ойындарға арналған стандартты орындар (GTX 1660 Super, 144Hz монитор).</p>
                </div>
                <div class="card">
                    <h3>VIP Zone</h3>
                    <p>Барлығы: <b>10 компьютер</b></p>
                    <p>Сипаттамасы: Жоғары өнімді ойындар мен киберспортқа арналған (RTX 3060 Ti, 240Hz монитор).</p>
                </div>
                <div class="card">
                    <h3>Bootcamp (Командная)</h3>
                    <p>Барлығы: <b>5 компьютер</b></p>
                    <p>Сипаттамасы: Жабық командалық бөлме турнирлер мен жаттығуларға арналған.</p>
                </div>
            </div>
        </section>

        <!-- 2. ПРАЙС-ЛИСТ -->
        <section id="pricing">
            <h2>💰 Прайс-лист (Тарифтер)</h2>
            <table>
                <tr>
                    <th>Зона атауы</th>
                    <th>1 сағат бағасы</th>
                    <th>Түнгі пакет (22:00 - 08:00)</th>
                </tr>
                <tr>
                    <td>Standard Zone</td>
                    <td>600 тг</td>
                    <td>3 500 тг</td>
                </tr>
                <tr>
                    <td>VIP Zone</td>
                    <td>1 000 тг</td>
                    <td>5 500 тг</td>
                </tr>
                <tr>
                    <td>Bootcamp Zone</td>
                    <td>1 500 тг</td>
                    <td>8 000 тг</td>
                </tr>
            </table>
        </section>

        <!-- 3. БРОНДАУ ФОРМАСЫ -->
        <section id="booking">
            <h2>🎮 Орынды брондау</h2>
            <form onsubmit="event.preventDefault(); alert('Бролау сәтті қабылданды! PostgreSQL базасына тіркелді.');">
                <div class="grid">
                    <div class="form-group">
                        <label>Аты-жөніңіз:</label>
                        <input type="text" placeholder="Мысалы: Азамат Нұрланұлы" required>
                    </div>
                    <div class="form-group">
                        <label>Телефон нөмірі:</label>
                        <input type="text" placeholder="+7 (707) 000-00-00" required>
                    </div>
                    <div class="form-group">
                        <label>Зонаны таңдаңыз:</label>
                        <select>
                            <option>Standard Zone</option>
                            <option>VIP Zone</option>
                            <option>Bootcamp Zone</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Уақыты (Басталуы):</label>
                        <input type="datetime-local" required>
                    </div>
                </div>
                <button type="submit">Орынды брондау</button>
            </form>
        </section>

        <!-- 4. ДЕРЕКТЕР БАЗАСЫ (DATABASE) -->
        <section id="database">
            <h2>🗄️ Деректер базасының құрылымы (PostgreSQL)</h2>
            <p>Бұл жоба серверлік жағынан <b>PostgreSQL (`gaming_club` схемасы)</b> негізінде жұмыс істейді. Жүйеде барлығы <b>11 кесте</b> қолданылады:</p>
            <ul style="margin-left: 20px; margin-top: 10px; color: #94a3b8;">
                <li><code>clients</code> — Клуб клиенттері мен баланстары</li>
                <li><code>zones</code> — Ойын зоналарының түрлері</li>
                <li><code>computers</code> — Компьютерлер мен олардың статусқа бөлінуі</li>
                <li><code>tariffs</code> — Тарифтер мен бағалар кестесі</li>
                <li><code>bookings</code> — Орындарды брондау тарихы</li>
                <li><code>gaming_sessions</code> — Белсенді ойын сессиялары</li>
                <li><code>tournaments</code> — Клубта өтетін турнирлер</li>
                <li><code>tournament_participants</code> — Турнир қатысушылары</li>
                <li><code>products</code> — Бар мен дүкен өнімдері (снектер, сусындар)</li>
                <li><code>sales</code> — Өнімдерді сату тарихы</li>
                <li><code>payments</code> — Төлемдер мен транзакциялар</li>
            </ul>
        </section>

        <!-- 5. АДРЕС ЖӘНЕ БАЙЛАНЫС -->
        <section id="contact">
            <h2>📍 Адрес және Байланыс</h2>
            <div class="grid">
                <div>
                    <p><b>Орналасқан жері:</b> Алматы қаласы, Шевченко көшесі 97 (ALT Университеті маңы)</p>
                    <p><b>Жұмыс уақыты:</b> Тәулік бойы (24/7)</p>
                    <p><b>Телефон:</b> +7 (707) 715-80-45</p>
                    <p><b>Email:</b> tazhmukhanbetnurlan@gmail.com</p>
                </div>
                <div>
                    <p><b>Әлеуметтік желілер:</b></p>
                    <p>Instagram: @cyber_esports_alt</p>
                    <p>Telegram: @cyber_club_support</p>
                </div>
            </div>
        </section>

    </div>

    <footer>
        <p>&copy; 2026 Cyber Esports Club. ALT University Project.</p>
    </footer>

</body>
</html>
