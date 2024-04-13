#🔎🩻 NessusVulnerablitityManagmentAnalysis-VMWare

## Objective and Description
In this project, we will be conducting multiple scans on a Windows 10 virtual machine with VirtualBox. The vulnerability scanning tool we will be using is Tenable Nessus to manage, analyze, and remediate vunlerabilities in our system. We seek to eliminate or reduce risk to an acceptable and benign level. We must evaluate the levels of risk to prioritize what is critical, high, medium, and low risk. We will be given different reports with descriptions and solutions in order to resolve the vulnerabilities. We will run a few different scans. A normal non-credentialed scan, a credentialed scan, a scan with an old depricated firefox browser installation, and a final scan with firefox removed and all possible system updates made to the host. We will compare each scan to see what has changed and what we can learn.
### Skills Learned
- Configure Windows 10 for vulnerability scanning
- Deploy VirtualBox with hosts
- Install, deploy, manage, and analyze Tenable Nessus for vulnerability and remediation
  

### Tools Used
- VirtualBox 
- Windows 10
- Tenable Nessus
- Windows Configuration

## Steps
- Step 1: We will start off by conducting our first basic network scan. We enter the IP address of our host that is being scanned and give it a name of Windows 10 Single Host. The results show mostly information about existing services on the host and 1 vulnerability at a medium risk level. It states that the SMB remote server doesn't have a signing requirement enabled. Meaning that an unauthenticated, remote attacker can exploit this to conduct man-in-the-middle attacks against the SMB server. This can be updated so that the SMB enforces digital signing on all communications. 
  
  <img src="https://i.imgur.com/8DJX4M7.png" height="20%" width="20%" alt="Vulnerability Management Project Steps"/> <img src="https://i.imgur.com/HZ4Swxr.png" height="20%" width="20%" alt="Vulnerability Management Steps"/> <img src="https://i.imgur.com/YKEyuGF.png" height="20%" width="20%" alt="Vulnerability Management Steps"/> <img src="https://i.imgur.com/nVT0Por.png" height="20%" width="20%" alt="Vulnerability Management Steps"/> 
- Step 2: Next, we will prep our host for a credentialed scan by by doing so me configurations on the host. First, we must go to our host and enable the remote registry service to allow our scanner to connect to and crawl through the the host's registry to look for unsecure configurations and other types of vulnerabilities that were missed by the basic scan. We must also  We also have to manualy add a key in the registry editor of our our host so that the scanner machine can easily connect to the host. We name the D.WORD "LocalAccountFilterPolicy" and set its value to 1. After that we go to user account controls and set to never notify when making changes to this computer to make the scan easier. Restart the host to implement changes.
  
  <img src="https://i.imgur.com/LIijsMY.png" height="30%" width="30%" alt="Vulnerability Management Project Steps"/> <img src="https://i.imgur.com/MkEOUNQ.png" height="30%" width="30%" alt="Vulnerability Management Project Steps"/> <img src="https://i.imgur.com/jAaVPg3.png" height="30%" width="30%" alt="Vulnerability Management Project Steps"/> 
- Step 3: In this step, we go ahead and run our credentialed scan. A credential scan does a more robust check on the ins and outs of the host for unsecure configurations and other vulnerabilities. It requires the host's username and password to fulfill this. It looks like not much has changed which tells us that this machine is updated and mostly patched.

  <img src="https://i.imgur.com/Mcurmg4.png" height="40%" width="40%" alt="Vulnerability Management Project Steps"/> <img src="https://i.imgur.com/gabnm7s.png" height="40%" width="40%" alt="Vulnerability Management Project Steps"/> 
- Step 4: For this step, we will download an old and outdated/depricated version of Firefox and install to our host machine. We will than run another credentialed scan to see what kind of vulenrabilities we see. We see that the old firefox comes back as a critical risk and must be eirher removed or upgrade. We remidiate vulnerabilites by patching, updating, removing, and configuring software running on our hosts.
  
<img src="https://i.imgur.com/ybQWhKe.png" height="40%" width="40%" alt="Vulnerability Management Project Steps"/> <img src="https://i.imgur.com/mDDkXha.png" height="40%" width="40%" alt="Vulnerability Management Project Steps"/> 

