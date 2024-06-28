# Configure-RHEL-for-CIS-Benchmark

## Install OpenScap Scanner and SCAP Security Guide into the server
	$  sudo yum install openscap-scanner scap-security-guide

## Set the profile as CIS and Run the the evaluation to Generate the report as html
	$  sudo oscap xccdf eval --profile xccdf_org.ssgproject.content_profile_cis --report /tmp/report.html /usr/share/xml/scap/ssg/content/ssg-rhel8-ds.xml

## The initial report will be like this following picture,
![image](https://github.com/Aththas/Configure-RHEL-for-CIS-Benchmark/assets/121440481/474247d5-007f-451a-9a6f-bbbac6be8aad)


## Now let's configure our RHEL server according to CIS Benchmark

