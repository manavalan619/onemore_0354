FROM node:14.11.0-alpine
COPY . /app
WORKDIR /app
RUN npm install
RUN npm install -g @angular/cli
RUN npm install -g serve
RUN npm install -g concurrently
RUN npm upgrade -g @angular/cli
CMD ng build  && concurrently "ng build --watch" "serve dist/onemore"
EXPOSE 5000
