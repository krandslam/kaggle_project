workclass 컬럼 개수 줄이기<br>

원본 \: workclass<br>
방법1. &nbsp;\('Without-pay', 'Never-worked') &nbsp; \-> &nbsp; 'No-pay'<br>
방법2. &nbsp;\(' Local-gov', ' State-gov',  ' Federal-gov') &nbsp; \->  &nbsp;'Gov'<br>


결론<br>
lgb 정확도 비교 결과  &nbsp;\: &nbsp;방법2 &nbsp;< &nbsp; 원본 &nbsp;== &nbsp;방법1
