# File Permission Correction
After conducting a security audit within the `Stratos DC`, the Nautilus security team discovered misconfigured permissions on critical files. To address this, corrective actions are being taken by the production support team. Specifically, the file named `/etc/hostname` on `Nautilus App 3` server requires adjustments to its Access Control Lists (ACLs) as follows:

1. The file's user owner and group owner should be set to `root`.

2. `Others` should possess `read only` permissions on the file.

3. User `mariyam` must not have any permissions on the file.

4. User `rod` should be granted `rod` permission on the file.

## 1. Set owner and group owner to root
`sudo chown root:root /etc/hostname`

## 2. Set `Others` `read only` permissions
`sudo chmod 644 /etc/hostname`

## 3. Revoke all perm from `mariyam`
`setfacl u:mariyam:--- /etc/hostname`

## 4. Set `read only` to `rod`
`setfacl -m u:rod:r-- /etc/hostname`

`ls -l /etc/hostname`

`getfacl /etc/hostname`