# GIT �ʼ�
#### �����û���������
GIT�Ƿֲ�ʽ�ģ�ÿ���ڵ�(����)��Ҫ�Ա����ţ��û���+���䡣  
����ȫ���û��������䣨USERHOME/.gitconfig��  
`git config --global user.name "Your Name"`  
`git config --global user.email "email@example.com"`  
�鿴ȫ���û���������  
`git config --global user.name`  
`git config --global user.email `  
����ָ���ֿ���û��������䣨�ֿ�/.git/config��  
`git config user.name "username"`  
`git config user.email "email"`  
`git config user.name`  
`git config user.email `  
#### �򵥲���  
��һ��Ŀ¼��ִ����������Ŀ¼�ͱ�Ϊgit�Ĳֿ��ˣ�������.git  
`git init`  
�ļ���ӵ��ֿ�  
`git add filename`  
ȫ�����  
`git add .`   
ִ�к�û�з�����Ϣ��Unix����ѧ�ǡ�û����Ϣ���Ǻ���Ϣ��  
�ļ��ύ���ֿ�  
`git commit [filename] -m "wrote a readme file"`  
�鿴��ǰ�ֿ����ļ�״̬  
`git status`  
�ȽϹ��������ݴ�������  
`git diff [filename]`  
�Ƚ��ݴ����ͷ�֧����  
`git diff --cached [filename] `  
�鿴�޸���־  
`git log [--pretty=oneline] [filename]`  
���˵�ǰN���汾��N��^����HEAD�ǵ�ǰ�汾��ָ�룩  
`git reset --hard HEAD^`  
ע����windows cmd�У�^��ת���ַ�����Ҫд�� "^" ���� ^^  
���˵�ָ���汾�ţ�һ���ð汾��ǰ6λ��ģ��ƥ��ģ�  
`git reset --hard �汾��ǰNλ`  
�鿴��ʷ�����¼  
`git reflog`  
���ع����������˳��ݴ������֧���°汾��  
`git checkout -- filename`  
�����ݴ��������˵���֧���°汾��  
`git reset HEAD filename`  
git reset�����Ի��˰汾��Ҳ���Ի��˹�������  
GIT�Ƿֲ�ʽ�洢������û�����͵�Զ��֮ǰ���ڱ��صİ汾�����������ݴ�������֧�������Ըġ�  
ɾ���ļ�  
`git rm filename`  
`git commit filename -m "desc"`  

#### һЩ����  
��������Working Directory��������ִ��git init���Ǹ�Ŀ¼������.git���������ݡ�  
�汾�⣨Repository����.git��������ݡ�  
git add ������ļ��ύ�ݴ�����stage or index����  
git commit ������ݴ������ļ��ύ����֧��branch����  
#### GITHUB
GITHUBԶ��GIT�ֿ⣬https://github.com/  
����git��github��ssh���䣬������ssh��  
1���û���Ŀ¼/.ssh/id_rsa��id_rsa.pub�����û��������  
`ssh-keygen -t rsa -C "youremail@example.com"`  
���Բ�����������  
2����GITHUB��̨���ù�Կ(id_rsa.pub)����������ȷ�������ύ���ˡ�
����ͬ��  
1����github�ϴ���һ���ֿ⣨New Repository����Ȼ�� Clone or download����ʾ��  
  git@github.com:Too8G/Git.git  
2������Զ�̰汾�⣨origin��Զ�̰汾������֣����Ըġ�ֻ��Ա��ص�ǰ�汾����Ч��  
`git remote add origin git@github.com:Too8G/Git.git`  
3�������ذ汾�����͵�Զ�̰汾��ָ����֧�����û�й���������ʾ�޷�ʶ�� origin��
`git push -u origin master`  
���͵�Զ�̰汾��origin��master��֧����һ����-u�ǰѱ���master��֧��Զ��master��֧�����������Ժ�Ͳ����ˡ�  
�ұ��ر����ˣ���Ϊ�汾��������ͬ���ļ�����Ҫ��pull����push��  
4����Զ�̰汾��������  
`git pull origin master`  
�г�ͻ���ȴ�Զ�̰����µ�pull�������޸ĺ���push��ȥ��  



