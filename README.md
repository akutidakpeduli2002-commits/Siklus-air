<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🌊 Siklus Air di Bumi</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Animasi Hujan Background -->
    <div class="rain" id="rain"></div>

    <header>
        <h1>💧 Siklus Air di Bumi 🌍</h1>
        <p>Perjalanan Abadi Air dari Langit ke Bumi dan Kembali Lagi</p>
    </header>

    <div class="container">

        <!-- PENJELASAN SIKLUS AIR -->
        <section>
            <h2>Tahapan Siklus Air</h2>
            <div class="cycle-grid">
                <div class="cycle-card">
                    <span class="icon">☀️</span>
                    <h3>Evaporasi</h3>
                    <p>Air di laut, sungai, dan danau menguap karena panas matahari menjadi uap air.</p>
                </div>
                <div class="cycle-card">
                    <span class="icon">🌱</span>
                    <h3>Transpirasi</h3>
                    <p>Tumbuhan melepaskan uap air melalui daun ke atmosfer.</p>
                </div>
                <div class="cycle-card">
                    <span class="icon">☁️</span>
                    <h3>Kondensasi</h3>
                    <p>Uap air mendingin di udara dan berubah menjadi titik-titik air membentuk awan.</p>
                </div>
                <div class="cycle-card">
                    <span class="icon">🌧️</span>
                    <h3>Presipitasi</h3>
                    <p>Air jatuh ke bumi dalam bentuk hujan, salju, atau hujan es.</p>
                </div>
                <div class="cycle-card">
                    <span class="icon">🏞️</span>
                    <h3>Infiltrasi</h3>
                    <p>Air meresap ke dalam tanah menjadi air tanah yang menyuburkan tanaman.</p>
                </div>
                <div class="cycle-card">
                    <span class="icon">🌊</span>
                    <h3>Run Off</h3>
                    <p>Air mengalir di permukaan tanah menuju sungai, danau, dan akhirnya ke laut.</p>
                </div>
            </div>
        </section>

        <!-- ANGGOTA KELOMPOK -->
        <section>
            <h2>👥 Anggota Kelompok</h2>
            <div class="members">
                <div class="member">
                    <div class="name">Saffa</div>
                    <div class="role">Struktur HTML & Header</div>
                </div>
                <div class="member">
                    <div class="name">Kiran</div>
                    <div class="role">CSS Styling & Animasi</div>
                </div>
                <div class="member">
                    <div class="name">Hikmah</div>
                    <div class="role">Konten Materi Siklus Air</div>
                </div>
                <div class="member">
                    <div class="name">Yusuf</div>
                    <div class="role">Desain Kartu & Layout</div>
                </div>
                <div class="member">
                    <div class="name">Evan</div>
                    <div class="role">Footer & Responsif</div>
                </div>
            </div>
        </section>

        <!-- KUIS -->
        <section>
            <h2>🧠 Kuis Singkat</h2>
            <div id="quiz-box">
                <div id="quiz-question">Memuat soal...</div>
                <div class="quiz-options" id="quiz-options"></div>
                <div id="quiz-result"></div>
                <button id="next-btn" style="display:none;" onclick="nextQuestion()">Soal Berikutnya ➡️</button>
            </div>
        </section>

        <!-- GAME -->
        <section>
            <h2>🎮 Game: Tangkap Tetesan Air!</h2>
            <p style="text-align:center; margin-bottom:15px;">
                Gerakkan mouse (atau jari) untuk menggeser ember dan tangkap tetesan air sebanyak-banyaknya!
            </p>
            <div id="game-area">
                <div id="bucket"></div>
            </div>
            <div id="game-info">
                <span>💧 Skor: <b id="score">0</b></span>
                <span>⏱️ Waktu: <b id="timer">30</b>s</span>
                <span>❤️ Nyawa: <b id="lives">3</b></span>
            </div>
            <div style="text-align:center;">
                <button id="start-game" onclick="startGame()">▶️ Mulai Game</button>
            </div>
        </section>

    </div>

    <footer>
        <p>Dibuat dengan <span class="heart">♥</span> oleh Kelompok Siklus Air | © 2026</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

/* ===== 5 KODE RGB YANG DIGUNAKAN =====
   1. rgb(30, 144, 255)  -> Biru Air (DodgerBlue)
   2. rgb(135, 206, 250) -> Biru Langit Muda (LightSkyBlue)
   3. rgb(255, 215, 0)   -> Kuning Matahari (Gold)
   4. rgb(34, 139, 34)   -> Hijau Daun (ForestGreen)
   5. rgb(255, 255, 255) -> Putih Bersih (White)
*/

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, sans-serif;
}

body {
    background: linear-gradient(180deg, rgb(135, 206, 250) 0%, rgb(30, 144, 255) 100%);
    min-height: 100vh;
    color: rgb(255, 255, 255);
    overflow-x: hidden;
}

/* ===== HEADER ===== */
header {
    background: rgba(30, 144, 255, 0.85);
    padding: 25px;
    text-align: center;
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    position: relative;
    z-index: 10;
}

header h1 {
    font-size: 2.8em;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    animation: bounce 2s infinite;
}

header p {
    margin-top: 8px;
    font-size: 1.1em;
    font-style: italic;
}

@keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
}

/* ===== ANIMASI HUJAN DI BACKGROUND ===== */
.rain {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 1;
}

.drop {
    position: absolute;
    width: 3px;
    height: 15px;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 50%;
    animation: fall linear infinite;
}

@keyframes fall {
    0% { transform: translateY(-100vh); opacity: 1; }
    100% { transform: translateY(100vh); opacity: 0.3; }
}

/* ===== CONTAINER ===== */
.container {
    max-width: 1100px;
    margin: 30px auto;
    padding: 20px;
    position: relative;
    z-index: 5;
}

section {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(8px);
    border-radius: 20px;
    padding: 30px;
    margin-bottom: 30px;
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
    border: 2px solid rgba(255, 255, 255, 0.3);
}

section h2 {
    color: rgb(255, 215, 0);
    text-align: center;
    font-size: 2em;
    margin-bottom: 20px;
    text-shadow: 1px 1px 3px rgba(0,0,0,0.4);
}

/* ===== SIKLUS AIR (CARDS) ===== */
.cycle-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-top: 20px;
}

.cycle-card {
    background: linear-gradient(135deg, rgb(30, 144, 255), rgb(135, 206, 250));
    padding: 25px;
    border-radius: 15px;
    text-align: center;
    transition: transform 0.3s, box-shadow 0.3s;
    border: 3px solid rgb(255, 215, 0);
}

.cycle-card:hover {
    transform: translateY(-10px) rotate(-2deg);
    box-shadow: 0 15px 30px rgba(0,0,0,0.3);
}

.cycle-card .icon {
    font-size: 3.5em;
    margin-bottom: 10px;
    display: block;
}

.cycle-card h3 {
    color: rgb(255, 215, 0);
    margin-bottom: 10px;
}

/* ===== ANGGOTA KELOMPOK ===== */
.members {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 15px;
}

.member {
    background: rgb(34, 139, 34);
    padding: 20px;
    border-radius: 15px;
    text-align: center;
    transition: transform 0.3s;
    border: 3px solid rgb(255, 215, 0);
}

.member:hover {
    transform: scale(1.05);
}

.member .name {
    font-size: 1.4em;
    font-weight: bold;
    color: rgb(255, 215, 0);
    margin-bottom: 8px;
}

.member .role {
    font-size: 0.95em;
    color: rgb(255, 255, 255);
}

/* ===== KUIS ===== */
#quiz-box {
    background: rgba(255, 255, 255, 0.2);
    padding: 25px;
    border-radius: 15px;
    text-align: center;
}

#quiz-question {
    font-size: 1.3em;
    margin-bottom: 20px;
    font-weight: bold;
}

.quiz-options {
    display: grid;
    gap: 12px;
    margin-bottom: 20px;
}

.quiz-options button {
    padding: 12px;
    background: rgb(30, 144, 255);
    color: rgb(255, 255, 255);
    border: 2px solid rgb(255, 255, 255);
    border-radius: 10px;
    cursor: pointer;
    font-size: 1em;
    transition: all 0.3s;
}

.quiz-options button:hover {
    background: rgb(255, 215, 0);
    color: rgb(30, 144, 255);
    transform: scale(1.03);
}

#quiz-result {
    font-size: 1.2em;
    font-weight: bold;
    margin-top: 15px;
    min-height: 30px;
}

/* ===== GAME ===== */
#game-area {
    position: relative;
    width: 100%;
    height: 400px;
    background: linear-gradient(180deg, rgb(135, 206, 250) 0%, rgb(30, 144, 255) 100%);
    border-radius: 15px;
    overflow: hidden;
    border: 3px solid rgb(255, 215, 0);
    cursor: none;
}

#bucket {
    position: absolute;
    bottom: 10px;
    width: 80px;
    height: 60px;
    background: rgb(34, 139, 34);
    border: 3px solid rgb(255, 255, 255);
    border-radius: 0 0 10px 10px;
    left: 50%;
    transform: translateX(-50%);
    transition: left 0.1s;
}

.water-drop {
    position: absolute;
    width: 20px;
    height: 25px;
    background: rgb(255, 255, 255);
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
    box-shadow: 0 0 10px rgba(255,255,255,0.8);
}

#game-info {
    display: flex;
    justify-content: space-around;
    margin-top: 15px;
    font-size: 1.2em;
    font-weight: bold;
}

#game-info span {
    background: rgb(30, 144, 255);
    padding: 8px 20px;
    border-radius: 10px;
    border: 2px solid rgb(255, 215, 0);
}

#start-game, #next-btn {
    padding: 12px 30px;
    background: rgb(255, 215, 0);
    color: rgb(30, 144, 255);
    border: none;
    border-radius: 25px;
    font-size: 1.1em;
    font-weight: bold;
    cursor: pointer;
    margin-top: 15px;
    transition: transform 0.2s;
}

#start-game:hover, #next-btn:hover {
    transform: scale(1.1);
}

/* ===== FOOTER ===== */
footer {
    text-align: center;
    padding: 20px;
    background: rgba(0,0,0,0.3);
    color: rgb(255, 255, 255);
    margin-top: 30px;
}

footer .heart {
    color: rgb(255, 215, 0);
}

@media (max-width: 600px) {
    header h1 { font-size: 2em; }
    section h2 { font-size: 1.5em; }
    #game-area { height: 300px; }
}
