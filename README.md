# Virtualbox setup
## Introduction:
This is a detailed documentation on setting up a virtual box on your mac machine.
## Specifications:
Os - Mac sonoma 14.5
## Steps to setup a virtual box:
1. Go to the official VirtualBox website: https://www.virtualbox.org/
2. Click on the "Downloads" link in the top navigation menu.
3. On the Downloads page, you'll see various packages for different host operating systems. Select the appropriate package for your OS (e.g., Windows, macOS, or Linux). In our case it is Mac Os.
4. Double-click on the downloaded DMG file to open it.
5. Double-click on the VirtualBox package icon to start the installation. - Follow the on-screen instructions to complete the installation.
6. Once the installation is complete, you can launch VirtualBox from the Applications folder. Then then the following screen will be opened.
   <img width="566" alt="Screenshot 2024-08-06 at 10 56 53 PM" src="https://github.com/user-attachments/assets/a33f41b9-3f14-4c31-a35c-598631f195a6">
7. Download the ISO image from the Ubuntu official website of your specific version - here i am selectiong Ubuntu 22.0.4 version
8. Go to your Virtual box and click on new. a new virtual box wizard will be opened like below.
   <img width="566" alt="Screenshot 2024-08-06 at 10 11 05 PM" src="https://github.com/user-attachments/assets/b400186f-d3c2-4024-b5bf-77cd601b8a47">
9. Fill the details specified like name and iso file path etc. click on next
    <img width="566" alt="Screenshot 2024-08-06 at 10 14 47 PM" src="https://github.com/user-attachments/assets/d0742f87-9e5d-4658-bab1-d05475c6dd44">
10. To enable the automatic install we need to prepopulate our username and password here in addition to our machine name so that it can be configured automatically during first boot.
11. Change the default values to you username and password. and click on next
    <img width="566" alt="Screenshot 2024-08-06 at 10 15 03 PM" src="https://github.com/user-attachments/assets/82987a23-6b3f-44df-86bc-9a9addd71dd8">
12. In this section we can specifiy how much of our host machine’s memory and processors the virtual machine can use.
    <img width="566" alt="Screenshot 2024-08-06 at 10 15 14 PM" src="https://github.com/user-attachments/assets/b275e1d4-39ad-4f52-b0d6-9ddddc1d9850">
13. Then we need to specify the size of the hard disc for the virtual machine. For Ubuntu we recommend around 25 GB as a minimum.
    <img width="566" alt="Screenshot 2024-08-06 at 10 15 24 PM" src="https://github.com/user-attachments/assets/ae280397-f261-4579-beb4-716e2f04924b">
14. Preview the selection and click on finish then a new virtual machine will be created.
    <img width="566" alt="Screenshot 2024-08-06 at 10 50 51 PM" src="https://github.com/user-attachments/assets/a346ffdd-20ee-432b-a8dc-593cff080a48">
15. Click on start to start your VM.
16. on the first boot the ubuntu image will be installed (this initial setup takes some time)and and a login page will be displayed.
    <img width="566" alt="Screenshot 2024-08-06 at 10 08 00 PM" src="https://github.com/user-attachments/assets/c7a899cc-2240-4685-82bc-5d8e5238d76f">
17. After login your ubuntu VM is ready use. you can accerss your Ubuntu desktop.
   <img width="645" alt="Screenshot 2024-08-06 at 11 29 58 PM" src="https://github.com/user-attachments/assets/2b2df5c5-e7bb-46ac-b663-c8dbc0f2f91d">

## Steps to host a website on your VM
1. To host a website you need to install nginx on your ubuntu VM.
2. Open terminal of your VM and run the following commands.
   `` sudo apt-get update
      sudo apt-get install nginx`` 
    <img width="566" alt="Screenshot 2024-08-06 at 9 46 38 PM" src="https://github.com/user-attachments/assets/b3d9c878-0f5f-4570-8596-4e2c10173a7d">
3. After successful installation of nginx. run the below commands to start the nginx server.
   `` sudo systemctl start nginx ``
4. Go to your Vm's browser and type 127.0.0.1/ . If the installation is successful you can see the below page.
   <img width="566" alt="Screenshot 2024-08-06 at 9 55 16 PM" src="https://github.com/user-attachments/assets/b4c3941b-8393-4d54-8acc-ad8853182906">
5. Again go to terminbal and switch to /var/www/html folder remove the default html page and create your own index.html page.
6. Restart nginx and check the local host url. You can view your webpage in the browser.
   `` sudo systemctl restart nginx ``
   <img width="646" alt="Screenshot 2024-08-06 at 10 05 18 PM" src="https://github.com/user-attachments/assets/2fe699e7-687b-43c0-984c-565b0fc3a033">
## Steps to scan the VM with 'nmap':
1. Go your mac open terminal and install nmap through Homebrew.
   `` brew install nmap``
2. Afetr successful installation. Go to your virtual machine and pic the ip of that VM.
3. Run the following commands to scan your through nmap
 ``` nmap -sn VM_IP // to do the ping scan
    nmap VM_IP // to scan the open ports
    nmap -sV VM_IP // Detect service versions running on the VM
    sudo nmap -A VM_IP // to run a comprehensive scan ```


    











