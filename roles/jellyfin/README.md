# ansible-jellyfin
# Moddified Version of: sleepy-nols/ansible-jellyfin
Ansible role to install and configure [Jellyfin](https://jellyfin.org/) on Debian-like systems.

<a href="https://github.com/sleepy-nols/ansible-jellyfin/actions/workflows/ansible-lint.yml">
<img alt="ansible-lint" src="https://github.com/sleepy-nols/ansible-jellyfin/actions/workflows/ansible-lint.yml/badge.svg"/>
</a>

<a href="https://github.com/sleepy-nols/ansible-jellyfin/actions/workflows/ansible-galaxy-push-role.yml">
<img alt="push-galaxy" src="https://github.com/sleepy-nols/ansible-jellyfin/actions/workflows/ansible-galaxy-push-role.yml/badge.svg"/>
</a>

<a href="https://galaxy.ansible.com/ui/standalone/roles/sleepy-nols/jellyfin">
<img alt="Ansible Galaxy" src="https://img.shields.io/badge/Ansible_Galaxy-sleepy--nols.jellyfin-blue"/>
</a>
<br><br>

The default deployment without any variables changed is not a vanilla deployment as several quality of life improvements are made.

**Features:**
- fully configurable config files (ansible management of settings normally tweaked in webUI)
---
## Role Variables and Defaults

```yml
jellyfin_user: "jellyfin"
```
User that Jellyfin runs as.

```yml
jellyfin_group: "jellyfin"
```
Group that Jellyfin runs as.


---
### Jellyfin

```yml
jellyfin_cache_dir: "/var/cache/jellyfin"
jellyfin_log_dir: "/var/log/jellyfin"
jellyfin_config_dir: "/etc/jellyfin"
jellyfin_data_dir: "/var/lib/jellyfin"
```
Jellyfin directories.

```yml
jellyfin_ffmpeg_bin: "/usr/lib/jellyfin-ffmpeg/ffmpeg"
jellyfin_web_bin: "/usr/share/jellyfin/web"
```

```
---
## Example Playbook

```yml
- hosts: jellyfin-hosts
  roles:
    - sleepy-nols.jellyfin
```

---
## Contributing

Contributions on are welcome. :)

---
## License
GPLv3
