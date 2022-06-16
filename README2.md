IDE：VSCode，安装以下三个插件


指定语言版本 0.8.1

禁止使用不了解原理、不知道功能边界的第三方库

禁止出现编译警告

所有函数必须明确标示可见性

禁止不可预期次数的循环

原则上禁止100次以上的循环

禁止直接使用加减乘除取模，+-*/%，必须使用SafeMath.sol库

命名规范
文件、合约、库、事件、枚举及结构体命名
当文件里只包含一个合约时，文件命名应该与合约命名相同。
当文件里包含不只一个合约时，文件命名应该根据项目内容合理命名。
合约、库、事件及结构体命名应该使用单词首字母大写的方式，这个方式也称为：驼峰式命名法，比如：SimpleToken， SmartBank， CertificateHashRepository，Player。

函数、参数、变量及修饰器
函数、参数、变量及修饰器应该使用首单词小写后面单词大写的方式，这个方式也称为：驼峰式命名法，是一种混合大小写的方式，如：
函数名应该如：getBalance，transfer，verifyOwner，addMember。构造函数除外
参数和变量应该如：initialSupply，senderAddress，account，isPreSale。
常量应该使用全大写及下划线分割大词的方式，如：MAX_BLOCKS，TOKEN_NAME，CONTRACT_VERSION。
修饰器应该如：onlyAfter，onlyOwner。
如果局部变量与全局变量冲突，在局部变量后面加下划线，initialSupply_。
在require，if，for，while判断块中，将不变量写在左边
例如：require(0 < fee, "1035");
例如：if (0 == amount) {
     }

异常
异常提示统一使用状态码(存储在数据库表ido_server.solidity_error_code)，不要重复使用，使用后将state标为1
require(0 < fee, "1035");

代码缩进、换行-统一使用插件的格式化