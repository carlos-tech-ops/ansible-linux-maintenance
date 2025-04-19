# ansible-linux-maintenance

Automated Linux maintenance with Ansible.  
Includes tasks for system updates, information gathering, and report logging.

---

## Phase 2: First Ansible Playbook Execution (Completed)

**Project:** `ansible-linux-maintenance`  
**Objective:** Automate Fedora system maintenance from macOS via Ansible.

### ✅ Tasks Achieved:
- Connected from macOS to Fedora using SSH key-based authentication.
- Created inventory, configuration, and playbook structure using GitHub web interface.
- Wrote and executed first Ansible playbook with `--ask-become-pass`:
  - Updated all Fedora packages.
  - Gathered system facts.
  - Logged system info to `/var/log/system_info.log`.

### ⚙️ Tools Used:
- macOS (Controller Node)
- Fedora 41 (Managed Node)
- Ansible 2.18.4
- GitHub

---

**Next Step:** Automate this playbook using Ansible Tower (AWX) or integrate with cron and Git workflows.
