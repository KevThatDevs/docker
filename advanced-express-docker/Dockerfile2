# Build time
FROM node:16
WORKDIR /app

# Grab the package.json and npm install
COPY package.json .
RUN npm install

# Optimization to not re-run npm install if no new npm packages installed
# This double re-adding COPY package.json as it doesn't change often
COPY . ./
EXPOSE 3000

# Runtime
CMD ["node", "index.js"]