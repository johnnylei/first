## git �ʼ�
> git ��������

- git svn ����
    - GIT�Ƿֲ�ʽ�ģ�SVN���ǣ�����GIT�������Ƿֲ�ʽ�İ汾����ϵͳ������SVN��CVS�ȣ�����ĵ����������һ��git�����Ա�clone,����updateȥԶ�ˣ���
    - GIT�����ݰ�Ԫ���ݷ�ʽ�洢����SVN�ǰ��ļ������е���Դ����ϵͳ���ǰ��ļ���Ԫ��Ϣ������һ������.svn,.cvs�ȵ��ļ����
    - GIT��֧��SVN�ķ�֧��ͬ����֧��SVN��һ�㲻�ر𣬾��ǰ汾���е������һ��Ŀ¼��
    - GITû��һ��ȫ�ֵİ汾�ţ���SVN�У�ĿǰΪֹ���Ǹ�SVN���GITȱ�ٵ�����һ��������
    - GIT������������Ҫ����SVN��GIT�����ݴ洢ʹ�õ���SHA-1��ϣ�㷨������ȷ���������ݵ������ԣ�ȷ�����������̹��Ϻ���������ʱ���Ͷ԰汾����ƻ���
    
- ��������
![image](/src/img/work_flow.png)
- ��������
    - 
    - ��������Ŀ¼
    - �ݴ�����
        - ִ��add����֮���ݴ�����Ŀ¼�������£�ͬʱ�������޸ģ������������ļ����ݱ�д�뵽������е�һ���µĶ����У����ö����ID����¼���ݴ������ļ������У�.git/index����
        - commit,�ݴ�����Ŀ¼��д���汾�⣨����⣩�У�master ��֧������Ӧ�ĸ��¡��� master ָ���Ŀ¼�������ύʱ�ݴ�����Ŀ¼����
        - git reset HEAD, �ݴ�����Ŀ¼���ᱻ��д���� master ��ָ֧���Ŀ¼�����滻�����ǹ���������Ӱ�졣
        - git rm --cached <file>,��ֱ�Ӵ��ݴ���ɾ���ļ����������������ı䡣
        - git checkout ./git checkout -- <file> �����ݴ���ȫ����ָ�����ļ��滻���������ļ������������Σ�գ��������������δ��ӵ��ݴ����ĸĶ���
        - git checkout HEAD ./git checkout HEAD <file> ���� HEAD ָ��� master ��֧�е�ȫ�����߲����ļ��滻�ݴ������Լ��������е��ļ����������Ҳ�Ǽ���Σ���Եģ���Ϊ�����������������δ�ύ�ĸĶ���Ҳ������ݴ�����δ�ύ�ĸĶ���
- ��������
    - git init ����repository
    - �����˵�ssh pub key ���뵽 ~/.ssh/authorized_keys ��
    - ͨ��git clone��-b ָ��branch��
    - �����ָ��-b��������������Ĭ��master��֧
    - git add ����Ҫ���յ�����д�뻺�棬
    - git commit ��¼�������Ŀ���
    - git push/git push�ύ����ȡ
    - git config ���������ļ�
    - git branch���Բ鿴��ǰproject��branch
    - git branch -a ���Բ鿴���е�Branch
    - git checkout (brank) �л�branch
    - git branch (branch) ����branch
    - git meger (branch) ���Խ����branch meger����
    - git checkout -b (localbarnchname)  (remotebranchname) ���Դ�Զ��checkout ����Ҫ�ķ�֧����Ϊclone��ʱ��ֻ��cloneһ����֧��
    - git diff HEAD �鿴���е�diff
    - git diff ��δ����ĸĶ�
    - git diff --cached �鿴�ѻ���ĸĶ�
    - git log oneline ��Log
    - git log --graph �����ڻ�ͼ
    - git status/git status -s �Բ鿴�����ϴ��ύ֮���Ƿ����޸ġ�
    - git tag -a v1.0 ����汾��
    - git log --online --decorate -graph/git tag -a v0.9 85fc7e7 ���Բ鿴�汾��
- ����github����
    - ssh-keygen -t rsa -C "leiyuqing_jing@163.com", ��������ַӦ��Ϊgithub�󶨵������ַ
    - �ص�github�ϣ����� Account Settings���˻����ã������ѡ��SSH Keys��Add SSH Key,title����ճ��������������ɵ�key��
    - ssh -T git@github.com ��֤�Ƿ���ϵgithub�ɹ�
    - ��github���洴��repostory, ����github���ṩ�ĵ�ַ��git remote add origin git@github.com:tianqixin/w3cschool.cc.git
    - ����.git �����config �ļ�����ָ����ͬ·��
```
[remote "72server"]
	
url = www@121.40.213.72:/tmp/project/.git
	
fetch = +refs/heads/*:refs/remotes/b2/*

[branch "b2"]
	
remote = b2
	
merge = refs/heads/b2

[remote "gitserver"]
	
url = https://github.com/johnnylei/first.git
	
fetch = +refs/heads/*:refs/remotes/b2/*

[remote "all"]  
    url = https://github.com/johnnylei/first.git
  
    fetch = +refs/heads/*:refs/remotes/b2/*
    url = www@121.40.213.72:/tmp/project/.git
    fetch = +refs/heads/*:refs/remotes/b2/*
```
- �߽�����
    - git remote/git remote -v�鿴Զ����Ϣ
    - git fetch ��Զ�ֿ̲������·�֧������,������ִ�������Ҫִ��git merge Զ�̷�֧�������ڵķ�֧
    - 