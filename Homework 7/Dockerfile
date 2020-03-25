FROM python:alpine

COPY . /app/django-app
WORKDIR /app/django-app
RUN pip install -r /app/django-app/requirements.txt
RUN chmod +x /app/django-app/manage.py
RUN rm -rf /app/django-app/requirements.txt
RUN ["python", "manage.py", "migrate"]

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
