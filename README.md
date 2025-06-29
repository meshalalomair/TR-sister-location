# TR-sister-location
OPIP
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <title>نظام كشف الاختراق</title>
  <style>
    body {
      margin: 0; padding: 0;
      background: #000;
      color: #0f0;
      font-family: monospace;
      overflow: hidden;
    }
    #console {
      white-space: pre;
      padding: 20px;
      font-size: 18px;
    }
    #btn {
      display: none;
      position: fixed;
      top: 40%;
      left: 50%;
      transform: translate(-50%, -50%);
      padding: 15px 25px;
      background: #900;
      color: #fff;
      font-size: 20px;
      border: none;
      cursor: pointer;
    }
    #final {
      display: none;
      position: fixed;
      top: 40%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: #000;
      color: #fff;
      font-size: 24px;
      text-align: center;
      padding: 30px;
    }
  </style>
</head>
<body>

<audio id="alert" src="alert.mp3" preload="auto"></audio>
<div id="console"></div>
<button id="btn">استعادة السيطرة</button>
<div id="final"></div>

<script>
const lines = [
 "[INFO] Connection established to device ID: H-Mutairi_909",
 "[WARNING] Unauthorized access attempt detected...",
 "[TRACE] IP Address matched to \"Hesham Al-Mutairi\"",
 "",
 "🚨 Initiating forced control mode...",
 "📡 Syncing with device memory (68% completed)",
 "💾 Accessing internal files...",
 "🧠 Attempting neural profile extraction...",
 "",
 "⚠️ WARNING: Remote control activation initiated.",
 ">>> Device Hijacked.",
 "",
 "🔴 تم التحكم بالجهاز: 68%"
];

const consoleEl = document.getElementById('console');
const btn = document.getElementById('btn');
const alertSound = document.getElementById('alert');
const finalEl = document.getElementById('final');

let i = 0;
alertSound.play();

function typeLine() {
  if (i < lines.length) {
    consoleEl.textContent += lines[i] + "\n";
    i++;
    setTimeout(typeLine, 1000);
  } else {
    setTimeout(showButton, 2000);
  }
}

function showButton() {
  btn.style.display = "block";
}

btn.addEventListener('click', () => {
  consoleEl.style.display = 'none';
  btn.style.display = 'none';
  finalEl.style.display = 'block';
  finalEl.innerHTML = '🚫 فشلت المحاولة… أنت الآن مراقَب بالكامل يا هشام.<br/><br/>' +
                      '<span style="color:#0f0;">😂 مقلب فاخر من مشعل…<br/>لا تغلط على رجال مرة ثانية يا هشومي.<br/>تعلّم تسكِّر الواي فاي لايف.</span>';
});

// بدء كتابة
typeLine();
</script>

</body>
</html>
