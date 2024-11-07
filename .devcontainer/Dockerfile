# Use an official lightweight Node.js image
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:0-18

# Set the working directory inside the container
WORKDIR /workspace

# Install pnpm (if not already available in the base image)
RUN npm install -g pnpm

# Pre-cache pnpm dependencies (optional, to speed up installs)
RUN pnpm add -g pnpm

# Expose necessary ports (if you're running a local server)
EXPOSE 4321

# Install dependencies when the container starts (optional optimization)
CMD ["pnpm", "install", "--frozen-lockfile", "--no-prefer-frozen", "--prod"]
