FROM node:18-alpine
WORKDIR /app
RUN echo 'const http = require("http"); http.createServer((req, res) => res.end("Backend API is running!")).listen(5000);' > server.js
EXPOSE 5000
CMD ["node", "server.js"]