# Reset Job Template Verbosity

First create a new credential, set the **CREDENTIAL TYPE** to _Ansible Tower_. Then
enter in the Tower Hostname, Tower Username, and Tower Oauth Token.

Next create a new Job Template that will use this playbook in the project you have
setup for access. In the **CREDENTIALS** field make sure to include your _Machine_
credential to access your inventory and the _Ansible Tower_ credential you just created.

You will also likely want to set a **LIMIT** of one host, since you only need the
job template to run once.

By default this playbook will create a list of Job Templates that have a verbosity
greater than 0. It will then reset the **VERBOSITY** back to 'zero'.

You can set a schedule if you'd like to have this run once a week to make sure the
verbosity level of job templates is reset to 'zero'.