## Decrease and conquer
insert sort
## Transform and conquer
정렬 후 계산

### Insert Sort
```javascript
let i, j, k;
let list = [4,12,3,4,1];

for(i=1; i<list.length; i++){
  k = list[i];
  j = i-1;
  
  while( j>=0 && list[j] > k ) {
    list[j] = k;
    j--;
  }
  list[j+1] = k
}
```
