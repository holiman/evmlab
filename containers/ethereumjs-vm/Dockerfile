from node:alpine

WORKDIR /ethereum

RUN apk update && apk upgrade && apk add --no-cache g++ python python-dev git make bash && git clone --branch state-test-from-source https://github.com/jwasinger/ethereumjs-vm && cd ethereumjs-vm  && npm install

ENTRYPOINT ["node", "/ethereum/ethereumjs-vm/tests/tester.js" ]
