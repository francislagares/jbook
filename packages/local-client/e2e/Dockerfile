FROM cypress/base:10

WORKDIR /app

COPY package.json .

RUN yarn install

COPY . .

# verify that Cypress has been installed correctly.
# running this command separately from "cypress run" will also cache its result
# to avoid verifying again when running the tests
RUN npx cypress verify