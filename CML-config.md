# Cisco Modeling Labs Virtualization Requirements

Cisco Modeling Labs requires hardware virtualization support. Before running CML in VMware, verify BIOS settings and disable Windows hypervisor features that may conflict with VMware nested virtualization.

---

# 1. Enable Virtualization in BIOS/UEFI

Restart the computer and enter BIOS/UEFI.

Common key:

```
F2
```

Enable:

```
Intel VT-x / Intel Virtualization Technology
```

or:

```
AMD-V / SVM Mode
```

Recommended:

```
Intel VT-d
```

(if available)

Save changes and reboot.

---

# 2. Verify Virtualization in Windows

Open Command Prompt as Administrator:

```
systeminfo
```

Check:

```
Virtualization-based security: Status: Not enabled
```

Check Hyper-V Requirements:

```
Hyper-V Requirements:
    VM Monitor Mode Extensions: Yes
    Virtualization Enabled In Firmware: Yes
    Second Level Address Translation: Yes
    Data Execution Prevention Available: Yes
```

---

# 3. Disable Windows Virtualization Features

Open:

```
optionalfeatures.exe
```

Disable:

```
Hyper-V
Virtual Machine Platform
Windows Hypervisor Platform
Windows Sandbox
```

Restart Windows after changing features.

---

# 4. Disable Core Isolation Memory Integrity

Open:

```
Windows Security
> Device Security
> Core Isolation
```

Disable:

```
Memory Integrity
```

Restart Windows.

---

# 5. Configure VMware Nested Virtualization

Open:

```
VMware
> Virtual Machine Settings
> Processors
```

Enable:

```
Virtualize Intel VT-x/EPT
```

or:

```
Virtualize AMD-V/RVI
```


