FROM python:2.7
ENV PYTHONUNBUFFERED 1
RUN mkdir /code
WORKDIR /code
ADD docker/requirements.txt /code/
RUN pip install -r requirements.txt
ADD https://raw.githubusercontent.com/vishnubob/wait-for-it/55c54a5abdfb32637b563b28cc088314b162195e/wait-for-it.sh /code/
RUN ["chmod", "+x", "/code/wait-for-it.sh"]
ADD src /code/