# Linux Netfilter Program (7-17-2015)

A Simple program use netfilter hook to filter designated incoming/outgoing packets.


## Installation

First, you should compile the kernel module separately in **_{Program Path}/src/KernelModule_**, execute "**_make_**" in shell.

Then, you can test it by executing "**_insmod myhook.ko_**" in shell to load this kernel module and executing "**_rmmod myhook_**" to unload it.

You can see the kernel module running infomation in **_/var/log/message_**.

The program will auto load and unload this kernel module.

Second, you should install 3 dependent packages in **_{Program Path}/dependents_**.

You may need add "**_#include \<stdint.h\>_**" to **_libnetfilter_queue/libnetfilter_queue.h_** and add "**_#include \<netinet/in.h\>_**" to **_netfilter.h_**.

Then, you should change kernel module path in your system in **_src/Application/main.c_** line 303, or you can comment line 302,303,304,378,379 and load the kernel module yourself.

Now, you can run this program by executing**_./Linux_Netfilter_Program_**, and you can use **-i** to add ip address and use **__-h__** to add hostname(it will be resolved to ip address).

All the filtering rule will be saved in **_./filterlist_** file, you can change it by modifying this file.

You can see the program running infomation in **_./log_** file.

If you have any question, you can contact me by email.


### My email

[1][qq416206@gmail.com](mailto:qq416206@gmail.com)

[2][qy1256@163.com](mailto:qy1256@163.com)
