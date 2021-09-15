# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.191.1/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version: bionic, focal
ARG VARIANT="focal"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive && apt-get -y install --no-install-recommends apache2 php libapache2-mod-php sqlite3 php-sqlite3 phpliteadmin
RUN rm /etc/apache2/sites-available/000-default.conf
RUN rm /etc/apache2/apache2.conf

ADD 000-default.conf /etc/apache2/sites-available
ADD apache2.conf /etc/apache2

#RUN chmod 777 /workspaces/ -R


#RUN cp /workspaces/lunch-app/000-default.conf /etc/apache2/sites-available
#RUN cp /workspaces/lunch-app/apache2.conf /etc/apache2
#RUN service apache2 start
