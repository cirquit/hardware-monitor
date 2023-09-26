# Basic Hardware Monitor With CUDA Support

Single file implementation of a hardware monitor to be used with `tensorboard`, `wandb` and other logging solutions which want to work with a dictionary. Put it in your codebase and use however you like.

A very basic hardware monitor based on `psutil` that enables tracking of:

* network bandwidth
* disk read/write bandwidth
* disk read/write counters
* context switches
* average CPU load (1,5,15 min)
* memory utilization
* process memory (resident, virtual, lib, etc.)

If a GPU is available, over `pynvml`:

* framebuffer memory
* bar1 memory
* gpu/memory "utilization"
* temperature
* power
* throttle reasons

If a GPU is available, and `torch`:

* all of the stats in `torch.cuda.memory_stats()`
* average (small, large, all) segment size
* average block size
* average inactive block size
* allocation rounding overhead
* memory fragmentation

### TODO

* An example application with torch
* Write some tests
* Better decapsulation between `psutil`, `pynvml` and `torch`

### Reference

If you found this useful and want to cite the work, please use the following bibtex:

```
@misc{aisenko2023,
  author = {Alexander, Isenko},
  title = {Basic Hardware Monitor},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/cirquit/hardware-monitor}},
  commit = {<current-commit-hash>}
}
```