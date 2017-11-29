# Setup Considerations

## Introduction to System Setup for Deep Learning Tasks
At this very early stage in your journey to graduate the program I think it is essential to understand a few basic things I personally struggled with.  You will need a few pieces of software and many of these software packages rely on each other.  In this project you start your work in AI(Artificial Intelligence)/ML(Machine Learning)/DL(Deep Learning) and all the libraries and tools that go along with that.  Multiple methods of installation will get you to your end goal of being able to complete this project.  What does that mean?  Well we have containers, virtual machines, cloud instances, and virtual environments, and bare metal.  If you aren't familiar with these terms that is fine.  I will give you the gist very quickly.

 - Containers - Docker, LXC,
   - Much lighter then a full virtual machine, but almost the same thing.
 - Virtual Machines - Virtual Box, VM Ware, Parallels, 
   - Usually easier to use then Docker, but uses slightly more resources.
 - Cloud Instances - OpenStack, Amazon EC2, 
   - You don't need to have your own GPU
 - Virtual Environments - Chroot
   - Very similar to Docker except without the extra tools
  - Python Virtual Environments - Anaconda
    - Separates your systems python packages and libraries apart so they work perfectly without breaking anything, or having version conflicts.
  
## So many options
If none of these things make sense to you that is okay.  If something does make sense to you then go that route.  If you already are familiar with Linux and you know how to enter commands into a terminal then the easiest method to start in my personal opinion is to use Anaconda on a bare metal Ubuntu 16.04 install, or VM Ware system.  Obviously each method has their own issues, but this is what I would recommend.  When going over the pitfalls if you are looking on which method to use, or if you wish just use one and look at the possible pitfalls so you can avoid them.

## Possible Pitfalls

### Bare Metal Version and Dependency Purgatory, maybe it isn't so bad?
One of the reasons Docker is usually suggested as the method to use is because the bare metal approach has a learning curve as well.  If you know nothing of installing software on Linux, adding software repositories, and just the interface differences it can create a problem for people trying to teach you.  Obviously in many companies these tasks are broken up depending on your job title.  I am guessing most people taking this course though are not apart of some huge corporation where they have an IT guy on staff to setup a care free Linux install that runs TensorFlow backend with Keras front end and perfectly working CUDA drivers.  I do believe though as a good developer especially some one that will end up working in something related to machine learning should know.  You should know how to use Linux because it is the OS of choice in the field.  You should know how to use Python.  In order to use Python on Linux without causing a bunch of problems you should use a Python virtual environment.  The method I recommend is using Anaconda.  After you get past these things that are honestly VERY simply to use.  I am talking you can literally copy and past commands for installation and just use the root environment for Anaconda and you are good.  You can add another repository to Anaconda

**CUDA**
https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604

**Ubuntu APT**
NOTE - Add more about pinning, this is related to adding the CUDA 8 since CUDA 9 will break Tensorflow
https://help.ubuntu.com/community/PinningHowto

**Tensorflow/Anaconda**
https://www.tensorflow.org/install/install_linux
- Add conda Forge for pre-compiled tensorflow?

### Docker, Current Recommended Approach and Learned Lessons
Many people go for solutions that have their own learning curve and stumbling blocks.  Setting up and using Docker is usually one of the recommended methods of working on Udacity projects especially later on in the course.  I heard many people having difficulty with this.  That isn't because it isn't a good solution where it applies.  It is simply because Docker is another thing you have to learn when you are already trying to learn about how to Classify Traffic Signs for example.  That is why I would say if you can just use a bare metal system, or a Virtual Machine that **EASILY** allows you to use the GPU.  I am talking a simply toggle switch.  That isn't to say Docker can't also be easy, but you will have to know how to do certain things like displaying GUI applications easily, shutting images down, managing disks, and connecting in to the container.  It can usually be done pretty easily though.

**Add your trials here**

### Cloud Instance Latency
**Add more**
