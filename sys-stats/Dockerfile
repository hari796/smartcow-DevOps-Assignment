# Pull latest official node image
FROM centos:centos7

# Expose ports
EXPOSE 3000
EXPOSE 35729

# Set working directory
WORKDIR /app

# Add /app/node_modules/.bin to environment variables
ENV PATH /root/DevOps-Assignment/sys-stats/node_modules/.bin:$PATH

# Copy package files and install app dependencies
#COPY /root/DevOps-Assignment/sys-stats/package.json  /app/package.json
#COPY /root/DevOps-Assignment/sys-stats/yarn.lock /app/package-lock.json
RUN cd ~
RUN curl -sL https://rpm.nodesource.com/setup_14.x | bash -
RUN yum -y install nodejs
RUN yum -y install gcc-c++ make
#RUN npm install -g npm@7.6.3
#RUN npx create-react-app my-app
RUN npm install react-scripts -g

# Add React app to working dire
ADD . /app

# Start the React app
CMD ["npm", "start"]

