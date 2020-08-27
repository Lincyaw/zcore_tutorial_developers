# 物理内存：VMO 对象

## 虚拟内存对象（Virtual Memory Object，VMO）
`VMO`表示虚拟内存的一个连续区域，可以映射到多个地址空间中。
`VMO`在内核和用户空间中用于表示分页内存和物理内存。它们是进程之间以及内核和用户空间之间共享内存的标准方法。

> 根据文档梳理 VMO 的主要特性

## 实现 VMO 对象框架

> 实现 VmObject 结构，其中定义 VmObjectTrait 接口，并提供三个具体实现 Paged, Physical, Slice

## HAL：用文件模拟物理内存

> 初步介绍 mmap，引出用文件模拟物理内存的思想
>
> 创建文件并用 mmap 线性映射到进程地址空间
>
> 实现 pmem_read, pmem_write

## 实现物理内存 VMO

> 用 HAL 实现 VmObjectPhysical 的方法，并做单元测试

## 实现切片 VMO

> 实现 VmObjectSlice，并做单元测试
