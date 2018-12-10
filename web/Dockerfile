FROM python:3.6
ENV PYTHONUNBUFFERED 1
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
ADD requirements.txt /usr/src/app/
RUN pip install -r requirements.txt
ADD . /usr/src/app/
# sampleファイルをadd
ADD flask_sample.py ./usr/src/app/
# 実行
CMD ["gunicorn", "flask_sample:app", "-b", "0.0.0.0:5000"]
