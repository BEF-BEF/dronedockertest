FROM python:3.7.12

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN apt-get update && apt-get install -y python3-opencv
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

RUN chmod +x launch.sh
ENTRYPOINT [ "./launch.sh" ]