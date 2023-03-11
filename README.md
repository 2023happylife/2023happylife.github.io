<!DOCTYPE html>
<html>
<head>
</head>
<body>
 <h1>쌀누룩 발효식품 공방 효담</h1>
 <p>쌀누룩은 발효식품으로 장기능 개선과 피부건강에 효과적인 제품다.</p>

<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
    </form>
<ul id="product-list">
  <li>쌀누룩 요거트</li>
  <li>콤부차</li>
  <li>제품 3</li>
  <li>제품 4</li>
  <li>제품 5</li>
</ul>

<p>제품 개수: <span id="product-count"></span></p>

<script>
  // 제품 목록 요소를 가져옵니다.
  const productList = document.getElementById('product-list');
  // 제품 개수를 계산하여 표시할 요소를 가져옵니다.
  const productCount = document.getElementById('product-count');
  // 제품 개수를 계산하여 표시합니다.
  productCount.textContent = productList.children.length;
</script>

       </body>
</html> 

<ul id="product-list">
  <li>제품 1</li>
  <li>제품 2</li>
  <li>제품 3</li>
  <li>제품 4</li>
  <li>제품 5</li>
</ul>

<ul id="product-list">
  <li>
    <span class="product-name">콤부차</span>
    <div class="product-controls">
      <button class="product-count-btn" data-count="1">+1</button>
      <button class="product-count-btn" data-count="2">+2</button>
      <span class="product-count">0</span>
    </div>
  </li>
  <li>
    <span class="product-name">제품 2</span>
    <div class="product-controls">
      <button class="product-count-btn" data-count="1">+1</button>
      <button class="product-count-btn" data-count="2">+2</button>
      <span class="product-count">0</span>
    </div>
  </li>
  <li>
    <span class="product-name">제품 3</span>
    <div class="product-controls">
      <button class="product-count-btn" data-count="1">+1</button>
      <button class="product-count-btn" data-count="2">+2</button>
      <span class="product-count">0</span>
    </div>
  </li>
</ul>

<ul>
  <li>
    <span>콤부차</span>
    <button class="count-btn" data-count="1">+1</button>
    <button class="count-btn" data-count="2">+2</button>
    <span class="count">0</span>
  </li>
</ul>

<script>
  // 버튼 클릭 이벤트 처리
  const countBtns = document.querySelectorAll('.count-btn');
  const countSpans = document.querySelectorAll('.count');
  const productNames = document.querySelectorAll('li span');
  
  countBtns.forEach((btn, index) => {
    btn.addEventListener('click', () => {
      const count = parseInt(btn.getAttribute('data-count'));
      const currentCount = parseInt(countSpans[index].textContent);
      const newCount = currentCount + count;
      countSpans[index].textContent = newCount;
    });
  });
</script>


