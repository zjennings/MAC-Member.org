FROM python:2.7
ENV PYTHONUNBUFFERED 1
RUN mkdir /service
WORKDIR /service
ADD docker/requirements.txt /service/
RUN pip install -r requirements.txt
ADD https://raw.githubusercontent.com/vishnubob/wait-for-it/55c54a5abdfb32637b563b28cc088314b162195e/wait-for-it.sh /service/
RUN ["chmod", "+x", "/service/wait-for-it.sh"]
ADD src /service/src/