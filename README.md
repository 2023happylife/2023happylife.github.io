<!DOCTYPE html>
<html>
<head>
</head>
<body>
 <h1>쌀누룩 발효식품 공방 효담</h1>
 <p>쌀누룩은 발효식품으로 장기능 개선과 피부건강에 효과적인 제품이니다.</p>

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

<p>보여줄 제품 개수:
  <select id="product-count-selector">
    <option value="5">5개</option>
    <option value="10">10개</option>
    <option value="15">15개</option>
  </select>
</p>

<p>선택된 제품 개수: <span id="product-count"></span></p>

<script>
  // 제품 목록 요소를 가져옵니다.
  const productList = document.getElementById('product-list');
  // 선택 옵션 요소를 가져옵니다.
  const productCountSelector = document.getElementById('product-count-selector');
  // 선택된 제품 개수를 표시할 요소를 가져옵니다.
  const productCount = document.getElementById('product-count');

  // 선택 옵션 변경 시 이벤트를 처리하는 함수를 작성합니다.
  function handleProductCountChange() {
    // 선택된 제품 개수를 계산합니다.
    const selectedCount = parseInt(productCountSelector.value, 10);
    // 제품 개수를 계산하여 표시합니다.
    productCount.textContent = productList.children.length > selectedCount ? selectedCount : productList.children.length;
  }

  // 선택 옵션 변경 시 이벤트를 처리합니다.
  productCountSelector.addEventListener('change', handleProductCountChange);

  // 페이지 로드 시 제품 개수를 초기화합니다.
  handleProductCountChange();
</script>
