# ansible-dev-tasks
Reusable ansible tasks used for spinning up dev sites.

**Troubleshooting**

*Not a good solution security-wise* <br>
If provisioning fails stating "Failed to validate the SSL certificate for deb.nodesource.com:443":
    
    open apt_virtualenv.yml
    replace get_url: url=https://deb.nodesource.com/setup_4.x dest=/home/vagrant/nodejs.sh with
    get_url: validate_certs=False url=http://deb.nodesource.com/setup_4.x dest=/home/vagrant/nodejs.sh
