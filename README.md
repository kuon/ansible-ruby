
# THIS REPOSITORY HAS MOVED

New URL: https://git.goyman.com/kuon/ansible-ruby

Why I moved everything out of GitHub:

https://github.com/kuon/WhyILeftGithub/blob/main/README.md

----

# Ruby

Compiles and install ruby using [ruby-build](https://github.com/rbenv/ruby-build)
on RHEL based OS'es.

## Security

### rbenv-build download location

Due some business requirements, some may be required to possess the installation
files for rbenv-build. For that reason, you have an option to upload the
`ruby-build` installation files yourself into your host and point it in your
`rbenv_targz_url` var.

### Compile and runs ruby as an unprivileged user

You may probably want to compile and run ruby as an unprivileged user, so the
config by default assumes that you have an `deploy` user. If you want to disable
it or change this user, just change the `use_unprivileged_user` and
`unprivileged_user_name` vars.

## Requirements

Tested with Ansible 1.9 and 2.0.

## Role Variables

- `ruby_install_path` - Path where ruby will be installed, default to `$HOME/.rubies/ruby-2.2.4`
- `ruby_version` - Full version of the ruby to install (MRI) default to `2.2.4`
- `rbenv_targz_url` - Set it to the downloaded tar.gz from
[ruby-build releases](https://github.com/rbenv/ruby-build/releases).
- `use_unprivileged_user` - Sets whether you are _sudoing_ to a different user.
- `unprivileged_user_name` - If the previous option is yes, then set this user here.

## Dependencies

none

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
     - { role: kuon.ruby, ruby_install_path: '/opt/ruby' }
```
## License

MIT.
