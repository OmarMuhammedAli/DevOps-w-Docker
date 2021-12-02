# Start from the alpine image that is smaller but no fancy features.
FROM alpine:3.13

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

# Copy the application source code from the current directory into the workdir creating a usr/src/app/hello.sh
COPY hello.sh .

#Alternatively, if we skipped chmod earlier, we can add execution permission during the build.
RUN chmod +x hello.sh

# When running docker run, the command will be ./hello.sh
CMD ./hello.sh