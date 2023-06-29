# datatables
데이터테이블스 
## 개요
Datatables 라이브러리의 사용 방법에 대해 설명한 문서입니다.
### 링크  
https://datatables.net/examples/index
## 사용법
### 기능 활성화/비활성화 
false or true
    $('#example').DataTable({
    paging: false,
    ordering: false,
    info: false,
    });
### 테마 변경 (css)
https://datatables.net/manual/styling/theme-creator

### 정렬 
&#91;&#91;컬럼 번호, 'desc or asc'&#93;&#93;
    $('#example').DataTable({
        order: &#91;&#91;3, 'desc'&#93;&#93;,
    });

### 컬럼 숨기기
* target : 컬럼 번호
* visible : false or true
* searchable: false or true
    $('#example').DataTable({
        columnDefs: [
{
target: 2,
visible: false,
searchable: false,
},
{
target: 3,
visible: false,
},
],
});

### colspan, rowspan 
* &lt;th colspan ="2"&gt;&lt;/th&gt;
* &lt;th rowspan="1"&gt;&lt;/th&gt;

### 옵션 위치 

### 페이징 모양
* numbers  : 페이지 번호만
* simple : 이전 및 다음 버튼만
* simple_numbers : 이전 및 다음 버튼과 페이지 번호
* full : 처음, 이전, 다음 및 마지막 버튼
* full_numbers : 처음, 이전, 다음 및 마지막 버튼과 페이지 번호
* first_last_numbers : 처음 및 마지막 버튼과 페이지 번호
    $('#example').DataTable({
        pagingType: 'full_numbers',
    });
### 쉼표, 소수점
    $('#example').DataTable({
        language: {
            decimal: ',',
            thousands: '.',
        },
    });

## 스타일
테이블 클래스 이름

* display : stripe, hover,row-border,order-column 모두 적용
* cell-border : 테두리가 있는 셀
* compact : 셀 패딩을 줄여 데이터 밀도를 높임
* hover : 마우스를 올리면 행 강조
* nowrap : 줄 바꿈 비활성화
* order-border : 정렬 누르면 열 강조
* row-border : 테두리가 있는 행
* stripe : 얼룩말 줄무늬 행

## 정렬 
* dt[-head|-body]-left : 왼쪽 정렬 텍스트
* dt[-head|-body]-center :가운데 정렬 텍스트
* dt[-head|-body]-right : 오른쪽 정렬 텍스트
* dt[-head|-body]-justify : 정렬된 텍스트 양쪽 맞춤
* dt[-head|-body]-nowrap : 줄바꿈 정렬 텍스트

## 참고자료

1 컬럼별 검색, 날짜 기간 검색, FOOTER와 SUMMARY
https://naloblog.tistory.com/374

2 옵션 항목 위치 변경하기
https://ponyozzang.tistory.com/504

3 금액 단위 표시 설정하기
https://ponyozzang.tistory.com/503
