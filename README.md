# ipa_admin

This is a collection of playbooks you can use to administer freeipa servers with Ansible.  It takes advantage of the freeipa/freeipa_ansible collection.  A requirements.yml file is included which can be used to install the collection and dependencies via ansible-galaxy or via project checkout in Ansible Tower.

# idm_admin_creds.yml
You will need to edit the variable file named idm_admin_creds.yml with the ipa_admin_password variable set to your ipa admin password.

You should encrypt this file using ansible-vault to ensure the credentials are not stored in clear text.

If you're using Ansible Tower, you will need to create a credential to decrypt this vaulted variable file.  That credential will need to be used along with a machine credential in your job template.

