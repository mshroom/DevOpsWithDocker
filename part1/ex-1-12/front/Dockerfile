FROM node:latest
WORKDIR /mydir
COPY ./frontend-example-docker /mydir
RUN npm install
EXPOSE 5000
ENV API_URL=http://localhost:8000
CMD npm start
