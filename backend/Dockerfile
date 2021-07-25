FROM node:14

WORKDIR /usr/src

RUN apt-get update && apt-get install -y git
RUN git clone https://gitlab.com/triangleyj/2021-summer-wheel-assignment.git

WORKDIR /usr/src/2021-summer-wheel-assignment/backend
RUN npm install

EXPOSE 3008
ENTRYPOINT ["npm", "start"]
