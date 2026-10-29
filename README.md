# 군집 분석 실습 데이터 불러오기

아래 주소의 `사용자명`, `저장소명`, `브랜치명`을 실제 GitHub 정보로 바꾼 뒤 Google Colab 또는 Jupyter Notebook에서 실행합니다. CSV가 하위 폴더에 있다면 파일명 앞에 해당 폴더 경로를 추가합니다.

```python
import pandas as pd

url = 'https://raw.githubusercontent.com/사용자명/저장소명/브랜치명/obesity_clustering.csv'
df = pd.read_csv(url)
df.head()
```

공개 저장소의 Raw 주소를 사용합니다.

---

데이터 출처: [UCI Machine Learning Repository](https://doi.org/10.24432/C5H31Z), *Estimation of Obesity Levels Based On Eating Habits and Physical Condition* (2019). [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). 교육용으로 정답 열 제거, 행 순서 변경, 식별자 추가 및 일부 값의 공란 처리를 적용했습니다.
