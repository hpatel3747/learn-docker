#base image that build extends
#FROM    python:3.12
#WORKDIR /usr/local/app
FROM node:20-alpine
WORKDIR /app


# install dependencies
#COPY    requirements.txt ./
#RUN     pip install --no-cache-dir -r requirements.txt
COPY . .


#copy  in the source code
#COPY    srv ./src
#EXPOSE  5000

#setup an app user so the container doesnt run as the root user
#RUN useradd app
#USER app
RUN yarn install -production
#CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
CMD ["node", "./src/index.js"]
#