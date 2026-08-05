# Stage 1: Build the React application
FROM node:18-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Serve compiled static files with Nginx
FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html
# Note: If your team uses Vite instead of Create React App, change /app/build to /app/dist
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]