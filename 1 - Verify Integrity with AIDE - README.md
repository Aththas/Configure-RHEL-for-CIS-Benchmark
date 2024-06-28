# 1. Verify Integrity with AIDE

## 1.1 Install AIDE
	$  sudo yum install aide

## 1.2 Build and Test AIDE Database
	To generate a new database (By default, the database will be written to the file /var/lib/aide/aide.db.new.gz.)
	$  sudo /usr/sbin/aide --init

	To install the generated Database to the file /var/lib/aide/aide.db.gz
	$  sudo cp /var/lib/aide/aide.db.new.gz /var/lib/aide/aide.db.gz

	Initiate a manual check (If this check produces any unexpected output, investigate)
	$  sudo /usr/sbin/aide --check

## 1.3 Configure AIDE to Verify the Audit Tools
#### 1.3.1 auditctl is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/auditctl' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/auditctl.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/auditctl' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/auditctl.*#/usr/sbin/auditctl p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/auditctl' line with specific attributes to the end of /etc/aide.conf)
   	$  echo "/usr/sbin/auditctl p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf

#### 1.3.2 auditd is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/auditd' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/auditd.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/auditd' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/auditd.*#/usr/sbin/auditd p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/auditd' line with specific attributes to the end of /etc/aide.conf)
   	$  echo "/usr/sbin/auditd p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf

#### 1.3.3 ausearch is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/ausearch' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/ausearch.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/ausearch' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/ausearch.*#/usr/sbin/ausearch p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/ausearch' line with specific attributes to the end of /etc/aide.conf)
   	$  echo "/usr/sbin/ausearch p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf

#### 1.3.4 aureport is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/aureport' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/aureport.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/aureport' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/aureport.*#/usr/sbin/aureport p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/aureport' line with specific attributes to the end of /etc/aide.conf)
   	$  echo "/usr/sbin/aureport p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf

#### 1.3.5 autrace is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/autrace' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/autrace.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/autrace' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/autrace.*#/usr/sbin/autrace p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/autrace' line with specific attributes to the end of /etc/aide.conf)
   	$  echo "/usr/sbin/autrace p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf

#### 1.3.6 rsyslogd is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/rsyslogd' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/rsyslogd.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/rsyslogd' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/rsyslogd.*#/usr/sbin/rsyslogd p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/rsyslogd' line with specific attributes to the end of /etc/aide.conf)
   	$  echo "/usr/sbin/rsyslogd p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf

#### 1.3.7 augenrules is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/augenrules' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/augenrules.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/augenrules' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/augenrules.*#/usr/sbin/augenrules p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/augenrules' line with specific attributes to the end of /etc/aide.conf)
   	$ echo "/usr/sbin/augenrules p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf

## 1.4 Configure Periodic Execution of AIDE
	To implement a daily execution of AIDE at 4:05am using cron
 	$ echo "05 4 * * * root /usr/sbin/aide --check" | sudo tee -a /etc/crontab

  	To implement a weekly execution of AIDE at 4:05am using cron
	$ echo "05 4 * * 0 root /usr/sbin/aide --check" | sudo tee -a /etc/crontab

 Explanation of the above daily, weekly execution of AIDE:

	1. Minute (05): This field specifies the minute of the hour when the command will run. In this case, it’s set to 5, meaning the command will run at 5 minutes past the hour.
	2. Hour (4): This field specifies the hour of the day (in 24-hour format) when the command will run. Here, it’s set to 4, meaning the command will run at 4 AM.
	3. Day of Month (*): This field specifies the day of the month when the command will run. The asterisk (*) means the command will run every day of the month.
	4. Month (*): This field specifies the month when the command will run. The asterisk (*) means the command will run every month.
	5. Day of Week (*): This field specifies the day of the week when the command will run. The asterisk (*) means the command will run every day of the week / Day of Week (0): Run on Sunday (0 or 7 represents Sunday).
	6. root: This field specifies the user under which the command should run. Here, root means the command will be executed with root privileges.
	7. '/usr/sbin/aide --check': This is the command to be executed. In this case, it runs AIDE (Advanced Intrusion Detection Environment) with the --check option, which checks the integrity of the system files against a previously generated database.

## Run the the evaluation again after the changes
	$  sudo oscap xccdf eval --profile xccdf_org.ssgproject.content_profile_cis --report /tmp/report.html /usr/share/xml/scap/ssg/content/ssg-rhel8-ds.xml

 ## Report
 ![image](https://github.com/Aththas/Configure-RHEL-for-CIS-Benchmark/assets/121440481/daa6558c-cbcd-4ac4-8133-7d31b2a7dd74)

