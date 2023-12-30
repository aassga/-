# -吳曜廷 面試題目 

請回覆下列3個問題，並將程式碼上傳到 github 後分享鏈接給我們。

JavaScript: 字串反轉
function reverseString(str) {
  // 實作你的解答	
  return str.reverse()
}

console.log(reverseString("Hello")); // 預期輸出: "olleH”
2. JavaScript: 陣列過濾
問題：寫一個JavaScript函式，接受一個數字陣列，並返回該陣列中所有大於5的數字。 

範例：

function filterNumbersGreaterThanFive(numbers) {
  // 實作你的解答
  return numbers.filter((el)=> el<5)
}

const numbers = [2, 8, 4, 10, 1, 7];
console.log(filterNumbersGreaterThanFive(numbers)); // 預期輸出: [8, 10, 7]
3. JavaScript: 重構
問題：重構這段程式碼並說明原因

function formatName(firstName, lastName) {
  // 使用模板字符串來組合名字和姓氏
  const formattedName = `${firstName || ''} ${lastName || ''}`.trim();

  return formattedName;
}

重構的理由如下：

模板字符串： 使用模板字符串使得組合名字和姓氏更加簡潔和清晰。

避免多次修改同一變數： 直接在一行中使用模板字符串避免了多次修改 formattedName 變數的需要。

預設值： 使用 || '' 來確保如果 firstName 或 lastName 是 undefined 或 null 時，不會在組合字符串中顯示為 "undefined" 或 "null"。

trim()： 使用 trim() 方法來去除字符串首尾的空格，以確保返回的字符串是整潔的。


4. React: 條件渲染
問題：在React中，如何根據條件渲染兩種不同的內容？

範例：

function ConditionalRendering({ isLoggedIn }) {
  // 實作你的條件渲染
  if (isLoggedIn) {
    return '滿足條件的內容';
  } else {
    return '不滿足條件的內容';
  }
}
5. React: 組件
問題：使用React創建一個簡單的計數器組件，具有增加和減少計數的按鈕。

import React, { useState } from 'react';

function Counter() {
  // 使用狀態（useState）來追蹤計數值
  const [count, setCount] = useState(0);

  // 增加計數的函數
  const increaseCount = () => {
    setCount(count + 1);
  };

  // 減少計數的函數
  const decreaseCount = () => {
    setCount(count - 1);
  };

  return (
    <div>
      <h1>計數器</h1>
      <p>當前計數：{count}</p>
      <button onClick={increaseCount}>增加</button>
      <button onClick={decreaseCount}>減少</button>
    </div>
  );
}

export default Counter;
