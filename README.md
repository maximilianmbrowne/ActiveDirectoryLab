
# Watch the video of me installing Active Directory HERE:

https://www.loom.com/share/9cf29b0aeb884cfd81a3195d343e0d05

# Installing Active Directory on a Windows Server Virtual Machine

This guide walks through installing **Active Directory Domain Services (AD DS)** on a Windows Server virtual machine and promoting the server to a Domain Controller.

## Prerequisites
- A Windows Server Virtual Machine (Windows Server 2016/2019/2022)
- Administrator privileges on the VM

---

## Steps

### 1. Open Server Manager
Upon logging into the Windows Server VM, **Server Manager** should open automatically.  
If not, launch it from the Start menu.

---

### 2. Add Roles and Features
1. In Server Manager, click **Manage** in the top-right corner.
2. Select **Add Roles and Features**.
3. In the wizard, choose:
   - **Role-based or feature-based installation**
   - Select the local server when prompted

---

### 3. Install Active Directory Domain Services (AD DS)
1. In the **Server Roles** list, check **Active Directory Domain Services**.
2. Add any required features when prompted.
3. Continue through the wizard and click **Install**.

---

### 4. Promote the Server to a Domain Controller
After installation, a notification flag will appear in Server Manager.

1. Click **Promote this server to a domain controller**.
2. Choose **Add a new forest**.
3. Enter the root domain name:  
   **`testing.local`**

---

### 5. Configure Domain Controller Options
1. Set the **Forest Functional Level** and **Domain Functional Level** as desired (defaults are fine).
2. Enable **DNS** (default).
3. Create a **Directory Services Restore Mode (DSRM)** password and store it safely.

---

### 6. Complete the Installation
1. Proceed through the remaining wizard steps.
2. Click **Install**.

The server will automatically **restart** after promotion.

---

### 7. Verify Active Directory Installation
After the reboot:

- Log back in.
- Open **Server Manager** → **Tools**.
- Confirm that **Active Directory Users and Computers**, **DNS**, and related tools are present.

This confirms that **Active Directory is successfully installed and configured**.

---

## Finished!
You now have a functional **Active Directory Domain Controller** running under the domain **testing.local**.

