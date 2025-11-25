##########################################################################
# Stage 1 - Builder
##########################################################################
FROM node:18-alpine AS builder

WORKDIR /app

# Copy package.json and install only prodcution package
COPY package*.json ./
RUN npm install --prodcution

#Copy all app source code
COPY . .

##########################################################################
# Stage 2 - Final Runtime image
##########################################################################
FROM node:18-alpine AS runtime

WORKDIR /app

#Copy only what we need from builder stage
COPY --from=builder /app /app

EXPOSE 3000
CMD ["npm", "start"]