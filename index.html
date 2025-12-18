<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>금액 평균 계산기 (Firebase)</title>

  <!-- Firebase SDK -->
  <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>

  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 400px;
      margin: 40px auto;
    }
    input, button {
      padding: 8px;
      font-size: 16px;
    }
    li {
      display: flex;
      justify-content: space-between;
      margin-bottom: 6px;
    }
    .delete {
      background: red;
      color: white;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>

<h2>금액 기록</h2>

<input type="number" id="amountInput" placeholder="금액 입력">
<button onclick="saveAmount()">저장</button>

<h3>저장된 금액</h3>
<ul id="amountList"></ul>

<h3>평균 금액: <span id="average">0</span> 원</h3>

<script>
  // 🔥 Firebase 설정 (여기에 본인 설정 붙여넣기)
  const firebaseConfig = {
    apiKey: "AIzaSyBCEHZSZe2wpeHc6WctUcjyUuNS8p3fxqI",
    authDomain: "hwidao-5f9de.firebaseapp.com",
    projectId: "hwidao-5f9de",
  };

  firebase.initializeApp(firebaseConfig);
  const db = firebase.firestore();
  const collectionRef = db.collection("amounts");

  // 금액 저장
  function saveAmount() {
    const input = document.getElementById("amountInput");
    const value = Number(input.value);

    if (!value) {
      alert("금액을 입력하세요");
      return;
    }

    collectionRef.add({
      amount: value,
      createdAt: firebase.firestore.FieldValue.serverTimestamp()
    });

    input.value = "";
  }

  // 금액 삭제
  function deleteAmount(id) {
    collectionRef.doc(id).delete();
  }

  // 실시간 렌더링
  collectionRef.orderBy("createdAt").onSnapshot(snapshot => {
    const list = document.getElementById("amountList");
    const avgSpan = document.getElementById("average");

    list.innerHTML = "";
    let sum = 0;
    let count = 0;

    snapshot.forEach(doc => {
      const data = doc.data();
      sum += data.amount;
      count++;

      const li = document.createElement("li");
      li.innerHTML = `
        <span>${data.amount.toLocaleString()} 원</span>
        <button class="delete" onclick="deleteAmount('${doc.id}')">삭제</button>
      `;
      list.appendChild(li);
    });

    const average = count ? Math.round(sum / count) : 0;
    avgSpan.textContent = average.toLocaleString();
  });
</script>

</body>
</html>
