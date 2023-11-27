# CI/CD - TP3

## Connexion 
```
ssh student@149.202.85.73
```
mdp : ?Student_56

```
ssh root@machine2
```
mdp : ?2Student_56

```
echo "Nom: Jametti
Prénom: Nolan" >> /root/info.txt
```

## Installer rpm and gcc
```
sudo apt-get install rpm -y && \
sudo apt-get install gcc -y
```

## AddUser
```
sudo adduser test
chsh -s /bin/bash
su test
```

## Code source helloworld.c
```
echo "#include <stdio.h>

int main() {
   printf(\"Hello World\\n\");
   return 0;
}" >> ./helloworld.c
```

## Compile and test Hello-world.c
```
gcc -o helloworld helloworld.c
./helloworld
```

## Build package
```
sudo apt-get install rpmdevtools
mkdir -p ~/rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}
```

## Principe de rpmbuild
```
touch spec.spec
rpmbuild -ba spec.spec
```

Attention, pas complet : 
```
rpm -qlp ~/rpmbuild/RPMS/<ton_architecture>/nom_du_fichier.rpm
```
