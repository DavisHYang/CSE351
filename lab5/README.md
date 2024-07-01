## Lab 5 - Writing a Dynamic Storage Allocator
In this lab, you will be writing a dynamic storage allocator for C programs, i.e., your own version of the `malloc` and `free` routines. This is a classic implementation problem with many interesting algorithms and opportunities to put several of the skills you have learned in this course to good use. However, be warned that it is quite involved, so start early!

### Learning Objectives
- Implement a memory allocator using an explicit free list.
- Examine how algorithm choice impacts tradeoffs between utilization and throughput.
- Read and modify a substantial C program.
- Improve your C programming skills including gaining more experience with structs, pointers, macros, and debugging.

### Format
Your dynamic storage allocator will consist of the following three functions (and several helper functions), which are declared in `mm.h` and defined in `mm.c`:

- `int mm_init(void);`
- `void* mm_malloc(size_t size);`
- `void mm_free(void* ptr);`

The `mm.c` file we have given you partially implements an allocator using an explicit free list. Your job is to complete this implementation by filling out `mm_malloc` and `mm_free`. The three main memory management functions should work as follows:

- `mm_init` (provided): Before calling `mm_malloc` or `mm_free`, the application program (i.e., the trace-driven driver program that you will use to evaluate your implementation) calls `mm_init` to perform any necessary initializations, such as allocating the initial heap area. The return value is -1 if there was a problem in performing the initialization, 0 otherwise.
- `mm_malloc`: The `mm_malloc` routine returns a pointer to an allocated block payload of at least `size` bytes. (`size_t` is a type for describing sizes; it's an unsigned integer that can represent a size spanning all of memory, so on x86_64 it is a 64-bit unsigned value.) The entire allocated block should lie within the heap region and should not overlap with any other allocated block.
- `mm_free`: The `mm_free` routine frees the block pointed to by `ptr`. It returns nothing. This routine is guaranteed to work only when the passed pointer (`ptr`) was returned by an earlier call to `mm_malloc` and has not yet been freed. These semantics match the semantics of the corresponding malloc and free routines in libc. Type `man malloc` in the shell for complete documentation.
We will compare your implementation to the version of malloc supplied in the standard C library (libc). Since the libc malloc always returns payload pointers that are aligned to 8 bytes, your malloc implementation should do likewise and always return 8-byte aligned pointers.



Full details at [Lab 5 Overview Page](https://courses.cs.washington.edu/courses/cse351/24sp/labs/lab5.html).
