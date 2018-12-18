### Set up the server

~~~
ansible-playbook -i hosts server.yml --extra-vars "ansible_user=root"
~~~

## Set up drupal

~~~
ansible-playbook -i hosts drupal.yml --extra-vars '{"ansible_user":"root"}'
~~~

## Set up SSL

Install the role:
~~~
ansible-galaxy install -r requirements-letsencrypt.yml
~~~

~~~
ansible-playbook -i hosts drupal.yml --extra-vars '{"ansible_user":"root"}'
~~~