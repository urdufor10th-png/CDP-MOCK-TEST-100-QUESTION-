# CDP-MOCK-TEST-100-QUESTION-
CTET DEC 2026
<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CTET CDP Mock Test - Instant Answer & Detailed Explanation</title>

  <!-- EmailJS SDK (Student Lead ko seedhe aapke Gmail par bhejne ke liye) -->
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>

  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
    body { background-color: #f1f5f9; color: #1e293b; padding: 14px; }
    .wrapper { max-width: 820px; margin: 0 auto; }

    /* 1. Lead Gate Form */
    .gate-card {
      background: #ffffff;
      padding: 28px;
      border-radius: 12px;
      box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
      border: 1px solid #e2e8f0;
      max-width: 480px;
      margin: 40px auto;
    }
    .gate-card h2 { color: #1e3a8a; font-size: 1.35rem; margin-bottom: 6px; text-align: center; }
    .gate-card p { font-size: 0.88rem; color: #64748b; margin-bottom: 20px; text-align: center; }

    .form-group { margin-bottom: 14px; }
    .form-group label { display: block; font-size: 0.85rem; font-weight: 600; margin-bottom: 6px; color: #334155; }
    .form-group input {
      width: 100%; padding: 10px 14px; border: 1.5px solid #cbd5e1; border-radius: 6px; font-size: 0.95rem; outline: none;
    }
    .form-group input:focus { border-color: #2563eb; }

    .otp-inline { display: flex; gap: 8px; }
    .btn-send-otp {
      padding: 0 16px; background: #0284c7; color: white; border: none; border-radius: 6px;
      font-size: 0.85rem; font-weight: 600; cursor: pointer; white-space: nowrap;
    }
    .btn-submit {
      width: 100%; padding: 12px; background: #16a34a; color: white; border: none;
      border-radius: 6px; font-size: 1rem; font-weight: 700; cursor: pointer; margin-top: 10px;
    }
    .btn-submit:disabled, .btn-send-otp:disabled { background: #94a3b8; cursor: not-allowed; }

    /* 2. Mock Test View */
    #test-view { display: none; }
    header {
      background: #1e3a8a; color: white; padding: 16px; border-radius: 10px; margin-bottom: 14px;
      display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 12px;
    }
    .stats { display: flex; gap: 10px; font-size: 0.85rem; }
    .badge { padding: 6px 12px; border-radius: 6px; font-weight: 600; }
    .badge-tot { background: #3b82f6; }
    .badge-cor { background: #16a34a; }
    .badge-wro { background: #dc2626; }

    /* Palette */
    .palette-toggle {
      background: white; border: 1px solid #cbd5e1; padding: 8px 14px; border-radius: 6px;
      cursor: pointer; font-weight: 600; margin-bottom: 12px; width: 100%; text-align: left; font-size: 0.9rem;
    }
    .palette-grid {
      display: none; background: white; padding: 12px; border-radius: 8px; margin-bottom: 14px;
      max-height: 180px; overflow-y: auto; border: 1px solid #cbd5e1;
      grid-template-columns: repeat(auto-fill, minmax(36px, 1fr)); gap: 6px;
    }
    .palette-grid.active { display: grid; }
    .pal-btn {
      height: 34px; border: 1px solid #cbd5e1; background: #f8fafc; border-radius: 4px;
      cursor: pointer; font-weight: 600; font-size: 0.8rem;
    }
    .pal-btn.current { border: 2px solid #1e3a8a; }
    .pal-btn.correct { background: #bbf7d0; color: #166534; border-color: #22c55e; }
    .pal-btn.wrong { background: #fecaca; color: #991b1b; border-color: #ef4444; }

    /* Card */
    .card {
      background: white; padding: 20px; border-radius: 10px; border: 1px solid #e2e8f0;
      box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05); margin-bottom: 16px;
    }
    .q-head { font-weight: 700; color: #2563eb; margin-bottom: 8px; font-size: 0.95rem; }
    .q-txt { font-size: 1.05rem; line-height: 1.6; margin-bottom: 16px; white-space: pre-line; color: #0f172a; }
    .options { display: flex; flex-direction: column; gap: 10px; }
    .opt-btn {
      text-align: left; padding: 12px 14px; border: 1.5px solid #cbd5e1; background: #f8fafc;
      border-radius: 8px; cursor: pointer; font-size: 0.95rem; line-height: 1.4; transition: all 0.15s ease-in-out;
    }
    .opt-btn:hover:not(:disabled) { background: #f1f5f9; border-color: #94a3b8; }
    .opt-btn.correct { background: #dcfce7 !important; border-color: #16a34a !important; color: #14532d !important; font-weight: 600; }
    .opt-btn.wrong { background: #fee2e2 !important; border-color: #dc2626 !important; color: #7f1d1d !important; font-weight: 600; }

    /* Detailed Explanation Box */
    .explanation-card {
      display: none;
      margin-top: 18px;
      padding: 16px;
      border-radius: 8px;
      background: #f8fafc;
      border-left: 5px solid #2563eb;
      font-size: 0.93rem;
      line-height: 1.6;
    }
    .explanation-card.show { display: block; }
    .exp-title {
      font-weight: 700;
      color: #1e3a8a;
      margin-bottom: 6px;
      display: flex;
      align-items: center;
      gap: 6px;
    }
    .exp-text { color: #334155; }

    .nav-btns { display: flex; justify-content: space-between; margin-top: 16px; }
    .nav-btn { padding: 10px 20px; border-radius: 6px; border: none; background: #1e3a8a; color: white; font-weight: 600; cursor: pointer; }
    .nav-btn:disabled { background: #94a3b8; cursor: not-allowed; }
  </style>
</head>
<body>

<div class="wrapper">

  <!-- 1. REGISTRATION GATE -->
  <div id="gate-view" class="gate-card">
    <h2>CTET CDP Online Mock Test</h2>
    <p>Apna vivaran bharein aur mock test shuru karein</p>

    <div class="form-group">
      <label>Pura Naam (Full Name)</label>
      <input type="text" id="u_name" placeholder="Apna naam darj karein" required>
    </div>

    <div class="form-group">
      <label>Mobile Number</label>
      <div class="otp-inline">
        <input type="tel" id="u_phone" maxlength="10" placeholder="10 ankon ka mobile number">
        <button class="btn-send-otp" id="btn-otp" onclick="handleSendOTP()">OTP Bhejein</button>
      </div>
    </div>

    <div class="form-group" id="otp-field" style="display: none;">
      <label>Darj Karein OTP (Enter OTP)</label>
      <input type="text" id="u_otp" maxlength="4" placeholder="Prapt OTP dalein">
      <small id="otp-hint" style="color: #0284c7; display: block; margin-top: 4px;"></small>
    </div>

    <div class="form-group">
      <label>Rajya (State)</label>
      <input type="text" id="u_state" placeholder="Jaise: Bihar, UP, Delhi">
    </div>

    <div class="form-group">
      <label>Zila (District)</label>
      <input type="text" id="u_district" placeholder="Jaise: Samastipur, Patna">
    </div>

    <button class="btn-submit" id="btn-start" onclick="handleVerifyAndStart()">Verify & Start Test</button>
    <div id="status-msg" style="text-align:center; font-size:0.85rem; margin-top:10px; font-weight:600;"></div>
  </div>

  <!-- 2. TEST VIEW -->
  <div id="test-view">
    <header>
      <div>
        <h1 style="font-size:1.15rem;">CTET CDP 100 Questions Practice</h1>
        <small id="user-display" style="opacity: 0.85;"></small>
      </div>
      <div class="stats">
        <span class="badge badge-tot" id="stat-q">Q: 1/100</span>
        <span class="badge badge-cor" id="stat-cor">Correct: 0</span>
        <span class="badge badge-wro" id="stat-wro">Wrong: 0</span>
      </div>
    </header>

    <button class="palette-toggle" onclick="togglePalette()">📋 Question Palette (1-100) Dekhein / Chhupayein</button>
    <div class="palette-grid" id="palette"></div>

    <div class="card">
      <div class="q-head" id="q-head">Question 1</div>
      <div class="q-txt" id="q-txt">Question loading...</div>
      <div class="options" id="opt-container"></div>
      
      <!-- Detailed Explanation Box -->
      <div class="explanation-card" id="exp-box">
        <div class="exp-title">💡 Vistrit Vyakhya (Explanation):</div>
        <div class="exp-text" id="exp-text"></div>
      </div>
    </div>

    <div class="nav-btns">
      <button class="nav-btn" id="btn-prev" onclick="prevQ()">Previous</button>
      <button class="nav-btn" id="btn-next" onclick="nextQ()">Next</button>
    </div>
  </div>

</div>

<script>
/* ================= EMAILJS CONFIGURATION ================= */
const EMAILJS_PUBLIC_KEY = "YOUR_PUBLIC_KEY";      // EmailJS Public Key
const EMAILJS_SERVICE_ID = "YOUR_SERVICE_ID";      // EmailJS Service ID
const EMAILJS_TEMPLATE_ID = "YOUR_TEMPLATE_ID";    // EmailJS Template ID

(function() {
  if (EMAILJS_PUBLIC_KEY !== "YOUR_PUBLIC_KEY") {
    emailjs.init(EMAILJS_PUBLIC_KEY);
  }
})();

/* ================= OTP VERIFICATION ================= */
let generatedOTP = null;

function handleSendOTP() {
  const phone = document.getElementById("u_phone").value.trim();
  if (!/^\d{10}$/.test(phone)) {
    alert("Kripya sahi 10-digit mobile number dalein.");
    return;
  }
  generatedOTP = Math.floor(1000 + Math.random() * 9000).toString();
  document.getElementById("otp-field").style.display = "block";
  document.getElementById("otp-hint").innerText = `(Testing ke liye aapka OTP hai: ${generatedOTP})`;
  alert(`Aapka OTP hai: ${generatedOTP}`);
  document.getElementById("btn-otp").innerText = "Resend OTP";
}

function handleVerifyAndStart() {
  const name = document.getElementById("u_name").value.trim();
  const phone = document.getElementById("u_phone").value.trim();
  const otpEntered = document.getElementById("u_otp").value.trim();
  const state = document.getElementById("u_state").value.trim();
  const district = document.getElementById("u_district").value.trim();
  const statusMsg = document.getElementById("status-msg");

  if (!name || !phone || !state || !district) {
    alert("Kripya sabhi column (Naam, Mobile, Rajya, Zila) bharein.");
    return;
  }
  if (!generatedOTP || otpEntered !== generatedOTP) {
    alert("Galat OTP! Kripya sahi OTP dalein.");
    return;
  }

  statusMsg.style.color = "#0284c7";
  statusMsg.innerText = "Data send ho raha hai...";
  document.getElementById("btn-start").disabled = true;

  const templateParams = {
    student_name: name,
    student_phone: phone,
    student_state: state,
    student_district: district,
    submission_time: new Date().toLocaleString()
  };

  if (EMAILJS_PUBLIC_KEY !== "YOUR_PUBLIC_KEY") {
    emailjs.send(EMAILJS_SERVICE_ID, EMAILJS_TEMPLATE_ID, templateParams)
      .then(() => startTest(name))
      .catch(() => startTest(name));
  } else {
    console.log("Mock lead recorded:", templateParams);
    startTest(name);
  }
}

function startTest(studentName) {
  document.getElementById("gate-view").style.display = "none";
  document.getElementById("test-view").style.display = "block";
  document.getElementById("user-display").innerText = `Student: ${studentName}`;
  initPalette();
  loadQuestion();
}

/* ================= 100 QUESTIONS DATA WITH EXPLANATIONS ================= */
const officialKey = {
  1:"c", 2:"a", 3:"a", 4:"c", 5:"a", 6:"a", 7:"a", 8:"a", 9:"d", 10:"a",
  11:"b", 12:"c", 13:"c", 14:"a", 15:"a", 16:"c", 17:"c", 18:"c", 19:"b", 20:"b",
  21:"b", 22:"b", 23:"a", 24:"d", 25:"b", 26:"b", 27:"a", 28:"b", 29:"a", 30:"a",
  31:"b", 32:"c", 33:"b", 34:"b", 35:"b", 36:"b", 37:"b", 38:"d", 39:"d", 40:"a",
  41:"b", 42:"c", 43:"b", 44:"d", 45:"a", 46:"b", 47:"a", 48:"c", 49:"c", 50:"a",
  51:"d", 52:"b", 53:"a", 54:"a", 55:"a", 56:"d", 57:"c", 58:"b", 59:"b", 60:"a",
  61:"d", 62:"d", 63:"a", 64:"a", 65:"a", 66:"a", 67:"c", 68:"c", 69:"a", 70:"c",
  71:"a", 72:"c", 73:"a", 74:"d", 75:"b", 76:"a", 77:"b", 78:"b", 79:"c", 80:"a",
  81:"a", 82:"a", 83:"b", 84:"b", 85:"b", 86:"b", 87:"a", 88:"c", 89:"d", 90:"d",
  91:"c", 92:"b", 93:"a", 94:"b", 95:"a", 96:"a", 97:"a", 98:"b", 99:"b", 100:"a"
};

const questions = [
  {
    id: 1,
    text: "अभिकथन (A): आंतरिक अभिप्रेरणा बच्चे को बाहरी दबाव या पुरस्कार के बिना, आंतरिक संतुष्टि के लिए स्वेच्छा से कार्य करने के लिए प्रेरित करती है।\nकारण (R): प्रशंसा, प्रतियोगिता और पुरस्कार आंतरिक अभिप्रेरणा के उदाहरण हैं।",
    opts: [
      { k: "a", t: "(a) A और R दोनों सही हैं तथा R, A की सही व्याख्या करता है।" },
      { k: "b", t: "(b) A और R दोनों सही हैं, लेकिन R, A की सही व्याख्या नहीं करता।" },
      { k: "c", t: "(c) A सही है, लेकिन R गलत है।" },
      { k: "d", t: "(d) A गलत है, लेकिन R सही है।" }
    ],
    exp: "अभिकथन (A) सही है क्योंकि आंतरिक अभिप्रेरणा में व्यक्ति अपनी आत्म-संतुष्टि और आनंद के लिए कार्य करता है। कारण (R) गलत है क्योंकि प्रशंसा, प्रतियोगिता और पुरस्कार 'बाह्य अभिप्रेरणा' (Extrinsic Motivation) के उदाहरण हैं, आंतरिक के नहीं।"
  },
  {
    id: 2,
    text: "अभिकथन (A): एक अनुकूल शिक्षण अधिगम वातावरण विद्यार्थियों को सीखी गई अवधारणाओं को नई एवं विभिन्न परिस्थितियों में लागू करने में सहायता करता है।\nकारण (R): सहायक कक्षा वातावरण विद्यार्थियों को सक्रिय रूप से सीखने, अवधारणाओं को समझने तथा उनके विभिन्न संदर्भों में प्रयोग के अवसर प्रदान करता है।",
    opts: [
      { k: "a", t: "(a) A और R दोनों सही हैं तथा R, A की सही व्याख्या करता है।" },
      { k: "b", t: "(b) A और R दोनों सही हैं, लेकिन R, A की सही व्याख्या नहीं करता।" },
      { k: "c", t: "(c) A सही है, लेकिन R गलत है।" },
      { k: "d", t: "(d) A गलत है, लेकिन R सही है।" }
    ],
    exp: "अनुकूल और सहायक कक्षा वातावरण बच्चों को अन्वेषण और विविध संदर्भों में ज्ञान के व्यावहारिक प्रयोग का अवसर देता है, जिससे वे सीखी गई बातों को नई परिस्थितियों में लागू कर पाते हैं। अतः A और R दोनों सही हैं तथा R सही व्याख्या है।"
  },
  {
    id: 3,
    text: "अधिगम की स्थिति में निम्नलिखित में से कौन-से कारक एक-दूसरे को परस्पर प्रभावित करते हैं?",
    opts: [
      { k: "a", t: "(a) व्यक्ति, पर्यावरण और व्यवहार" },
      { k: "b", t: "(b) बुद्धि, स्मृति और अभिप्रेरणा" },
      { k: "c", t: "(c) शिक्षक, पाठ्यक्रम और परीक्षा" },
      { k: "d", t: "(d) भाषा, संस्कृति और अनुशासन" }
    ],
    exp: "अल्बर्ट बंडूरा के सामाजिक-संज्ञानात्मक सिद्धांत (Triadic Reciprocal Causation) के अनुसार व्यक्ति (व्यक्तिगत कारक), पर्यावरण और व्यवहार तीनों एक-दूसरे को निरंतर परस्पर प्रभावित करते हैं।"
  },
  {
    id: 4,
    text: "एक शिक्षार्थी मुख्यतः इस उद्देश्य से अध्ययन करता है कि वह अपने सहपाठियों की तुलना में स्वयं को अधिक सक्षम और सफल सिद्ध कर सके। यह व्यवहार किस प्रकार के लक्ष्य अभिविन्यास (Goal Orientation) को दर्शाता है?",
    opts: [
      { k: "a", t: "(a) निपुणता-परिहार" },
      { k: "b", t: "(b) प्रदर्शन-परिहार" },
      { k: "c", t: "(c) प्रदर्शन-उपागम" },
      { k: "d", t: "(d) निपुणता-उपागम" }
    ],
    exp: "जब कोई विद्यार्थी दूसरों से बेहतर प्रदर्शन करने, प्रशंसा पाने या खुद को श्रेष्ठ दिखाने के उद्देश्य से पढ़ता है, तो इसे 'प्रदर्शन-उपागम लक्ष्य' (Performance-Approach Goal) कहा जाता है।"
  },
  {
    id: 5,
    text: "अभिकथन (A): अभिप्रेरणा के आरोपण सिद्धांत के अनुसार, अपनी सफलता या असफलता के कारणों के बारे में शिक्षार्थी की धारणा उसके भविष्य के अभिप्रेरणा स्तर और प्रदर्शन को प्रभावित कर सकती है।\nकारण (R): जब शिक्षार्थी अपने परिणामों का कारण प्रयास जैसे आंतरिक और नियंत्रणीय कारकों को मानते हैं, तो उनके कार्य में बने रहने और भविष्य के प्रदर्शन में सुधार करने की संभावना अधिक होती है।",
    opts: [
      { k: "a", t: "(a) A और R दोनों सही हैं तथा R, A की सही व्याख्या करता है।" },
      { k: "b", t: "(b) A और R दोनों सही हैं, लेकिन R, A की सही व्याख्या नहीं करता।" },
      { k: "c", t: "(c) A सही है, लेकिन R गलत है।" },
      { k: "d", t: "(d) A गलत है, लेकिन R सही है।" }
    ],
    exp: "बर्नार्ड वेनर (Bernard Weiner) के आरोपण सिद्धांत (Attribution Theory) के अनुसार जब बच्चे सफलता/असफलता का कारण अपने 'प्रयास' (आंतरिक व नियंत्रणीय कारक) को मानते हैं, तो वे भविष्य में अधिक मेहनत करते हैं। अतः A और R दोनों सही हैं।"
  },
  {
    id: 6,
    text: "निम्नलिखित में से कौन-सी स्थिति प्रभावी अधिगम के लिए सबसे उपयुक्त मानी जाती है?",
    opts: [
      { k: "a", t: "(a) संतुलित प्रोत्साहन, भय से मुक्त वातावरण के साथ" },
      { k: "b", t: "(b) भय के साथ अत्यधिक प्रोत्साहन" },
      { k: "c", t: "(c) उच्च भय और कम अभिप्रेरणा" },
      { k: "d", t: "(d) प्रोत्साहन और अभिप्रेरणा का पूर्ण अभाव" }
    ],
    exp: "सीखने के लिए सबसे अनुकूल स्थिति भय-मुक्त, तनाव-रहित वातावरण और मध्यम/संतुलित स्तर की उत्तेजना और प्रोत्साहन होती है।"
  },
  {
    id: 7,
    text: "प्रभावी कक्षा-शिक्षण के सिद्धांतों के अनुसार, 'प्रिंट-समृद्ध और संसाधन-समृद्ध कक्षा वातावरण' मुख्यतः क्या सुनिश्चित करता है?",
    opts: [
      { k: "a", t: "(a) पर्याप्त शिक्षण-अधिगम सामग्री (TLM) की उपलब्धता तथा उपयुक्त कक्षा व्यवस्था" },
      { k: "b", t: "(b) कक्षा में कठोर अनुशासन और पूर्ण शांति" },
      { k: "c", t: "(c) कक्षा-शिक्षण में शिक्षण-सहायक सामग्रियों के उपयोग में कमी" },
      { k: "d", t: "(d) केवल पाठ्यपुस्तक-आधारित अधिगम पर निर्भरता" }
    ],
    exp: "प्रिंट और संसाधन-समृद्ध वातावरण बच्चों को विभिन्न TLM, चार्ट, पुस्तकों और गतिविधियों के माध्यम से स्वतंत्र रूप से भाषा और अवधारणाओं को खोजने के भरपूर अवसर देता है।"
  },
  {
    id: 8,
    text: "अभिकथन (A): पठन वैकल्य से जूझ रहे बच्चों के सीखने को सुगम बनाने के लिए शिक्षकों को पुस्तकों के अलावा विभिन्न प्रकार के संसाधनों का प्रयोग करना चाहिए व उन्हें लिखित परीक्षा में अतिरिक्त समय देना चाहिए।\nतर्क (R): पठन वैकल्य की चुनौती वाले विद्यार्थियों को पढ़ने में कठिनाई होती है।",
    opts: [
      { k: "a", t: "(a) (A) और (R) दोनों सही हैं और (R) सही व्याख्या करता है (A) की।" },
      { k: "b", t: "(b) (A) और (R) दोनों सही हैं लेकिन (R) सही व्याख्या नहीं है (A) की।" },
      { k: "c", t: "(c) (A) सही है लेकिन (R) गलत है।" },
      { k: "d", t: "(d) (A) और (R) दोनों गलत है।" }
    ],
    exp: "डिस्लेक्सिया (पठन वैकल्य) में बच्चों को शब्दों को डिकोड करने व पढ़ने में समस्या होती है, इसलिए ऑडियो संसाधन और अतिरिक्त समय जैसे उचित समायोजन (Accommodations) देना आवश्यक है।"
  },
  {
    id: 9,
    text: "निम्न में से कौन-सा कथन अधिगम अशक्तताओं जैसे कि पठनवैकल्य, गुणजवैकल्य, इत्यादि के संदर्भ में सही है?",
    opts: [
      { k: "a", t: "(a) अधिगम अशक्तता से जूझते सभी विद्यार्थी एक जैसे होते हैं।" },
      { k: "b", t: "(b) अधिगम अशक्तता से जूझते विद्यार्थियों के अधिगम आकलन के लिए मानकीकृत परीक्षण सबसे बेहतर होते हैं।" },
      { k: "c", t: "(c) अध्यापक - केन्द्रित शिक्षाशास्त्र, अधिगम अशक्तता से जूझते विद्यार्थियों के संज्ञानात्मक विकास को सुसाधित करने के लिए सर्वोत्तम होते हैं।" },
      { k: "d", t: "(d) अधिगम अशक्तता, तंत्रिका संबंधी और वातावरणीय दोनों तरह के कारकों से प्रभावित होती हैं।" }
    ],
    exp: "अधिगम अक्षमताएं जैविक/तंत्रिका संबंधी (Neurological) कारणों के साथ-साथ अनुपयुक्त परिवेशीय और शैक्षणिक कारकों से भी प्रभावित होती हैं।"
  },
  {
    id: 10,
    text: "अभिकथन (A): अधिसंज्ञान केवल अपनी सोच के प्रति जागरूक होने तक सीमित नहीं है, बल्कि इसमें अपनी सीखने और सोचने की प्रक्रियाओं की योजना बनाना, उनकी निगरानी करना तथा आवश्यकता के अनुसार उनमें सुधार करना भी शामिल है।\nकारण (R): अधिसंज्ञान के दो प्रमुख पक्ष हैं- संज्ञान के बारे में ज्ञान तथा संज्ञान का विनियमन, जिनके माध्यम से शिक्षार्थी अपनी संज्ञानात्मक प्रक्रियाओं को समझता और नियंत्रित करता है।",
    opts: [
      { k: "a", t: "(a) A और R दोनों सही हैं तथा R, A की सही व्याख्या करता है।" },
      { k: "b", t: "(b) A और R दोनों सही हैं, लेकिन R, A की सही व्याख्या नहीं करता।" },
      { k: "c", t: "(c) A सही है, लेकिन R गलत है।" },
      { k: "d", t: "(d) A गलत है, लेकिन R सही है।" }
    ],
    exp: "मेटाकॉग्निशन (अधिसंज्ञान) का अर्थ अपनी सोच के बारे में सोचना है। इसके दो मुख्य घटक होते हैं: संज्ञान का ज्ञान (Knowledge of Cognition) और संज्ञान का विनियमन (Regulation of Cognition)। अतः A और R दोनों सही हैं।"
  }
];

// Q11 to Q100 Fillers with Questions and Conceptual Explanations
for (let i = 11; i <= 100; i++) {
  const ansKey = officialKey[i];
  questions.push({
    id: i,
    text: `PDF Question No. ${i} (CTET CDP Official Document)\n\nKripya apne PDF question-paper me prashn sankhya ${i} ko dekhein aur sahi uttar chunein.`,
    opts: [
      { k: "a", t: "(a) Option A" },
      { k: "b", t: "(b) Option B" },
      { k: "c", t: "(c) Option C" },
      { k: "d", t: "(d) Option D" }
    ],
    exp: `Is prashn ka sahi uttar vikalp (${ansKey.toUpperCase()}) hai. CTET aur NCF ke niyam anusar child-centered, inclusive aur constructivist learning approach ko sabse uchit maana jata hai.`
  });
}

let curIdx = 0;
const answered = {};

function initPalette() {
  const pal = document.getElementById("palette");
  pal.innerHTML = "";
  for (let i = 1; i <= 100; i++) {
    const btn = document.createElement("button");
    btn.className = "pal-btn";
    btn.id = "pal-" + i;
    btn.innerText = i;
    btn.onclick = () => { curIdx = i - 1; loadQuestion(); };
    pal.appendChild(btn);
  }
}

function togglePalette() {
  document.getElementById("palette").classList.toggle("active");
}

function loadQuestion() {
  const q = questions[curIdx];
  const qNum = q.id;
  const correct = officialKey[qNum];

  document.getElementById("q-head").innerText = `Question ${qNum} of 100`;
  document.getElementById("q-txt").innerText = q.text;
  document.getElementById("stat-q").innerText = `Q: ${qNum}/100`;

  const box = document.getElementById("opt-container");
  box.innerHTML = "";

  const expBox = document.getElementById("exp-box");
  const expText = document.getElementById("exp-text");
  expBox.classList.remove("show");

  const isDone = answered[qNum] !== undefined;

  q.opts.forEach(o => {
    const btn = document.createElement("button");
    btn.className = "opt-btn";
    btn.innerText = o.t;
    btn.disabled = isDone;

    if (isDone) {
      if (o.k === correct) btn.classList.add("correct");
      if (answered[qNum] === o.k && o.k !== correct) btn.classList.add("wrong");
    }

    btn.onclick = () => {
      answered[qNum] = o.k;
      const palBtn = document.getElementById("pal-" + qNum);
      if (o.k === correct) {
        palBtn.classList.add("correct");
      } else {
        palBtn.classList.add("wrong");
      }
      updateScore();
      loadQuestion();
    };
    box.appendChild(btn);
  });

  // Agar question solve ho gaya hai to detailed explanation show karein
  if (isDone) {
    expText.innerText = q.exp || `Sahi Vikalp: (${correct.toUpperCase()})`;
    expBox.classList.add("show");
  }

  // Highlight in palette
  document.querySelectorAll(".pal-btn").forEach((b, idx) => {
    b.classList.toggle("current", idx === curIdx);
  });

  document.getElementById("btn-prev").disabled = curIdx === 0;
  document.getElementById("btn-next").disabled = curIdx === questions.length - 1;
}

function updateScore() {
  let cor = 0, wro = 0;
  for (let q in answered) {
    if (answered[q] === officialKey[q]) cor++;
    else wro++;
  }
  document.getElementById("stat-cor").innerText = `Correct: ${cor}`;
  document.getElementById("stat-wro").innerText = `Wrong: ${wro}`;
}

function prevQ() { if (curIdx > 0) { curIdx--; loadQuestion(); } }
function nextQ() { if (curIdx < questions.length - 1) { curIdx++; loadQuestion(); } }
</script>

</body>
</html>
