Run the commands:

python manage.py makemigrations
python manage.py migrate

docker build . -t hw:2.1
docker run -d -p 5000:8000 hw:2.1