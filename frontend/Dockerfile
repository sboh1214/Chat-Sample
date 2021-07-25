FROM nginx:1.21

WORKDIR /usr/src

RUN apt-get update

RUN apt-get install -y git
RUN git clone https://gitlab.com/triangleyj/2021-summer-wheel-assignment.git

RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
RUN apt-get install -y nodejs

WORKDIR /usr/src/2021-summer-wheel-assignment

ENV VUE_APP_BACK_HOST_PORT=chat.sboh.dev

RUN npm install
RUN npm run build

RUN cp -frp ./dist/ /usr/share/nginx/html/
