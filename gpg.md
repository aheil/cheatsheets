# Show keys

```bash
gpg --list-keys
```

will resultin in something similar to 

```bash
pub   rsa2048 2013-11-02 [SC] [expires: 2020-11-02]
      EA2376234EAB23369092847825EE2349087235CE
uid           [unknown] Andreas Heil <andreas.heil@example.org>
uid           [unknown] [jpeg image of size 4881]
sub   rsa2048 2013-11-02 [E] [expires: 2020-11-02]
```

# Import existing privat key 

```bash
gpg --import private.key
```
# Trust a key 

```bash
gpg --edit-key EE17046BC0E0692E11EC89A68F69260C38C9C219 trust quit 
```
and entering e.g. <kbd>5/kbd>

will result in someting similar to

```bash
pub   rsa2048 2013-11-02 [SC] [expires: 2020-11-02]
      EA2376234EAB23369092847825EE2349087235CE
uid           [ultimate] Andreas Heil <andreas.heil@example.org>
uid           [ultimate] [jpeg image of size 4881]
sub   rsa2048 2013-11-02 [E] [expires: 2020-11-02]
```
