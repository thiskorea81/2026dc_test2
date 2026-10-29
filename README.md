# 군집 분석 실습 데이터

## 속성 설명

| 속성 | 설명 | 값 또는 단위 |
| --- | --- | --- |
| `record_id` | 각 기록을 구별하는 식별 번호 | 7자리 정수 |
| `Gender` | 성별 | Male=남성, Female=여성 |
| `Age` | 나이 | 세 |
| `Height` | 키 | m |
| `Weight` | 체중 | kg |
| `family_history_with_overweight` | 과체중 가족력 여부 | yes=있음, no=없음 |
| `FAVC` | 고열량 음식을 자주 먹는지 여부 | yes=그렇다, no=아니다 |
| `FCVC` | 채소 섭취 빈도 지표 | 1~3, 값이 클수록 자주 섭취 |
| `NCP` | 하루 주요 식사 횟수 지표 | 1~4 |
| `CAEC` | 식사 사이 음식 섭취 빈도 | no=없음, Sometimes=가끔, Frequently=자주, Always=항상 |
| `SMOKE` | 흡연 여부 | yes=흡연, no=비흡연 |
| `CH2O` | 하루 물 섭취량 지표 | 1~3, 값이 클수록 섭취량이 많음 |
| `SCC` | 섭취 열량을 확인·관리하는지 여부 | yes=그렇다, no=아니다 |
| `FAF` | 신체 활동 빈도 지표 | 0~3, 값이 클수록 자주 활동 |
| `TUE` | 기술 기기 사용 시간 지표 | 0~2, 값이 클수록 사용 시간이 김 |
| `CALC` | 음주 빈도 | no=없음, Sometimes=가끔, Frequently=자주, Always=항상 |
| `MTRANS` | 주로 이용하는 교통수단 | Automobile=자동차, Motorbike=오토바이, Bike=자전거, Public_Transportation=대중교통, Walking=도보 |

이 데이터에는 합성 자료가 포함되어 있어 나이와 응답 지표에 소수가 나타날 수 있습니다. 물 섭취량·활동 빈도·기기 사용 시간의 지표는 리터·횟수·시간 단위의 직접 측정값과 구별됩니다.

## GitHub에서 데이터 불러오기

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
