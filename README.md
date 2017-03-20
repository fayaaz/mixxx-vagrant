# Compile Mixxx in a vagrant box

Use this repo to build vagrant from source on Ubuntu

Just run `vagrant up`

Make sure you have guest tools to test the X stuff properly. It can sometimes take a `vagrant reload` after the guest tools are installed.
To automate the installation of the guest tools the plugin vagrant-vbguest will do most of the work.

Install with `vagrant plugin install vagrant-vbguest`

Once the provisioning/building is done you can check the software by:
1. Open VirtualBox provider and show the build VM
2. Login as the `Ubuntu` user with password `Ubuntu` (pick Openbox as your environment)
3. Right click anywhere and open the terminal emulator
4. Run `/opt/mixxx/bin/mixxx`

ToDo: Add another step to build the deb file