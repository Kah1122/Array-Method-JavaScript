# Tất cả Array Methods trong JavaScript

Dưới đây là danh sách đầy đủ các phương thức mảng trong JavaScript với ví dụ minh họa:

## Phương thức biến đổi mảng (Mutating Methods)

### 1. `push()` - Thêm phần tử vào cuối mảng
```javascript
const fruits = ['apple', 'banana'];
fruits.push('orange'); // ['apple', 'banana', 'orange']
```

### 2. `pop()` - Xóa phần tử cuối mảng
```javascript
const fruits = ['apple', 'banana', 'orange'];
const last = fruits.pop(); // 'orange', mảng còn: ['apple', 'banana']
```

### 3. `shift()` - Xóa phần tử đầu mảng
```javascript
const fruits = ['apple', 'banana', 'orange'];
const first = fruits.shift(); // 'apple', mảng còn: ['banana', 'orange']
```

### 4. `unshift()` - Thêm phần tử vào đầu mảng
```javascript
const fruits = ['banana', 'orange'];
fruits.unshift('apple'); // ['apple', 'banana', 'orange']
```

### 5. `splice()` - Thêm/Xóa phần tử tại vị trí bất kỳ
```javascript
const fruits = ['apple', 'banana', 'orange'];
// Xóa 1 phần tử từ vị trí index 1
fruits.splice(1, 1); // ['apple', 'orange']

// Thêm phần tử tại vị trí index 1
fruits.splice(1, 0, 'grape'); // ['apple', 'grape', 'orange']
```

### 6. `reverse()` - Đảo ngược mảng
```javascript
const numbers = [1, 2, 3];
numbers.reverse(); // [3, 2, 1]
```

### 7. `sort()` - Sắp xếp mảng
```javascript
const numbers = [3, 1, 2];
numbers.sort(); // [1, 2, 3]

const words = ['banana', 'apple', 'cherry'];
words.sort(); // ['apple', 'banana', 'cherry']
```

### 8. `fill()` - Điền giá trị vào mảng
```javascript
const numbers = [1, 2, 3, 4];
numbers.fill(0, 2, 4); // [1, 2, 0, 0] - điền số 0 từ vị trí 2 đến 4
```

## Phương thức truy cập (Accessor Methods - không thay đổi mảng gốc)

### 9. `concat()` - Nối mảng
```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const combined = arr1.concat(arr2); // [1, 2, 3, 4]
```

### 10. `slice()` - Cắt mảng
```javascript
const fruits = ['apple', 'banana', 'orange', 'grape'];
const sliced = fruits.slice(1, 3); // ['banana', 'orange']
```

### 11. `join()` - Chuyển mảng thành chuỗi
```javascript
const fruits = ['apple', 'banana', 'orange'];
const str = fruits.join(', '); // 'apple, banana, orange'
```

### 12. `toString()` - Chuyển mảng thành chuỗi
```javascript
const numbers = [1, 2, 3];
const str = numbers.toString(); // '1,2,3'
```

### 13. `indexOf()` - Tìm vị trí phần tử
```javascript
const fruits = ['apple', 'banana', 'orange'];
const index = fruits.indexOf('banana'); // 1
```

### 14. `lastIndexOf()` - Tìm vị trí phần tử từ cuối
```javascript
const numbers = [1, 2, 3, 2, 1];
const index = numbers.lastIndexOf(2); // 3
```

### 15. `includes()` - Kiểm tra phần tử có tồn tại
```javascript
const fruits = ['apple', 'banana', 'orange'];
const hasBanana = fruits.includes('banana'); // true
```

## Phương thức lặp (Iteration Methods)

### 16. `forEach()` - Lặp qua từng phần tử
```javascript
const numbers = [1, 2, 3];
numbers.forEach((num, index) => {
  console.log(`numbers[${index}] = ${num}`);
});
```

### 17. `map()` - Tạo mảng mới từ mảng cũ
```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2); // [2, 4, 6]
```

### 18. `filter()` - Lọc phần tử theo điều kiện
```javascript
const numbers = [1, 2, 3, 4, 5];
const even = numbers.filter(num => num % 2 === 0); // [2, 4]
```

### 19. `reduce()` - Tính toán tích lũy
```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((total, num) => total + num, 0); // 10
```

### 20. `reduceRight()` - Tính toán tích lũy từ phải sang trái
```javascript
const numbers = [1, 2, 3, 4];
const result = numbers.reduceRight((total, num) => total + num, 0); // 10
```

### 21. `every()` - Kiểm tra tất cả phần tử thỏa điều kiện
```javascript
const numbers = [2, 4, 6, 8];
const allEven = numbers.every(num => num % 2 === 0); // true
```

### 22. `some()` - Kiểm tra có phần tử nào thỏa điều kiện
```javascript
const numbers = [1, 3, 5, 7, 8];
const hasEven = numbers.some(num => num % 2 === 0); // true
```

### 23. `find()` - Tìm phần tử đầu tiên thỏa điều kiện
```javascript
const numbers = [1, 2, 3, 4, 5];
const firstEven = numbers.find(num => num % 2 === 0); // 2
```

### 24. `findIndex()` - Tìm vị trí phần tử đầu tiên thỏa điều kiện
```javascript
const numbers = [1, 2, 3, 4, 5];
const firstEvenIndex = numbers.findIndex(num => num % 2 === 0); // 1
```

### 25. `findLast()` - Tìm phần tử cuối cùng thỏa điều kiện
```javascript
const numbers = [1, 2, 3, 4, 5];
const lastEven = numbers.findLast(num => num % 2 === 0); // 4
```

### 26. `findLastIndex()` - Tìm vị trí phần tử cuối cùng thỏa điều kiện
```javascript
const numbers = [1, 2, 3, 4, 5];
const lastEvenIndex = numbers.findLastIndex(num => num % 2 === 0); // 3
```

## Phương thức mới trong ES6+

### 27. `from()` - Tạo mảng từ đối tượng giống mảng
```javascript
const str = 'hello';
const arr = Array.from(str); // ['h', 'e', 'l', 'l', 'o']
```

### 28. `of()` - Tạo mảng từ các đối số
```javascript
const numbers = Array.of(1, 2, 3, 4); // [1, 2, 3, 4]
```

### 29. `keys()` - Trả về iterator chứa keys của mảng
```javascript
const fruits = ['apple', 'banana', 'orange'];
const keys = fruits.keys();
for (const key of keys) {
  console.log(key); // 0, 1, 2
}
```

### 30. `values()` - Trả về iterator chứa values của mảng
```javascript
const fruits = ['apple', 'banana', 'orange'];
const values = fruits.values();
for (const value of values) {
  console.log(value); // 'apple', 'banana', 'orange'
}
```

### 31. `entries()` - Trả về iterator chứa cặp [key, value]
```javascript
const fruits = ['apple', 'banana', 'orange'];
const entries = fruits.entries();
for (const [index, fruit] of entries) {
  console.log(index, fruit); // 0 'apple', 1 'banana', 2 'orange'
}
```

### 32. `flat()` - Làm phẳng mảng đa chiều
```javascript
const arr = [1, [2, 3], [4, [5, 6]]];
const flat1 = arr.flat(); // [1, 2, 3, 4, [5, 6]]
const flat2 = arr.flat(2); // [1, 2, 3, 4, 5, 6]
```

### 33. `flatMap()` - Kết hợp map() và flat()
```javascript
const numbers = [1, 2, 3];
const result = numbers.flatMap(num => [num, num * 2]); // [1, 2, 2, 4, 3, 6]
```

### 34. `copyWithin()` - Sao chép phần tử trong mảng
```javascript
const numbers = [1, 2, 3, 4, 5];
numbers.copyWithin(0, 3); // [4, 5, 3, 4, 5]
```

### 35. `toReversed()` - Tạo mảng mới đảo ngược (ES2023)
```javascript
const numbers = [1, 2, 3];
const reversed = numbers.toReversed(); // [3, 2, 1], numbers vẫn là [1, 2, 3]
```

### 36. `toSorted()` - Tạo mảng mới đã sắp xếp (ES2023)
```javascript
const numbers = [3, 1, 2];
const sorted = numbers.toSorted(); // [1, 2, 3], numbers vẫn là [3, 1, 2]
```

### 37. `toSpliced()` - Tạo mảng mới đã splice (ES2023)
```javascript
const numbers = [1, 2, 3, 4];
const spliced = numbers.toSpliced(1, 2, 5, 6); // [1, 5, 6, 4], numbers không đổi
```

### 38. `with()` - Tạo mảng mới với phần tử thay thế (ES2023)
```javascript
const numbers = [1, 2, 3];
const newArray = numbers.with(1, 99); // [1, 99, 3], numbers không đổi
```

## Các phương thức tĩnh của Array

### 39. `Array.isArray()` - Kiểm tra có phải là mảng không
```javascript
Array.isArray([1, 2, 3]); // true
Array.isArray('hello'); // false
```

Các phương thức mảng JavaScript được chia thành:
1. **Mutating Methods**: Thay đổi mảng gốc (push, pop, splice, sort, reverse, etc.)
2. **Accessor Methods**: Không thay đổi mảng gốc (concat, slice, join, etc.)
3. **Iteration Methods**: Duyệt qua các phần tử (forEach, map, filter, reduce, etc.)
4. **ES6+ Methods**: Các phương thức mới (flat, flatMap, from, of, etc.)
5. **ES2023 Methods**: Các phương thức không đột biến mới (toReversed, toSorted, with, etc.)
