[Uploading index2-3.html…]()

<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#0b1220">
<title>OXANA BITCOIN PRO</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:#0b1220;color:#fff;font-family:Tahoma,Arial,sans-serif}
header{text-align:center;padding:22px;background:#131e30;border-bottom:1px solid #34445d}
h1{color:#f0b90b;margin:0 0 8px}
main{max-width:720px;margin:auto;padding:14px}
.card{background:#172337;border:1px solid #34445d;border-radius:14px;padding:17px;margin-bottom:14px}
h2{font-size:17px;color:#f0b90b;margin:0 0 14px}
.price{font-size:29px;font-weight:bold;direction:ltr;text-align:right}
.muted{font-size:13px;color:#aab8cc;line-height:1.9}
input{width:100%;padding:13px;margin:8px 0;background:#0c1728;color:white;border:1px solid #43536c;border-radius:8px;direction:ltr}
button{padding:12px 15px;margin:4px;border:0;border-radius:8px;background:#f0b90b;color:#171717;font-weight:bold;cursor:pointer}
.secondary{background:#34445d;color:white}
.danger{background:#a93c48;color:white}
.send-button{background:#159957;color:white;width:100%;font-size:16px;margin-top:12px;padding:15px}
.actions{display:flex;flex-wrap:wrap;gap:5px}
.stat{display:flex;justify-content:space-between;gap:10px;padding:10px 0;border-bottom:1px solid #34445d}
.tx{padding:12px;margin-top:8px;background:#0c1728;border-radius:8px;overflow-wrap:anywhere;font-size:12px}
.tx a{display:block;color:#f0b90b;margin-top:8px}
.warning{background:#392e16;border:1px solid #76602a;padding:12px;border-radius:8px;color:#f5d88c;font-size:13px;line-height:1.9;margin-top:12px}
footer{text-align:center;padding:20px;color:#8291a8;font-size:12px}
</style>
</head>
<body>

<header>
<h1>OXANA BITCOIN PRO</h1>
<div class="muted">داشبورد مدیریت بیت‌کوین</div>
</header>

<main>

<section class="card">
<h2>قیمت بیت‌کوین</h2>
<div class="price" id="btcPrice">در حال دریافت...</div>
<p id="priceStatus" class="muted">اتصال به بازار...</p>
</section>

<section class="card">
<h2>مدیریت آدرس کیف پول</h2>
<label for="btcAddress">آدرس عمومی بیت‌کوین</label>
<input id="btcAddress" placeholder="آدرس عمومی BTC" autocomplete="off" spellcheck="false">
<div class="actions">
<button id="saveAddress">ذخیره و بررسی</button>
<button id="refreshAddress" class="secondary">به‌روزرسانی</button>
<button id="clearAddress" class="danger">پاک کردن</button>
</div>
<p id="addressStatus" class="muted">آدرسی ثبت نشده است.</p>
</section>

<section class="card">
<h2>اطلاعات کیف پول</h2>
<div class="stat"><span>موجودی تأییدشده</span><strong id="confirmed">—</strong></div>
<div class="stat"><span>موجودی تأییدنشده</span><strong id="pending">—</strong></div>
<div class="stat"><span>تعداد تراکنش‌ها</span><strong id="txCount">—</strong></div>
</section>

<section class="card">
<h2>آخرین تراکنش‌ها</h2>
<div id="transactions" class="muted">ابتدا آدرس عمومی را ثبت کنید.</div>
</section>

<section class="card">
<h2>محاسبه کارمزد و ارسال بیت‌کوین</h2>
<label for="destination">آدرس مقصد</label>
<input id="destination" placeholder="آدرس دریافت‌کننده BTC" autocomplete="off" spellcheck="false">

<label for="amount">مقدار بیت‌کوین (BTC)</label>
<input id="amount" type="number" min="0" step="0.00000001" placeholder="مثلاً 0.001">

<div class="stat"><span>مقدار ساتوشی</span><strong id="sats">—</strong></div>
<div class="stat"><span>نرخ کارمزد</span><strong id="feeRate">—</strong></div>
<div class="stat"><span>کارمزد تخمینی</span><strong id="fee">—</strong></div>
<div class="stat"><span>مجموع مبلغ و کارمزد</span><strong id="total">—</strong></div>

<p id="sendStatus" class="muted">مقصد و مقدار را وارد کنید.</p>

<div class="actions">
<button id="calculateSend">محاسبه کارمزد</button>
<button id="clearSend" class="danger">پاک کردن فرم</button>
</div>

<button id="realSend" class="send-button">بازکردن درخواست ارسال در کیف پول</button>

<div class="warning">
این دکمه درخواست پرداخت استاندارد بیت‌کوین (BIP21) را به کیف پول سازگار منتقل می‌کند. تراکنش فقط پس از بررسی، امضا و تأیید شما در کیف پول ارسال می‌شود.
<br><br>
این داشبورد کلید خصوصی ندارد و به‌تنهایی تراکنش را امضا یا منتشر نمی‌کند. بازشدن کیف پول به معنی ارسال قطعی نیست.
<br><br>
کارمزد نمایش‌داده‌شده تخمینی است و کارمزد نهایی را کیف پول تعیین می‌کند.
</div>
</section>

<section class="card">
<h2>Trust Wallet</h2>
<button id="openTrust">بازکردن Trust Wallet</button>
<p id="walletStatus" class="muted">پشتیبانی از درخواست پرداخت بیت‌کوین به نسخه و تنظیمات کیف پول بستگی دارد.</p>
</section>

</main>

<footer>OXANA BITCOIN PRO</footer>

<script>
"use strict";

const $=id=>document.getElementById(id);
const API="https://blockstream.info/api";
let requestId=0;

function validAddress(a){
 if(!a||a.length>90)return false;
 return /^[13][a-km-zA-HJ-NP-Z1-9]{25,34}$/.test(a)||
 /^bc1[ac-hj-np-z02-9]{11,71}$/i.test(a);
}

function setStatus(t,error=false){
 $("addressStatus").textContent=t;
 $("addressStatus").style.color=error?"#ff8080":"#8de0a8";
}

function resetWallet(){
 $("confirmed").textContent="—";
 $("pending").textContent="—";
 $("txCount").textContent="—";
 $("transactions").textContent="آدرسی ثبت نشده است.";
}

async function loadPrice(){
 try{
  const r=await fetch("https://api.coinbase.com/v2/prices/BTC-USD/spot");
  if(!r.ok)throw Error();
  const d=await r.json();
  $("btcPrice").textContent="$"+Number(d.data.amount).toLocaleString("en-US",{maximumFractionDigits:2});
  $("priceStatus").textContent="قیمت از Coinbase دریافت شد.";
 }catch(e){
  $("priceStatus").textContent="دریافت قیمت ناموفق بود.";
 }
}

async function loadAddress(){
 const a=$("btcAddress").value.trim();
 if(!validAddress(a)){
  setStatus("ساختار اولیه آدرس معتبر نیست.",true);
  return;
 }
 const id=++requestId;
 setStatus("در حال دریافت اطلاعات شبکه...");
 try{
  const r=await fetch(API+"/address/"+encodeURIComponent(a));
  if(!r.ok)throw Error("دریافت اطلاعات آدرس ناموفق بود.");
  const d=await r.json();
  if(id!==requestId)return;
  const c=d.chain_stats.funded_txo_sum-d.chain_stats.spent_txo_sum;
  const p=d.mempool_stats.funded_txo_sum-d.mempool_stats.spent_txo_sum;
  $("confirmed").textContent=(c/1e8).toFixed(8)+" BTC";
  $("pending").textContent=(p/1e8).toFixed(8)+" BTC";
  $("txCount").textContent=d.chain_stats.tx_count+d.mempool_stats.tx_count;
  localStorage.setItem("oxana_public_address",a);
  await loadTransactions(a,id);
  if(id===requestId)setStatus("اطلاعات به‌روزرسانی شد.");
 }catch(e){
  if(id===requestId)setStatus(e.message,true);
 }
}

async function loadTransactions(a,id){
 const r=await fetch(API+"/address/"+encodeURIComponent(a)+"/txs");
 if(!r.ok)throw Error("دریافت تراکنش‌ها ناموفق بود.");
 const list=await r.json();
 if(id!==requestId)return;
 const box=$("transactions");
 box.replaceChildren();
 if(!list.length){
  box.textContent="تراکنشی پیدا نشد.";
  return;
 }
 list.slice(0,6).forEach(tx=>{
  const item=document.createElement("div");
  item.className="tx";
  const hash=document.createElement("div");
  hash.textContent=tx.txid;
  const link=document.createElement("a");
  link.href="https://blockstream.info/tx/"+encodeURIComponent(tx.txid);
  link.target="_blank";
  link.rel="noopener noreferrer";
  link.textContent="مشاهده تراکنش";
  item.append(hash,link);
  box.appendChild(item);
 });
}

function clearAddress(){
 requestId++;
 $("btcAddress").value="";
 localStorage.removeItem("oxana_public_address");
 resetWallet();
 setStatus("آدرس پاک شد.");
}

function getPaymentDetails(){
 const a=$("destination").value.trim();
 const raw=$("amount").value;
 const amount=Number(raw);
 if(!validAddress(a))throw Error("آدرس مقصد معتبر نیست.");
 if(!raw||!Number.isFinite(amount)||amount<=0)throw Error("مقدار BTC معتبر وارد کنید.");
 const sats=Math.round(amount*1e8);
 if(!Number.isSafeInteger(sats)||sats<1)throw Error("مقدار واردشده معتبر نیست.");
 return {address:a,sats:sats};
}

async function calculateSend(){
 let details;
 try{
  details=getPaymentDetails();
 }catch(e){
  $("sendStatus").textContent=e.message;
  return;
 }
 $("sats").textContent=details.sats.toLocaleString("en-US")+" sats";
 $("sendStatus").textContent="در حال دریافت نرخ کارمزد...";
 try{
  const r=await fetch("https://mempool.space/api/v1/fees/recommended");
  if(!r.ok)throw Error();
  const f=await r.json();
  const rate=Number(f.halfHourFee);
  if(!Number.isFinite(rate)||rate<=0)throw Error();
  const fee=Math.ceil(rate*140);
  const total=details.sats+fee;
  if(!Number.isSafeInteger(total))throw Error();
  $("feeRate").textContent=rate+" sat/vB";
  $("fee").textContent=fee.toLocaleString("en-US")+" sats";
  $("total").textContent=(total/1e8).toFixed(8)+" BTC";
  $("sendStatus").textContent="محاسبه انجام شد. برای ادامه دکمه ارسال را بزنید.";
 }catch(e){
  $("feeRate").textContent="—";
  $("fee").textContent="—";
  $("total").textContent="—";
  $("sendStatus").textContent="دریافت کارمزد ناموفق بود.";
 }
}

function realSend(){
 let details;
 try{
  details=getPaymentDetails();
 }catch(e){
  $("sendStatus").textContent=e.message;
  return;
 }
 const btcAmount=(details.sats/1e8).toFixed(8);
 const confirmed=window.confirm(
  "آیا می‌خواهید درخواست پرداخت بیت‌کوین را به کیف پول منتقل کنید؟\n\n"+
  "آدرس مقصد:\n"+details.address+
  "\n\nمبلغ: "+btcAmount+" BTC"+
  "\n\nآدرس و مبلغ را در کیف پول دوباره بررسی کنید."
 );
 if(!confirmed)return;

 const paymentURI="bitcoin:"+details.address+"?amount="+btcAmount;
 $("sendStatus").textContent="در حال بازکردن درخواست پرداخت در کیف پول...";
 $("walletStatus").textContent="درخواست پرداخت آماده انتقال است. تأیید نهایی باید در کیف پول انجام شود.";
 window.location.href=paymentURI;
}

function clearSend(){
 $("destination").value="";
 $("amount").value="";
 $("sats").textContent="—";
 $("feeRate").textContent="—";
 $("fee").textContent="—";
 $("total").textContent="—";
 $("sendStatus").textContent="فرم پاک شد.";
}

$("saveAddress").addEventListener("click",loadAddress);
$("refreshAddress").addEventListener("click",loadAddress);
$("clearAddress").addEventListener("click",clearAddress);
$("calculateSend").addEventListener("click",calculateSend);
$("clearSend").addEventListener("click",clearSend);
$("realSend").addEventListener("click",realSend);

$("openTrust").addEventListener("click",()=>{
 $("walletStatus").textContent="در حال بازکردن Trust Wallet...";
 window.location.href="https://link.trustwallet.com/";
});

function initialize(){
 const saved=localStorage.getItem("oxana_public_address");
 if(saved&&validAddress(saved)){
  $("btcAddress").value=saved;
  loadAddress();
 }
 loadPrice();
 setInterval(loadPrice,60000);
}

initialize();
</script>
</body>
</html>
