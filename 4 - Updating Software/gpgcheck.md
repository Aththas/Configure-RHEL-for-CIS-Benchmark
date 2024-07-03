# What is gpgcheck?
gpgcheck is a configuration setting used in package management systems, such as **yum** and **dnf** on RPM-based Linux distributions (e.g., CentOS, Red Hat, Fedora). It determines whether the packages being installed or updated are verified using GPG (GNU Privacy Guard) signatures.

## Key Points about gpgcheck:
### 1. Purpose:

gpgcheck ensures that the packages being installed or updated come from a trusted source.

It verifies the authenticity and integrity of the packages using GPG signatures.

### 2. How It Works:

When gpgcheck is enabled, the package manager checks the GPG signature of each package against the GPG key imported into the system.

If the signature is valid and matches the trusted key, the package is considered safe to install.

If the signature verification fails, the package manager will not install or update the package and will raise an error.

### 3. Configuration:

The gpgcheck setting can be enabled or disabled in the repository configuration files (e.g., /etc/yum.conf, /etc/yum.repos.d/*.repo).

### 4. Values:

gpgcheck=1: Enables GPG signature verification.

gpgcheck=0: Disables GPG signature verification.
