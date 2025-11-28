# Ansible Rsyslog
[![CI](https://github.com/supertarto/ansible-role-rsyslog/actions/workflows/ci.yml/badge.svg)](https://github.com/supertarto/ansible-role-rsyslog/actions/workflows/ci.yml)

Role to install an configure Rsyslog with Ansible.

## Requirements
None

## Tested plateform
* Debian 12 (Bookworm)
* Debian 13 (Trixie)

## Role variables
Those variables are used to determine who is the owner of the files created by rsyslog, and to define the associated rights.

```yml
rsyslog_file_owner: root
rsyslog_file_group: adm
rsyslog_file_create_mode: "0640"
rsyslog_dir_create_mode: "0755"
rsyslog_umask: "0022"
```

Configuration path
```yml
rsyslog_work_directory: /var/spool/rsyslog
rsyslog_include_config: /etc/rsyslog.d/*.conf
```

Path to the logs files. Uncomment those you want to use or declare them in your inventory or playbook.
```yml
# rsyslog_auth_log: "/var/log/auth/auth.log"
# rsyslog_syslog_log: "/var/log/syslog-d/syslog.log"
# rsyslog_cron_log: "/var/log/cron/cron.log"
# rsyslog_daemon_log: "/var/log/daemon/daemon.log"
# rsyslog_kern_log: "/var/log/kern/kern.log"
# rsyslog_lpr_log: "/var/log/lpr/lpr.log"
# rsyslog_mail_log: "/var/log/mail/mail.log"
# rsyslog_user_log: "/var/log/user/user.log"
# rsyslog_mail_info_log: "/var/log/mail/mail.info"
# rsyslog_mail_warn_log: "/var/log/mail/mail.warn"
# rsyslog_mail_err_log: "/var/log/mail/mail.err"
# rsyslog_debug_log: "/var/log/debug-d/debug.log"
# rsyslog_messages_log: "/var/log/messages-d/messages.log"
```

## License
GPL V3.0
