# DigitalOceanLamp
This Ansible script with create a droplet within DigitalOcean that contains Ubuntu, 18.04 if not changed, with LAMP. This also has a simple start of an HTML script to start a page. 

To get started you will need to first create a token, or have a token, from your DigitalOcean account. Once you have that you can place it within DOlamp.yml script where it specifies <Your Digital Ocean Token>. Save the changes and enter into the inventory.yml.

In the inventory.yml file under the webservers it says DigitalOceanTest, this is what your droplet will be called. You can change it your domain or any name you would like. Note the more names you have, the more droplets it will create
For example:
webservers:
  hosts:
    DigitalOceanTest:
    DigitalOceanTest2:
and so on. 
Also in the inventory you will see some variables, these will be needed in the for the SSH key to allow you to remote into the droplet within the same script. 

Next is the index.html, This file is a simple html page that just gets it off the appache default page. You can add the Tab title and some simple text in the body. You can also add your own html file with ion this or just reference the new within the code itself. 

When running the playbook you will want to run as follows:
ansible-playbook -i inventoryu.yml DOlamp.yml --ask-become-pass
and then when prompted enter in your password. 

Have a great day. 
