# NSO-A2 - Automation with Ansible

This program is a set of Ansible playbooks that automate the deployment of a Flask application on Apache web server behind a HAProxy load balancer. The first playbook installs Apache2, mod-wsgi, Python and Flask on the webservers. It then creates a Flask application directory with a sample Python Flask application and its configuration files. Finally, it configures Apache to use mod-wsgi for the Flask application and restarts the Apache service.

The second playbook installs HAProxy and Apache2 on the HAProxy server. It then configures HAProxy to load balance requests to the Apache webservers and redirects HTTP traffic to port 8080 on the Apache server. It restarts both HAProxy and Apache services.

The last playbook displays the IP address of the HAProxy server and sends HTTP requests to it using the "uri" module in Ansible. It registers the output from servers devA and devB and devC and displays it using the "debug" module.

* To enable Ansible to connect to all hosts, SSH access needs to be set up.

* command to run

" ansible-playbook -i hosts site.yaml "
