<!-- Free Fire UID Verify Button -->
<div class="verify-box">
  <h3>🎮 Free Fire ID Verification</h3>
  <input type="text" id="ffUid" placeholder="Enter Free Fire UID">
  <button onclick="verifyUID()">✅ Verify ID</button>
  <p id="verifyResult"></p>
</div>

<style>
.verify-box {
  max-width: 400px;
  margin: 20px auto;
  padding: 20px;
  background: #111;
  border-radius: 15px;
  text-align: center;
  color: white;
}

.verify-box input {
  width: 90%;
  padding: 12px;
  margin: 10px 0;
  border-radius: 8px;
  border: 1px solid #444;
  background: #222;
  color: white;
}

.verify-box button {
  width: 95%;
  padding: 12px;
  border: none;
  border-radius: 8px;
  background: #ff9800;
  color: white;
  font-weight: bold;
  cursor: pointer;
}

.verify-box button:hover {
  background: #ffb300;
}

#verifyResult {
  margin-top: 12px;
}
</style>

<script>
function verifyUID() {
  const uid = document.getElementById("ffUid").value.trim();
  const result = document.getElementById("verifyResult");

  if (!uid) {
    result.innerHTML = "❌ Please enter your Free Fire UID.";
    return;
  }

  if (!/^[0-9]{5,15}$/.test(uid)) {
    result.innerHTML = "❌ Invalid UID format.";
    return;
  }

  result.innerHTML = "⏳ Verifying UID...";

  // Demo verification
  setTimeout(() => {
    result.innerHTML = "✅ UID format verified: " + uid;
  }, 1000);
}
</script>
