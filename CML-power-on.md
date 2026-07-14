# Cisco Modeling Labs Initial Setup

This guide covers the initial configuration wizard after importing the Cisco Modeling Labs (CML) OVA and starting the appliance.

---

# First Boot

After importing the CML OVA into VMware, power on the virtual machine.

Wait for the CML appliance to complete the boot process.

The console will launch the initial setup wizard.

The wizard will guide you through:

1. Hostname configuration
2. System administrator account
3. Initial user credentials
4. Network configuration
5. Final setup

---

# 1. Hostname Configuration

Configure the appliance hostname.

Example:

```
Hostname:
CML01
```

---

# 2. System Administrator Account

Configure the system administrator account.

Example:

```
Username:
sysadmin
```

Create a secure password.

This account is used for:

- Appliance administration
- System management
- Console access

---

# 3. Initial User Credentials

Create the first CML user account.

This account is used to access the CML web interface.

Example:

```
Username:
admin
```

Set a password:

```
Password:
********
```

---

# 4. Network Configuration

Choose how the CML appliance receives an IP address.

Options:

```
DHCP
```

or:

```
Static IP
```

---

# DHCP Configuration

Select DHCP if your network provides automatic addressing.

The appliance will receive:

- IP address
- Subnet mask
- Default gateway
- DNS information

---

# Static IP Configuration

Recommended for lab environments.

Configure:

```
IP Address:
192.168.1.100

Subnet Mask:
255.255.255.0

Default Gateway:
192.168.1.1

DNS Server:
192.168.1.1
```

---

# Complete Setup

After entering all required information, CML will apply the configuration.

The console will display:

```
System ready
```

and show the assigned IP address.

Example:

```
CML IP Address:
192.168.1.100
```

