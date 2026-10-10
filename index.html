<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,user-scalable=no">
<title>Hacker Terminal</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Courier New',monospace;-webkit-tap-highlight-color:transparent}
body{background:#000;color:#0f0;min-height:100vh;padding:12px;overflow-x:hidden;text-shadow:0 0 5px #0f0}
.matrix{position:fixed;inset:0;z-index:0;opacity:.18;pointer-events:none}
.wrap{position:relative;z-index:2;max-width:900px;margin:0 auto}
.hdr{background:rgba(0,20,0,.9);border:2px solid #0f0;border-radius:10px;padding:12px;margin-bottom:12px;display:flex;justify-content:space-between;align-items:center;box-shadow:0 0 20px #0f0}
.hdr h1{font-size:14px;letter-spacing:3px}
.hdr .st{font-size:11px;animation:blk 1s infinite}
@keyframes blk{50%{opacity:.3}}
.panel{background:rgba(0,20,0,.85);border:2px solid #0f0;border-radius:10px;padding:12px;box-shadow:0 0 15px rgba(0,255,0,.3)}
.term{background:#000;border:1px solid #0f0;border-radius:6px;padding:10px;height:460px;overflow-y:auto;font-size:12px;line-height:1.5}
.term::-webkit-scrollbar{width:6px}
.term::-webkit-scrollbar-thumb{background:#0f0}
.term .line{white-space:pre-wrap;word-break:break-all;margin-bottom:2px}
.term .in{display:flex;gap:6px;margin-top:4px}
.term .in input{flex:1;background:transparent;border:none;color:#0f0;font-family:inherit;font-size:12px;outline:none;caret-color:#0f0}
.term .pr{color:#0f0;font-weight:bold}
.tst{position:fixed;bottom:20px;left:50%;transform:translateX(-50%);background:#0f0;color:#000;padding:10px 20px;border-radius:20px;font-size:12px;font-weight:bold;z-index:9999}
.warn{color:#ff0}.danger{color:#f00;animation:blk .3s infinite}.ok{color:#0f0}.info{color:#0ff}.err{color:#f00;font-weight:bold}
.lock{position:fixed;inset:0;background:rgba(0,0,0,.95);z-index:10000;display:none;align-items:center;justify-content:center;padding:20px}
.lock.show{display:flex}
.lock-box{background:linear-gradient(160deg,#1a0000,#000);border:3px solid #f00;border-radius:20px;padding:26px;max-width:400px;width:100%;text-align:center;box-shadow:0 0 60px rgba(255,0,0,.9);animation:pop .4s}
@keyframes pop{from{transform:scale(.7);opacity:0}to{transform:scale(1);opacity:1}}
.lock-box .sk{font-size:70px;display:block;margin-bottom:14px;animation:shk .5s infinite}
@keyframes shk{0%,100%{transform:rotate(-5deg)}50%{transform:rotate(5deg)}}
.lock-box h2{color:#f00;font-size:20px;margin-bottom:12px;text-transform:uppercase;letter-spacing:2px}
.lock-box .msg{color:#ff0;font-size:13px;margin-bottom:14px;line-height:1.6}
.lock-box input{width:100%;background:#000;border:2px solid #f00;border-radius:10px;padding:12px;color:#f00;font-size:14px;text-align:center;outline:none;margin-bottom:10px;letter-spacing:2px}
.lock-box input:focus{border-color:#ff0}
.lock-box .tm{color:#ff0;font-size:26px;font-weight:bold;margin:10px 0}
.lock-box .er{color:#f00;font-size:12px;margin-bottom:10px;min-height:16px;font-weight:bold}
.lock-box .btn{width:100%;padding:12px;background:linear-gradient(135deg,#f00,#800);border:none;border-radius:10px;color:#fff;font-weight:bold;font-size:14px;font-family:inherit;cursor:pointer;letter-spacing:2px;text-transform:uppercase;box-shadow:0 4px 0 #400}
.lock-box .btn:active{transform:translateY(4px);box-shadow:none}
</style>
</head>
<body>
<canvas class="matrix" id="mx"></canvas>
<div class="wrap">
<div class="hdr">
<h1>☠ HACKER TERMINAL v2.0</h1>
<div class="st">● ONLINE</div>
</div>
<div class="panel">
<div class="term" id="term">
<div class="line info">Hacker Terminal v2.0</div>
<div class="line">Nhập <span class="warn">/chayhack</span> để chạy</div>
<div class="line">Nhập <span class="info">help</span> để xem lệnh</div>
<div class="line">&nbsp;</div>
<div class="in"><span class="pr">root@hacker:~$</span><input id="inp" autocomplete="off" autofocus></div>
</div>
</div>
</div>

<div class="lock" id="lock">
<div class="lock-box">
<span class="sk">☠</span>
<h2>⛔ BỊ KHÓA ⛔</h2>
<div class="msg" id="lmsg">Bạn đã nhập sai!<br>Vui lòng chờ đợi...</div>
<div class="tm" id="ltm">5</div>
<div class="msg">Nhập mật khẩu để tiếp tục:</div>
<input id="lpass" type="password" placeholder="Mật khẩu..." autocomplete="off">
<div class="er" id="lerr"></div>
<button class="btn" onclick="unlock()">🔓 XÁC NHẬN</button>
</div>
</div>

<script>
function tst(m){var t=document.createElement('div');t.className='tst';t.textContent=m;document.body.appendChild(t);setTimeout(function(){t.style.opacity='0';t.style.transition='.3s'},1500);setTimeout(function(){t.remove()},1900)}

var mx=document.getElementById('mx'),cx=mx.getContext('2d');
mx.width=innerWidth;mx.height=innerHeight;
var mc='ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789@#$%&*',mf=14,md=[];
for(var i=0;i<Math.floor(mx.width/mf);i++)md[i]=1;
setInterval(function(){
  cx.fillStyle='rgba(0,0,0,.05)';cx.fillRect(0,0,mx.width,mx.height);
  cx.fillStyle='#0f0';cx.font=mf+'px monospace';
  for(var i=0;i<md.length;i++){
    cx.fillText(mc[Math.floor(Math.random()*mc.length)],i*mf,md[i]*mf);
    if(md[i]*mf>mx.height&&Math.random()>.975)md[i]=0;
    md[i]++;
  }
},50);

var term=document.getElementById('term'),inp=document.getElementById('inp'),running=false;

function p(t,c){var d=document.createElement('div');d.className='line'+(c?' '+c:'');d.innerHTML=t;term.appendChild(d);term.scrollTop=term.scrollHeight;while(term.children.length>600)term.removeChild(term.firstChild)}

function rh(n){var c='0123456789ABCDEF',s='';for(var i=0;i<n;i++)s+=c[Math.floor(Math.random()*16)];return s}
function ri(){return [0,0,0,0].map(function(){return Math.floor(Math.random()*255)}).join('.')}
function rm(){var c='0123456789ABCDEF',s='';for(var i=0;i<6;i++){s+=c[Math.floor(Math.random()*16)]+c[Math.floor(Math.random()*16)];if(i<5)s+=':'}return s}

function bp(f,d,t){try{var a=window._ac||(window._ac=new(window.AudioContext||window.webkitAudioContext)());var o=a.createOscillator(),g=a.createGain();o.connect(g);g.connect(a.destination);o.type=t||'square';o.frequency.value=f;g.gain.setValueAtTime(.02,a.currentTime);g.gain.exponentialRampToValueAtTime(.001,a.currentTime+d);o.start();o.stop(a.currentTime+d)}catch(e){}}

// ============ PASSWORD ============
var DEFAULT_PASS='1234';
var PASS_KEY='hacker_pass_v3';
var PASS=DEFAULT_PASS;
try{var sv=localStorage.getItem(PASS_KEY);if(sv)PASS=sv}catch(e){}

var cd=0,lt=null;

function showLock(){
  document.getElementById('lock').classList.add('show');
  document.getElementById('lpass').value='';
  document.getElementById('lerr').textContent='';
  document.getElementById('lmsg').innerHTML='Bạn đã nhập sai!<br>Vui lòng chờ đợi...';
  cd=5;
  document.getElementById('ltm').textContent=cd;
  document.getElementById('ltm').style.color='#ff0';
  document.getElementById('lpass').disabled=true;
  document.querySelector('.lock-box .btn').disabled=true;
  document.querySelector('.lock-box .btn').style.opacity='.5';
  if(lt)clearInterval(lt);
  lt=setInterval(function(){
    cd--;document.getElementById('ltm').textContent=cd;bp(400,.05);
    if(cd<=0){
      clearInterval(lt);
      document.getElementById('ltm').textContent='✓';
      document.getElementById('ltm').style.color='#0f0';
      document.getElementById('lmsg').innerHTML='Đã hết thời gian chờ!<br>Nhập mật khẩu để tiếp tục:';
      document.getElementById('lpass').disabled=false;
      document.querySelector('.lock-box .btn').disabled=false;
      document.querySelector('.lock-box .btn').style.opacity='1';
      document.getElementById('lpass').focus();
    }
  },1000);
  try{var a=window._ac||(window._ac=new(window.AudioContext||window.webkitAudioContext)());[300,400,500].forEach(function(f,i){setTimeout(function(){var o=a.createOscillator(),g=a.createGain();o.connect(g);g.connect(a.destination);o.type='sawtooth';o.frequency.value=f;g.gain.setValueAtTime(.08,a.currentTime);g.gain.exponentialRampToValueAtTime(.001,a.currentTime+.3);o.start();o.stop(a.currentTime+.3)},i*200)})}catch(e){}
}

function unlock(){
  if(cd>0)return;
  var v=document.getElementById('lpass').value;
  if(v===PASS){
    document.getElementById('lerr').style.color='#0f0';
    document.getElementById('lerr').textContent='✓ ĐÚNG! ĐANG MỞ KHÓA...';
    [800,1000,1200].forEach(function(f,i){setTimeout(function(){bp(f,.1)},i*100)});
    setTimeout(function(){
      document.getElementById('lock').classList.remove('show');
      tst('✓ Đã mở khóa!');
      p('[✓] Truy cập được cấp phép','ok');
      p('&nbsp;');
      inp.focus();
    },1200);
  } else {
    document.getElementById('lerr').style.color='#f00';
    document.getElementById('lerr').textContent='✗ SAI MẬT KHẨU!';
    document.getElementById('lpass').value='';
    bp(150,.5,'sawtooth');
  }
}

document.getElementById('lpass').addEventListener('keydown',function(e){if(e.key==='Enter')unlock()});

// ============ CHANGE PASSWORD ============
var pwState={active:false,step:0,oldPw:'',newPw:''};

function startChangePw(){
  pwState.active=true;
  pwState.step=1;
  pwState.oldPw='';
  pwState.newPw='';
  p('','');
  p('🔑 ĐỔI MẬT KHẨU','info');
  p('Nhập mật khẩu cũ:','warn');
}

function cancelChangePw(){
  pwState.active=false;
  pwState.step=0;
  p('[✗] Đã hủy đổi mật khẩu','err');
  p('&nbsp;');
}

function handlePwStep(v){
  if(pwState.step===1){
    if(v===PASS){
      pwState.oldPw=v;
      pwState.step=2;
      p('✓ Mật khẩu cũ đúng','ok');
      p('Nhập mật khẩu mới (từ 4 ký tự):','warn');
    } else {
      p('✗ Mật khẩu cũ sai!','err');
      cancelChangePw();
      bp(200,.3,'sawtooth');
    }
  } else if(pwState.step===2){
    if(!v||v.length<4){
      p('✗ Mật khẩu mới phải từ 4 ký tự! Nhập lại:','err');
      bp(200,.2,'sawtooth');
      return;
    }
    pwState.newPw=v;
    pwState.step=3;
    p('✓ Mật khẩu mới đã nhập','ok');
    p('Xác nhận lại mật khẩu mới:','warn');
  } else if(pwState.step===3){
    if(v===pwState.newPw){
      PASS=v;
      try{localStorage.setItem(PASS_KEY,v)}catch(e){}
      p('✓✓✓ ĐỔI MẬT KHẨU THÀNH CÔNG!','ok');
      p('Mật khẩu mới đã được lưu.','ok');
      p('&nbsp;');
      tst('✓ Đã đổi mật khẩu!');
      [1000,1200,1500].forEach(function(f,i){setTimeout(function(){bp(f,.1)},i*100)});
      pwState.active=false;
      pwState.step=0;
    } else {
      p('✗ Xác nhận không khớp! Hủy thao tác.','err');
      cancelChangePw();
      bp(200,.3,'sawtooth');
    }
  }
}

// ============ HACK SEQUENCE ============
var phase=[
  ['[PHASE 1/6] RECONNAISSANCE','info'],
  ['Initializing hack sequence...','ok'],
  ['Spoofing MAC: '+rm(),'info'],
  ['Routing through TOR...','warn'],
  ['TOR node: '+ri()+':9001','info'],
  ['AES-256-GCM tunnel established','ok'],
  ['[PHASE 2/6] NETWORK SCAN','info'],
  ['Target: '+ri(),'warn'],
  ['Running nmap -sS -A -T4...','info'],
  ['  Port 22/tcp   open  ssh      OpenSSH 8.2','ok'],
  ['  Port 80/tcp   open  http     nginx 1.18.0','ok'],
  ['  Port 443/tcp  open  https    nginx 1.18.0','ok'],
  ['  Port 3306/tcp open  mysql    MySQL 8.0.27','warn'],
  ['  Port 8080/tcp open  http-alt Tomcat 9.0','ok'],
  ['OS: Linux 5.x (Ubuntu 22.04)','info'],
  ['Vulns found: 12 (3 critical)','danger'],
  ['[PHASE 3/6] EXPLOITATION','info'],
  ['CVE-2024-1234: RCE via Tomcat','danger'],
  ['Crafting payload...','warn'],
  ['  Payload size: 4096 bytes','info'],
  ['  Shellcode: x86_64/linux/exec','info'],
  ['Sending to /manager/html','warn'],
  ['  [HTTP/1.1 200 OK]','ok'],
  ['  [+] Shell uploaded','ok'],
  ['  [+] Reverse shell: '+ri()+':4444','ok'],
  ['[PHASE 4/6] PRIVILEGE ESCALATION','info'],
  ['Current user: www-data','info'],
  ['Searching SUID binaries...','warn'],
  ['  /usr/bin/sudo    SUID','danger'],
  ['Exploiting sudo (CVE-2021-3156)','danger'],
  ['Reading /etc/shadow...','warn'],
  ['  root:$6$'+rh(16)+'$'+rh(43),'danger'],
  ['hashcat -m 1800...','warn'],
  ['  Hashrate: 85.4 MH/s','info'],
  ['  [+] CRACKED: root:hunter2','ok'],
  ['  [+] ROOT ACCESS GRANTED','ok'],
  ['[PHASE 5/6] DATA EXFILTRATION','info'],
  ['Dumping MySQL...','warn'],
  ['  production_db (2.4 GB)','info'],
  ['  [+] 1,247,893 records','ok'],
  ['Encrypting with GPG RSA-4096...','warn'],
  ['Uploading to C&C '+ri()+':443','warn'],
  ['  [+] Transfer complete','ok'],
  ['[PHASE 6/6] PERSISTENCE','info'],
  ['Installing backdoor...','warn'],
  ['  [+] /usr/bin/.systemd-service','ok'],
  ['  [+] cron job added','ok'],
  ['  [+] SSH key added','ok'],
  ['Wiping logs...','warn'],
  ['  [+] /var/log/* cleared','ok'],
  ['  [+] bash_history wiped','ok'],
  ['Spoofing timestamps...','warn'],
  ['  [+] Done','ok'],
  ['Removing forensic traces...','warn'],
  ['  [+] 0 artifacts remaining','ok']
];

function runHack(){
  if(running){tst('Đang chạy!');return}
  running=true;
  p('','');p('██████████████████████████████████████','danger');
  p('█   ☠  PRO HACK SEQUENCE v2.0  ☠   █','danger');
  p('██████████████████████████████████████','danger');
  p('','');p('[!] SYSTEM WILL BE COMPROMISED','warn');
  p('[!] Duration: 20 seconds','warn');p('[!] ESC to abort','warn');p('','');
  
  var dur=20000,st=Date.now(),pi=0,ei=0,mi=null,xei=null,pgi=null,pb=null;
  var ex=[];for(var k=0;k<25;k++)ex.push('0x'+rh(8)+': '+rh(2)+' '+rh(2)+' '+rh(2)+' '+rh(2)+' '+rh(2)+' '+rh(2)+' '+rh(2)+' '+rh(2));
  
  pgi=setInterval(function(){
    var e=Date.now()-st,r=Math.max(0,Math.ceil((dur-e)/1000)),pc=Math.min(100,Math.floor(e/dur*100));
    if(pb&&pb.parentNode)pb.parentNode.removeChild(pb);
    pb=document.createElement('div');pb.className='line warn';
    var b='█'.repeat(Math.floor(pc/2))+'░'.repeat(50-Math.floor(pc/2));
    pb.innerHTML='<span class="warn">['+b+'] '+pc+'% | T-00:'+String(r).padStart(2,'0')+'</span>';
    term.appendChild(pb);term.scrollTop=term.scrollHeight;
    if(e>=dur){
      clearInterval(pgi);clearInterval(mi);clearInterval(xei);
      if(pb&&pb.parentNode)pb.parentNode.removeChild(pb);
      p('','');p('██████████████████████████████████████','ok');
      p('█  ✓ SYSTEM FULLY COMPROMISED ✓   █','ok');
      p('█  Data: 2.4 GB stolen            █','ok');
      p('█  Backdoors: 3 active            █','ok');
      p('█  Traces: 0 remaining            █','ok');
      p('██████████████████████████████████████','ok');
      p('','');p('[√] Goodbye, hacker.','ok');
      try{var a=window._ac||(window._ac=new(window.AudioContext||window.webkitAudioContext)());[400,600,800,1000,1200].forEach(function(f,i){setTimeout(function(){var o=a.createOscillator(),g=a.createGain();o.connect(g);g.connect(a.destination);o.type='sine';o.frequency.value=f;g.gain.setValueAtTime(.08,a.currentTime);g.gain.exponentialRampToValueAtTime(.001,a.currentTime+.3);o.start();o.stop(a.currentTime+.3)},i*180)})}catch(e){}
      running=false;tst('SYSTEM COMPROMISED!');
    }
  },200);
  
  mi=setInterval(function(){
    if(pi>=phase.length)return;
    p('  '+phase[pi][0],phase[pi][1]);
    if(phase[pi][1]==='danger')bp(1200,.08,'sawtooth');
    else if(phase[pi][1]==='warn')bp(800,.05);
    else bp(600,.03);
    pi++;
  },380);
  
  xei=setInterval(function(){
    if(ei>=ex.length)return;
    p('  '+ex[ei],'ok');ei++;
  },280);
}

// ============ COMMANDS ============
var VALID_CMDS=['help','clear','ip','whoami','scan','banner','date'];
var VALID_SLASH=['/chayhack','/chayhacksai','/toimuoidoimk'];

function isValidCmd(lo){
  if(VALID_SLASH.indexOf(lo)>-1)return true;
  if(VALID_CMDS.indexOf(lo)>-1)return true;
  if(lo.indexOf('echo ')==='0')return true;
  return false;
}

function triggerLock(reason){
  p('','');
  p('[!] LỆNH KHÔNG HỢP LỆ!','err');
  if(reason)p('[!] '+reason,'err');
  p('[!] Hệ thống sẽ khóa trong 5 giây...','danger');
  p('','');
  try{var a=window._ac||(window._ac=new(window.AudioContext||window.webkitAudioContext)());[300,250,200,150,100].forEach(function(f,i){setTimeout(function(){var o=a.createOscillator(),g=a.createGain();o.connect(g);g.connect(a.destination);o.type='sawtooth';o.frequency.value=f;g.gain.setValueAtTime(.1,a.currentTime);g.gain.exponentialRampToValueAtTime(.001,a.currentTime+.3);o.start();o.stop(a.currentTime+.3)},i*200)})}catch(e){}
  setTimeout(showLock,800);
}

function cmd(c){
  if(!c)return;
  c=c.trim();if(!c)return;

  if(pwState.active){
    p('<span class="pr">root@hacker:~$</span> *****');
    handlePwStep(c);
    p('&nbsp;');
    inp.focus();
    return;
  }

  p('<span class="pr">root@hacker:~$</span> '+c);
  var lo=c.toLowerCase();

  if(lo==='/toimuoidoimk'){
    startChangePw();
    return;
  }

  if(!isValidCmd(lo)){
    triggerLock('Không phải câu lệnh đã đăng ký');
    return;
  }

  if(lo==='/chayhacksai'){triggerLock('Nhập sai /chayhacksai');return}
  if(lo==='/chayhack'||lo==='chayhack'){runHack();return}

  var out='';
  if(lo==='help'){
    out='Lệnh:\n  /chayhack      - Chạy hack 20s\n  /chayhacksai   - Test lệnh sai\n  /toimuoidoimk  - Đổi mật khẩu\n  help           - Trợ giúp\n  clear          - Xóa màn hình\n  ip             - Lấy IP\n  whoami         - User hiện tại\n  scan           - Quét port\n  banner         - Logo\n  date           - Ngày giờ\n  echo [x]       - In x';
  } else if(lo==='clear'){term.innerHTML='';return}
  else if(lo==='ip'){
    p('Đang lấy IP...','info');
    fetch('https://api.ipify.org?format=json').then(function(r){return r.json()}).then(function(d){p('Your IP: '+d.ip,'info')}).catch(function(){p('Your IP: '+ri(),'info')});
    return;
  }
  else if(lo==='whoami')out='root@hacker\nUser: administrator\nAccess: SUPERUSER';
  else if(lo==='scan'){
    out='Scanning '+ri()+'...';
    [21,22,23,80,443,3306,3389,8080].forEach(function(x){out+='\n  Port '+x+': '+(Math.random()>.6?'OPEN':'closed')});
  }
  else if(lo==='banner')out='  ██╗  ██╗ █████╗  ██████╗██╗  ██╗███████╗██████╗\n  ██║  ██║██╔══██╗██╔════╝██║ ██╔╝██╔════╝██╔══██╗\n  ███████║███████║██║     █████╔╝ █████╗  ██████╔╝\n  ██╔══██║██╔══██║██║     ██╔═██╗ ██╔══╝  ██╔══██╗\n  ██║  ██║██║  ██║╚██████╗██║  ██╗███████╗██║  ██║\n  ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝';
  else if(lo==='date')out=new Date().toLocaleString('vi-VN');
  else if(lo.indexOf('echo ')==='0')out=c.substring(5);
  
  if(out)out.split('\n').forEach(function(l){p(l,'ok')});
  p('&nbsp;');
}

inp.addEventListener('keydown',function(e){
  if(e.key==='Enter'){var v=this.value;this.value='';cmd(v);inp.focus()}
  if(e.key==='Escape'){
    running=false;
    if(pwState.active){cancelChangePw();inp.focus();return}
    tst('Đã dừng');
  }
});
setTimeout(function(){inp.focus()},300);
</script>
</body>
</html>
