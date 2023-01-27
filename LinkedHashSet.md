### LinkedHashSet
📌 프로그래머스 Day13 '중복된 문자 제거' 문제 다른 사람 풀이 중 발견 <br>
<br>
- Set에는 HashSet과 TreeSet만 있는 줄 알았는데 아니었다.
- HashSet은 Set의 특성 상 중복이 안되고 순서가 없음. 따라서 값을 출력할 때마다 순서가 바뀐다.(속도가 가장 빠르다. O(1))<br>
- 하지만 LinkedHashSet은 중복이 안되는 특성은 그대로지만, 넣은 순서대로 출력이 된다.👻(wow)<br>
- Linked 특성 상 논리적 순서를 갖기 때문인 것 같다.<br>
- 참고로 TreeSet은 오름차순으로 자동 정렬해준다.<br>
- Set의 하위 클래스이기 때문에 Set<> set = new LinkedHashSet<>(); 으로 객체 생성 후 사용
- 추가 : add(Object)<br>
- 특정 단어 삭제 : remove(Object) / 전체 삭제 : clear();
