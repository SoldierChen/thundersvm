GPU-SVM
======
This GPU-SVM project is based on MASCOT which is a GPU-based implementation for SVM cross-validation. GPU-SVM now has modules for SVM classification. We are currently upgrading GPU-SVM to support SVM with probability output and SVM regression.

The associated paper of this source code is: <i>Wen, Zeyi, et al. "MASCOT: fast and highly scalable SVM cross-validation using GPUs and SSDs." 2014 IEEE International Conference on Data Mining</i>.

Report bugs to: name@domain where name=wenzeyi and domain=(google's email)

This software is licensed under Apache Software License v2.0.

Requirement(s):
=
CUDA 7.5 or later; g++ 4.8 or later

FAQ:
======
1. How can I use the source code?<br>
<b>A</b>: Download the repository and then issue "make" command under the fold where our Makefile is located. After the command is completed, you will see a binary file named "mascot" in the "bin" folder. To start playing it, run the "run.sh" script. The dataset shown in run.sh is available <a href="http://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary.html">here</a> in LibSVM site.

2. What is the format of the input file?<br>
<b>A</b>: The file format is the same as the format of files in LibSVM site.

3. Does this version support the Windows OS?<br>
<b>A</b>: No. However, the code should work on Windows OS, although we have tested it on Windows.

4. Do I have to install an SSD if I want to use GPU-SVM?<br>
<b>A</b>: No. GPU-SVM works fine with HDDs, although SSDs would help improve the efficiency.

5. What are the meanings of the options?<br>
<b>A</b>: -b is for SVM with/without probability output; -o is for setting the task type (e.g. training or cross-validation); -g is for setting the gamma value; -c is for setting the penalty value of C; -f is to let GPU-SVM know the data dimensionality (this parameter is optional).

6. I got "error while loading shared libraries: libcudart.so.6.0: wrong ELF class: ELFCLASS32", when I run the executable file "mascot".<br>
<b>A</b>: Running the command ''sudo ldconfig /usr/local/cuda/lib64'' should resolve the problem..
