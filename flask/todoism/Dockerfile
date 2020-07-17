FROM python:3.7-alpine
COPY . /app
WORKDIR /app
RUN pip install --upgrade pip
RUN pip install -r requirements.txt
CMD ["set FLASK_APP=todoism"] && CMD["set FLASK_ENV=development"]
CMD ["flask", "initdb"] && CMD ["flask", "translate", "compile"]
CMD ["flask", "run", "--host=0.0.0.0"]
