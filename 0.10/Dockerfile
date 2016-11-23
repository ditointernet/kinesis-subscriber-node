FROM node:0.10.45

# Install Java
RUN apt-get update && apt-get install -y default-jre default-jdk

# Define the environment variable JAVA_HOME
RUN echo "export JAVA_HOME=\"$(update-alternatives --query java | grep 'Value: ' | grep -o '/.*/jre')\"" >> ~/.bashrc
