FROM openjdk:11.0.12-jdk

RUN apt-get update && apt-get install -y \
    curl \
    zip

RUN curl -Ls https://download.jetbrains.com/webide/PhpStorm-2021.1.2.tar.gz | tar -xvz

# The directory name is unpredictable, containing the phpstorm version number e.g. PhpStorm-211.7142.44
# Here we symlink the script to a predictable location for use by the app
RUN ln -s $(find . -type d -name "PhpStorm-*")/bin/phpstorm.sh phpstorm.sh
