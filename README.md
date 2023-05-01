# Notes


## Smb no read write access

[Solution](https://askubuntu.com/questions/1393272/unable-to-change-permissions-and-usergroup-of-smb-mounted-directory)

![image](https://user-images.githubusercontent.com/40700226/235507138-2f142571-4444-4462-ab3f-5862601f1974.png)


Old command:

`sudo mount -t cifs -o username=christian,uid=1000,gid=1000 //xxx.xxx.xxx.xxx/home /mnt/nas`

New command:

`sudo mount -t cifs -o credentials=/home/christian/.smbcredentials,uid=1000,gid=1000 //xxx.xxx.xxx.xxx/home /mnt/nas`

