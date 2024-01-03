1. Tạo ssh key

```
ssh-keygen -t ed25519 -C "your_email@example.com"
hoặc
 ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

2. Add ssh key vào ssh-agent

```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

3. Sao chép ssh key public

```
cat ~/.ssh/id_ed25519.pub
```

4. Nhúng ssh key public vừa sao chép vào ssh key trong github

5. Test connect:

```
ssh -T git@github.com
```

- Sign nhiều account

```
vi ~/.ssh/config

#github avnendv
Host github.com
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_ed25519

#gitlab avnendv
Host gitlab.com
        HostName gitlab.com
        User git
        PreferredAuthentications publickey
        IdentityFile ~/.ssh/id_gitlab_avnendv
```
