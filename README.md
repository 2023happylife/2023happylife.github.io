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


