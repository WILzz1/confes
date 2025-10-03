
<html lang="id">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Ungkap Cinta — Suratkecil</title>
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root{ --rose:#ff4d7e; --soft:#fff0f6; --deep:#3b2b4a; }
    body{ font-family: 'Poppins', system-ui, -apple-system, 'Segoe UI', Roboto, Arial; background: linear-gradient(180deg,#fffafa 0%, #fff6fb 100%); color:var(--deep); }
    .hero{ padding:4rem 0; }
    .card-love{ border:0; border-radius:14px; background:linear-gradient(180deg, rgba(255,77,126,0.06), #fff); box-shadow:0 10px 30px rgba(59,43,74,0.06); }
    .heart-anim{ width:110px; height:110px; display:inline-block; background:radial-gradient(circle at 30% 30%, #fff6 0%, transparent 40%); border-radius:50%; position:relative; }
    .heart-anim::before,.heart-anim::after{ content:''; position:absolute; left:50%; top:30%; width:60px; height:90px; background:var(--rose); border-radius:60px 60px 0 0; transform-origin:50% 100%; }
    .heart-anim::before{ transform:translateX(-50%) rotate(-45deg); }
    .heart-anim::after{ transform:translateX(-50%) rotate(45deg); }
    .pulse{ animation:pulse 1.2s infinite; }
    @keyframes pulse{ 0%{ transform:scale(1); } 50%{ transform:scale(1.06);} 100%{ transform:scale(1);} }
    .cta{ background:linear-gradient(90deg,var(--rose), #ff85b7); color:#fff; border-radius:999px; padding:.6rem 1.2rem; border:0; }
    .note{ font-size:.95rem; color:#6b536d; }
    .card-preview{ min-height:180px; }
    .floating-heart{ position:fixed; right:18px; bottom:18px; width:60px; height:60px; border-radius:50%; display:flex; align-items:center; justify-content:center; box-shadow:0 8px 20px rgba(255,77,126,0.12); }
    .print-hidden{ display:none; }

    @media print{ .no-print{ display:none !important; } .print-hidden{ display:block !important; } }
  </style>
</head>
<body>
  <header class="container py-3">
    <nav class="d-flex justify-content-between align-items-center">
      <h3 class="m-0">confes untuk mu my honey fey</h3>
      <small class="text-muted">simpan yaa sayangg</small>
    </nav>
  </header>

  <main class="container hero">
    <div class="row g-4">
      <div class="col-md-6">
        <div class="card p-4 card-love">
          <div class="d-flex align-items-center gap-3">
            <div class="heart-anim pulse"></div>
            <div>
              <h4 class="mb-1">From :Lyly</h4>
              <p class="note mb-0">Dear sayangg ku, maap aku membuat kamu marah hehehe, ini hadiah ku untuk mu</p>
            </div>
          </div>

          <form id="loveForm" class="mt-3">
            <div class="mb-2">
              <label class="form-label">Untuk</label>
              <input id="toInput" type="text" class="form-control" placeholder="my baby honey feyy" value="Sayangku">
            </div>
            <div class="mb-2">
              <label class="form-label">Pesan</label>
              <textarea id="msgInput" rows="5" class="form-control" placeholder="Tulis dari hati...">“Aku bilang sekarang karena kalau aku simpan lebih lama, takutnya hatiku meledak kayak balon.Aku bilang ini karena aku nyaman banget sama kamu, dan aku takut kalau aku terus simpan malah jadi beban buat aku sendiri.Dan aku takut jika tidak mengungkap kan nya sekarang kamu sama orang lain."</textarea>
            </div>
            <div class="mb-3 d-flex gap-2">
              <select id="styleSelect" class="form-select w-auto">
                <option value="classic">Klasik</option>
                <option value="poetic">Puitis</option>
                <option value="funny">Lucu </option>
                <option value="funny">Baca dulu yang atas ya sayang </option>
              </select>
              <button type="button" class="cta" id="previewBtn">Pratinjau</button>
              <button type="button" class="btn btn-outline-secondary" id="copyBtn">Salin</button>
            </div>
          </form>

          <div class="mt-2 text-muted small">Tip: klik <strong>Pratinjau</strong> untuk melihat kartu, lalu pilih <strong>Cetak</strong> atau <strong>Kirim</strong>.</div>
        </div>
      </div>

      <div class="col-md-6">
        <div class="card p-3 card-love">
          <div class="d-flex justify-content-between align-items-center mb-2">
            <h5 class="m-0">Kartu Pratinjau</h5>
            <div class="d-flex gap-2 no-print">
              <button id="printBtn" class="btn btn-sm btn-outline-primary">Cetak</button>
              <button id="emailBtn" class="btn btn-sm btn-outline-success">Kirim Email</button>
            </div>
          </div>

          <div id="preview" class="border rounded-3 p-3 card-preview" style="background:linear-gradient(180deg,#fff,#fff9fb);">
            <h6 id="pTo">Untuk: <span class="fw-semibold">Sayangku</span></h6>
            <div id="pMsg" style="white-space:pre-wrap;">would be mine?.</div>
            <div class="mt-3 text-end text-muted">— <span id="pFrom">Me</span></div>
          </div>

          <div class="mt-3 d-flex gap-2">
            <button id="downloadBtn" class="btn btn-outline-secondary">Unduh .txt</button>
            <button id="shareBtn" class="btn btn-primary ms-auto">Bagikan (salin link)</button>
          </div>
        </div>
      </div>
    </div>

    <section class="mt-4">
      <div class="row">
        <div class="col-md-4">
          <div class="card p-3 card-love">
            <h6>for u versi singkat</h6>
            <p class="mb-0">"Kau membuat hari-hariku lebih terang. Terima kasih sudah ada."</p>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card p-3 card-love">
            <h6>for u versi lucu</h6>
            <p class="mb-0">"“Kamu itu mirip sandal jepit. Kalau nggak ada, aku pasti kelabakan ke mana-mana.”"</p>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card p-3 card-love">
            <h6>for u versi hati</h6>
            <p class="mb-0">"would be mine my baby honey feyy?."</p>
          </div>
        </div>
      </div>
    </section>

  </main>

  <div class="floating-heart no-print" id="floatHeart" title="Halo!">❤</div>

  <footer class="container py-4 text-center text-muted small no-print">© 2025 Ungkap Cinta — From Lyly dibuat dengan sepenuh hati</footer>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    // Elements
    const toInput = document.getElementById('toInput');
    const msgInput = document.getElementById('msgInput');
    const styleSelect = document.getElementById('styleSelect');
    const previewBtn = document.getElementById('previewBtn');
    const pTo = document.getElementById('pTo');
    const pMsg = document.getElementById('pMsg');
    const pFrom = document.getElementById('pFrom');
    const copyBtn = document.getElementById('copyBtn');
    const downloadBtn = document.getElementById('downloadBtn');
    const emailBtn = document.getElementById('emailBtn');
    const printBtn = document.getElementById('printBtn');
    const shareBtn = document.getElementById('shareBtn');

    function applyStyle(text, style){
      if(style === 'poetic') return text + '\n\nSetiap kata ini kugoreskan dari rinduku.';
      if(style === 'funny') return text + '\n\nPS: Jangan lupa bawa cemilan ya :)';
      return text; // classic
    }

    function updatePreview(){
      const to = toInput.value || 'Sayangku';
      let msg = msgInput.value || '';
      msg = applyStyle(msg, styleSelect.value);
      pTo.innerHTML = `Untuk: <span class="fw-semibold">${escapeHtml(to)}</span>`;
      pMsg.textContent = msg;
      pFrom.textContent = 'Aku';
    }

    previewBtn.addEventListener('click', ()=>{ updatePreview(); });
    toInput.addEventListener('input', updatePreview);
    msgInput.addEventListener('input', updatePreview);
    styleSelect.addEventListener('change', updatePreview);

    copyBtn.addEventListener('click', async ()=>{
      updatePreview();
      const text = `${toInput.value}\n\n${applyStyle(msgInput.value, styleSelect.value)}\n\n— Aku`;
      try{ await navigator.clipboard.writeText(text); alert('Teks berhasil disalin!'); }
      catch(e){ alert('Gagal menyalin. Silakan salin manual.'); }
    });

    downloadBtn.addEventListener('click', ()=>{
      const content = `Untuk: ${toInput.value}\n\n${applyStyle(msgInput.value, styleSelect.value)}\n\n— Aku`;
      const blob = new Blob([content], {type:'text/plain'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a'); a.href = url; a.download = 'pesan_cinta.txt'; document.body.appendChild(a); a.click(); a.remove(); URL.revokeObjectURL(url);
    });

    emailBtn.addEventListener('click', ()=>{
      const subject = encodeURIComponent('Untukmu');
      const body = encodeURIComponent(`Untuk: ${toInput.value}\n\n${applyStyle(msgInput.value, styleSelect.value)}\n\n— Aku`);
      window.location.href = `mailto:?subject=${subject}&body=${body}`;
    });

    printBtn.addEventListener('click', ()=>{ window.print(); });

    shareBtn.addEventListener('click', ()=>{
      const text = `Untuk: ${toInput.value} -- ${msgInput.value}`;
      try{ navigator.clipboard.writeText(text); alert('Teks pratinjau disalin — bagikan di chat atau media sosial!'); }
      catch(e){ prompt('Salin teks berikut:', text); }
    });

    // Simple escape to avoid injecting HTML
    function escapeHtml(unsafe) {
      return unsafe.replace(/[&<>"']/g, function(m) { return ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":"&#039;"})[m]; });
    }

    // Init
    updatePreview();
  </script>
</body>
</html>
