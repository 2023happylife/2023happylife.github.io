<!DOCTYPE html>
<html>
<head>
</head>
<body>
 <h1>쌀누룩 발효식품 공방 효담</h1>
 <p>쌀누룩은 발효식품으로 장기능 개선과 피부건강에 효과적인 제품입니다.</p>

<ul>
  <li>
    <span>콤부차</span>
    <div class="count-box">
      <button class="minus-btn">-</button>
      <span class="count">0</span>
      <button class="plus-btn">+</button>
    </div>
  </li>
</ul>

<style>
  .count-box {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    height: 30px;
    border: 1px solid black;
    border-radius: 4px;
  }
  
  .count-box button {
    width: 30px;
    height: 30px;
    background-color: transparent;
    border: none;
    cursor: pointer;
  }
  
  .count-box .count {
    margin: 0 10px;
    font-size: 1.2rem;
    font-weight: bold;
  }
</style>

<script>
  // 버튼 클릭 이벤트 처리
  const minusBtns = document.querySelectorAll('.minus-btn');
  const plusBtns = document.querySelectorAll('.plus-btn');
  const countSpans = document.querySelectorAll('.count');
  const productNames = document.querySelectorAll('li span');
  
  minusBtns.forEach((btn, index) => {
    btn.addEventListener('click', () => {
      const currentCount = parseInt(countSpans[index].textContent);
      const newCount = Math.max(currentCount - 1, 0);
      countSpans[index].textContent = newCount;
    });
  });
  
  plusBtns.forEach((btn, index) => {
    btn.addEventListener('click', () => {
      const currentCount = parseInt(countSpans[index].textContent);
      const newCount = currentCount + 1;
      countSpans[index].textContent = newCount;
    });
  });
</script>

<!DOCTYPE html>
<html>
<head>
	<title>콤부차</title>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<style>
		.container {
			display: flex;
			align-items: center;
			justify-content: space-between;
			padding: 10px;
			border: 1px solid #ddd;
			border-radius: 5px;
			max-width: 400px;
			margin: 0 auto;
		}
		.product-name {
			font-size: 20px;
		}
		.quantity {
			display: flex;
			align-items: center;
			margin-left: 10px;
		}
		.quantity label {
			font-size: 16px;
			margin-right: 10px;
		}
		.quantity input {
			padding: 5px;
			width: 50px;
			border-radius: 5px;
			border: 1px solid #ddd;
			text-align: center;
		}
	</style>
</head>
<body>
	<div class="container">
		<div class="product-name">콤부차</div>
		<div class="quantity">
			<label>수량:</label>
			<input type="number" min="0" max="10" step="1" value="0">
		</div>
	</div>
</body>
</html>

