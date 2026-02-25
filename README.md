<!-- ─── LIVE DEMO BLOCK ─── -->
<div style="margin-top:50px;text-align:center;">

  <button onclick="runLiveDemo()" 
    style="
      padding:16px 36px;
      font-size:1rem;
      font-weight:700;
      border:none;
      border-radius:16px;
      cursor:pointer;
      color:white;
      background:linear-gradient(135deg,#4f46e5,#7c3aed,#a21caf);
      background-size:200% 200%;
      transition:all .4s ease;
      box-shadow:0 10px 30px rgba(79,70,229,.4);
    "
    onmouseover="this.style.transform='translateY(-4px) scale(1.03)';this.style.boxShadow='0 15px 40px rgba(79,70,229,.5)';"
    onmouseout="this.style.transform='none';this.style.boxShadow='0 10px 30px rgba(79,70,229,.4)';"
  >
    🚀 Run Live Demo
  </button>

  <div id="demoOutput"
    style="
      margin-top:24px;
      padding:20px;
      border-radius:16px;
      background:#f8fafc;
      border:1px solid #e2e8f0;
      font-family:monospace;
      font-size:.9rem;
      min-height:60px;
      transition:all .3s ease;
    ">
    Click the button to simulate a data pipeline...
  </div>

</div>

<script>
function runLiveDemo() {
  const output = document.getElementById("demoOutput");

  output.style.background = "#f8fafc";
  output.style.borderColor = "#e2e8f0";

  output.innerHTML = "⏳ Extracting data from API...";

  setTimeout(() => {
    output.innerHTML = "🔄 Transforming data with Pandas & PySpark...";
  }, 1200);

  setTimeout(() => {
    output.innerHTML = "📊 Loading data into Data Warehouse...";
  }, 2400);

  setTimeout(() => {
    output.innerHTML = "✅ Pipeline executed successfully!";
    output.style.background = "#ecfdf5";
    output.style.borderColor = "#10b981";
  }, 3600);
}
</script>
<!-- ─── END LIVE DEMO BLOCK ─── -->
