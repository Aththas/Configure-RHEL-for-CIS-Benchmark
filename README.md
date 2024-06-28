# Configure-RHEL-for-CIS-Benchmark

## Install OpenScap Scanner and SCAP Security Guide into the server
	$  sudo yum install openscap-scanner scap-security-guide

## Set the profile as CIS and Run the the evaluation to Generate the report as html
	$  sudo oscap xccdf eval --profile xccdf_org.ssgproject.content_profile_cis --report /tmp/report.html /usr/share/xml/scap/ssg/content/ssg-rhel8-ds.xml

## The initial report will be like this following picture,
![image](https://github.com/Aththas/Configure-RHEL-for-CIS-Benchmark/assets/121440481/474247d5-007f-451a-9a6f-bbbac6be8aad)


## Now let's configure our RHEL server according to CIS Benchmark

### 1. Verify Integrity with AIDE

#### 1.1 Install AIDE
	$  sudo yum install aide

#### 1.2 Build and Test AIDE Database
	To generate a new database (By default, the database will be written to the file /var/lib/aide/aide.db.new.gz.)
	$  sudo /usr/sbin/aide --init

	To install the generated Database to the file /var/lib/aide/aide.db.gz
	$  sudo cp /var/lib/aide/aide.db.new.gz /var/lib/aide/aide.db.gz

	Initiate a manual check (If this check produces any unexpected output, investigate)
	$  sudo /usr/sbin/aide --check

#### 1.3 Configure AIDE to Verify the Audit Tools
##### 1.3.1 auditctl is checked in /etc/aide.conf
  	To check (Searches for the line containing '/usr/sbin/auditctl' in /etc/aide.conf, used -i to ignore case)
   	$  grep -i '^.*/usr/sbin/auditctl.*$' /etc/aide.conf

  	If Found,(Replaces the existing '/usr/sbin/auditctl' line with a new one containing specific attributes)
   	$  sed -i "s#.*/usr/sbin/auditctl.*#/usr/sbin/auditctl p+i+n+u+g+s+b+acl+xattrs+sha512#" /etc/aide.conf

  	If Not Found,(Appends the new '/usr/sbin/auditctl' line with specific attributes to the end of /etc/aide.conf)
   	$  echo "/usr/sbin/auditctl p+i+n+u+g+s+b+acl+xattrs+sha512" >> /etc/aide.conf


	

##### 3. auditd is checked in /etc/aide.conf
##### 4. ausearch is checked in /etc/aide.conf
##### 5. aureport is checked in /etc/aide.conf
##### 6. autrace is checked in /etc/aide.conf
##### 7. rsyslogd is checked in /etc/aide.conf
##### 8. augenrules is checked in /etc/aide.conf

#### 1.4 Configure Periodic Execution of AIDE
$

