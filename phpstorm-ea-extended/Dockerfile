FROM openjdk:11.0.12-jdk

RUN apt-get update && apt-get install -y \
    curl \
    zip

RUN curl -Ls https://download.jetbrains.com/webide/PhpStorm-2021.1.3.tar.gz | tar -xvz

# The directory name is unpredictable, containing the phpstorm version number e.g. PhpStorm-211.7142.44
# Here we symlink the script to a predictable location for use by the app
RUN ln -s $(find . -type d -name "PhpStorm-*")/bin/phpstorm.sh phpstorm.sh

RUN cd $(find . -type d -name "PhpStorm-*")/plugins && curl -Lo ea_extended.jar https://plugins.jetbrains.com/files/7622/150115/PhpInspectionsEA.jar?pluginId=7622
