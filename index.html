<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>🌱 GROW A GARDEN MEGA SHOP</title>
<style>
body { font-family:sans-serif; margin:0; padding:0; background: var(--bg); color: var(--text); }
:root { --bg:#fff; --text:#000; --card:#f3f3f3; }
.dark { --bg:#121212; --text:#fff; --card:#1e1e1e; }
header { padding:10px; background:green; color:#fff; display:flex; justify-content:space-between; align-items:center; position:relative; }
.menu-btn { font-size:24px; cursor:pointer; margin-left:10px; }
.dropdown { display:none; position:absolute; top:50px; right:10px; background:var(--card); border-radius:8px; padding:10px; box-shadow:0 2px 6px rgba(0,0,0,0.3); z-index:100; }
.dropdown button { display:block; width:100%; margin:5px 0; }
.container { padding:15px; }
.card { background:var(--card); padding:10px; border-radius:12px; margin-bottom:10px; position:relative; }
button { padding:8px 12px; margin:4px 0; border:none; border-radius:10px; cursor:pointer; background:green; color:#fff; }
input, select, textarea { width:100%; padding:8px; margin:5px 0; border-radius:8px; border:1px solid #ccc; }
.chat-box { max-height:300px; overflow-y:auto; background:var(--card); padding:10px; border-radius:10px; margin-bottom:10px; display:flex; flex-direction:column; gap:5px;}
.message { display:flex; align-items:flex-start; gap:5px; margin:5px 0; }
.message .from { font-weight:bold; }
.profile-img { width:100px; height:100px; border-radius:50%; object-fit:cover; margin-bottom:10px; }
.ad-owner-img { width:50px; height:50px; border-radius:50%; object-fit:cover; float:right; margin-left:10px; }
.profile-header { display:flex; align-items:center; gap:10px; justify-content:space-between; }
.ad-actions { margin-top:10px; display:flex; gap:5px; flex-wrap:wrap;}
.back-btn { margin-bottom:10px; }
.eye-btn { position:absolute; top:35px; left:10px; cursor:pointer; background:none; border:none; font-size:16px; }
.relative { position:relative; }
</style>
</head>
<body>
<header>
  <span id="appName">🌱 GROW A GARDEN MEGA SHOP</span>
  <div>
    <span class="menu-btn" onclick="toggleDropdown()">☰</span>
    <button onclick="toggleTheme()">🌓</button>
    <select id="langSelect" onchange="changeLang()">
      <option value="ar">عربي</option>
      <option value="en">English</option>
    </select>
    <div class="dropdown" id="dropdownMenu">
      <button onclick="render()">الرئيسية</button>
      <button onclick="showFollowers()">المتابعين</button>
      <button onclick="showFollowing()">المتابعة</button>
      <button onclick="showMyAccount()">حسابي</button>
      <button onclick="showNewAd()">نشر إعلان</button>
      <button onclick="showChats()">المحادثات</button>
      <button onclick="showSearch()">البحث</button>
      <button onclick="logout()">تسجيل خروج</button>
      <div id="adminMenu" style="display:none;">
        <hr>
        <button onclick="showAllUsers()">كل المستخدمين</button>
        <button onclick="showReports()">التقارير</button>
      </div>
    </div>
  </div>
</header>

<div class="container" id="app"></div>

<script>
let users = JSON.parse(localStorage.getItem("users") || "[]");
let ads = JSON.parse(localStorage.getItem("ads") || "[]");
let chats = JSON.parse(localStorage.getItem("chats") || "[]");
let reports = JSON.parse(localStorage.getItem("reports") || "[]");
let currentUser = JSON.parse(localStorage.getItem("currentUser") || "null");
let lang = localStorage.getItem("lang") || "ar";
const adminEmail = "haddadgabi9@gmail.com";
const adminPass = "ga1bi2ha3dd4ad";

function save(){
  localStorage.setItem("users",JSON.stringify(users));
  localStorage.setItem("ads",JSON.stringify(ads));
  localStorage.setItem("chats",JSON.stringify(chats));
  localStorage.setItem("reports",JSON.stringify(reports));
  localStorage.setItem("currentUser",JSON.stringify(currentUser));
  localStorage.setItem("lang",lang);
}

function toggleDropdown(){
  const menu = document.getElementById("dropdownMenu");
  menu.style.display = menu.style.display==="block"?"none":"block";
}
function toggleDropdownClose(){ document.getElementById("dropdownMenu").style.display="none"; }
function toggleTheme(){ document.body.classList.toggle("dark"); }
function changeLang(){ lang = document.getElementById("langSelect").value; save(); render(); }

function backButton(){ render(); } // زر الرجوع للصفحة الرئيسية

// ====================== الصفحة الرئيسية ======================
function render(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  if(!currentUser) return showLogin();
  document.getElementById("adminMenu").style.display=(currentUser.email.toLowerCase()===adminEmail.toLowerCase())?"block":"none";

  let html=`<h2>${lang==="ar"?"مرحبا":"Welcome"} ${currentUser.username || currentUser.email}</h2><hr><h3>📢 ${lang==="ar"?"الإعلانات":"Ads"}</h3>`;
  ads.forEach(ad=>{
    let owner = users.find(u => u.email === ad.owner);
    let ownerImg = owner && owner.profile ? `<img src="${owner.profile}" class="ad-owner-img">` : "";
    html += `<div class="card">
      <div class="profile-header">
        ${ownerImg}
        <div>
          <p><b>${owner.username}</b></p>
          <div class="ad-actions">
            <button onclick="showMessage('${owner.email}')">${lang==="ar"?"مراسلة":"Message"}</button>
            <button onclick="showProfile('${owner.email}')">${lang==="ar"?"عرض الملف الشخصي":"Profile"}</button>
            <button onclick="showReportAd(${ad.id})">${lang==="ar"?"إبلاغ":"Report"}</button>
            ${(currentUser.email === ad.owner || currentUser.email.toLowerCase() === adminEmail.toLowerCase()) ? `<button onclick="deleteAd(${ad.id})">🗑 ${lang==="ar"?"حذف":"Delete"}</button>` : ""}
          </div>
        </div>
      </div>
      <p><b>${ad.title}</b></p>
      ${ad.img ? `<img src="${ad.img}" width="100%">` : ""}
    </div>`;
  });
  app.innerHTML=html;
}

// ====================== صفحات المستخدم ======================
function showFollowers(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  let followers = currentUser.followers || [];
  let html=`<button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button><h2>${lang==="ar"?"المتابعين":"Followers"}</h2>`;
  if(followers.length===0) html+="<p>"+(lang==="ar"?"لا يوجد متابعين":"No followers")+"</p>";
  else followers.forEach(email=>{
    let u = users.find(x=>x.email===email);
    if(u) html+=`<div class="card"><img src="${u.profile||''}" class="profile-img"><p>${u.username}</p><button onclick="showProfile('${u.email}')">${lang==="ar"?"عرض الملف الشخصي":"Profile"}</button></div>`;
  });
  app.innerHTML=html;
}

function showFollowing(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  let following = users.filter(u=>u.followers && u.followers.includes(currentUser.email));
  let html=`<button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button><h2>${lang==="ar"?"المتابعة":"Following"}</h2>`;
  if(following.length===0) html+="<p>"+(lang==="ar"?"لا تتابع أحد":"Not following anyone")+"</p>";
  else following.forEach(u=>html+=`<div class="card"><img src="${u.profile||''}" class="profile-img"><p>${u.username}</p><button onclick="showProfile('${u.email}')">${lang==="ar"?"عرض الملف الشخصي":"Profile"}</button></div>`);
  app.innerHTML=html;
}

function showMyAccount(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  app.innerHTML=`
    <button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button>
    <h2>${lang==="ar"?"حسابي":"My Account"}</h2>
    <img src="${currentUser.profile||''}" class="profile-img">
    <p><b>${lang==="ar"?"اسم المستخدم":"Username"}:</b> ${currentUser.username}</p>
    <p><b>Email:</b> ${currentUser.email}</p>
    <button onclick="showNewAd()">${lang==="ar"?"نشر إعلان":"Post Ad"}</button>
    <div class="ad-actions">
      <button onclick="alert('Add friend coming')">${lang==="ar"?"كصديق":"Add Friend"}</button>
      <button onclick="showMessage('${currentUser.email}')">${lang==="ar"?"مراسلة":"Message"}</button>
    </div>
  `;
}

// ====================== نشر إعلان ======================
function showNewAd(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  app.innerHTML=`
    <button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button>
    <h2>${lang==="ar"?"نشر إعلان":"Post Ad"}</h2>
    <input id="adTitle" placeholder="${lang==="ar"?"عنوان الإعلان":"Ad Title"}">
    <input type="file" id="adImg" accept="image/*">
    <button onclick="postAd()">${lang==="ar"?"نشر":"Post"}</button>
  `;
}

function postAd(){
  const title=document.getElementById("adTitle").value.trim();
  const file=document.getElementById("adImg").files[0];
  if(!title) return alert(lang==="ar"?"العنوان مطلوب":"Title required");
  let reader=new FileReader();
  reader.onload=e=>{
    const ad={id:Date.now(),title,owner:currentUser.email,img:e.target.result};
    ads.push(ad);
    save();
    render();
  };
  if(file) reader.readAsDataURL(file);
  else { const ad={id:Date.now(),title,owner:currentUser.email,img:null}; ads.push(ad); save(); render(); }
}

// ====================== الدردشة المتقدمة ======================
function showChats(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  let html=`<button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button>
    <h2>${lang==="ar"?"المحادثات":"Chats"}</h2>
    <div id="chatUsers"></div>
    <div class="chat-box" id="chatBox"></div>
    <input id="chatInput" placeholder="${lang==="ar"?"اكتب رسالة":"Type message"}">
    <button onclick="sendChat()">${lang==="ar"?"إرسال":"Send"}</button>`;
  app.innerHTML=html;
  renderChatUsers();
}

function renderChatUsers(){
  const chatUsersDiv = document.getElementById("chatUsers");
  chatUsersDiv.innerHTML="<h3>"+(lang==="ar"?"المستخدمون":"Users")+"</h3>";
  users.forEach(u=>{
    if(u.email!==currentUser.email){
      let btn = `<button onclick="openChat('${u.email}')">${u.username}</button>`;
      chatUsersDiv.innerHTML += `<div class="card">${btn}</div>`;
    }
  });
}

let activeChatUser=null;
function openChat(email){
  activeChatUser=email;
  renderChatsMessages();
}

function renderChatsMessages(){
  const chatBox = document.getElementById("chatBox");
  chatBox.innerHTML="";
  chats.filter(c=> (c.from===currentUser.email && c.to===activeChatUser) || (c.from===activeChatUser && c.to===currentUser.email))
       .forEach(c=>{ chatBox.innerHTML += `<div class="message"><span class="from">${c.from===currentUser.email?lang==="ar"?"أنت":"You":c.from}:</span> ${c.msg}</div>` });
}

function sendChat(){
  const msg=document.getElementById("chatInput").value.trim();
  if(!msg || !activeChatUser) return;
  chats.push({from:currentUser.email,to:activeChatUser,msg});
  save();
  document.getElementById("chatInput").value="";
  renderChatsMessages();
}

// ====================== البحث ======================
function showSearch(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  app.innerHTML=`
    <button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button>
    <h2>${lang==="ar"?"بحث":"Search"}</h2>
    <input id="searchInput" placeholder="${lang==="ar"?"ابحث عن إعلان أو مستخدم":"Search ad or user"}">
    <button onclick="performSearch()">${lang==="ar"?"بحث":"Search"}</button>
    <div id="searchResults"></div>
  `;
}

function performSearch(){
  const val=document.getElementById("searchInput").value.toLowerCase();
  let results='';
  users.forEach(u=>{
    if(u.username.toLowerCase().includes(val)) results+=`<div class="card">${u.username}<button onclick="showProfile('${u.email}')">${lang==="ar"?"عرض الملف الشخصي":"Profile"}</button></div>`;
  });
  ads.forEach(ad=>{
    if(ad.title.toLowerCase().includes(val)) results+=`<div class="card">${ad.title}</div>`;
  });
  document.getElementById("searchResults").innerHTML=results||"<p>"+(lang==="ar"?"لا توجد نتائج":"No results")+"</p>";
}

// ====================== تسجيل الدخول/تسجيل خروج ======================
function showLogin(){
  toggleDropdownClose();
  document.getElementById("app").innerHTML=`
    <h2>${lang==="ar"?"تسجيل الدخول":"Login"}</h2>
    <input id="username" placeholder="${lang==="ar"?"اسم المستخدم":"Username"}">
    <div class="relative">
      <input id="pass" type="password" placeholder="${lang==="ar"?"كلمة المرور":"Password"}">
      <button class="eye-btn" onclick="togglePassword()">👁</button>
    </div>
    <input id="email" placeholder="${lang==="ar"?"البريد":"Email"}">
    <button onclick="login()">${lang==="ar"?"دخول":"Login"}</button>
    <button onclick="showRegister()">${lang==="ar"?"إنشاء حساب":"Register"}</button>`;
}

function togglePassword(){
  const input=document.getElementById("pass");
  input.type = input.type==="password"?"text":"password";
}

function login(){
  const email=document.getElementById("email").value.trim();
  const pass=document.getElementById("pass").value;
  const username=document.getElementById("username").value.trim();
  if(email.toLowerCase()===adminEmail.toLowerCase() && pass===adminPass){
    let u=users.find(x=>x.email.toLowerCase()===adminEmail.toLowerCase());
    if(!u){ u={email:adminEmail,pass:adminPass,followers:[],profile:null,username:"Admin"}; users.push(u); save();}
    currentUser=u; save(); render(); return;
  }
  const u=users.find(x=>x.email.toLowerCase()===email.toLowerCase() && x.pass===pass && x.username===username);
  if(u){ currentUser=u; save(); render(); }
  else alert(lang==="ar"?"معلومات خاطئة":"Wrong info");
}

function showRegister(){
  toggleDropdownClose();
  document.getElementById("app").innerHTML=`
    <h2>${lang==="ar"?"إنشاء حساب":"Register"}</h2>
    <input id="username" placeholder="${lang==="ar"?"اسم المستخدم":"Username"}">
    <input id="email" placeholder="${lang==="ar"?"البريد":"Email"}">
    <input type="password" id="pass" placeholder="${lang==="ar"?"كلمة المرور":"Password"}">
    <input type="file" id="profileImg" accept="image/*">
    <button onclick="register()">${lang==="ar"?"تسجيل":"Register"}</button>
    <button onclick="showLogin()">⬅ ${lang==="ar"?"رجوع":"Back"}</button>`;
}

function register(){
  const username=document.getElementById("username").value.trim();
  const email=document.getElementById("email").value.trim();
  const pass=document.getElementById("pass").value;
  if(!username || !email || !pass) return alert(lang==="ar"?"جميع الحقول مطلوبة":"All fields required");
  if(users.find(x=>x.email.toLowerCase()===email.toLowerCase())) return alert(lang==="ar"?"موجود مسبقاً":"Already exists");
  const file=document.getElementById("profileImg").files[0];
  let reader = new FileReader();
  reader.onload = e => {
    const newUser = {
      username,
      email,
      pass,
      profile: e.target.result || null,
      followers: []
    };
    users.push(newUser);
    currentUser = newUser;
    save();
    render();
  };
  if(file) reader.readAsDataURL(file);
  else {
    const newUser = {
      username,
      email,
      pass,
      profile: null,
      followers: []
    };
    users.push(newUser);
    currentUser = newUser;
    save();
    render();
  }
}

// ====================== البلاغات ======================
function showReportAd(adId){
  const reason = prompt(lang==="ar"?"اكتب سبب البلاغ":"Write reason for report");
  if(reason){
    reports.push({adId, reporter:currentUser.email, reason});
    save();
    alert(lang==="ar"?"تم إرسال البلاغ":"Report sent");
  }
}

// ====================== حذف إعلان ======================
function deleteAd(adId){
  if(confirm(lang==="ar"?"هل أنت متأكد من الحذف؟":"Are you sure to delete?")){
    ads = ads.filter(a=>a.id!==adId);
    save();
    render();
  }
}

// ====================== عرض الملف الشخصي ======================
function showProfile(email){
  const user = users.find(u=>u.email===email);
  if(!user) return alert(lang==="ar"?"المستخدم غير موجود":"User not found");
  const app = document.getElementById("app");
  let html=`<button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button>
    <h2>${lang==="ar"?"الملف الشخصي":"Profile"}</h2>
    <img src="${user.profile||''}" class="profile-img">
    <p><b>${lang==="ar"?"اسم المستخدم":"Username"}:</b> ${user.username}</p>
    <p><b>Email:</b> ${user.email}</p>
    <button onclick="followUser('${user.email}')">${user.followers && user.followers.includes(currentUser.email)?(lang==="ar"?"إلغاء متابعة":"Unfollow"):(lang==="ar"?"متابعة":"Follow")}</button>
    <button onclick="showMessage('${user.email}')">${lang==="ar"?"مراسلة":"Message"}</button>
    ${(currentUser.email.toLowerCase()===adminEmail.toLowerCase())?`<button onclick="deleteUser('${user.email}')">🗑 ${lang==="ar"?"حذف المستخدم":"Delete User"}</button>`:""}`;
  app.innerHTML=html;
}

function followUser(email){
  const user = users.find(u=>u.email===email);
  if(!user) return;
  if(!user.followers) user.followers=[];
  const idx = user.followers.indexOf(currentUser.email);
  if(idx>=0) user.followers.splice(idx,1);
  else user.followers.push(currentUser.email);
  save();
  showProfile(email);
}

// ====================== حذف مستخدم (للادمن) ======================
function deleteUser(email){
  if(confirm(lang==="ar"?"هل أنت متأكد من حذف المستخدم؟":"Are you sure to delete user?")){
    users = users.filter(u=>u.email!==email);
    ads = ads.filter(a=>a.owner!==email);
    chats = chats.filter(c=>c.from!==email && c.to!==email);
    save();
    render();
  }
}

// ====================== إدارة الأدمن ======================
function showAllUsers(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  let html=`<button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button><h2>${lang==="ar"?"كل المستخدمين":"All Users"}</h2>`;
  users.forEach(u=>{
    html+=`<div class="card">
      <img src="${u.profile||''}" class="profile-img">
      <p>${u.username}</p>
      <div class="ad-actions">
        <button onclick="showProfile('${u.email}')">${lang==="ar"?"عرض الملف الشخصي":"Profile"}</button>
        <button onclick="deleteUser('${u.email}')">🗑 ${lang==="ar"?"حذف":"Delete"}</button>
        <button onclick="showMessage('${u.email}')">${lang==="ar"?"مراسلة":"Message"}</button>
      </div>
    </div>`;
  });
  app.innerHTML=html;
}

function showReports(){
  toggleDropdownClose();
  const app=document.getElementById("app");
  let html=`<button class="back-btn" onclick="backButton()">⬅ ${lang==="ar"?"رجوع":"Back"}</button><h2>${lang==="ar"?"التقارير":"Reports"}</h2>`;
  if(reports.length===0) html+="<p>"+(lang==="ar"?"لا توجد تقارير":"No reports")+"</p>";
  reports.forEach(r=>{
    const ad = ads.find(a=>a.id===r.adId);
    const reporter = users.find(u=>u.email===r.reporter);
    html+=`<div class="card">
      <p><b>${lang==="ar"?"المعلن":"Ad"}:</b> ${ad?ad.title:"-"}<br>
      <b>${lang==="ar"?"المبلغ":"Reporter"}:</b> ${reporter?reporter.username:"-"}<br>
      <b>${lang==="ar"?"السبب":"Reason"}:</b> ${r.reason}</p>
    </div>`;
  });
  app.innerHTML=html;
}

// ====================== تسجيل خروج ======================
function logout(){ currentUser=null; save(); showLogin(); }

// بدء التطبيق
showLogin();
</script>
</body>
</html>
