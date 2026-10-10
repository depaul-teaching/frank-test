# The clean Dockerfile you produced in Week 2. Nothing to change here this
# week: Week 3 is about composing this service with a database.
FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

RUN useradd --create-home appuser
USER appuser

EXPOSE 8000

#ENTRYPOINT ["uvicorn", "main:app"] had to combine them becasue my main.py file is another dictory and its 
# making a copy   
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
