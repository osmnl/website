FROM mcr.microsoft.com/vscode/devcontainers/ruby:2

# ENV Variables required by Jekyll
ENV LANG=en_US.UTF-8 \
    LANGUAGE=en_US:en \
    TZ=America/Chicago \
    LC_ALL=en_US.UTF-8 \
    LANG=en_US.UTF-8 \
    LANGUAGE=en_US

# Install jekyll
RUN gem install bundler jekyll

# Install a version of Node.js using nvm for dynamic front end content
ARG NODE_VERSION="lts/*"
RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && nvm install ${NODE_VERSION} 2>&1"

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment this line to install additional gems.
# RUN gem install <your-gem-names-here>
# RUN bundle install

# [Optional] Uncomment this line to install global node packages.
# RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && npm install -g <your-package-here>" 2>&1
