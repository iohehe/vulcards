# branch name

{% embed url="https://hackerone.com/reports/1256777" %}

### How-to:



1. Create two users, `attacker01` and `victim01`
2. Log in as `attacker01`
3. Create a group `attack_group` by visiting [https://gitlab.domain.com/groups/new#create-group-pane](https://gitlab.domain.com/groups/new#create-group-pane)
4. Go to [https://gitlab.domain.com/groups/attack\_group/-/settings/repository](https://gitlab.domain.com/groups/attack\_group/-/settings/repository) and expand the "Default initial branch name" tab
5. Enter `<script>alert(1);</script>` as "Default initial branch name" and click "save changes"



![](<../../../.gitbook/assets/image (3).png>)



1. Go to [https://gitlab.domain.com/groups/attack\_group](https://gitlab.domain.com/groups/attack\_group) and click the button "New project" and choose to create a "Create blank project"
2. Name the project `attacking_project` and click "Create project"
3. Now the project will load and the alert should pop up.

![](<../../../.gitbook/assets/image (1) (2) (1).png>)

optional: 9. On the project main page click the "Invite members" button and invite `victim01` as a Developer 10. Log in with `victim01` 11. Visit [https://gitlab.domain.com/attack\_group/attacking-project](https://gitlab.domain.com/attack\_group/attacking-project) and the script will run for the victim as well
