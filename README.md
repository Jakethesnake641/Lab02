## Lab 02

- Name: Jacob Wing
- Email: wing.10@wright.edu

## Part 1 Answers

Command to SSH to AWS instance:

ssh -i /home/jacobwing641/CEG2350-Vockey.pem ubuntu@34.231.79.55

## Part 2 Answers

1. `chmod u+r bubbles.txt`
    - Means: Give the user the ability to read "bubbles.txt."
2. `chmod u=rw,g-w,o-x banana.cabana`
    - Means: Allows the user the ability to read and write to (create files for) "banana.cabana," remove the group's ability to write to "banana.cabana," and remove other users ability to execute in "banana.cabana."
3. `chmod a=w snow.md`
    - Means: Gives the user, the group, and others the ability to write to "snow.md."
4. `chmod 751 program`
    - Means: The user has the ability to read, write to, and execute in the "program" file, the group has the ability to read, and execute to the "program" file, and others can execute in the "program" file.
5. `chmod -R ug+w share`
    - Means: Recursively grants write permission to both the user and group for the share directory and its contents.

## Part 3 Answers

1. Command to create new user: sudo adduser newuser
2. Path to user's home directory: /home/newuser
3. Evaluate if `ubuntu` can add files to user's home directory: ls -ld /home/newuser
4. Command to switch to user: su - newuser
5. Command(s) to go to user's home directory: cd ~
6. Evaluate if user can add files to user's home directory: touch ~/testfile
7. Command to switch to `ubuntu`: exit
8. Command to return to `ubuntu` home directory: cd ~

## Part 4 Answers

For each, write the command used or answer the question posed.

1. Command to create group named `crew`: sudo addgroup crew
2. Command(s) to add `ubuntu` & user to group `crew`:  sudo usermod -aG crew ubuntu
sudo usermod -aG crew newuser
3. Command to modify `share` to have group ownership of `crew`: sudo chown :crew share
4. Command to switch to user: su - newuser
5. Command to add file to `share`: touch /path/to/share/newfile.txt
6. Evaluate why these steps allowed the above action:The group crew was assigned ownership of share, and newuser and ubuntu were added to the group.
If the group permissions allow write access, then all members of crew can add files.


## Part 5 Answers

For each, write the command used or answer the question posed.

1. Command to create file using `sudo`:  sudo touch /etc/configfile.conf 
2. Evaluate (in plain text) the permission of the file: ls -l /etc/configfile.conf
3. Provide a method to edit the file without modifying permissions: sudo vim /etc/configfile.conf
4. Command(s) to modify permissions: sudo chmod u+w /etc/configfile.conf

## Citations

To add citations, provide the site and a summary of what it assisted you with.  If generative AI was used, include which generative AI system was used and what prompt(s) you fed it.
