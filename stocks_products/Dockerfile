FROM python:3.10

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

COPY requirements.txt .

RUN pip install --upgrade pip
RUN pip install gunicorn
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

#RUN python manage.py migrate

#CMD ["python", "manage.py", "runserver", "-b", "0.0.0.0:8000"]


CMD ["gunicorn", "stocks_products.wsgi", "-b", "0.0.0.0:8000"]