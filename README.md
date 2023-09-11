newlib-prebuilt
===============
### ChatGPT
> To provide the necessary system-dependent functions when using Newlib
> in a bare-metal environment, you'll need to implement the required
> low-level I/O functions. Here are the steps you can follow:
> 
> 1. Identify the required system-dependent functions: Review the Newlib documentation or the source code to determine which functions you need
> to provide. The essential functions typically include `_read`,
> `_write`, `_open`, `_close`, and `_lseek` for file I/O operations.
> 
> 1. Implement the low-level I/O functions: Write the implementations for the required functions based on your bare-metal platform. These
> functions should interact directly with your hardware peripherals or
> any other means of communication available on your system.
> 
>    - `_read`: Implement this function to read data from a file or input device. You may read data from a UART, SPI, or any other input
> source and return the number of bytes read.
> 
>    - `_write`: Implement this function to write data to a file or output device. You'll need to send the data to the appropriate output
> interface, such as a UART, SPI, or display, based on your hardware.
> 
>    - `_open`: Implement this function to open a file or resource. You can define your own file handling mechanism or utilize any underlying
> storage devices available in your bare-metal system.
> 
>    - `_close`: Implement this function to close a file or resource. Perform any necessary cleanup or release any resources associated with
> the file or resource.
> 
>    - `_lseek`: Implement this function to change the position within a file. You can define the behavior of seeking within a file based on
> your specific requirements.
> 
>    You may also need to implement other functions such as `_isatty`
> and `_fstat` depending on the requirements of your bare-metal system.
> 
> 1. Customize linker scripts: Depending on your bare-metal system, you may need to modify the linker scripts to ensure that the Newlib
> functions are linked correctly with your application code.
> 
> 1. Build and link your code: Compile your code using the appropriate toolchain and linker flags, ensuring that the Newlib library is linked
> properly with your application.
> 
> 1. Test and debug: Verify that the Newlib functions work as expected in your bare-metal environment. Test various file I/O operations and
> ensure that the low-level I/O functions are correctly interacting with
> your hardware.
> 
> It's important to note that the specific details of implementing the
> system-dependent functions will depend on your bare-metal platform and
> the peripherals available. You may need to consult the documentation
> and reference materials specific to your hardware to understand the
> interaction with the peripherals and the necessary low-level code
> required.
> 
> Additionally, keep in mind that Newlib is a C library and does not
> provide any hardware abstraction layer (HAL) or device drivers. You'll
> need to develop or adapt any necessary device drivers to interact with
> your hardware peripherals effectively.

### Reference
- https://github.com/bminor/newlib/blob/master/.github/workflows/cygwin.yml
- https://hackaday.com/2021/07/19/the-newlib-embedded-c-standard-library-and-how-to-use-it/
- https://www.cs.ccu.edu.tw/~pahsiung/courses/esd/resources/newlib.pdf
