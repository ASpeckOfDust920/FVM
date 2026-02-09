

                      Windows Featherweight Virtual Machine (FVM)


 Overview

 FVM (Featherweight Virtual Machine) is a lightweight virtualization technology built
 on the resource isolation mechanism of the operating system kernel. Unlike
 traditional hardware virtualization architectures, FVM does not require emulation of
 the complete hardware stack. It enables the creation of multiple mutually isolated
 execution environments on a single physical host, achieving a balance between
 efficient resource utilization and security isolation.


 Architecture Design
 
 FVM constructs a virtualization layer between the operating system kernel and the
 application layer, utilizing an innovative Copy-on-Write (CoW) mechanism. This
 design allows virtual machine processes to directly share host system resources
 while ensuring complete runtime isolation. Each virtual machine only needs to
 record the differential state relative to the host environment, eliminating the need to
 replicate a full operating system image. This significantly reduces storage and
 runtime overhead.


 Core Technical Features

 1.Resource Efficiency
   • Kernel-Sharing Architecture: Shares the host operating system kernel and system
      libraries, eliminating redundant system overhead.
   • Lightweight Images: Virtual machine image sizes are significantly reduced, typically
      at the MB level.
   • Rapid Deployment Capability: Supports millisecond-level startup and dynamic
      elastic scaling.

 2.Deep Security Isolation
   • Process Space Isolation: Achieves complete isolation of process views through
      namespace technology.
   • System Resource Control: Supports fine-grained quota limits for CPU, memory,
      storage, and I/O.
   • Policy-Driven Protection: Implements comprehensive security controls based on
     a policy engine.

 3.Fine-Grained Resource Management
  The system enforces comprehensive control over each virtual machine through a
  unified policy engine, including but not limited to:
  • Process operation filtering and auditing
  • Network virtualization and auditing
  • File virtualization and auditing
  • Registry virtualization and auditing
  • Kernel object virtualization and auditing
  • Service virtualization and auditing
  • Screen protection and printing control
  • Desktop isolation and protection
  • Memory isolation and protection
  • Data tagging or encrypted flow and auditing
  • SDK interface integration with the policy engine


 Application Scenarios

   • Security Sandbox: Executes untrusted code or analyzes malware, isolating
      high-risk applications to prevent system contamination.
   • Data Protection: Provides an isolated runtime environment for sensitive
      work data to prevent data leakage and unauthorized access.
   • Application Multi-Instance: Enables running multiple single-instance applications
      simultaneously on a single computer.
   • Cloud Desktop Infrastructure: Virtualizes multiple cloud application desktop
      environments, supporting simultaneous remote connections and operations from
      multiple thin clients.
   • Comprehensive Terminal Closed-Loop Protection System: Implements differentiated
      security policies based on terminal roles, blocks virus propagation between hosts,
      between hosts and virtual machines, and between virtual machines, prevents illegal
      data leakage, and builds an all-around protection system.


 Synchronization Mechanism
  FVM supports bidirectional state synchronization:
  • Compliant state changes within the virtual machine can be submitted to the host.
  • Host security updates can be pushed to the virtual machine in real time.
  • Differential synchronization is supported to reduce data transmission overhead.





 
                            Windows 轻量级虚拟机(FVM)


 概述

 FVM（Featherweight Virtual Machine）是一种基于操作系统内核的资源隔离机制构建
 的轻量级虚拟化技术。与传统硬件虚拟化架构不同，FVM无需模拟完整的硬件堆栈，能够在
 单一物理主机上创建多个相互隔离的执行环境，实现资源高效利用与安全隔离的平衡。


 架构设计
 
 FVM在操作系统内核与应用程序层之间构建虚拟化层，采用创新的写时复制（Copy-on-
 Write）机制。该设计使虚拟机进程能够直接共享主机系统资源，同时确保运行时环境的完
 全隔离。每个虚拟机仅需记录与主机环境的差异状态，无需复制完整的操作系统镜像，大幅
 降低了存储与运行开销。

    
 核心技术特性

 1. 资源高效性
   • 内核共享架构：共享主机操作系统内核与系统库，消除冗余系统开销
   • 轻量化镜像：虚拟机镜像体积显著缩小，通常为MB级别
   • 快速部署能力：支持毫秒级启动与动态弹性伸缩

 2. 深度安全隔离
   • 进程空间隔离：通过命名空间技术实现进程视图的完全隔离
   • 系统资源管控：支持CPU、内存、存储和I/O的精细化配额限制
   • 策略驱动防护：基于策略引擎实现全方位的安全控制

 3. 细粒度资源管理
  系统通过统一策略引擎对每个虚拟机实施全方位管控，包括但不限于：
   • 进程操作的过滤与审计
   • 网络虚拟化与审计
   • 文件虚拟化与审计
   • 注册表虚拟化与审计
   • 内核对象虚拟化与审计
   • 服务虚拟化与审计
   • 屏幕防护与打印管控
   • 桌面隔离与防护
   • 内存隔离与防护
   • 数据标记或加密流转与审计
   • SDK接口对接策略引擎


 应用场景

  • 安全沙箱：执行不可信代码或分析恶意软件，隔离高风险应用运行，防止系统污染
  • 数据保护：为敏感工作数据提供隔离运行环境，防止数据泄露和非法访问
  • 应用多开：在单台计算机上同时运行多个单实例应用
  • 云桌面基础设施：虚拟化多个云应用桌面环境，支持多个瘦客户端同时远程连接与操作
  • 全终端闭环防护体系：基于终端角色实施差异化安全策略，阻断主机间、主机与虚拟机、
    虚拟机间的病毒传播，防止数据非法泄露，构建全方位防护体系
 
   
 同步机制

 FVM支持双向状态同步：
  • 虚拟机内合规状态变更可提交至主机
  • 主机安全更新可实时推送至虚拟机
  • 支持差分同步减少数据传输开销





