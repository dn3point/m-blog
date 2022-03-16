# How to install FFmpeg on RHEL 8

Follow these steps to install FFmpeg on RHEL 8. Test successfully on AWS EC2 instance with Red Hat Enterprise Linux 8 (64-bit (x86)).

1. Install and enable EPEL
    
    ```bash
    sudo yum install -y install [https://download.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm](https://download.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm)
    ```
    
2. Install and enable RPM Fusion
    
    ```bash
    sudo yum -y localinstall --nogpgcheck https://download1.rpmfusion.org/free/el/rpmfusion-free-release-8.noarch.rpm https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-8.noarch.rpm
    ```
    
3. Install Libsdl2
    
    ```bash
    sudo yum -y install https://vault.centos.org/centos/8/PowerTools/x86_64/os/Packages/SDL2-2.0.10-2.el8.x86_64.rpm
    ```
    
4. Install FFmpeg
    
    ```bash
    sudo yum -y install ffmpeg ffmpeg-devel
    ```
    
5. Verify FFmpeg installation
    
    ```bash
    ffmpeg -version
    ```