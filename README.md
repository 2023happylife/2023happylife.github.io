       <h1>발효식품 공방 효담</h1>
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
