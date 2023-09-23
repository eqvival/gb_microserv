FROM python:3.11.5

#RUN set -eux; \
#	apt-get update; \
#	apt-get install -y \
#		libbluetooth-dev \
#		pip3-install\
#		curl\
#		flask\
#	; \
#	rm -rf /var/lib/apt/lists/*

RUN apt update -y && apt upgrade -y
#RUN apt install pip3-install
RUN apt install curl
#RUN apt install flask
COPY requirements.txt .  
RUN pip install --upgrade pip && pip install -r requirements.txt
COPY app.py . 
RUN set -eux;\
        chmod ugo+x app.py
#RUN python app.py
CMD ["python", "app.py", "&"]
