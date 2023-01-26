23.01.07 프로그래머스 코딩테스트 입문 Day6 문제 풀이 중 StringBuilder 사용
<br><br>
- 자바에서 String은 변경불가능한 객체이다.
- String을 합치는 과정(String 객체끼리 더하는 과정)에서는 새로운 String 객체가 생성되는 과정이 반복되므로, 메모리의 할당과 해제가 반복된다.
- 즉, 비효율적이다.<br><br>
- StringBuilder는 변경 가능한 문자열을 만들어준다.
- StringBuilder 객체를 생성한 후, append() 메소드로 연결하고자 하는 문자열을 넣어준다.
- 출력 시에는 toStirng()을 붙여야 하고, String 변수에 넣을 때도 마찬가지다.

<br><br><br>

23.01.08 프로그래머스 코딩테스트 입문 Day6 문제 풀이 중 repeat() 사용
<br><br>
- repeat()은 자바11부터 추가된 String 메서드
- 주어진 파라미터 횟수만큼 문자열을 반복한다.
- 파라미터를 0으로 지정하면 빈 문자열, 음수로 지정하면 IllegalArgumentExceptionthrow 에러를 반환한다.
- repeat() 메서드를 사용하면 내부적으로 Arrays.fill() 및 System.arraycopy() 메서드를 호출하여 새 문자열을 만든다.

<br><br><br>

23.01.27 프로그래머스 코딩테스트 입문 Day13 문제 풀이 중 join() 사용
<br><br>
- 자바8부터 StringJoiner.class와 String.Join() API를 이용해서 문자열 연결이 가능해짐
- 참고 : https://parkhyeokjin.github.io/java/2019/07/18/StringJoining.html
- StringJoiner.class 활용 소스
```java
public class Joning{
    String[] str = {"hello", "java", "World"};
    @Test
    public void java8Joiner() {
        StringJoiner joiner = new StringJoiner(" ");
        for(int i = 0; i < str.length; i++) {
            joiner.add(str[i]);
        }
        assertEquals("hello java World", joiner.toString());
    }
}
```
- String.join() 활용 소스
```java
public class Joning{
    String[] str = {"hello", "java", "World"};
    @Test
    public void java8StringJoin() {
                 assertEquals("hello java World", String.join(" ", str));
    }
}
```
- 만약 Stream의 collect() 안에서 사용하고 싶으면, Collectors.joining()을 사용하면 됨
