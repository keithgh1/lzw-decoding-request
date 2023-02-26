This repo was setup to provide two examples of files compressed using an early implemention of LZW. This uses an initial bits/code size of 9.

The goal is find a modern way of decoding these compressed files. The uncompressed versions of those files are also included for verification.

Ideally, a python function is created, using existing libary code, if available, that accepts the input _compressed files, and generates the associated uncompresed versions

The _compressed files include a header, CFM (compressed file marker?), '9' which I'm assuming is 9 bits, and a filename. The filename is a null-terminated string which I believe has a maximum (25) character length. The original uncompressed size is located near offset 0x26(hex), and also near the end of the file. I think the raw LZW data stream would start around offset 0x28(hex).
