FROM webdevops/php-dev:7.3
COPY php.ini /opt/docker/etc/php/
RUN apt-get update \
    && apt-get install -y zsh vim gnupg2 wget \
    && wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh || true \
    && git config --global user.email "${GIT_EMAIL}" \
    && git config --global user.name "${GIT_NAME}" \
    && git config --global core.fileMode false \
    && mkdir -p /root/.ssh \