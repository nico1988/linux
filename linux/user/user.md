- 创建用户
 一、创建用户：

1、使用命令 useradd

例：useradd user1——创建用户user1
    useradd –e 12/30/2009 user2——创建user2,指定有效期2009-12-30到期
    用户的缺省UID从500向后顺序增加，500以下作为系统保留账号，可以指定UID，

例：useradd –u 600 user3


2、使用 passwd 命令为新建用户设置密码
例：passwd user1
注意：没有设置密码的用户不能使用。

 

3、命令 usermod 修改用户账户
例：将用户 user1的登录名改为  u1，
usermod –l u1 user1
例：将用户 user1 加入到 users组中，
usermod –g users user1


例：将用户 user1 目录改为/users/us1
usermod –d /users/us1 user1

 

4、使用命令 userdel 删除用户账户
例：删除用户user2
userdel user2
例：删除用户 user3，同时删除他的工作目录
userdel –r user3

 

5、查看用户信息
id命令查看一个用户的UID和GID, 例：查看user4的id
id user4
finger命令 ——可以查看用户的主目录、启动shell、用户名、地址、电话等信息
例：finger user4

 

 

二、用户组：

6、命令 groupadd创建用户组
groupadd –g 888 users
创建一个组users，其GID为888

 

7、命令 gpasswd为组添加用户
只有root和组管理员能够改变组的成员：
例：把 user1加入users组
gpasswd –a user1 users
例：把 user1退出users组
gpasswd –d user1 users

8、命令groupmod修改组
groupmod –n user users       修改组名user为users

 

9、groupdel删除组
groupdel users    删除组users