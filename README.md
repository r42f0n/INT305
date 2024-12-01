java c
INT305 
Assessment Lab 
INT305 – ASSESSMENT 2 
Assessment Number 
1 
Contribution to Overall Marks 
15% 
Submission Deadline 
12/Dec/2024 
Assessment Objective This assessment aims at evaluating   students’ ability to exploit the deep learning knowledge,   which   is   accumulated   during   lectures,   and   after-class   study,   to   analyze,   design,   implement,   develop,   test and document the images classification using CNN framework. The assessment will be based   on the   Pytorch software.
General Guidelines 
1.       The descriptions   in the   Problem Specifications   are   required   to   be   analyzed   with   mathematic   equations, combined with the explanations of all   elements   in   each   equation.
2.       The   modified   part of the source codes   is   required   to   include   in   the   report.
3.       The   final   classification    performance   that   you   obtain   should   be   reported   in   the   lab   report.   Meanwhile, the screenshot of the final   performance   results   is also   required   in the   report.
4.       For    the    final   performance   results   that   you   obtained,   the   numeric   quantitative   results   are   required.   In   addition,   is   also   important   to   include   some   subjective   image   examples   in   the   report.
5.       Students   need   to   conduct   the   coding   and   experiment   all   by   yourself.   The   obtained   results   cannot    be    shared,    and      each      student      should      analyze      the      results      and    write      the      report   individually.6.       Report name: INT305-Lab-Name-studentID.pdf   (e.g.   INT305-Lab-SanZhang-12345657.pdf)
7.       Late   submission   by   email    is not acceptable   for   Assignment   2.    Please   pay   attention   to   the   cut-off deadline. Your assignment will   not   be graded after the   cut-off   deadline.
8.       For late assignments,   a   penalty   of five   points will   be deducted for   each   day   past the   deadline.   If you submitted within 1 hour after the deadline time, it   is   acceptable   for   reserved   as   normal   submission. After 1 hour, your assignment will be counted as late submission. (same for CW1)
Handwritten digits (MNIST) recognition  
Overall Description: 
This   lab   is to   use the   Pytorch software and CNN (Convolutional   Neural   Network) framework   for handwritten digits classification.   Image classification aims to   predict the   category   of   object   in   an   image (one   image can only   have one   object   in   it).   It   has   attracted   much   attention within   the computer vision community   in   recent years as an   important component for   computer vision applications, such as self-driving vehicles, video surveillance and   robotics.   It   is also the foundation of other computer vision   research topics, such as   object   detection   and   instance   segmentation. 
CNN   is a framework with   both feature extraction and classification   using   deep   convolutional   neural   network. A typical CNN   pipeline   is shown   below.

Figure   1. CNN   image classification   pipeline.The   Dataset we will   use   is   MNIST dataset,   it   has a training set of   60,000   examples,   and   a   test   set   of   10,000 examples. The dataset   is originally available on   Yann   Lecun’s   website.   The   followings         are examples of   handwritten digits   in   MNIST   dataset.

Figure 2.   Examples of   handwritten digits   in   MNIST   dataset.
Problem Specifications: 
1.       Please describe the   2   key   components   in   the   CNN   framework:   the   convolutional   kernel   and   the   loss functions   used   in the framework. (20%)
2.       Please train (or   fine-tune)   and   test   the   framework   on   MNIST   and   report   the   final   accuracy   performance that you   have achieved.   Please also   report some well classified and misclassified   images   by   including the   images and corresponding classification confidence   value.   (40%). 
3.       Propose your own   method to   further   improve   the   classification   performance   or   reduce   the   model size. You   need also compare different   methods with the   performance you   obtained   and explain why. The final classification accuracy   is   not   the   most   important   part, you   may better   refer to some   latest   published   papers and code these state of the   art   methods   to improve the   performance. The explanation and analysis of your   adopted   method   is   highly   related to your final score.   (40%)
Environment Preparation: 
1 Install Anaconda 
1.1   Install   Anaconda   on   Windows
Anaconda   is open-source software that contains Jupyter, spyder, etc that   is   used   for   large   data   processing, data analytics,   heavy scientific computing.
Conda   is a   package and environment   management system that   is available   across Windows,   Linux, and   MacOS, similar to   PIP.   It   helps   in the   installation of   packages and   dependencies associated with a specific   language   like   python, C++, Java, Scala, etc.   Conda   is   also   an environment   manager and   helps to switch   between different environments with just a   few   commands.
Step   1: Visit this website
https://www.anaconda.com/products/individual-d and download the Anaconda   installer.

Step 2:       Click on the   downloaded   .exe file   and   click   on   Next.

Step 3: Agree to the terms   and   conditions.

Step 4: Select the   installation type.

Step 5: Choose   the   installation   location.

Step 6:   Now check the checkbox to add   Anaconda   to   your   environment   Path   and   c代 写INT305 – ASSESSMENT 2C/C++
代做程序编程语言lick   Install.

This will start the   installation.
Step 7: After the   installation   is complete you’ll get the   following   message,   here   click   on   Next.

Step 8: You’ll get the following screen once   the   installation   is   ready   to   be   used.   Here   click   on   Finish.

Verifying the   installation:
Now open   up the Anaconda   Power Shell   prompt and   use the   below command   to   check   the   conda version:
coda   -V
If conda   is   installed successfully, you will get a   message as   shown   below:

1.2   Install   Anaconda   on   Linux
Prerequisites 
Firstly, open terminal on your   Ubuntu system and execute   the   command   mentioned   below   to   update   packages   repository:
sudo   apt update
Then   install the curl   package, which   is further   required for the downloading the   installation   script.
sudo apt   install   curl   -y
Step 1 – Prepare the Anaconda Installer 
Now   I will go to the   /tmp   directory and for this   purpose we   will   use   cd   command.   cd   /tmp
Next,   use the curl command   line   utility to download the Anaconda   installer   script   from   the
official   site. Visit   the   Anaconda   installer   scriptdownload   pageto   check   for   the   latest   versions.   Then, download the script   as   below:
curl --output anaconda.sh https://repo.anaconda.com/archive/Anaconda3-
2021.05-Linux-x86_64.sh
To check the script. SHA-256 checksum,   I will   use this   command with   the   file   name,   though   this   step   is optional:
sha256sum anconda.sh
Output:
25e3ebae8905450ddac0f5c93f89c467   anaconda.sh
Check   if the   hash code   is   matching with code showing on   download   page.
Step 2 – Installing Anaconda on Ubuntu 
Your system   is   ready to   install Anaconda.   Let’s   move to the text step and execute   the   Anaconda   installer script. as   below:
bash   anaconda.sh
Follow the wizard   instructions to complete Anaconda   installation   process.   You   need to   provide   inputs during   installation   process   as described   below:
01. Use above command to   run the downloaded   installer script. with the bash shell.

02. Type “yes” to accept the Anaconda   license agreement to   continue.

03. Verify the directory   location for Anaconda   installation on   Ubuntu 20.04 system. Just   hit Enter to continue   installer to that   directory.

04. Type “yes” to   initialize the Anaconda   installer on your system.

05. You will see the   below   message on successful Anaconda   installation on   Ubuntu 20.04   system.



The Anaconda   Installation Completed Sucessfully on your   Ubuntu system.   Installer added the   environment settings   in   .bashrc file.   Now, activate the   installation   using following command:
source   ~/.bashrc
Now we are   in the default   base of the   programming environment.   To verify   the   installation   we   will open   conda   list.
conda   list   Output:
# packages in environment at   /home/tecadmin/anaconda3:
#
# Name                                                Version                                              Build   Channel
_ipyw_jlab_nb_ext_conf         0.1.0                                                py38_0
_libgcc_mutex                               0.1                                                          main
alabaster                                          0.7.12                              pyhd3eb1b0_0
anaconda                                           2021.05                                           py38_0
anaconda-client                           1.7.2                                                py38_0
anaconda-navigator                  2.0.3                                                py38_0
anaconda-project                        0.9.1                                 pyhd3eb1b0_1
anyio                                                   2.2.0                            py38h06a4308_1
appdirs                                              1.4.4                                                      py_0
2 Install and configure PyTorch on your machine. 
First, you'll   need to setup a   Python environment.
Open Anaconda   manager via Start   - Anaconda3   - Anaconda   PowerShell   Prompt and test your   versions:
You can check your   Python version   by   running the following command:   python   –-version
You can check your Anaconda version   by   running the following command: conda –-version

Now, you can   install   PyTorch   package from   binaries via Conda.
1          Navigate   to https://pytorch.org/.
Select the   relevant   PyTorch   installation details:   •PyTorch   build – stable.
•Your   OS
•Package – Conda
•Language –   Python
•Compute   Platform. – CPU.

2       Open Anaconda   manager   and   run the   command   as   it   specified   in   the   installation   instructions.conda install pytorch torchvision torchaudio cpuonly   -c   pytorch

3          Confirm and complete the   extraction   of the   required   packages.

Let’s verify   PyTorch   installation   by   running sample   PyTorch code to construct a   randomly   initialized tensor.
4          Open the Anaconda   PowerShell   Prompt and   run the following command.   python
import torch
x   = torch.rand(2,   3)   print(x)
The output should   be a   random   5x3 tensor. The   numbers will   be   different,   but   it   should   look   similar to the   below.

References
[1]http://yann.lecun.com/exdb/mnist/ 
[2]https://github.com/Eng-Abdelrahman- 
M/handwritten_digit_recognition/blob/main/handwritten_digit_recognition.ipynb 

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
