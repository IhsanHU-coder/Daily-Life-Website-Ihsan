<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Panduan Setup — Daily Life Ihsan</title>
<style>
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;background:#F8F7F4;color:#1A1916;line-height:1.6;}
.top{background:#1A1916;color:#F8F7F4;padding:2rem 1.5rem;text-align:center;}
.top h1{font-size:24px;margin-bottom:6px;}
.top p{font-size:14px;opacity:.6;}
.wrap{max-width:760px;margin:0 auto;padding:2rem 1.25rem 4rem;}
.phase{background:#fff;border:1px solid #E5E2DA;border-radius:14px;margin-bottom:1.5rem;overflow:hidden;}
.phase-head{padding:1.25rem 1.5rem;display:flex;align-items:center;gap:14px;border-bottom:1px solid #F2F0EC;cursor:pointer;user-select:none;}
.phase-num{width:36px;height:36px;border-radius:50%;background:#1A1916;color:#F8F7F4;font-size:15px;font-weight:600;display:flex;align-items:center;justify-content:center;flex-shrink:0;}
.phase-num.done{background:#27724A;}
.phase-num.warn{background:#9A7C0A;}
.phase-title{font-size:16px;font-weight:600;flex:1;}
.phase-sub{font-size:13px;color:#A09D98;}
.phase-arrow{font-size:18px;color:#A09D98;transition:transform .2s;}
.phase-arrow.open{transform:rotate(180deg);}
.phase-body{padding:1.5rem;display:none;}
.phase-body.open{display:block;}
.step{display:flex;gap:14px;margin-bottom:1.25rem;}
.step:last-child{margin-bottom:0;}
.step-n{width:26px;height:26px;border-radius:50%;background:#EBF2FC;border:1px solid #B5D4F4;color:#1A4A8A;font-size:12px;font-weight:600;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;}
.step-body{flex:1;}
.step-body strong{display:block;font-size:14px;margin-bottom:4px;}
.step-body p,.step-body li{font-size:13px;color:#6B6860;margin-bottom:4px;}
.step-body ul{padding-left:16px;}
.step-body ul li{margin-bottom:3px;}
code{background:#F2F0EC;border:1px solid #E5E2DA;border-radius:5px;padding:2px 7px;font-size:12px;font-family:'Courier New',monospace;color:#1A1916;}
.code-block{background:#1A1916;color:#E8E4DC;border-radius:10px;padding:1rem 1.25rem;font-size:12px;font-family:'Courier New',monospace;margin:10px 0;overflow-x:auto;white-space:pre;line-height:1.7;}
.code-block .cm{color:#6B8A6B;}
.code-block .ck{color:#7EC8E3;}
.code-block .cv{color:#E8C87A;}
.code-block .hi{color:#FF9E64;font-weight:bold;}
.img-box{background:#F2F0EC;border:1px solid #E5E2DA;border-radius:8px;padding:14px;margin:10px 0;font-size:13px;color:#6B6860;text-align:center;}
.img-box .ico{font-size:28px;margin-bottom:6px;}
.tag-ok{background:#E8F5EE;color:#27724A;border:1px solid #A8D8BC;border-radius:6px;padding:3px 10px;font-size:12px;font-weight:500;display:inline-block;margin-bottom:8px;}
.tag-warn{background:#FAF3D8;color:#9A7C0A;border:1px solid #D4B84A;border-radius:6px;padding:3px 10px;font-size:12px;font-weight:500;display:inline-block;margin-bottom:8px;}
.tag-info{background:#EBF2FC;color:#1A4A8A;border:1px solid #B5D4F4;border-radius:6px;padding:3px 10px;font-size:12px;font-weight:500;display:inline-block;margin-bottom:8px;}
.divider{height:1px;background:#F2F0EC;margin:1rem 0;}
.btn-copy{background:#1A1916;color:#F8F7F4;border:none;border-radius:7px;padding:8px 16px;font-size:13px;cursor:pointer;float:right;margin-bottom:6px;}
.btn-copy:hover{background:#333;}
.alert{background:#FAF3D8;border:1px solid #D4B84A;border-radius:8px;padding:12px 14px;font-size:13px;color:#6B5010;margin:10px 0;line-height:1.6;}
.alert strong{display:block;margin-bottom:3px;}
.success-box{background:#E8F5EE;border:1px solid #A8D8BC;border-radius:8px;padding:12px 14px;font-size:13px;color:#1A5C34;margin:10px 0;}
.link{color:#3B7FD4;text-decoration:underline;cursor:pointer;}
a{color:#3B7FD4;}
.faq-q{font-weight:600;font-size:14px;margin-top:1rem;margin-bottom:4px;}
.faq-a{font-size:13px;color:#6B6860;}
</style>
</head>
<body>

<div class="top">
  <h1>📋 Panduan Setup — Daily Life Ihsan</h1>
  <p>Ikuti langkah berikut dari atas ke bawah. Simpan file ini, tidak perlu internet untuk membacanya.</p>
</div>

<div class="wrap">

  <!-- OVERVIEW -->
  <div style="background:#EBF2FC;border:1px solid #B5D4F4;border-radius:12px;padding:1.25rem;margin-bottom:1.5rem;">
    <strong style="font-size:15px;color:#1A4A8A;">Apa yang akan kamu lakukan?</strong>
    <div style="margin-top:10px;display:grid;gap:8px;">
      <div style="font-size:13px;color:#1A4A8A;display:flex;gap:8px;align-items:flex-start;"><span>①</span><span>Buat project Firebase (database cloud gratis)</span></div>
      <div style="font-size:13px;color:#1A4A8A;display:flex;gap:8px;align-items:flex-start;"><span>②</span><span>Tempel kode Firebase ke file index.html</span></div>
      <div style="font-size:13px;color:#1A4A8A;display:flex;gap:8px;align-items:flex-start;"><span>③</span><span>Push ke GitHub → aktifkan GitHub Pages → website live</span></div>
      <div style="font-size:13px;color:#1A4A8A;display:flex;gap:8px;align-items:flex-start;"><span>④</span><span>Login dari HP dan laptop pakai akun yang sama — data sync otomatis</span></div>
    </div>
    <div style="margin-top:12px;font-size:12px;color:#3B7FD4;">⏱ Estimasi waktu: 20–30 menit</div>
  </div>

  <!-- FASE 1: FIREBASE PROJECT -->
  <div class="phase" id="ph1">
    <div class="phase-head" onclick="toggle('ph1')">
      <div class="phase-num">1</div>
      <div>
        <div class="phase-title">Buat Project Firebase</div>
        <div class="phase-sub">Daftar &amp; buat database cloud gratis</div>
      </div>
      <div class="phase-arrow" id="ph1-arrow">▼</div>
    </div>
    <div class="phase-body open" id="ph1-body">

      <div class="step">
        <div class="step-n">1</div>
        <div class="step-body">
          <strong>Buka Firebase Console</strong>
          <p>Pergi ke <a href="https://console.firebase.google.com" target="_blank">console.firebase.google.com</a></p>
          <p>Login dengan akun Google kamu (pakai akun yang sama yang mau jadi admin).</p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">2</div>
        <div class="step-body">
          <strong>Klik "Add project" / "Tambahkan project"</strong>
          <div class="img-box"><div class="ico">➕</div>Tombol biru besar di halaman utama Firebase Console</div>
          <ul>
            <li>Beri nama project, contoh: <code>daily-life-ihsan</code></li>
            <li>Google Analytics: boleh dimatikan (pilih "Not right now")</li>
            <li>Klik <strong>Create project</strong> → tunggu sebentar</li>
          </ul>
        </div>
      </div>

      <div class="step">
        <div class="step-n">3</div>
        <div class="step-body">
          <strong>Daftarkan Web App — dapatkan kode config</strong>
          <p>Di halaman project, klik ikon <code>&lt;/&gt;</code> (Web) untuk menambahkan web app.</p>
          <div class="img-box"><div class="ico">🌐</div>Ikon &lt;/&gt; ada di bagian "Get started by adding Firebase to your app"</div>
          <ul>
            <li>App nickname: <code>daily-ihsan-web</code> (bebas)</li>
            <li>❌ Jangan centang "Firebase Hosting" (kita pakai GitHub Pages)</li>
            <li>Klik <strong>Register app</strong></li>
          </ul>
          <p style="margin-top:8px;">Kamu akan lihat kode seperti ini — <strong>copy seluruh isinya</strong>:</p>
          <div class="code-block"><span class="ck">const</span> <span class="cv">firebaseConfig</span> = {
  <span class="cv">apiKey</span>: <span class="hi">"AIzaSy..."</span>,
  <span class="cv">authDomain</span>: <span class="hi">"daily-life-ihsan.firebaseapp.com"</span>,
  <span class="cv">projectId</span>: <span class="hi">"daily-life-ihsan"</span>,
  <span class="cv">storageBucket</span>: <span class="hi">"daily-life-ihsan.appspot.com"</span>,
  <span class="cv">messagingSenderId</span>: <span class="hi">"123456789"</span>,
  <span class="cv">appId</span>: <span class="hi">"1:123456..."</span>
};</div>
          <div class="alert"><strong>⚠ Penting!</strong> Simpan kode ini di Notepad/Notes HP kamu. Kamu perlu ini di Langkah selanjutnya.</div>
        </div>
      </div>

    </div>
  </div>

  <!-- FASE 2: FIRESTORE DATABASE -->
  <div class="phase" id="ph2">
    <div class="phase-head" onclick="toggle('ph2')">
      <div class="phase-num">2</div>
      <div>
        <div class="phase-title">Aktifkan Firestore Database</div>
        <div class="phase-sub">Tempat data disimpan di cloud</div>
      </div>
      <div class="phase-arrow" id="ph2-arrow">▼</div>
    </div>
    <div class="phase-body" id="ph2-body">

      <div class="step">
        <div class="step-n">1</div>
        <div class="step-body">
          <strong>Pergi ke Firestore</strong>
          <p>Di sidebar kiri Firebase Console → klik <strong>Build</strong> → <strong>Firestore Database</strong></p>
          <p>Klik tombol <strong>"Create database"</strong></p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">2</div>
        <div class="step-body">
          <strong>Pilih mode &amp; lokasi</strong>
          <ul>
            <li>Mode: pilih <strong>"Start in production mode"</strong></li>
            <li>Location: pilih <strong>asia-southeast1</strong> (Singapore, paling dekat)</li>
            <li>Klik <strong>Enable</strong></li>
          </ul>
        </div>
      </div>

      <div class="step">
        <div class="step-n">3</div>
        <div class="step-body">
          <strong>Set Security Rules (WAJIB)</strong>
          <p>Di halaman Firestore → klik tab <strong>Rules</strong> → hapus semua teks yang ada → tempel kode berikut:</p>
          <div class="code-block"><span class="ck">rules_version</span> = <span class="hi">'2'</span>;
<span class="ck">service</span> cloud.firestore {
  match /databases/{database}/documents {

    <span class="cm">// Data harian hanya bisa diakses pemiliknya</span>
    match /days/{docId} {
      allow read, write: if request.auth != null
        &amp;&amp; (resource == null || resource.data.uid == request.auth.uid)
        &amp;&amp; docId.matches(request.auth.uid + <span class="hi">'_.*'</span>);
    }

    <span class="cm">// Profil user hanya bisa dibaca/ditulis sendiri</span>
    match /users/{userId} {
      allow read, write: if request.auth != null
        &amp;&amp; request.auth.uid == userId;
    }

    <span class="cm">// Daftar email yang diizinkan (admin bisa write, semua auth bisa read)</span>
    match /allowed/{docId} {
      allow read: if request.auth != null;
      allow write: if request.auth != null
        &amp;&amp; request.auth.token.email == <span class="hi">"GANTI_EMAIL_ADMIN_KAMU@gmail.com"</span>;
    }
  }
}</div>
          <div class="alert"><strong>⚠ Ganti dulu!</strong> Pada baris terakhir, ganti <code>GANTI_EMAIL_ADMIN_KAMU@gmail.com</code> dengan email Google kamu yang asli sebelum klik Publish.</div>
          <p>Klik <strong>Publish</strong> setelah selesai edit.</p>
        </div>
      </div>

    </div>
  </div>

  <!-- FASE 3: FIREBASE AUTH -->
  <div class="phase" id="ph3">
    <div class="phase-head" onclick="toggle('ph3')">
      <div class="phase-num">3</div>
      <div>
        <div class="phase-title">Aktifkan Firebase Authentication</div>
        <div class="phase-sub">Sistem login email &amp; Google</div>
      </div>
      <div class="phase-arrow" id="ph3-arrow">▼</div>
    </div>
    <div class="phase-body" id="ph3-body">

      <div class="step">
        <div class="step-n">1</div>
        <div class="step-body">
          <strong>Buka Authentication</strong>
          <p>Di sidebar → <strong>Build</strong> → <strong>Authentication</strong> → klik <strong>"Get started"</strong></p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">2</div>
        <div class="step-body">
          <strong>Aktifkan Email/Password</strong>
          <p>Tab <strong>Sign-in method</strong> → klik <strong>Email/Password</strong> → toggle <strong>Enable</strong> → klik <strong>Save</strong></p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">3</div>
        <div class="step-body">
          <strong>Aktifkan Google Login (opsional tapi direkomendasikan)</strong>
          <p>Masih di Sign-in method → klik <strong>Google</strong> → toggle <strong>Enable</strong></p>
          <p>Isi <strong>Project support email</strong> dengan email kamu → klik <strong>Save</strong></p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">4</div>
        <div class="step-body">
          <strong>Tambahkan Authorized Domain</strong>
          <p>Tab <strong>Settings</strong> → <strong>Authorized domains</strong></p>
          <p>Klik <strong>Add domain</strong> → masukkan domain GitHub Pages kamu:</p>
          <div class="code-block">USERNAME.github.io</div>
          <p style="font-size:12px;color:#A09D98;">(Ganti USERNAME dengan username GitHub kamu. Contoh: <code>ihsan123.github.io</code>)</p>
          <div class="alert"><strong>Kalau belum tahu username GitHub:</strong> buat dulu akun GitHub di langkah berikutnya, baru balik ke sini untuk tambahkan domain.</div>
        </div>
      </div>

    </div>
  </div>

  <!-- FASE 4: EDIT index.html -->
  <div class="phase" id="ph4">
    <div class="phase-head" onclick="toggle('ph4')">
      <div class="phase-num warn">4</div>
      <div>
        <div class="phase-title">Edit File index.html</div>
        <div class="phase-sub">Tempel kode Firebase ke dalam file website</div>
      </div>
      <div class="phase-arrow" id="ph4-arrow">▼</div>
    </div>
    <div class="phase-body" id="ph4-body">

      <div class="alert"><strong>Ini bagian terpenting.</strong> Buka file <code>index.html</code> dengan teks editor. Bisa pakai Notepad (Windows), TextEdit (Mac), atau VS Code.</div>

      <div class="step">
        <div class="step-n">1</div>
        <div class="step-body">
          <strong>Cari bagian konfigurasi Firebase</strong>
          <p>Gunakan Ctrl+F (Find) di text editor, cari teks:</p>
          <div class="code-block">GANTI_API_KEY</div>
          <p>Kamu akan menemukan blok ini:</p>
          <div class="code-block"><span class="ck">const</span> <span class="cv">firebaseConfig</span> = {
  <span class="cv">apiKey</span>:            <span class="hi">"GANTI_API_KEY"</span>,
  <span class="cv">authDomain</span>:        <span class="hi">"GANTI_AUTH_DOMAIN"</span>,
  <span class="cv">projectId</span>:         <span class="hi">"GANTI_PROJECT_ID"</span>,
  <span class="cv">storageBucket</span>:     <span class="hi">"GANTI_STORAGE_BUCKET"</span>,
  <span class="cv">messagingSenderId</span>: <span class="hi">"GANTI_SENDER_ID"</span>,
  <span class="cv">appId</span>:             <span class="hi">"GANTI_APP_ID"</span>
};</div>
          <p>Ganti seluruh blok ini dengan kode yang kamu copy dari Firebase Console di Fase 1 langkah 3.</p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">2</div>
        <div class="step-body">
          <strong>Ganti email admin</strong>
          <p>Cari baris ini (satu baris saja):</p>
          <div class="code-block">const ADMIN_EMAIL = <span class="hi">"emailkamu@gmail.com"</span>;</div>
          <p>Ganti <code>emailkamu@gmail.com</code> dengan email Google kamu yang asli.</p>
          <div class="alert"><strong>Email ini harus sama persis</strong> dengan email Google yang kamu pakai untuk login ke Firebase Console.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-n">3</div>
        <div class="step-body">
          <strong>Simpan file</strong>
          <p>Ctrl+S (Windows) / Cmd+S (Mac) → file sudah siap.</p>
          <div class="success-box">✓ File index.html sudah siap di-deploy!</div>
        </div>
      </div>

    </div>
  </div>

  <!-- FASE 5: GITHUB -->
  <div class="phase" id="ph5">
    <div class="phase-head" onclick="toggle('ph5')">
      <div class="phase-num">5</div>
      <div>
        <div class="phase-title">Push ke GitHub &amp; Aktifkan GitHub Pages</div>
        <div class="phase-sub">Buat website online &amp; bisa diakses dari mana saja</div>
      </div>
      <div class="phase-arrow" id="ph5-arrow">▼</div>
    </div>
    <div class="phase-body" id="ph5-body">

      <div class="step">
        <div class="step-n">1</div>
        <div class="step-body">
          <strong>Buat akun GitHub (kalau belum punya)</strong>
          <p>Pergi ke <a href="https://github.com" target="_blank">github.com</a> → Sign up → verifikasi email.</p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">2</div>
        <div class="step-body">
          <strong>Buat repository baru</strong>
          <p>Klik tombol <strong>"+"</strong> di pojok kanan atas → <strong>New repository</strong></p>
          <ul>
            <li>Repository name: <code>daily-ihsan</code></li>
            <li>Visibility: <strong>Public</strong> (wajib untuk GitHub Pages gratis)</li>
            <li>✅ Centang <strong>"Add a README file"</strong></li>
            <li>Klik <strong>Create repository</strong></li>
          </ul>
        </div>
      </div>

      <div class="step">
        <div class="step-n">3</div>
        <div class="step-body">
          <strong>Upload file index.html</strong>
          <p>Di halaman repository → klik <strong>Add file</strong> → <strong>Upload files</strong></p>
          <div class="img-box"><div class="ico">📁</div>Drag &amp; drop file index.html ke area upload, atau klik "choose your files"</div>
          <p>Scroll ke bawah → klik <strong>Commit changes</strong></p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">4</div>
        <div class="step-body">
          <strong>Aktifkan GitHub Pages</strong>
          <p>Di repository → klik tab <strong>Settings</strong> (pojok kanan atas)</p>
          <p>Di sidebar kiri → klik <strong>Pages</strong></p>
          <ul>
            <li>Source: pilih <strong>Deploy from a branch</strong></li>
            <li>Branch: pilih <strong>main</strong>, folder <strong>/ (root)</strong></li>
            <li>Klik <strong>Save</strong></li>
          </ul>
          <p style="margin-top:8px;">Tunggu 1–2 menit. Refresh halaman. Website kamu live di:</p>
          <div class="code-block">https://<span class="hi">USERNAME</span>.github.io/<span class="hi">daily-ihsan</span>/</div>
          <div class="success-box">✓ Website sudah online! Buka URL di atas dari HP atau laptop mana saja.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-n">5</div>
        <div class="step-body">
          <strong>Update file di masa depan</strong>
          <p>Kalau mau update index.html (misalnya ganti sesuatu):</p>
          <ul>
            <li>Buka repository di GitHub</li>
            <li>Klik file <code>index.html</code> → klik ikon pensil ✏ (Edit)</li>
            <li>Atau: Upload ulang file baru via <strong>Add file → Upload files</strong></li>
            <li>Commit → GitHub Pages otomatis update dalam 1–2 menit</li>
          </ul>
        </div>
      </div>

    </div>
  </div>

  <!-- FASE 6: LOGIN PERTAMA -->
  <div class="phase" id="ph6">
    <div class="phase-head" onclick="toggle('ph6')">
      <div class="phase-num done">6</div>
      <div>
        <div class="phase-title">Login Pertama &amp; Tes Website</div>
        <div class="phase-sub">Daftar akun admin, coba dari HP</div>
      </div>
      <div class="phase-arrow" id="ph6-arrow">▼</div>
    </div>
    <div class="phase-body" id="ph6-body">

      <div class="step">
        <div class="step-n">1</div>
        <div class="step-body">
          <strong>Buka website di browser</strong>
          <p>Pergi ke <code>https://USERNAME.github.io/daily-ihsan/</code></p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">2</div>
        <div class="step-body">
          <strong>Daftar akun admin (sekali saja)</strong>
          <p>Klik tab <strong>Daftar</strong> di halaman login.</p>
          <ul>
            <li>Nama: nama kamu</li>
            <li>Email: email yang sama dengan <code>ADMIN_EMAIL</code> di index.html</li>
            <li>Kata sandi: buat sandi kamu (min. 6 karakter)</li>
          </ul>
          <p>Klik <strong>Buat Akun</strong> → kamu langsung masuk sebagai Admin.</p>
          <div class="success-box">✓ Kamu sekarang punya akun admin! Icon Admin muncul di topbar dan menu Admin ada di nav bawah.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-n">3</div>
        <div class="step-body">
          <strong>Tes dari HP</strong>
          <p>Buka URL yang sama dari HP kamu. Login dengan email &amp; sandi yang sama.</p>
          <p>Data checklist, habit, dan notes kamu akan <strong>sync otomatis</strong> antar perangkat!</p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">4</div>
        <div class="step-body">
          <strong>Tambahkan ke Home Screen HP (opsional)</strong>
          <p><strong>Android (Chrome):</strong> Buka website → ketuk ⋮ menu → <strong>Add to Home screen</strong></p>
          <p><strong>iPhone (Safari):</strong> Buka website → ketuk ↑ share → <strong>Add to Home Screen</strong></p>
          <div class="success-box">✓ Website jadi seperti app di HP kamu, lengkap dengan icon!</div>
        </div>
      </div>

    </div>
  </div>

  <!-- FASE 7: TAMBAH PENGGUNA -->
  <div class="phase" id="ph7">
    <div class="phase-head" onclick="toggle('ph7')">
      <div class="phase-num">7</div>
      <div>
        <div class="phase-title">Menambah Pengguna Lain (Opsional)</div>
        <div class="phase-sub">Izinkan orang lain mendaftar ke aplikasi kamu</div>
      </div>
      <div class="phase-arrow" id="ph7-arrow">▼</div>
    </div>
    <div class="phase-body" id="ph7-body">

      <div class="step">
        <div class="step-n">1</div>
        <div class="step-body">
          <strong>Login sebagai Admin</strong>
          <p>Buka website → login dengan akun admin kamu.</p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">2</div>
        <div class="step-body">
          <strong>Pergi ke panel Admin</strong>
          <p>Klik ikon ⚙ <strong>Admin</strong> di navbar bawah.</p>
        </div>
      </div>

      <div class="step">
        <div class="step-n">3</div>
        <div class="step-body">
          <strong>Tambah email yang diizinkan</strong>
          <p>Masukkan email orang yang mau diberi akses → pilih role <strong>User</strong> → klik <strong>Tambah</strong>.</p>
          <p>Sekarang orang itu bisa mendaftar dengan email tersebut di halaman Daftar.</p>
          <div class="tag-info">💡 Setiap user punya data sendiri-sendiri. Data kamu tidak tercampur dengan data orang lain.</div>
        </div>
      </div>

    </div>
  </div>

  <!-- FAQ -->
  <div class="phase" id="ph8">
    <div class="phase-head" onclick="toggle('ph8')">
      <div class="phase-num">?</div>
      <div>
        <div class="phase-title">Troubleshooting &amp; FAQ</div>
        <div class="phase-sub">Solusi masalah umum</div>
      </div>
      <div class="phase-arrow" id="ph8-arrow">▼</div>
    </div>
    <div class="phase-body" id="ph8-body">

      <div class="faq-q">❓ Website muncul tapi tidak bisa login, muncul error Firebase</div>
      <div class="faq-a">Cek apakah <code>firebaseConfig</code> di index.html sudah benar. Coba buka DevTools (F12) → tab Console, baca pesan error-nya.</div>

      <div class="faq-q">❓ Login Google muncul popup tapi langsung tutup / error</div>
      <div class="faq-a">Pastikan domain <code>USERNAME.github.io</code> sudah ditambahkan di Firebase Authentication → Settings → Authorized domains (Fase 3 langkah 4).</div>

      <div class="faq-q">❓ Daftar akun berhasil tapi tidak bisa login</div>
      <div class="faq-a">Pastikan email yang dipakai daftar sama persis dengan <code>ADMIN_EMAIL</code> di kode (untuk admin), atau sudah ditambahkan di panel Admin (untuk user biasa).</div>

      <div class="faq-q">❓ Data tidak sync ke HP / laptop lain</div>
      <div class="faq-a">Login dengan akun yang sama di semua device. Data disimpan per-user per-hari di Firestore, jadi selama login dengan akun sama, data akan sama.</div>

      <div class="faq-q">❓ Website bisa dibuka tapi layar putih kosong</div>
      <div class="faq-a">Buka DevTools (F12) → Console. Kemungkinan ada typo di firebaseConfig. Cek tanda kutip dan koma tidak ada yang hilang.</div>

      <div class="faq-q">❓ Bagaimana cara ubah checklist / habit default?</div>
      <div class="faq-a">Buka <code>index.html</code> → cari <code>const DC =</code> (checklist) dan <code>const DH =</code> (habits) → ubah isi arraynya → save → upload ulang ke GitHub.</div>

      <div class="faq-q">❓ Apakah Firebase gratis?</div>
      <div class="faq-a">Ya! Firebase Spark Plan (gratis) memberikan 1GB storage Firestore, 50.000 reads &amp; 20.000 writes per hari. Untuk penggunaan pribadi 1–5 orang, ini lebih dari cukup.</div>

      <div class="faq-q">❓ Bagaimana cara update website kalau mau ubah sesuatu?</div>
      <div class="faq-a">Edit file <code>index.html</code> → upload ke GitHub (Add file → Upload files) → GitHub Pages otomatis update. Atau klik nama file di GitHub → klik ✏ edit langsung di browser.</div>

      <div class="divider"></div>

      <div style="background:#F2F0EC;border-radius:8px;padding:14px;font-size:13px;color:#6B6860;">
        <strong style="color:#1A1916;display:block;margin-bottom:6px;">📁 File yang kamu butuhkan</strong>
        <p>• <code>index.html</code> — file website utama (yang sudah kamu download)</p>
        <p>• <code>PANDUAN.html</code> — file panduan ini (simpan offline)</p>
        <p style="margin-top:8px;">Simpan kedua file ini di folder yang aman di komputer kamu.</p>
      </div>

    </div>
  </div>

  <div style="text-align:center;font-size:13px;color:#A09D98;margin-top:2rem;">
    Daily Life Ihsan — Dibuat dengan penuh semangat 💪<br>
    Simpan file PANDUAN.html ini, bisa dibuka offline kapan saja.
  </div>

</div>

<script>
function toggle(id) {
  const body = document.getElementById(id+'-body');
  const arrow = document.getElementById(id+'-arrow');
  const isOpen = body.classList.contains('open');
  body.classList.toggle('open', !isOpen);
  arrow.classList.toggle('open', !isOpen);
}
// Open phase 1 by default
document.getElementById('ph1-arrow').classList.add('open');
</script>
</body>
</html>
