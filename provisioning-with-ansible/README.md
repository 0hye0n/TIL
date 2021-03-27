# Provisioning With Ansbile

ansible을 활용한 평소에 필요했던 playbook을 용도별로 정리
<br></br>
<br></br>

## playbook list
1. disk provisioning
    - create filesystem for each disk (x)
    - write /etc/fstab (x)
    - mount disk (x)

2. (계속 이어서 추가 예정)


<br></br>
<br></br>
## install ansible (mac os catalina 10.15.6 기준)
소유하고 있는 맥북 기준으로 설치해서 설치 방법이 약간 다를 수 있습니다:)
<br></br>
ansible official 문서에서는 macos에서 pip install command를 사용하여 설치하는것을 권장하므로 해당 방법으로 진행

<br></br>
PIP 설치 
```
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
$ python3 get-pip.py --user
```

<br></br>
ansible 설치 
```
$ python3 -m pip install --user ansible
```


<br></br>
paramiko 설치 
```
$ python3 -m pip install --user paramiko 
```

<br></br>
binary path 추가
```
// print python binary path
$ python3 -m site --user-base
${printed path}

// 각 pc shell 환경에 맞는 profile file에서 binary path 추가(현재 zsh 사용중)
// export $PATH:${printed path}/bin 
$ vi ~/.zshrc 
$ source ~/.zshrc
```





- 참고 (ansible 공식 문서 : https://docs.ansible.com/ansible/latest/index.html)