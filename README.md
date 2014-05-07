imodel
======

imodel是用c语言写的一个php的ORM框架.
```php
$user = new user_model();
$row = $user->fetch(array('userid=?'=>1));
echo $row->getUsername();
echo $row->getUserid();
if($row->getStatus()==0){
     $row->setMoney(0);
     $row->setManage(0);
     $row->setLogMessage('你已被管理员封闭');
     $row->update(); //更新用户ID为1的数据库
}elseif($row->getStatus()==-1){
     $row->delete(); //删除用户ID为1的用户
}
```
