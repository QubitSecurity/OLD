# PLURA

List of files to change when installing plura agent on the system.

### 1. PLURA Agent

    /etc/hosts
    /etc/yum.repos.d/plura.repo

### 2. Environment

    /etc/hosts
    /etc/yum.repos.d/plura.repo


### 3. Logging files

    /var/log/plura/*


### 4. Service registration

    /usr/lib/systemd/system/plura.service


### 5. rsyslog conf

    /etc/rsyslog.d/00-imfile.conf
    /etc/rsyslog.d/77-plura.conf
    /etc/rsyslog.d/99-plura.conf


### 6. auditd conf

    /etc/audisp/plugins.d/syslog.conf
    #active = no
    active = yes


### 7. libcurl package bug-fix

    /etc/profile.d/plura.sh


### 8. Log rotate

    /etc/logrotate.d/plura


### 9. Cron

    /etc/cron.d/plura
    /etc/cron.hourly/plogrotate


### 10. Certificate for SSL

    /etc/pki/*


### 11. Save package

    /var/lib/yum/*
    /var/lib/rpm/*


### 12. Temp files

    /var/log/*
    /var/cache/*

