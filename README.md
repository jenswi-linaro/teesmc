# Passing parameters to and from TEE

## Introduction
The SMC Calling Convention specifies which registers are used for passing
parameters in, but it does not specify what should be passed in the
registers.

Global Platform specifies TEE Client API which is capable of both passing
parameters by value and using shared memory depending on which method is
most convenient for a specific function.

This project describes a way of passing parameters that is compatible with
TEE Client API and SMC Calling Convention requirements.

## Design considerations
* Balance between efficiency and flexibility
* Easy handling by a hypervisor
* Consistent layout to avoid special cases

## Benefits of using this API
Minimize fragmentation of TEE driver in
* Hypervisors
* Secure monitors
* Linux kernel
* Linux user space


## Code
Available at https://github.com/jenswi-linaro/teesmc
