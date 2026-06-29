<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bài kiểm tra Từ vựng — Mùa Hè Cùng Ông Mặt Trời</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700;800&family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#FFF9EC;
    --bg-soft:#FFEFC7;
    --card:#FFFFFF;
    --brown-900:#6B4A23;
    --brown-700:#8A5E2B;
    --gold-600:#E3A93A;
    --gold-400:#F4C95D;
    --gold-300:#F7D67E;
    --gold-200:#FBE3A5;
    --gold-100:#FEF2D6;
    --teal:#5FB8AC;
    --teal-bg:#E2F4F1;
    --coral:#F0917F;
    --coral-bg:#FCE6E1;
    --text:#4A3A1E;
    --shadow: 0 10px 28px -12px rgba(180,130,30,0.28);
  }
  *{box-sizing:border-box;}
  body{
    margin:0;font-family:'Quicksand',sans-serif;
    background:
      radial-gradient(circle at 10% 6%, var(--bg-soft) 0%, transparent 45%),
      radial-gradient(circle at 95% 4%, #FFE3D4 0%, transparent 40%),
      var(--bg);
    color:var(--text);padding-bottom:60px;
  }
  h1,h2,h3,.display{font-family:'Baloo 2',sans-serif;}
  .wrap{max-width:980px;margin:0 auto;padding:0 20px;}

  .hero{position:relative;padding:38px 20px 26px;overflow:hidden;}
  .hero-inner{max-width:980px;margin:0 auto;display:flex;align-items:center;gap:22px;position:relative;z-index:2;}
  .sun{width:96px;height:96px;flex:none;filter:drop-shadow(0 6px 10px rgba(200,140,20,0.3));}
  .hero-text h1{font-size:clamp(21px,4vw,29px);color:var(--brown-900);margin:0 0 6px;line-height:1.25;}
  .hero-text p{margin:0;color:var(--brown-700);font-weight:600;font-size:14px;}
  .deco{position:absolute;opacity:.7;}

  .science{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin:18px auto 26px;max-width:980px;padding:0 20px;}
  .sci-card{background:var(--card);border-radius:18px;padding:16px 16px 14px;box-shadow:var(--shadow);border:1px solid var(--gold-200);}
  .sci-card .sci-icon{font-size:22px;}
  .sci-card h3{font-size:15px;margin:8px 0 4px;color:var(--brown-900);}
  .sci-card p{font-size:13px;line-height:1.5;margin:0;color:#5A4626;}

  .tabs{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;max-width:980px;margin:0 auto 22px;padding:0 20px;}
  .tab-btn{font-family:'Quicksand',sans-serif;font-weight:700;font-size:13.5px;background:var(--gold-100);color:var(--brown-700);border:none;padding:10px 16px;border-radius:999px;cursor:pointer;transition:.18s ease;}
  .tab-btn:hover{background:var(--gold-300);}
  .tab-btn.active{background:var(--brown-700);color:#fff;box-shadow:var(--shadow);}

  main{max-width:980px;margin:0 auto;padding:0 20px;}
  .topic-section{display:none;animation:fadeIn .35s ease;}
  .topic-section.active{display:block;}
  @keyframes fadeIn{from{opacity:0;transform:translateY(8px);}to{opacity:1;transform:translateY(0);}}

  .topic-header{display:flex;align-items:center;gap:12px;margin-bottom:6px;}
  .topic-header .ic{font-size:26px;}
  .topic-header h2{font-size:20px;color:var(--brown-900);margin:0;}
  .topic-sub{color:var(--brown-700);font-size:13.5px;margin:0 0 16px 0;}

  .note-box{background:var(--gold-100);border-radius:14px;padding:12px 18px;font-size:12.5px;color:#5A4626;margin-bottom:20px;border:1px dashed var(--gold-300);}
  .note-box b{color:var(--brown-900);}

  /* ---------- FLASHCARDS (Part 1) ---------- */
  .cards-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:16px;margin-bottom:20px;}
  .flip-card{height:200px;perspective:1200px;cursor:pointer;}
  .flip-inner{position:relative;width:100%;height:100%;transition:transform .55s cubic-bezier(.4,.2,.2,1);transform-style:preserve-3d;}
  .flip-card.flipped .flip-inner{transform:rotateY(180deg);}
  .face{position:absolute;inset:0;border-radius:16px;backface-visibility:hidden;padding:16px;display:flex;flex-direction:column;}
  .face-front{background:linear-gradient(150deg,var(--gold-400),var(--brown-700));color:#fff;justify-content:space-between;box-shadow:var(--shadow);}
  .face-front .tag{font-size:11px;font-weight:700;letter-spacing:.04em;opacity:.85;text-transform:uppercase;}
  .face-front .q-text{font-family:'Baloo 2',sans-serif;font-size:16px;line-height:1.35;}
  .face-front .hint{font-size:11.5px;opacity:.85;align-self:flex-end;}
  .face-back{background:var(--card);transform:rotateY(180deg);border:1.5px solid var(--gold-300);overflow-y:auto;justify-content:space-between;}
  .face-back .word-line{display:flex;align-items:baseline;gap:8px;flex-wrap:wrap;}
  .face-back .word-line .w{font-family:'Baloo 2',sans-serif;font-size:18px;color:var(--brown-900);}
  .face-back .word-line .ipa{color:var(--gold-600);font-weight:700;font-size:13px;}
  .face-back .word-line .speak-btn{border:none;background:var(--teal-bg);color:#2D7A6E;border-radius:50%;width:24px;height:24px;font-size:12px;cursor:pointer;margin-left:auto;}
  .face-back .a-text{font-size:12.5px;line-height:1.5;color:#473A22;white-space:pre-line;margin-top:4px;}
  .rate-row{display:flex;gap:6px;margin-top:8px;}
  .rate-btn{flex:1;border:none;border-radius:10px;padding:6px 4px;font-size:11px;font-weight:700;cursor:pointer;font-family:'Quicksand',sans-serif;}
  .rate-easy{background:var(--teal-bg);color:#2D7A6E;}
  .rate-review{background:var(--coral-bg);color:#B5523E;}
  .rate-btn.picked{outline:2px solid currentColor;}

  /* ---------- QUIZ (Part 2) ---------- */
  .quiz-block{background:var(--card);border-radius:20px;padding:20px 20px 22px;box-shadow:var(--shadow);margin-bottom:24px;}
  .quiz-block h3{margin:0 0 4px;font-size:16.5px;color:var(--brown-900);}
  .quiz-block .quiz-note{font-size:12.5px;color:var(--brown-700);margin:0 0 16px;}
  .q-item{margin-bottom:16px;padding-bottom:14px;border-bottom:1px solid var(--gold-200);}
  .q-item:last-of-type{border-bottom:none;}
  .q-text{font-size:14px;font-weight:700;color:#4A3415;margin-bottom:8px;}
  .opt-list{display:grid;grid-template-columns:1fr 1fr;gap:8px;}
  .opt{display:flex;align-items:center;gap:8px;background:var(--gold-100);border-radius:10px;padding:8px 10px;font-size:13px;cursor:pointer;border:1.5px solid transparent;transition:.15s;}
  .opt:hover{border-color:var(--gold-300);}
  .opt input{accent-color:var(--brown-700);}
  .opt.correct{background:var(--teal-bg);border-color:var(--teal);font-weight:700;}
  .opt.incorrect{background:var(--coral-bg);border-color:var(--coral);}
  .opt.disabled{cursor:default;}
  .submit-btn{background:var(--brown-700);color:#fff;border:none;border-radius:999px;padding:11px 26px;font-family:'Baloo 2',sans-serif;font-size:14.5px;font-weight:700;cursor:pointer;box-shadow:var(--shadow);transition:.15s;}
  .submit-btn:hover{background:var(--brown-900);}
  .submit-btn:disabled{opacity:.45;cursor:default;}
  .result-box{margin-top:14px;padding:12px 16px;border-radius:14px;font-weight:700;font-size:14px;display:none;}
  .result-good{background:var(--teal-bg);color:#2D7A6E;}
  .result-ok{background:var(--gold-100);color:#8A5E16;}
  .result-low{background:var(--coral-bg);color:#B5523E;}

  .hist-panel{background:var(--card);border-radius:18px;padding:16px 18px;box-shadow:var(--shadow);}
  .hist-panel h3{margin:0 0 10px;font-size:14.5px;color:var(--brown-900);}
  table.hist{width:100%;border-collapse:collapse;font-size:12.5px;}
  table.hist th{text-align:left;color:#9A7C45;font-weight:700;padding:4px 6px;border-bottom:1px solid var(--gold-200);}
  table.hist td{padding:6px 6px;border-bottom:1px solid var(--gold-200);}
  .empty-note{font-size:12.5px;color:#9A7C45;font-style:italic;}

  @media (max-width:720px){.hero-inner{flex-direction:column;text-align:center;} .science{grid-template-columns:1fr;} .opt-list{grid-template-columns:1fr;}}
</style>
</head>
<body>

<div class="hero">
  <div class="deco" style="top:6px;left:-6px;"><span style="font-size:38px;">🌴</span></div>
  <div class="deco" style="top:10px;right:5%;"><span style="font-size:34px;">🍉</span></div>
  <div class="deco" style="bottom:-6px;left:18%;"><span style="font-size:28px;">🍦</span></div>
  <div class="hero-inner">
    <svg class="sun" viewBox="0 0 100 100">
      <g stroke="#F4C95D" stroke-width="5" stroke-linecap="round">
        <line x1="50" y1="2" x2="50" y2="14"/>
        <line x1="50" y1="86" x2="50" y2="98"/>
        <line x1="2" y1="50" x2="14" y2="50"/>
        <line x1="86" y1="50" x2="98" y2="50"/>
        <line x1="15" y1="15" x2="23" y2="23"/>
        <line x1="77" y1="77" x2="85" y2="85"/>
        <line x1="85" y1="15" x2="77" y2="23"/>
        <line x1="23" y1="77" x2="15" y2="85"/>
      </g>
      <circle cx="50" cy="50" r="30" fill="#F7D67E"/>
      <circle cx="50" cy="50" r="30" fill="none" stroke="#E3A93A" stroke-width="2"/>
      <rect x="28" y="44" width="44" height="11" rx="5" fill="#6B4A23"/>
      <circle cx="38" cy="49.5" r="6" fill="#3E2A14"/>
      <circle cx="62" cy="49.5" r="6" fill="#3E2A14"/>
      <path d="M40 63 Q50 70 60 63" stroke="#6B4A23" stroke-width="3" fill="none" stroke-linecap="round"/>
    </svg>
    <div class="hero-text">
      <h1>Bài kiểm tra Từ vựng Mùa Hè ☀️</h1>
      <p>12 từ vựng đã học — gợi lại trước, kiểm tra sau, đúng theo cách trí nhớ ghi nhận thông tin lâu dài!</p>
    </div>
  </div>
</div>

<div class="science">
  <div class="sci-card">
    <div class="sci-icon">🧠</div>
    <h3>Truy xuất chủ động</h3>
    <p>Phần 1 đảo ngược chiều ghi nhớ: thay vì nhìn từ để nhớ nghĩa, em sẽ nhìn <b>nghĩa</b> và phải tự nhớ ra <b>từ tiếng Anh</b> — cách này ép não truy xuất sâu hơn.</p>
  </div>
  <div class="sci-card">
    <div class="sci-icon">🔁</div>
    <h3>Kiểm tra = Học lại</h3>
    <p>Theo "testing effect", việc tự kiểm tra giúp nhớ lâu hơn nhiều so với đọc lại lý thuyết. Phần 2 chính là cơ hội để kiến thức "khắc sâu" vào trí nhớ dài hạn.</p>
  </div>
  <div class="sci-card">
    <div class="sci-icon">📎</div>
    <h3>Ngữ cảnh quen thuộc</h3>
    <p>Phần 2 dùng lại đúng câu ví dụ em đã học — học và kiểm tra trong cùng ngữ cảnh giúp não liên kết từ với tình huống cụ thể, dễ nhớ hơn là học từ đơn lẻ.</p>
  </div>
</div>

<div class="tabs">
  <button class="tab-btn active" data-tab="recall">🧠 Phần 1: Gợi lại từ vựng</button>
  <button class="tab-btn" data-tab="quiz">📝 Phần 2: Bài kiểm tra</button>
</div>

<main>

  <!-- ============ PART 1: RECALL ============ -->
  <section class="topic-section active" id="sec-recall">
    <div class="topic-header"><span class="ic">🧠</span><h2>Phần 1 — Gợi lại từ vựng</h2></div>
    <p class="topic-sub">Khởi động trí nhớ trước khi vào bài kiểm tra chính thức.</p>
    <div class="note-box">☀️ <b>Cách làm:</b> Mặt trước thẻ là <b>nghĩa tiếng Việt</b>. Hãy cố nhớ ra <b>từ tiếng Anh</b> tương ứng trước khi bấm lật thẻ xem đáp án nhé!</div>
    <div class="cards-grid" id="cards-recall"></div>
  </section>

  <!-- ============ PART 2: QUIZ ============ -->
  <section class="topic-section" id="sec-quiz">
    <div class="topic-header"><span class="ic">📝</span><h2>Phần 2 — Bài kiểm tra</h2></div>
    <p class="topic-sub">12 câu lấy trực tiếp từ các câu ví dụ em đã học. Chọn từ đúng để hoàn thành câu.</p>
    <div class="quiz-block">
      <h3>🏖️ Hoàn thành câu</h3>
      <p class="quiz-note">Làm xong tất cả câu rồi mới bấm "Nộp bài" — đáp án chỉ hiện ra sau khi nộp.</p>
      <div id="quiz-list"></div>
      <button class="submit-btn" id="submit-btn">Nộp bài</button>
      <div class="result-box" id="result-box"></div>
    </div>
    <div class="hist-panel">
      <h3>📈 Lịch sử làm bài</h3>
      <div id="hist-wrap"><p class="empty-note">Em chưa nộp bài kiểm tra nào.</p></div>
    </div>
  </section>

</main>

<script>
/* ============================================================
   DATA — same 12 words from the vocabulary lesson
============================================================ */
const vocabData = [
  {id:"organisation", word:"organisation", ipa:"/ˌɔːɡənaɪˈzeɪʃən/", type:"(n)", vi:"tổ chức", en:"a group of people with a particular purpose, such as a business or a charity"},
  {id:"inhabitant", word:"inhabitant", ipa:"/ɪnˈhæbɪtənt/", type:"(n)", vi:"người dân, cư dân", en:"a person who lives in a particular place"},
  {id:"recommendation", word:"recommendation", ipa:"/ˌrekəmenˈdeɪʃən/", type:"(n)", vi:"lời khuyên, sự đề xuất", en:"a suggestion that something is good or suitable for a particular purpose"},
  {id:"memorable", word:"memorable", ipa:"/ˈmemərəbl/", type:"(adj)", vi:"đáng nhớ, khó quên", en:"worth remembering or easy to remember, because it is special"},
  {id:"expand", word:"expand", ipa:"/ɪkˈspænd/", type:"(v)", vi:"mở rộng, phát triển", en:"to become or make something become larger in size, number, or importance"},
  {id:"volatility", word:"volatility", ipa:"/ˌvɒləˈtɪləti/", type:"(n)", vi:"tính biến động, sự bất ổn", en:"a tendency to change quickly and unpredictably"},
  {id:"ambiguity", word:"ambiguity", ipa:"/ˌæmbɪˈɡjuːəti/", type:"(n)", vi:"sự mơ hồ, không rõ ràng", en:"the quality of being unclear or having more than one possible meaning"},
  {id:"resilience", word:"resilience", ipa:"/rɪˈzɪliəns/", type:"(n)", vi:"khả năng phục hồi, sự kiên cường", en:"the capacity to recover quickly from difficulties"},
  {id:"foster", word:"foster", ipa:"/ˈfɒstər/", type:"(v)", vi:"thúc đẩy, nuôi dưỡng (tinh thần, ý tưởng)", en:"to encourage the development or growth of ideas or feelings"},
  {id:"capitalize_on", word:"capitalize on", ipa:"/ˈkæpɪtəlaɪz ɒn/", type:"(phr. v)", vi:"tận dụng (cơ hội)", en:"to use a situation to your own advantage"},
  {id:"adaptability", word:"adaptability", ipa:"/əˌdæptəˈbɪləti/", type:"(n)", vi:"khả năng thích nghi", en:"the ability to adjust easily to new conditions"},
  {id:"proactive", word:"proactive", ipa:"/ˌprəʊˈæktɪv/", type:"(adj)", vi:"chủ động", en:"controlling a situation by making things happen rather than waiting for them to happen"}
];

/* Quiz questions built directly from the original example sentences */
const quizData = [
  {q:"We founded our ______ to help teenagers learn new languages.", options:["organisation","recommendation","resilience","ambiguity"], correct:0},
  {q:"The ______ of the village welcomed the exchange students warmly.", options:["inhabitants","organisations","recommendations","ambiguities"], correct:0},
  {q:"Based on your interests, we can make some useful ______.", options:["recommendations","inhabitants","ambiguities","resiliences"], correct:0},
  {q:"Studying abroad gave her some of the most ______ experiences of her life.", options:["memorable","proactive","volatile","ambiguous"], correct:0},
  {q:"The programme ______ to include several different countries.", options:["expanded","fostered","recommended","capitalized on"], correct:0},
  {q:"The ______ of the stock market made investors nervous.", options:["volatility","ambiguity","resilience","adaptability"], correct:0},
  {q:"The instructions were full of ______, so nobody knew what to do.", options:["ambiguity","resilience","adaptability","volatility"], correct:0},
  {q:"Her ______ helped her recover quickly after the setback.", options:["resilience","volatility","ambiguity","adaptability"], correct:0},
  {q:"Good teachers ______ a love of learning in their students.", options:["foster","expand","recommend","capitalize on"], correct:0},
  {q:"Successful companies know how to ______ new opportunities.", options:["capitalize on","foster","expand","recommend"], correct:0},
  {q:"______ is one of the most valuable skills in a changing world.", options:["Adaptability","Resilience","Volatility","Ambiguity"], correct:0},
  {q:"Being ______ means solving problems before they even happen.", options:["proactive","memorable","volatile","ambiguous"], correct:0}
];

/* ============================================================
   STORAGE
============================================================ */
const RATINGS_KEY="summer_test_ratings";
const HIST_KEY="summer_test_history";

function getRatings(){ try{return JSON.parse(localStorage.getItem(RATINGS_KEY))||{};}catch(e){return {};} }
function setRating(id, val){ const r=getRatings(); r[id]=val; localStorage.setItem(RATINGS_KEY, JSON.stringify(r)); }
function getHistory(){ try{return JSON.parse(localStorage.getItem(HIST_KEY))||[];}catch(e){return [];} }
function addHistory(entry){ const h=getHistory(); h.unshift(entry); localStorage.setItem(HIST_KEY, JSON.stringify(h.slice(0,30))); renderHistory(); }
function fmtDate(d){ return d.toLocaleDateString('vi-VN',{day:'2-digit',month:'2-digit',year:'numeric'})+" "+d.toLocaleTimeString('vi-VN',{hour:'2-digit',minute:'2-digit'}); }

/* ============================================================
   SPEECH
============================================================ */
function speak(text){
  try{
    if('speechSynthesis' in window){
      window.speechSynthesis.cancel();
      const u = new SpeechSynthesisUtterance(text);
      u.lang = 'en-GB';
      u.rate = 0.9;
      window.speechSynthesis.speak(u);
    }
  }catch(e){ /* ignore */ }
}

/* ============================================================
   RENDER PART 1 — RECALL FLASHCARDS (meaning -> word)
============================================================ */
function renderRecall(){
  const wrap=document.getElementById('cards-recall');
  wrap.innerHTML="";
  const ratings=getRatings();
  vocabData.forEach(v=>{
    const el=document.createElement('div');
    el.className="flip-card";
    el.innerHTML=`
      <div class="flip-inner">
        <div class="face face-front">
          <span class="tag">🇻🇳 Nghĩa tiếng Việt</span>
          <div class="q-text">${v.vi}</div>
          <span class="hint">🤔 Từ tiếng Anh là gì?</span>
        </div>
        <div class="face face-back">
          <div class="word-line">
            <span class="w">${v.word}</span>
            <span class="ipa">${v.ipa}</span>
            <button class="speak-btn" type="button">🔊</button>
          </div>
          <div class="a-text">${v.type}  ${v.en}</div>
          <div class="rate-row">
            <button class="rate-btn rate-easy" data-id="${v.id}" data-val="easy">✅ Nhớ ngay</button>
            <button class="rate-btn rate-review" data-id="${v.id}" data-val="review">🔁 Cần ôn lại</button>
          </div>
        </div>
      </div>`;
    el.addEventListener('click', (e)=>{
      if(e.target.closest('.speak-btn') || e.target.closest('.rate-btn')) return;
      el.classList.toggle('flipped');
    });
    wrap.appendChild(el);
    el.querySelector('.speak-btn').addEventListener('click', e=>{ e.stopPropagation(); speak(v.word); });
    el.querySelectorAll('.rate-btn').forEach(btn=>{
      btn.addEventListener('click', e=>{
        e.stopPropagation();
        setRating(btn.dataset.id, btn.dataset.val);
        el.querySelectorAll('.rate-btn').forEach(b=>b.classList.remove('picked'));
        btn.classList.add('picked');
      });
      if(ratings[v.id]===btn.dataset.val) btn.classList.add('picked');
    });
  });
}

/* ============================================================
   RENDER PART 2 — QUIZ
============================================================ */
function renderQuiz(){
  const wrap=document.getElementById('quiz-list');
  wrap.innerHTML="";
  quizData.forEach((item,i)=>{
    const qd=document.createElement('div'); qd.className="q-item";
    let optsHtml="";
    item.options.forEach((opt,oi)=>{
      optsHtml+=`<label class="opt" data-qi="${i}" data-oi="${oi}">
        <input type="radio" name="q${i}" value="${oi}"> <span>${opt}</span>
      </label>`;
    });
    qd.innerHTML=`<div class="q-text">${i+1}. ${item.q}</div><div class="opt-list">${optsHtml}</div>`;
    wrap.appendChild(qd);
  });
}

function gradeQuiz(){
  let score=0;
  const wrap=document.getElementById('quiz-list');
  quizData.forEach((item,i)=>{
    const checked=wrap.querySelector(`input[name="q${i}"]:checked`);
    const chosen = checked ? parseInt(checked.value) : -1;
    if(chosen===item.correct) score++;
    wrap.querySelectorAll(`.opt[data-qi="${i}"]`).forEach(label=>{
      const oi=parseInt(label.dataset.oi);
      label.classList.add('disabled');
      label.querySelector('input').disabled=true;
      if(oi===item.correct) label.classList.add('correct');
      else if(oi===chosen) label.classList.add('incorrect');
    });
  });
  const total=quizData.length;
  const box=document.getElementById('result-box');
  box.style.display='block';
  let cls='result-low', msg="Cố lên nào! Quay lại Phần 1 ôn lại các thẻ rồi thử lại nhé 💪";
  const pct=score/total;
  if(pct>=0.8){cls='result-good'; msg="Tuyệt vời! Ông Mặt Trời rất tự hào về em! ☀️🎉";}
  else if(pct>=0.5){cls='result-ok'; msg="Khá tốt! Ôn lại vài từ là chắc kiến thức ngay 🌟";}
  box.className='result-box '+cls;
  box.textContent=`Kết quả: ${score}/${total} câu đúng — ${msg}`;
  document.getElementById('submit-btn').disabled=true;
  addHistory({score, total, date:new Date().toISOString()});
}

function renderHistory(){
  const wrap=document.getElementById('hist-wrap');
  const h=getHistory();
  if(h.length===0){ wrap.innerHTML='<p class="empty-note">Em chưa nộp bài kiểm tra nào.</p>'; return; }
  let rows="";
  h.slice(0,10).forEach(e=>{
    const d=new Date(e.date);
    rows+=`<tr><td>${fmtDate(d)}</td><td>${e.score}/${e.total}</td></tr>`;
  });
  wrap.innerHTML=`<table class="hist"><tr><th>Thời gian</th><th>Điểm</th></tr>${rows}</table>`;
}

/* ============================================================
   TABS
============================================================ */
document.querySelectorAll('.tab-btn').forEach(btn=>{
  btn.addEventListener('click', ()=>{
    document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
    document.querySelectorAll('.topic-section').forEach(s=>s.classList.remove('active'));
    btn.classList.add('active');
    document.getElementById('sec-'+btn.dataset.tab).classList.add('active');
  });
});

document.getElementById('submit-btn').addEventListener('click', gradeQuiz);

/* ============================================================
   INIT
============================================================ */
renderRecall();
renderQuiz();
renderHistory();
</script>
</body>
</html>
