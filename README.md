# libvirt-terraform

To Check if Virtualization is enabled on your linux environment:

egrep -c '(svm|vmx)' /proc/cpuinfo
  should return the number of processors, greater than 0.
  
 lscpu 
  Should grep for 'Virtualization'. VT is turned on if you see VT-x and full in the output.
  
 Intall libvirt: (fedora...)
   sudo dnf install virt-top libguestfs-tools virt-manager
   
  Start libvirtd
    sudo systemctl enable --now libvirtd
Additional tools
  yum module install virt
  yum install virt-install virt-viewer
  
Verify
  virt-host-validate

Download terraform
  wget https://releases.hashicorp.com/terraform/0.13.4/terraform_0.13.4_linux_amd64.zip
  Unzip and copy terraform executable in /usr/local/sbin (in Path)
  
Check terraform version
  terraform version
  
Download terraform libvirt provider
  mkdir -p ~/.local/share/terraform/plugins
  Go to above directory
  mkdir registry.terraform.io
  Go to above directory
  mkdir dmacvicar
  Go to above directory
  mkdir libvirt
  Go to above directory
  mkdir 0.6.2
  Go to above directory
  mkdir linux_amd64
  Go to above directory
  
  Download libvirt terraform plugin
  Go to https://github.com/dmacvicar/terraform-provider-libvirt/releases and get the latest version (.tar.gz).
  Unzip it. (tar -xvzf file)
  
  Mkdir ~/examples and proceed to write the files.
  
  Go to ~/examples
  
  terraform init
  
  Write main.tf
