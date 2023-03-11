<!DOCTYPE html>
<html>
<head>
</head>
<body>
 <h1>쌀누룩 발효식품 공방 효담</h1>
 <p>쌀누룩은 발효식품으로 장기능 개선과 피부건강에 효과적인 제품입니다.</p>

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
