# Computer Vision Assignments
"Shrinked" assignments from CS131 (2019), a course at Stanford. 【完成作业时可以互相讨论，但是不要公开发布作业中你完成code。珍惜建设这些课程作业的人员的努力，为将来的学生保留美好的练习机会。】

## Introduction
Each assignment will contain a hw*.ipynb ipython notebook file that will guide you through the homework. This file will ask you to code up functions in other *.py files and may even ask you to fill in short answers or equations in the ipython notebook. All the instructions necessary for the homework are contained in these hw*.ipynb files.

#### Contents
Homework 0 sets up the course with an introduction on how to use images in python and numpy. It covers basic linear algebra that would be helpful through the course.

Homework 1 starts off the topics in computer vision by understanding concepts such as convolutions, linear systems and different kernels and how to design them to find certains signals in images. 

Homework 2 focuses on edge detection, applying it to lane detection to aid self driving cars. 

Homework 3 introduces SIFT and RANSAC, which are useful for finding corresponding points in multiple images, enabling applications like panorama creation, which is a common feature in most of our smart phones.

<!---
Moving beyond pixels and edges, homework 4 takes a wider view of the image and asks students to use a dynamic programming algorithm to define the energy of certain regions in an image. This energy definition allows us to find regions that are important, enabling different monitors with varying sizes (large projections, medium laptop screens and small cell phones) to display only the important portions of an image. We specifically ask students to implements different versions of seam carving while preserving the structure of objects in images.
-->

Homework 5 asks students to learn to segment images by assigning each pixel to a cluster, where each cluster represents a semantic object category. We analysze different unsupervised clustering algorithms like K-means and hierarchical aggolomerate clustering techniques. They also learn to apply their techniques to segments cats from images and evaluate how well different methods perform. 

Homework 6 and 7 introduce two fundamental tasks in computer vision: image classification and object detection respectively. Students learn to use different image features and classifiers to study how they influence results on such tasks. They are asked to consider the important of rotation, translation, scale and occlusion variance when deciding what features to use. They also study the curse of dimensionality and learn to apply principal component analysis and linear discriminant analysis to further improve their features while compressing their features. Students also explore common methods like sliding windows and deformable parts models to decompose objects into its individual components when detecting them.

Homework 8 ends the course by moving away from still images and into video and studying time dependent features. They learn to use optical flow to calculate motion in images, a technique useful for tracking people in images and classifying actions that people perform.

All the homeworks are under the MIT license.

## When are assignments due?
check the due dates on course homepage.

## How to submit your assignments?
After you have completed each assignment, you need to submit the following deliverables:

hw*.pdf - Export the hw*.ipynb ipython notebook as a PDF. In order to export notebook as a PDF, you will need to install additional libraries or File/Downloaded as HTML or Latex than print or convert it to a PDF.

hw*.ipynb, *.py - All the python files we ask you to code up must be submitted.

Zip your completed assignments (pdf, ipynb, py) with a name like [cv-HW* submission], and email it to me so that we have a record of your work. 


## How to start?
Before working on each homework, you need to setup a few things:
Make sure to install Python (>= 3.5, I tried 3.8) on your local machine. 

**Setting up a virtual environment via virtualenv:** we strongly recommend working using a single [virtual environment](http://docs.python-guide.org/en/latest/dev/virtualenvs/) for all homeworks. This will allow you to have a working environment with all the package dependencies within the repository of your homework, without messing up your work environment in other repositories.

All necessary dependencies for your homeworks can be found in a single requirements.txt, which has been placed at the root of the homework repository.

To set up a virtual environment with name `.env`, run the following inside your homework directory (ex: inside `cv_hw/`):

      sudo pip install virtualenv        # You will need to do this only once
      virtualenv -p python3 .env         # Creates a virtual environment with python3
      source .env/bin/activate           # Activate the virtual environment
      pip install -r requirements.txt    # Install all the dependencies
      # Work on the assignement for a while...
      deactivate                         # Exit the virtual environment when you're done

Note that every time you want to work on the assignment, you should run `source .env/bin/activate` (from within your assignment folder) to re-activate the virtual environment, and `deactivate` again whenever you are done.

**Setting up a virtual environment via conda:** 
I am more familar with conda. So I set up a virtual environment with the name `cvenv` via miniconda and install all the depedencies in the environment by "pip install -r requirements.txt".

**Working with [Jupyter notebooks](https://jupyter.org/):** in your assignment repository, start the notebook with the `jupyter notebook` command.

When working with a Jupyter notebook, you can edit the *.py files either in the Jupyter interface (in your browser) or with your favorite editor (Visual Studio Code, ...). Whenever you save a *.py file, the notebook will reload their content directly.

How do you download the assignments?
------------------------------------

All the assignments will be released via github. You can download the files directly from the website. But instead, we recommend, you use **git** to download the assignments because this will make it easy for you to update the assignments in case there is an update. The instructions below describe how to use git to download our assignments.

#### 1. Installing Git

Follow the instructions here:

    https://git-scm.com/book/en/v1/Getting-Started-Installing-Git

#### 2. Downloading the assignments and lecture notes to your local machine.

In terminal, run the following to copy the released homework directory to your desktop.

    git clone https://github.com/StanfordVL/CS131_release.git

Run the following to copy the lecture notes directory.

    git clone https://github.com/StanfordVL/CS131_notes

#### 3. In case there are updates to the assignments, update your local code using this.

To update your local repository to the newest commit, execute

    git pull

This will fetch the changes that TAs made in the remote directory, so your local directory will be up-to-date with the remote one. Be careful that sometimes if the TAs and you are changing the same lines, there will be a conflict, and you may have to fix the conflicts mannually.

In case you did something wrong and want to give up local changes, which hopefully never happens ;), execute

    git checkout -- <filename>
