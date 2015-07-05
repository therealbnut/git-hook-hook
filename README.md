## Git Hook Hooks

A template for version controlling [git hooks](http://git-scm.com/docs/githooks). This means that you can add hooks to enforce policies when making changes to a repository, or many other things.

Usually hooks are stored in `.git/hooks`, which is not under version control. Git Hook Hooks adds default hooks that point to `.githooks` instead, which ***is*** under version control.

### Warning
If other people have access to your repo they will be able to check in code that is run on your machine when you run git commands!

### Usage
Clone the `git-hook-hooks-template` directory somewhere on your hard drive, for example:

    git clone https://github.com/therealbnut/git-hook-hook.git ~/.ghh

Then change your `.gitconfig` to point the template directory:

    git config --global init.templatedir '~/.ghh/template'

Add any new scripts you want to run under the `.githooks/` directory.

Now every time you run `git init` it will update that repo with the new hooks! Note that there will also be a bunch of `.sample` scripts in `.git/hooks` that it is safe to remove.

### Configuration
If you want to be prompted to run the hook then add `GIT_HOOK_HOOK_PROMPT=YES` to your environment.
