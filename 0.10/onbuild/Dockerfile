FROM ditointernet/kinesis-subscriber-node

ENV NODE_ENV=development

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY package.json /usr/src/app/
ONBUILD RUN npm install
ONBUILD COPY . /usr/src/app

CMD ./node_modules/aws-kcl/bin/kcl-bootstrap --java /usr/bin/java -e -p ./config/$NODE_ENV.properties
