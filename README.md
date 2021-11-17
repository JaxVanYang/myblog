# Just Call Me Jax

This is the repository for my [blog](https://jaxvanyang.github.io).

## Configure Dev Environment

1. Install Ruby and other prerequisites:

    ```shell
    sudo apt install ruby-full build-essential zlib1g-dev
    ```

2. Configure RubyGems packages(called gems) to be installed in a folder under your home directory:

    ```shell
    echo '# Install Ruby Gems to ~/.gems' >> ~/.bashrc
    echo 'export GEM_HOME="$HOME/.gems"' >> ~/.bashrc
    echo 'export PATH="$HOME/.gems/bin:$PATH"' >> ~/.bashrc
    source ~/.bashrc
    ```

    or manually write the following lines in your .bashrc(or .zshrc, etc) file and execute `source ~/.bashrc`:

    ```shell
    # Install Ruby Gems to ~/.gems
    export GEM_HOME="$HOME/.gems"
    export PATH="$HOME/.gems/bin:$PATH"
    ```

3. 更改 RubyGems 为国内镜像源：

    ```shell
    gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
    ```

    确保只有 gems.ruby-china.com

    ```console
    $ gem sources -l
    https://gems.ruby-china.com
    ```

4. Install Jekyll and Bundler(they are gems):

    ```shell
    gem install jekyll bundler
    ```

## Quick Setup

1. Create an empty directory or use an existing one:

    ```shell
    mkdir -p ~/blog
    cd ~/blog
    ```

2. Initialize a new Jekyll site in an empty directory:

    ```shell
    jekyll new .
    ```

    or use an existing directory:

    ```shell
    jekyll new . --force
    ```

3. Test your site:

    ```shell
    bundle exec jekyll serve
    ```

4. Look aroud your site directory:

    ```console
    $ ls -l
    404.html  Gemfile  Gemfile.lock  README.md  _config.yml  _posts  _site  about.markdown  index.markdown
    ```

## Blogging

1. Check out this first: https://jekyllrb.com/docs/step-by-step/08-blogging/

2. Create new posts in [_posts](_posts) under your site directory.

## Deploy on GitHub Pages

1. Create a new empty repository on GitHub:

    ![create a new empty repository](assets/images/create-a-new-empty-repo.png)

2. Initialize the local repository and push it to Github:

    ```shell
    git init
    git add .
    git commit -m "first commit"
    git branch -M main
    git remote add origin <your_repo_url>
    git push -u origin main
    ```

3. Activate Github Pages
    
## Reference

- [Jekyll on Ubuntu](https://jekyllrb.com/docs/installation/ubuntu/)

- https://gems.ruby-china.com/

- https://jekyllrb.com/docs/