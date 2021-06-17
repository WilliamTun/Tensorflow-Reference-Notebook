# Distributed Training

## Terminology

### Devices:
- CPU
- GPU
- TPU 
A single machine can have several combinations of these devices

### Replica:
During raining. Copy of models variables being placed on several devices. 

### Worker:
A worker is software running on a device that's dedicated to training the replica that's on that device.
Usually, most variables in the replicas are trained independently of the other replicas. 

### Mirrored variables:
There are some non-independent variables that you want to be in sync across all devices. 
The variables within these models that we want to keep in sync across all of the devices we'll call mirrored variables.

## Distribution strategies
### Hardware considerations
- Single machine with multiple devices (CPU, GPU, TPU)
- Multi-machine

### Training
- Synchronous: All workers train over slices of data in sync with each other. Aggregate gradients each each stap using a reduce algo. 
- Asynchronous: All workers train independently.   