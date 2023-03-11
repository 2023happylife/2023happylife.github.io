<!DOCTYPE html>
<html>
<head>
</head>
<body>
 <h1>쌀누룩 발효식품 공방 효담</h1>
 <p>쌀누룩은 발효식품으로 장기능 개선과 피부건강에 효과적인 제품입니다.</p>

 <div>
  <span>콤부차</span>
  <input type="number" id="quantity" value="0" min="0">
  <button onclick="addToExcel()">확인</button>
</div>
function addToExcel() {
  // 선택된 콤부차 개수 가져오기
  var quantity = document.getElementById("quantity").value;
  
  // CSV 파일에 추가할 데이터 생성
  var data = "콤부차," + quantity;
  
  // CSV 파일 가져오기
  var csv = localStorage.getItem("csv");
  
  // 새로운 데이터를 CSV 파일에 추가
  csv += "\n" + data;
  
  // 업데이트된 CSV 파일을 로컬 스토리지에 저장
  localStorage.setItem("csv", csv);
}

 
 
 
<div class="container">
  <div class="product">
    <span>콤부차</span>
    <div class="quantity">
      <span>수량:</span>
      <input type="number" min="1" max="10" value="1" id="quantity">
    </div>
    <button id="add-to-cart">확인</button>
  </div>
</div>
 
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.product {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-right: 20px;
}

.quantity {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-right: 10px;
}

button {
  padding: 5px 10px;
  background-color: #4CAF50;
  border: none;
  color: white;
}
