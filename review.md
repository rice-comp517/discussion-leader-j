# Review

## Info

Reviewer Name: Jay Shi \
Paper Title: Unikernels: Library Operating Systems for the Cloud

## Summary

### Problem and why we care

Virtual machines are used extensively in the cloud to achieve economy of scale, but general purpose commodity operating systems are not optimized for often single purpose VMs. Making VMs run faster and lighter weight is profitable for cloud service providers.

### Gap in current approaches

VMs provide great isolation but have performance overhead. VM images are often bulky and contain code unnecessary for applications to execute. Containers are lighter weight and faster but offer less isolation and security.

### Hypothesis, Key Idea, or Main Claim

Unikernels are VMs running a libOS and single process application written in a single language in a single address space. They are as secure as ordinary VMs assuming the hypervisor is secure and as fast and light weight as containers. Specifically, type safety of the implementation language can help with the security of unikernels.

### Method for Proving the Claim

MirageOS is a functional prototype targetted at Xen implemented in OCaml, a type safe, garbage collected language.

### Method for evaluating

Boot time, threading performance, thread timer precision, random block read throughput, network latency, DNS performance, OpenFlow controller performance, dynamic web application performance, static page serving performance, codebase and binary size are measured and compared to those of other systems.

### Contributions: what we take away

## Pros (3-6 bullets)
- Unikernels are light weight. System components are provided as libraries and linked to as needed, producing small binary size.
- Unikernels are customizable. System components can be overridden with specialized libraries to suit application needs.
- Unikernels are fast. Due to the lack of userspace/kernel boundary, some system calls can be made more efficient
- Unikernels are scalable. Multiple communicating unikernels can form an application running like a distributed system.
- Unikernels are secure. Besides the security provided by the hypervisor, static type checking and garbage collection can prevent a lot of memory errors.

## Cons (3-6 bullets)
- An application in a unikernel can only be implemented in one language.
- Multiple processes are not supported in one unikernel.
- It is hard for unikernels to elimiate code written in unsafe language, for example from the runtime and the hypervisor.
- The single address space model is prone to attacks, which may be why a type safe language is used.

### What is your analysis of the proposed?

I do not think unikernels can replace containers, because the container ecosystem is already mature and they require application programmers to program differently than what they might have been used to, but I do think unikernels are very useful for cloud service providers who profit out of performance and security in that they allow for a larger degree of customization.

## Details Comments, Observations, Questions

I wish that the paper can be more clear about the line between what is required for a unikernel and the nice, additional features. For example, type safety is used to enhance security but I have also seen other unikernels that support unsafe languages, so type safety does not seem to be a part of the definition of unikernels.
