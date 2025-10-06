# IAM-Portfolio
About my IAM journey
I want to specialize in IAM. 
27/9/25: I learnt how to create a branch and open and merge a pull request
04/10/25:  Ubuntu VM Setup & Troubleshooting
- Downloaded **Ubuntu 22.04 LTS (ISO)** and installed it on **VirtualBox**.
- Opened the Ubuntu desktop, launched the terminal, and practiced basic Linux commands: pwd,ls,cat,whoami,ls -a, ls -l.
  
Problems I Encountered and How I Solved Them
1. VMware and VirtualBox Conflict
Error: vmwgfx seems to be running on an unsupported hypervisor. This configuration is likely broken.
Cause: VMware was still installed on my system and conflicted with VirtualBox’s virtualization drivers.
Fix: I uninstalled VMware, restarted my PC, and then re-launched the VirtualBox installation. The error disappeared.

2. Ubuntu Desktop Flickering
Issue: The Ubuntu desktop kept flickering whenever I minimized the window.
Fix: In VirtualBox settings: Graphics Controller: VMSVGA (or VBoxSVGA if VMSVGA causes flicker)
Video Memory: 128 MB (max) , 3D Acceleration: Enabled
Alternatively, use:
Fullscreen Mode: Right Ctrl + F..... Scaled Mode: Right Ctrl + C
Installing Guest Additions also helps with smoother display.

3. Network Activation Failed
Error: Activation of network connection failed
Fix: VirtualBox → Settings → Network → Adapter 1 → Attached to: NAT
Restarted the VM and tested internet connectivity using:
ping -c 4 google.com
Received 100% success and no packet loss.

5. Unattended Installation Behavior
Issue: VirtualBox’s unattended installer completed automatically but tried to reinstall on reboot.
Fix: Removed the Ubuntu ISO from Storage → Controller: IDE so the VM boots directly from the virtual disk.

Notes for Others Facing Similar Issues
If you have both VMware and VirtualBox installed, they’ll conflict. Uninstall one, restart, then proceed.
For flickering or graphics lag, tweak Graphics Controller and 3D Acceleration options.
Use NAT for internet connectivity in your VM.
Guest Additions improves performance — install it once Ubuntu is fully set up.

<img width="960" height="505" alt="image" src="https://github.com/user-attachments/assets/b0b54472-0484-4232-b926-06a508fa16c5" />
