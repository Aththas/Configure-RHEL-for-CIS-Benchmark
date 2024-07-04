# sysctl Command
Purpose: The sysctl command is used to view and modify kernel parameters at runtime.

## Key Features:
**Kernel Parameters**: Manages kernel parameters, which control various aspects of the operating system's behavior.

**Runtime Configuration**: Changes made with sysctl are effective immediately but may not persist across reboots unless explicitly saved to a configuration file.

**Configuration Files**: Uses /etc/sysctl.conf and /etc/sysctl.d/*.conf files for persistent settings.

## Common Usage
1. View a Kernel Parameter
    
2. Set a Kernel Parameter Temporarily

3. Apply Changes from Configuration Files

4.  Make Changes Permanent (Edit /etc/sysctl.conf or create a file in /etc/sysctl.d/)

# systemctl Command
Purpose: The systemctl command is used to manage system services and the systemd system and service manager.

## Key Features:
**Service Management**: Start, stop, enable, disable, and check the status of services.

**System State**: Manage the state of the system, such as rebooting or shutting down.

**Unit Files**: Manages different types of units, including services, sockets, timers, and mount points.

## Common Usage
1. Start a service

2. Stop a servive

3. Enable a Service (start at boot)

4. Disable a Service (do not start at boot)

5. Check the Status of a Service

6. Reload All Unit Files

# Summary
![image](https://github.com/Aththas/Configure-RHEL-for-CIS-Benchmark/assets/121440481/ea29af5f-3045-4f4f-ba29-af1e9e3a144e)
