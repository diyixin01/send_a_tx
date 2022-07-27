# send_a_tx

比特币系统中使用的脚本语言很简单，唯一能访问的内存空间就是一个栈，是基于栈的语言，这点和通用脚本语言的区别很大。

我们观察这个交易：


![image](https://user-images.githubusercontent.com/75195549/181292438-a44aa294-e6a8-427c-9fa6-966a5d3ed728.png)


这个交易有一个输入和两个输出，其中一个输出已经被花出去了，另一个没有被花出去。


# 比特币脚本
# 输入脚本


输入脚本包含两个操作，分别将两个很长的数压入栈中。


![image](https://user-images.githubusercontent.com/75195549/181293248-1bc7245c-4667-4718-a743-83dcf9e86f63.png)



# 输出脚本

输出脚本有两行，分别对应上面的两个输出，即每个输出有自己单独的一段脚本。


![image](https://user-images.githubusercontent.com/75195549/181293394-52b042d1-9da6-4a1c-b473-7a0cfd8ea150.png)


# Parse the struct

![image](https://user-images.githubusercontent.com/75195549/181294322-5c388ec8-b380-4593-9efb-df6d2fdc71f6.png)

从上到下分别为：

交易的id

交易的哈希值

使用的比特币协议版本号

交易的大小

交易的生效时间，0表示立即生效.非0值表示过几个区块后才允许上链

交易的输入


交易的输出


目前已经有个几个确认(包括自己及其后面有多少区块上链)


交易产生的时间


该交易所在区块产生的时间





# Parse the input

从上到下分别为：









