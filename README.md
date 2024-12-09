# User Management Scenario
This script demonstrates managing a user's account and access in a Linux system.

## Key Takeaways:
1. Use `useradd` to create a new user.
2. Use `usermod` with the `-g` option to assign a primary group.
3. Use `chown` to transfer file ownership to a user.
4. Use `usermod -a -G` to add a user to a secondary group.
5. Use `userdel` to remove a user and `groupdel` to delete unnecessary groups.

## Task 1: Add a New User
Add a new user called researcher9
```
sudo useradd researcher9
```
Key Takeaway: `useradd` creates a new user with default settings.

# Add the user to the primary group research_team
```
sudo usermod -g research_team researcher9
```
Key Takeaway: `usermod -g` assigns a primary group to a user.

![image](https://github.com/user-attachments/assets/c3ec2cd0-a574-4a6e-a0ca-b44e3bb1f982)

## Task 2: Assign File Ownership
Make researcher9 the owner of the project_r.txt file
```
sudo chown researcher9 /home/researcher2/projects/project_r.txt
```
Key Takeaway: `chown` changes the owner of a file or directory.

![image](https://github.com/user-attachments/assets/3d6cada5-a7b1-42e9-b8d4-9f7b93a889d0)

## Task 3: Add the User to a Secondary Group
Add researcher9 to the secondary group sales_team while keeping research_team as the primary group
```
sudo usermod -a -G sales_team researcher9
```
Key Takeaway: `usermod -a -G` appends a user to a secondary group without affecting the primary group.

![image](https://github.com/user-attachments/assets/78e9d008-36ce-4cb0-a726-35d5a9bd9bf3)

## Task 4: Delete a User
Delete the user researcher9 from the system
```
sudo userdel researcher9
```
Key Takeaway: `userdel` removes a user but leaves behind their home directory and files (use -r to delete them).

Remove the researcher9 group as it is no longer required
```
sudo groupdel researcher9
```
Key Takeaway: `groupdel` removes a group from the system if it is no longer in use.

![image](https://github.com/user-attachments/assets/34393015-8ab7-4ac2-8f93-9827dbee30d3)
