




# Welcome_Page
CICD Setup for Node.js


##I create The Docker file here is the description for it: ##

# Step 1: Use the official Node.js image as the base image
FROM node:16

# Step 2: Set the working directory inside the container
WORKDIR /usr/src/app

# Step 3: Copy the package.json and package-lock.json (if exists) to the container
COPY package*.json ./

# Step 4: Install the dependencies
RUN npm install

# Step 5: Copy the rest of your application code to the container
COPY . .

# Step 6: Expose the port your application will run on
EXPOSE 3000

# Step 7: Command to start your Node.js application
CMD ["node", "app.js"]
