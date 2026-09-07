# Use the official Apify Node.js base image
FROM apify/actor-node:20

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm --quiet set progress=false \
    && npm install --omit=dev --omit=optional \
    && echo "All NPM packages installed" \
    && rm -rf ~/.npm

# Copy source files
COPY . ./

# Run the actor
CMD npm start
