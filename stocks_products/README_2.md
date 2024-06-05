Run the commands:

python manage.py makemigrations


docker build . -t hw:2.2
docker run -d -p 5000:8000 hw:2.2