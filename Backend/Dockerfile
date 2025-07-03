# ---------- build image ----------
FROM node:20-alpine

WORKDIR /app

# Install only prod deps for lean image
COPY package*.json ./
RUN npm ci --only=production

# Copy source and expose API port
COPY . .
EXPOSE 3105

CMD ["node", "server.js"]

