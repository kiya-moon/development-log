### Arrays.copyOf
- 배열 복사 시 사용 <br>
- 예시
``` Java
int[] sample = Arrays.copyOf(복사할 배열, 복사할 배열 크기);
```
<br><br>

### Arrays.copyOfRange
- 배열의 범위를 지정하여 복사 시 사용<br>
- 예시
``` Java
int[] sample = Arrays.copyOfRange(복사할 배열, 복사 시작 인덱스, 복사 끝 인덱스(-1));
// 예를 들어 복사 시작 인덱스를 1, 복사 끝 인덱스를 3으로 지정하면,
// 복사 대상 배열의 1번 인덱스부터 2번 인덱스까지를 복사할 수 있다.
```
