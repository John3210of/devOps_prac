FROM python:3.11.9

# 현재 작업 디렉터리를 컨테이너 내 /app에 복사
WORKDIR /app

# 필요한 패키지 설치
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# 현재 디렉터리의 모든 파일을 /app으로 복사
COPY . /app/

# 포트 8000번 개방
EXPOSE 8000

# Django 서버 실행 명령
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
