**irq_softirq_exit**  
Full Name: IRQ SoftIRQ Exit  
Meaning: Counts the occurrences of soft interrupt (softirq) handlers exiting. Softirqs are deferred work that is executed in response to hardware interrupts or kernel events.  

**irq_softirq_entry**  
Full Name: IRQ SoftIRQ Entry  
Meaning: Tracks the occurrences of soft interrupt handlers starting to execute. It measures the entry point of the softirq handling mechanism.  

**irq_softirq_raise**  
Full Name: IRQ SoftIRQ Raise  
Meaning: Measures the occurrences of softirqs being raised. Raising a softirq signals the kernel to schedule deferred work for later execution.  

**kmem_kmem_cache_free**  
Full Name: Kernel Memory Cache Free  
Meaning: Counts the number of times objects are released back to kernel memory caches. Kernel memory caches are used for efficient allocation and deallocation of small objects.  

**kmem_kmem_cache_alloc**  
Full Name: Kernel Memory Cache Allocate  
Meaning: Counts the occurrences of objects being allocated from kernel memory caches. These operations are optimized for frequent allocations of fixed-sized objects.  

**net_netif_rx**  
Full Name: Network Interface Receive  
Meaning: Tracks the number of packets received by network interfaces and handed over to the kernel for further processing.  

**net_netif_rx_ni_exit**  
Full Name: Network Interface Receive Non-Interruptible Exit  
Meaning: Counts the exits from non-interruptible network receive processing paths. Indicates the completion of such processing.  

**net_netif_rx_ni_entry**  
Full Name: Network Interface Receive Non-Interruptible Entry  
Meaning: Tracks the entry points into non-interruptible processing for packets received by the network interface.  

**rpm_rpm_usage**  
Full Name: Runtime Power Management Usage  
Meaning: Measures the usage count of runtime power management for devices. Reflects how often devices' power management routines are accessed.  

**rpm_rpm_resume**  
Full Name: Runtime Power Management Resume  
Meaning: Tracks the number of times devices are resumed from a low-power state by the runtime power management system.  
