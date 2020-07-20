# ipa_admin

This is a collection of playbooks you can use to administer freeipa servers with Ansible.  It takes advantage of the freeipa/freeipa_ansible collection.  

# Using the requirements.yml
A requirements.yml file is included which can be used to install the collection dependencies via ansible-galaxy or via project checkout in Ansible Tower.

### With Ansible Galaxy
If you are using the upstream Ansible project or Ansible Engine you can install the collection requirements via ansible-galaxy:

`$ ansible-galaxy install -r collections/requirements.yml`

This will install the collection to the default directory for collections on your ansible control node.

### Automatically in Ansible Tower
If you are using this repository as a project in Ansible Tower, the requirements will be downloaded and installed automatically on project checkout.

# idm_admin_creds.yml
You will need to edit the variable file named idm_admin_creds.yml with the ipa_admin_password variable set to your ipa admin password.

You should encrypt this file using ansible-vault to ensure the credentials are not stored in clear text.

If you're using Ansible Tower, you will need to create a credential to decrypt this vaulted variable file.  That credential will need to be used along with a machine credential in your job template.

