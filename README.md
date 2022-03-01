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


# How to compare before and after agent installation

### 1. Before installing the agent, capture the entire file list

    /find / -ls > 2022-02-21-0-all.txt
    find / -ls 2 > /dev/null|grep -v "/proc/"|grep -v "/sys/" > 2022-02-21-1-all.txt
    * /proc/*, /sys/* Real-time system information provided by the Linux kernel. Exclude from checklist


### 2. List of files 10 minutes before installation

    find / -cmin -10 -ls 2>/dev/null|grep -v "/proc/"|grep -v "/sys/" > before-date-10.txt

### 3. List of files 1 minutes before installation

    find / -cmin -1 -ls 2>/dev/null|grep -v "/proc/"|grep -v "/sys/" > before-date-1.txt

### 4. List of files 1 minutes after installation

    find / -cmin -1 -ls 2>/dev/null|grep -v "/proc/"|grep -v "/sys/" > after-date-1.txt





