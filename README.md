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
    - git push [alias] [branch]/ git pull [alias] [branch] ָ��Զ�˺ͷ�֧
- �����ֲ�

```
git init                                                  # ��ʼ������git�ֿ⣨�����²ֿ⣩
git config --global user.name "xxx"                       # �����û���
git config --global user.email "xxx@xxx.com"              # �����ʼ�
git config --global color.ui true                         # git status�������Զ���ɫ
git config --global color.status auto
git config --global color.diff auto
git config --global color.branch auto
git config --global color.interactive auto
git clone git+ssh://git@192.168.53.168/VT.git             # cloneԶ�ֿ̲�
git status                                                # �鿴��ǰ�汾״̬���Ƿ��޸ģ�
git add xyz                                               # ���xyz�ļ���index
git add .                                                 # ���ӵ�ǰ��Ŀ¼�����и��Ĺ����ļ���index
git commit -m 'xxx'                                       # �ύ
git commit --amend -m 'xxx'                               # �ϲ���һ���ύ�����ڷ����޸ģ�
git commit -am 'xxx'                                      # ��add��commit��Ϊһ��
git rm xxx                                                # ɾ��index�е��ļ�
git rm -r *                                               # �ݹ�ɾ��
git log                                                   # ��ʾ�ύ��־
git log -1                                                # ��ʾ1����־ -nΪn��
git log -5
git log --stat                                            # ��ʾ�ύ��־����ر䶯�ļ�
git log -p -m
git show dfb02e6e4f2f7b573337763e5c0013802e392818         # ��ʾĳ���ύ����ϸ����
git show dfb02                                            # ��ֻ��commitid��ǰ��λ
git show HEAD                                             # ��ʾHEAD�ύ��־
git show HEAD^                                            # ��ʾHEAD�ĸ�����һ���汾�����ύ��־ ^^Ϊ�������汾 ^5Ϊ��5���汾
git tag                                                   # ��ʾ�Ѵ��ڵ�tag
git tag -a v2.0 -m 'xxx'                                  # ����v2.0��tag
git show v2.0                                             # ��ʾv2.0����־����ϸ����
git log v2.0                                              # ��ʾv2.0����־
git diff                                                  # ��ʾ����δ�����index�ı��
git diff --cached                                         # ��ʾ���������index����δcommit�ı��
git diff HEAD^                                            # �Ƚ�����һ���汾�Ĳ���
git diff HEAD -- ./lib                                    # �Ƚ���HEAD�汾libĿ¼�Ĳ���
git diff origin/master..master                            # �Ƚ�Զ�̷�֧master���б��ط�֧master��û�е�
git diff origin/master..master --stat                     # ֻ��ʾ������ļ�������ʾ��������
git remote add origin git+ssh://git@192.168.53.168/VT.git # ����Զ�̶��壨����push/pull/fetch��
git branch                                                # ��ʾ���ط�֧
git branch --contains 50089                               # ��ʾ�����ύ50089�ķ�֧
git branch -a                                             # ��ʾ���з�֧
git branch -r                                             # ��ʾ����ԭ����֧
git branch --merged                                       # ��ʾ�����Ѻϲ�����ǰ��֧�ķ�֧
git branch --no-merged                                    # ��ʾ����δ�ϲ�����ǰ��֧�ķ�֧
git branch -m master master_copy                          # ���ط�֧����
git checkout -b master_copy                               # �ӵ�ǰ��֧�����·�֧master_copy�����
git checkout -b master master_copy                        # �����������
git checkout features/performance                         # ����Ѵ��ڵ�features/performance��֧
git checkout --track hotfixes/BJVEP933                    # ���Զ�̷�֧hotfixes/BJVEP933���������ظ��ٷ�֧
git checkout v2.0                                         # ����汾v2.0
git checkout -b devel origin/develop                      # ��Զ�̷�֧develop�����±��ط�֧devel�����
git checkout -- README                                    # ���head�汾��README�ļ����������޸Ĵ�����ˣ�
git merge origin/master                                   # �ϲ�Զ��master��֧����ǰ��֧
git cherry-pick ff44785404a8e                             # �ϲ��ύff44785404a8e���޸�
git push origin master                                    # ����ǰ��֧push��Զ��master��֧
git push origin :hotfixes/BJVEP933                        # ɾ��Զ�ֿ̲��hotfixes/BJVEP933��֧
git push --tags                                           # ������tag���͵�Զ�ֿ̲�
git fetch                                                 # ��ȡ����Զ�̷�֧�������±��ط�֧������merge��
git fetch --prune                                         # ��ȡ����ԭ����֧���������������ɾ���ķ�֧
git pull origin master                                    # ��ȡԶ�̷�֧master��merge����ǰ��֧
git mv README README2                                     # �������ļ�READMEΪREADME2
git reset --hard HEAD                                     # ����ǰ�汾����ΪHEAD��ͨ������mergeʧ�ܻ��ˣ�
git rebase
git branch -d hotfixes/BJVEP933                           # ɾ����֧hotfixes/BJVEP933������֧�޸��Ѻϲ���������֧��
git branch -D hotfixes/BJVEP933                           # ǿ��ɾ����֧hotfixes/BJVEP933
git ls-files                                              # �г�git index�������ļ�
git show-branch                                           # ͼʾ��ǰ��֧��ʷ
git show-branch --all                                     # ͼʾ���з�֧��ʷ
git whatchanged                                           # ��ʾ�ύ��ʷ��Ӧ���ļ��޸�
git revert dfb02e6e4f2f7b573337763e5c0013802e392818       # �����ύdfb02e6e4f2f7b573337763e5c0013802e392818
git ls-tree HEAD                                          # �ڲ������ʾĳ��git����
git rev-parse v2.0                                        # �ڲ������ʾĳ��ref���ڵ�SHA1 HASH
git reflog                                                # ��ʾ�����ύ�����������ڵ�
git show HEAD@{5}
git show master@{yesterday}                               # ��ʾmaster��֧�����״̬
git log --pretty=format:'%h %s' --graph                   # ͼʾ�ύ��־
git show HEAD~3
git show -s --pretty=raw 2be7fcb476
git stash                                                 # �ݴ浱ǰ�޸ģ���������ΪHEAD״̬
git stash list                                            # �鿴�����ݴ�
git stash show -p stash@{0}                               # �ο���һ���ݴ�
git stash apply stash@{0}                                 # Ӧ�õ�һ���ݴ�
git grep "delete from"                                    # �ļ��������ı���delete from��
git grep -e '#define' --and -e SORT_DIRENT
git gc
git fsck
```