

https://github.com/noname007/mykernel


- make allnoconfig
- make
- qemu -kernel arch/x86/boot/bzImage 从qemu窗口中您可以看到my_start_kernel在执行，同时my_timer_handler时钟中断处理程序周期性执行。
cd mykernel 您可以看到qemu窗口输出的内容的代码mymain.c和myinterrupt.c
- 当前有一个CPU执行C代码的上下文环境，同时具有中断处理程序的上下文环境，我们初始化好了系统环境。
- 您只要在mymain.c基础上继续写进程描述PCB和进程链表管理等代码，在myinterrupt.c的基础上完成进程切换代码，一个可运行的小OS kernel就完成了。
- start to write your own OS kernel,enjoy it!
