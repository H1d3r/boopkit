# ENOHONK

Linux eBPF backdoor (TCP/UDP) for spawning reverse shells. Less Honkin. More Tonkin. 

This is a research project, that is currently under active development. I will publish a release once the code is well vetted. 

### Compile Time Dependencies 

 - 'clang'
 - 'linux-headers'
 - 'llvm'

### eBPF Tracepoint Selection

For now we start with `tracepoints/tcp/tcp_probe` just to trigger arbitrary code given a specific TCP packet filter.

In the future we want to build an alternative TCP handshake where we deliberately trigger `tracepoints/tcp/tcp_retransmit_synack` given a "remote" caller.

### References

 - [ebpf-kill-example](https://github.com/niclashedam/ebpf-kill-example) by Niclas Hedam
 - [go-ebpf-examples](https://github.com/leodido/go-ebpf-examples) by Leonardo DiDonato

