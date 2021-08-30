FROM php:7.3-cli

RUN apt-get update && apt-get install -y \
    curl \
    git \
    zip

RUN curl -Lo PhpStorm.tar.gz https://download.jetbrains.com/webide/PhpStorm-2021.1.2.tar.gz

RUN tar -xzf PhpStorm.tar.gz --one-top-level --strip-components 1

RUN curl -Lo java.tar.gz https://javadl.oracle.com/webapps/download/AutoDL?BundleId=244575_d7fc238d0cbf4b0dac67be84580cfb4b

RUN tar -xzf java.tar.gz --one-top-level --strip-components 1

RUN curl -Lo ea_inspections.jar https://plugins.jetbrains.com/files/7622/122694/PhpInspectionsEA.jar?updateId=122694&pluginId=7622&family=INTELLIJ

RUN mv ea_inspections.jar PhpStorm/plugins
