<h1>Auditing file permissions in Linux</h1>

<h2>Description:</h2>

As a security professional at a large organization, I work with the research team to ensure that users have the appropriate permissions to access files. This allows them to do their regular duties, but also helps to keep the file system secure.

As part of the job, I regularly audit the file system permissions to make sure they match the authorization that should be given. If they do not match, I modify the permissions to authorize the appropriate users and remove any unauthorized access.

<b>Audit Goal:</b><br/> 
<ul>
  <li>To ensure that users on the research team have the appropriate permissions to access files on the file system.</li>
</ul>

<b>Audit Scope:</b><br/> 
<ul>
  <li>Examination of existing file system permissions.</li>
  <li>Determination of whether permissions match authorization.</li>
 <li>Modification of permissions to authorize appropriate users and remove unauthorized access.</li>
</ul>

By using Linux commands, you can audit file permissions and modify them as needed to ensure that only authorized users have access to files. This helps to keep the file system secure and protect the confidentiality, integrity, and availability of data.


<h2>Environments Used:</h2>

- <b>Windows 10</b>

<h2>Audit walk-through:</h2>

- Check file and directory details
  ![image](https://github.com/ktwindisch/LinuxUserPermissionAudit/assets/56203054/288f1a6c-0d13-43c3-8fbe-7363d5c04a38)
  ![image](https://github.com/ktwindisch/LinuxUserPermissionAudit/assets/56203054/e1d66ef6-db09-4ca6-ae3f-90395b9f57f3)

- Describe the permissions string
  ![image](https://github.com/ktwindisch/LinuxUserPermissionAudit/assets/56203054/f59db33d-4af8-4c64-bffb-2dbbb93cce24)
  ![image](https://github.com/ktwindisch/LinuxUserPermissionAudit/assets/56203054/cb7d31e0-aff0-4aaf-b695-556ad121e537)

- Change file permissions
  ![image](https://github.com/ktwindisch/LinuxUserPermissionAudit/assets/56203054/6f413340-a8e9-4aa9-bc2f-7ee2494dec81)<br/>
The chmod command will remove the write permissions for others on the file. Since the other category has been removed from write permission, only the user and group has the right permissions, per our audit instructions. The owner and group can still write to the file, but others cannot write to the file.<br/>

- Change file permissions on a hidden file
  ![image](https://github.com/ktwindisch/LinuxUserPermissionAudit/assets/56203054/b93275cf-ff21-4bf8-bb72-ba9d6f803473)

- Change directory permissions

The last thing we need to audit are the files and directories in the projects directory. They belong to the researcher2 user, so only researcher2 should be allowed to access the drafts directory and its contents. Let’s check the permissions and change them if necessary.
  ![image](https://github.com/ktwindisch/LinuxUserPermissionAudit/assets/56203054/16e62eb1-3e14-42da-83db-4662ce3711af)

<h4> Summary:  </h4>
This audit was to ensure that users on the research team have the appropriate permissions to access files on the file system by:<br/>
<br/>
<ul>
<li>Examining existing file system permissions, determining whether permissions match authorization.</li>
<li>Modifying permissions to authorize appropriate users.</li>
<li>Removing unauthorized access.</li><br/>
</ul>
It is important to regularly audit file system permissions to make sure they match authorization. The chmod command can be used to modify file permissions to authorize appropriate users and remove unauthorized access. Only authorized users should have access to files, as this helps to keep the file system secure.
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
