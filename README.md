# ThreadPool-2介绍

线程池是一种用于管理和调度线程的机制，它能够有效地重用线程、减少线程创建和销毁的开销，并且能够控制并发线程的数量。

第二版：基于可变参模板编程和引用折叠原理实现的线程池，基于条件变量、信号量和互斥锁实现线程安全的通信机制

运用C++ 11标准的面向对象编程、多线程编程、线程互斥、线程同步、异步任务、原子操作、CAS等

相比线程池第一版，代码更加精简，运用C++新特性较多

# 编译方式

g++ test_program.cpp -std=c++17 -lpthread  //生成可执行文件

./a.out                                    //执行可执行文件

# 项目技术

基于函数模板可变参编程与引用折叠原理，实现编写模板时能够轻松处理不确定数量的模板参数和任意类型的函数

基于future类型可得到提交任务的返回值，decltype推导返回类型、函数参数类型

基于条件变量condition_variable、信号量semphore和互斥锁mutex实现线程安全的通信机制

支持定制fixed固定线程数量模式或者cached线程数量动态增长/销毁模式

# 项目应用

高并发网络服务器

master-slave线程模型

耗时任务处理

任务调度系统
并行计算、计算密集型任务
