
FROM gcr.io/google-appengine/nodejs
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install --production
COPY . .
EXPOSE 3001
CMD ["node", "src/index.js"]



#FROM python:3.8
#EXPOSE 8081
#WORKDIR /app2
#COPY . ./
#RUN pip install -r requirements.txt
#CMD ["python", "app.py"]