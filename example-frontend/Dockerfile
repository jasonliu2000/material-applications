# adding comment for git track to file
FROM node:16

EXPOSE 4999

WORKDIR /usr/src/app

COPY . .

ENV REACT_APP_BACKEND_URL="http://localhost:8080"

# install deps from package.json
RUN npm install
# create build
RUN npm run build
# install package "serve" globally
RUN npm install -g serve

CMD ["serve", "-s", "-l", "4999","build"] 
