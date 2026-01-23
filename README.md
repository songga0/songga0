# GA YOUNG🦋

[![Solved.ac
프로필](http://mazassumnida.wtf/api/v2/generate_badge?boj=thdrkdud0307)](https://solved.ac/thdrkdud0307)
![songga0's GitHub stats](https://github-readme-stats.vercel.app/api?username=songga0&show_icons=true&theme=omni)


## Language
![C](https://img.shields.io/badge/C-A8B9CC.svg?&style=for-the-badge&logo=C&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C.svg?&style=for-the-badge&logo=Cplusplus&logoColor=white)
![python](https://img.shields.io/badge/python-3776AB.svg?&style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)

## DB
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white)

## Framework
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)

## Data Analysis & Visualization
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3776AB?style=for-the-badge&logo=matplotlib&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)

## Development Tools / Environment
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
django.db.utils.OperationalError: no such table: foal_prize_prediction_model
python manage.py shell << 'EOF'
from django.db import connection
from django.core.management.color import no_style
from django.db import models

# 데이터베이스에 존재하는 테이블 목록 가져오기
cursor = connection.cursor()
cursor.execute("SELECT name FROM sqlite_master WHERE type='table' AND name NOT LIKE 'sqlite_%' AND name NOT LIKE 'django_%';")
existing_tables = [row[0] for row in cursor.fetchall()]

print(f"존재하는 테이블: {existing_tables}")

# prediction 앱 테이블들
prediction_tables = [
    'foal_prize_prediction_model',
    'foal_recommend_prediction_model',
    'foal_prediction',
    'horse_entry_performance',
    'entry_performance_data',
    'racehorse',
    'knicks_feature_values',
    'preference_recommendation_stallion'
]

# core 앱 테이블들
core_tables = [
    'owner',
    'owner_mapping',
    'horse',
    'owner_horse_map',
    'relation_snapshot',
    'search_season',
    'season_relation_map',
    'knicks',
    'knicks_raw',
    'breeding_value',
    'report',
    'file_upload',
    'email_send',
    'report_generation'
]

# 존재하는 테이블만 삭제
all_tables = prediction_tables + core_tables
tables_to_delete = [t for t in all_tables if t in existing_tables]

if tables_to_delete:
    print(f"\n삭제할 테이블: {tables_to_delete}")
    for table in tables_to_delete:
        try:
            cursor.execute(f"DELETE FROM {table};")
            count = cursor.rowcount
            print(f"  {table}: {count}개 행 삭제")
        except Exception as e:
            print(f"  {table}: 삭제 실패 - {e}")
    connection.commit()
    print("\n데이터 삭제 완료")
else:
    print("\n삭제할 테이블이 없습니다.")
EOF


![Google Colab](https://img.shields.io/badge/Google%20Colab-%23F9A825.svg?style=for-the-badge&logo=googlecolab&logoColor=white)

## Collaboration & Version Control Tools
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white)

## API Development
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
