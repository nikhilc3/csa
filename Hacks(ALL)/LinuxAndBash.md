---
layout: default
title: Linux and Bash hacks
type: hacks
courses: { 'csa': {'week':0} }
---
<html>
    <head>
    </head>
    <body>
        <p>
            Last login: Tue Aug 22 23:32:58 on ttys002
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % ls
            2023ResearchProject
            Ap Comp Sci Principle
            Applications
            DSRP23
            Desktop
            Documents
            Downloads
            Lab4Graph
            Library
            MVQN
            Movies
            Music
            Pictures
            Postman Agent
            Public
            bin
            e7c424fd-d9ac-4ed4-b583-7d06fbd351fa.png
            fc1f90f1-8edd-4d48-99fc-7c57b32c1398.png
            iCloud Drive (Archive)
            iCloud Drive (Archive) - 1
            ijava-1.3.0.zip
            install.py
            java
            lib
            nltk_data
            opt
            src
            teambaddieflask
            vscode
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % jupyter kernel speclist
            [KernelApp] Starting kernel 'python3'
            [KernelApp] Connection file: /Users/nikhilchakravarthula/Library/Jupyter/runtime/kernel-449dd7e8-306f-41fc-82e3-68b385e94225.json
            [KernelApp] To connect a client: --existing kernel-449dd7e8-306f-41fc-82e3-68b385e94225.json
            ^C[KernelApp] Shutting down on signal 2
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % java --version
            openjdk 17.0.8 2023-07-18
            OpenJDK Runtime Environment Temurin-17.0.8+7 (build 17.0.8+7)
            OpenJDK 64-Bit Server VM Temurin-17.0.8+7 (build 17.0.8+7, mixed mode, sharing)
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % sudo apt install default0jre
            Password:
            The operation couldn’t be completed. Unable to locate a Java Runtime that supports apt.
            Please visit http://www.java.com for information on installing Java.

            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % ls
            2023ResearchProject
            Ap Comp Sci Principle
            Applications
            DSRP23
            Desktop
            Documents
            Downloads
            Lab4Graph
            Library
            MVQN
            Movies
            Music
            Pictures
            Postman Agent
            Public
            bin
            e7c424fd-d9ac-4ed4-b583-7d06fbd351fa.png
            fc1f90f1-8edd-4d48-99fc-7c57b32c1398.png
            iCloud Drive (Archive)
            iCloud Drive (Archive) - 1
            ijava-1.3.0.zip
            install.py
            java
            lib
            nltk_data
            opt
            src
            teambaddieflask
            vscode
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % df
            Filesystem                                                     512-blocks      Used Available Capacity iused      ifree %iused  Mounted on
            /dev/disk3s1s1                                                  478724992  17698152 250037496     7%  355382 1250187480    0%   /
            devfs                                                                 400       400         0   100%     692          0  100%   /dev
            /dev/disk3s6                                                    478724992   4194352 250037496     2%       2 1250187480    0%   /System/Volumes/VM
            /dev/disk3s2                                                    478724992   9250608 250037496     4%     835 1250187480    0%   /System/Volumes/Preboot
            /dev/disk3s4                                                    478724992     81984 250037496     1%      50 1250187480    0%   /System/Volumes/Update
            /dev/disk1s2                                                      1024000     12328    987904     2%       3    4939520    0%   /System/Volumes/xarts
            /dev/disk1s1                                                      1024000     12648    987904     2%      31    4939520    0%   /System/Volumes/iSCPreboot
            /dev/disk1s3                                                      1024000      1400    987904     1%      39    4939520    0%   /System/Volumes/Hardware
            /dev/disk3s5                                                    478724992 194995296 250037496    44% 1619217 1250187480    0%   /System/Volumes/Data
            /dev/disk3s7                                                    478724992    641872 250037496     1%   57467 1250187480    0%   /nix
            map auto_home                                                           0         0         0   100%       0          0  100%   /System/Volumes/Data/home
            /Users/nikhilchakravarthula/Downloads/Visual Studio Code 2.app  478724992 188678192 256352464    43% 1610736 1281762320    0%   /private/var/folders/2n/s4c2yyjx7wdb5w0336x9ttv00000gn/T/AppTranslocation/0CB01561-0468-4C10-A866-F6336D243B3B
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % java --version
            openjdk 17.0.8 2023-07-18
            OpenJDK Runtime Environment Temurin-17.0.8+7 (build 17.0.8+7)
            OpenJDK 64-Bit Server VM Temurin-17.0.8+7 (build 17.0.8+7, mixed mode, sharing)
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % %%script bash

            fg: no current job
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % cat <<EOF > /tmp/variables.sh
            heredoc> export project_dir=$HOME/vscode
            heredoc> export project=\$project_dir/teacher
            heredoc> export project_repo="https://github.com/nighthawkcoders/teacher.git"
            heredoc> EOF
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % source /tmp/variables.sh
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % echo "Project dir: $project_dir"
            echo "Project: $project"
            echo "Repo: $project_repo"

            Project dir: /Users/nikhilchakravarthula/vscode
            Project: /Users/nikhilchakravarthula/vscode/teacher
            Repo: https://github.com/nighthawkcoders/teacher.git
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % source /tmp/variables.sh
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % echo "Using conditional statement to create a project directory and project"

            Using conditional statement to create a project directory and project
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % cd ~ 
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % if [ ! -d $project_dir ]
            then
                echo "Directory $project_dir does not exists... makinng directory $project_dir"
                mkdir -p $project_dir
            fi
            echo "Directory $project_dir exists."
            Directory /Users/nikhilchakravarthula/vscode exists.
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % if [ ! -d $project ]
            then
                echo "Directory $project does not exists... cloning $project_repo"
                cd $project_dir
                git clone $project_repo
                cd ~
            fi
            echo "Directory $project exists."
            Directory /Users/nikhilchakravarthula/vscode/teacher does not exists... cloning https://github.com/nighthawkcoders/teacher.git
            Cloning into 'teacher'...
            remote: Enumerating objects: 1924, done.
            remote: Counting objects: 100% (492/492), done.
            remote: Compressing objects: 100% (192/192), done.
            remote: Total 1924 (delta 316), reused 468 (delta 300), pack-reused 1432
            Receiving objects: 100% (1924/1924), 8.53 MiB | 13.26 MiB/s, done.
            Resolving deltas: 100% (1231/1231), done.
            Directory /Users/nikhilchakravarthula/vscode/teacher exists.
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 ~ % source /tmp/variables.sh

            echo "Navigate to project, then navigate to area wwhere files were cloned"
            cd $project
            pwd

            echo ""
            echo "list top level or root of files with project pulled from github"
            ls
            Navigate to project, then navigate to area wwhere files were cloned
            /Users/nikhilchakravarthula/vscode/teacher

            list top level or root of files with project pulled from github
            Gemfile		_config.yml	_notebooks	csp.md		indexBlogs.md
            LICENSE		_data		_posts		csse.md		scripts
            Makefile	_includes	assets		images
            README.md	_layouts	csa.md		index.md
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % source /tmp/variables.sh

            echo "Navigate to project, then navigate to area wwhere files were cloned"
            cd $project
            pwd

            echo ""
            echo "list all files in long format"
            ls -al   # all files -a (hidden) in -l long listing
            Navigate to project, then navigate to area wwhere files were cloned
            /Users/nikhilchakravarthula/vscode/teacher

            list all files in long format
            zsh: unknown file attribute: h
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % source /tmp/variables.sh

            echo "Navigate to project, then navigate to area wwhere files were cloned"
            cd $project
            pwd

            echo ""
            echo "list all files in long format"
            ls -al   # all files -a (hidden) in -l long listing
            Navigate to project, then navigate to area wwhere files were cloned
            /Users/nikhilchakravarthula/vscode/teacher

            list all files in long format
            zsh: unknown file attribute: h
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % source /tmp/variables.sh

            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % echo "Navigate to project, then navigate to area wwhere files were cloned"

            Navigate to project, then navigate to area wwhere files were cloned
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % cd $project
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % pwd
            /Users/nikhilchakravarthula/vscode/teacher
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % echo ""
            echo "list all files in long format"
            ls -al   # all files -a (hidden) in -l long listing


            list all files in long format
            zsh: unknown file attribute: h
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % ls -al   # all files -a (hidden) in -l long listing

            zsh: unknown file attribute: h
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % ls 
            Gemfile		_config.yml	_notebooks	csp.md		indexBlogs.md
            LICENSE		_data		_posts		csse.md		scripts
            Makefile	_includes	assets		images
            README.md	_layouts	csa.md		index.md
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % ls -l
            total 96
            -rw-r--r--   1 nikhilchakravarthula  staff   122 Aug 23 12:14 Gemfile
            -rw-r--r--   1 nikhilchakravarthula  staff  1081 Aug 23 12:14 LICENSE
            -rw-r--r--   1 nikhilchakravarthula  staff  3131 Aug 23 12:14 Makefile
            -rw-r--r--   1 nikhilchakravarthula  staff  6853 Aug 23 12:14 README.md
            -rw-r--r--   1 nikhilchakravarthula  staff   607 Aug 23 12:14 _config.yml
            drwxr-xr-x   6 nikhilchakravarthula  staff   192 Aug 23 12:14 _data
            drwxr-xr-x  11 nikhilchakravarthula  staff   352 Aug 23 12:14 _includes
            drwxr-xr-x   6 nikhilchakravarthula  staff   192 Aug 23 12:14 _layouts
            drwxr-xr-x  38 nikhilchakravarthula  staff  1216 Aug 23 12:14 _notebooks
            drwxr-xr-x  12 nikhilchakravarthula  staff   384 Aug 23 12:14 _posts
            drwxr-xr-x   4 nikhilchakravarthula  staff   128 Aug 23 12:14 assets
            -rw-r--r--   1 nikhilchakravarthula  staff    92 Aug 23 12:14 csa.md
            -rw-r--r--   1 nikhilchakravarthula  staff    98 Aug 23 12:14 csp.md
            -rw-r--r--   1 nikhilchakravarthula  staff   108 Aug 23 12:14 csse.md
            drwxr-xr-x  34 nikhilchakravarthula  staff  1088 Aug 23 12:14 images
            -rw-r--r--   1 nikhilchakravarthula  staff  5149 Aug 23 12:14 index.md
            -rw-r--r--   1 nikhilchakravarthula  staff    53 Aug 23 12:14 indexBlogs.md
            drwxr-xr-x   8 nikhilchakravarthula  staff   256 Aug 23 12:14 scripts
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % ls -al
            total 104
            drwxr-xr-x  23 nikhilchakravarthula  staff   736 Aug 23 12:14 .
            drwxr-xr-x  16 nikhilchakravarthula  staff   512 Aug 23 12:14 ..
            drwxr-xr-x  12 nikhilchakravarthula  staff   384 Aug 23 12:14 .git
            drwxr-xr-x   3 nikhilchakravarthula  staff    96 Aug 23 12:14 .github
            -rw-r--r--   1 nikhilchakravarthula  staff   157 Aug 23 12:14 .gitignore
            -rw-r--r--   1 nikhilchakravarthula  staff   122 Aug 23 12:14 Gemfile
            -rw-r--r--   1 nikhilchakravarthula  staff  1081 Aug 23 12:14 LICENSE
            -rw-r--r--   1 nikhilchakravarthula  staff  3131 Aug 23 12:14 Makefile
            -rw-r--r--   1 nikhilchakravarthula  staff  6853 Aug 23 12:14 README.md
            -rw-r--r--   1 nikhilchakravarthula  staff   607 Aug 23 12:14 _config.yml
            drwxr-xr-x   6 nikhilchakravarthula  staff   192 Aug 23 12:14 _data
            drwxr-xr-x  11 nikhilchakravarthula  staff   352 Aug 23 12:14 _includes
            drwxr-xr-x   6 nikhilchakravarthula  staff   192 Aug 23 12:14 _layouts
            drwxr-xr-x  38 nikhilchakravarthula  staff  1216 Aug 23 12:14 _notebooks
            drwxr-xr-x  12 nikhilchakravarthula  staff   384 Aug 23 12:14 _posts
            drwxr-xr-x   4 nikhilchakravarthula  staff   128 Aug 23 12:14 assets
            -rw-r--r--   1 nikhilchakravarthula  staff    92 Aug 23 12:14 csa.md
            -rw-r--r--   1 nikhilchakravarthula  staff    98 Aug 23 12:14 csp.md
            -rw-r--r--   1 nikhilchakravarthula  staff   108 Aug 23 12:14 csse.md
            drwxr-xr-x  34 nikhilchakravarthula  staff  1088 Aug 23 12:14 images
            -rw-r--r--   1 nikhilchakravarthula  staff  5149 Aug 23 12:14 index.md
            -rw-r--r--   1 nikhilchakravarthula  staff    53 Aug 23 12:14 indexBlogs.md
            drwxr-xr-x   8 nikhilchakravarthula  staff   256 Aug 23 12:14 scripts
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % source /tmp/variables.sh
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % export posts=$project/_posts
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % cd $posts
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _posts % pwd
            /Users/nikhilchakravarthula/vscode/teacher/_posts
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _posts % ls -l
            total 176
            -rw-r--r--  1 nikhilchakravarthula  staff   7685 Aug 23 12:14 2023-08-16-Tools_Equipment.md
            -rw-r--r--  1 nikhilchakravarthula  staff   4650 Aug 23 12:14 2023-08-16-pair_programming.md
            -rw-r--r--  1 nikhilchakravarthula  staff   7137 Aug 23 12:14 2023-08-17-markdown-html_fragments.md
            -rw-r--r--  1 nikhilchakravarthula  staff   6659 Aug 23 12:14 2023-08-23-javascript-calculator.md
            -rw-r--r--  1 nikhilchakravarthula  staff  10642 Aug 23 12:14 2023-08-30-agile_methodolgy.md
            -rw-r--r--  1 nikhilchakravarthula  staff   3849 Aug 23 12:14 2023-08-30-javascript-music-api.md
            -rw-r--r--  1 nikhilchakravarthula  staff   5312 Aug 23 12:14 2023-09-06-javascript-motion-mario-oop.md
            -rw-r--r--  1 nikhilchakravarthula  staff   4812 Aug 23 12:14 2023-09-13-java-free_response.md
            -rw-r--r--  1 nikhilchakravarthula  staff  13220 Aug 23 12:14 2023-10-16-java-api-pojo-jpa.md
            -rw-r--r--  1 nikhilchakravarthula  staff   6819 Aug 23 12:14 2023-11-13-jwt-java-spring.md
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _posts % source /tmp/variables.sh
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _posts % export notebooks=$project/_notebooks
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _posts % cd $notebooks
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % pwd
            /Users/nikhilchakravarthula/vscode/teacher/_notebooks
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % ls -l
            total 1472
            -rw-r--r--  1 nikhilchakravarthula  staff   13014 Aug 23 12:14 2023-08-01-cloud_database.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    8992 Aug 23 12:14 2023-08-01-mario_player.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   43705 Aug 23 12:14 2023-08-02-cloud-workspace-automation.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   22060 Aug 23 12:14 2023-08-03-mario_block.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11791 Aug 23 12:14 2023-08-03-mario_platform.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   19450 Aug 23 12:14 2023-08-03-mario_tube.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   24387 Aug 23 12:14 2023-08-04-mario_background.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    3496 Aug 23 12:14 2023-08-07-mario_lesson.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   10110 Aug 23 12:14 2023-08-15-java-hello.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   25656 Aug 23 12:14 2023-08-16-github_pages_setup.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   16156 Aug 23 12:14 2023-08-16-linux_shell.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11466 Aug 23 12:14 2023-08-16-python_hello.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9425 Aug 23 12:14 2023-08-23-github_pages_anatomy.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   22674 Aug 23 12:14 2023-08-23-java-console_games.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9038 Aug 23 12:14 2023-08-23-python_tricks.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   10152 Aug 23 12:14 2023-08-30-javascript_top_10.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9689 Aug 23 12:14 2023-08-30-showcase-S1-pair.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    7192 Aug 23 12:14 2023-09-05-python-flask-anatomy.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   22157 Aug 23 12:14 2023-09-06-AWS-deployment.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   14380 Aug 23 12:14 2023-09-06-java-primitives.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11671 Aug 23 12:14 2023-09-06-javascript-input.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   13706 Aug 23 12:14 2023-09-12-java_menu_class.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9562 Aug 23 12:14 2023-09-13-java_fibonaccii_class.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   44217 Aug 23 12:14 2023-09-13-javascript_output.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   43423 Aug 23 12:14 2023-09-13-python-pandas_intro.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11578 Aug 23 12:14 2023-09-20-java-image_2D.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   26739 Aug 23 12:14 2023-09-20-javascript_motion_dog.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   13599 Aug 23 12:14 2023-10-02-java-spring-anatomy.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   12429 Aug 23 12:14 2023-10-09-java-chatgpt.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   15632 Aug 23 12:14 2023-10-09-javascript_api.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff  113091 Aug 23 12:14 2023-10-09-python_machine_learing_fitness.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   16271 Aug 23 12:14 2023-11-13-jwt-python-flask.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   15951 Aug 23 12:14 2023-11-13-vulnerabilities.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   18328 Aug 23 12:14 2023-11-20-jwt-java-spring-challenge.md
            -rw-r--r--  1 nikhilchakravarthula  staff   10745 Aug 23 12:14 2024-01-04-cockpit-setup.ipynb
            drwxr-xr-x  3 nikhilchakravarthula  staff      96 Aug 23 12:14 files
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % source /tmp/variables.sh
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % cd $notebooks/images
            cd: no such file or directory: /Users/nikhilchakravarthula/vscode/teacher/_notebooks/images
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % pwd
            /Users/nikhilchakravarthula/vscode/teacher/_notebooks
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % ls -l
            total 1472
            -rw-r--r--  1 nikhilchakravarthula  staff   13014 Aug 23 12:14 2023-08-01-cloud_database.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    8992 Aug 23 12:14 2023-08-01-mario_player.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   43705 Aug 23 12:14 2023-08-02-cloud-workspace-automation.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   22060 Aug 23 12:14 2023-08-03-mario_block.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11791 Aug 23 12:14 2023-08-03-mario_platform.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   19450 Aug 23 12:14 2023-08-03-mario_tube.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   24387 Aug 23 12:14 2023-08-04-mario_background.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    3496 Aug 23 12:14 2023-08-07-mario_lesson.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   10110 Aug 23 12:14 2023-08-15-java-hello.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   25656 Aug 23 12:14 2023-08-16-github_pages_setup.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   16156 Aug 23 12:14 2023-08-16-linux_shell.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11466 Aug 23 12:14 2023-08-16-python_hello.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9425 Aug 23 12:14 2023-08-23-github_pages_anatomy.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   22674 Aug 23 12:14 2023-08-23-java-console_games.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9038 Aug 23 12:14 2023-08-23-python_tricks.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   10152 Aug 23 12:14 2023-08-30-javascript_top_10.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9689 Aug 23 12:14 2023-08-30-showcase-S1-pair.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    7192 Aug 23 12:14 2023-09-05-python-flask-anatomy.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   22157 Aug 23 12:14 2023-09-06-AWS-deployment.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   14380 Aug 23 12:14 2023-09-06-java-primitives.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11671 Aug 23 12:14 2023-09-06-javascript-input.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   13706 Aug 23 12:14 2023-09-12-java_menu_class.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff    9562 Aug 23 12:14 2023-09-13-java_fibonaccii_class.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   44217 Aug 23 12:14 2023-09-13-javascript_output.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   43423 Aug 23 12:14 2023-09-13-python-pandas_intro.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   11578 Aug 23 12:14 2023-09-20-java-image_2D.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   26739 Aug 23 12:14 2023-09-20-javascript_motion_dog.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   13599 Aug 23 12:14 2023-10-02-java-spring-anatomy.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   12429 Aug 23 12:14 2023-10-09-java-chatgpt.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   15632 Aug 23 12:14 2023-10-09-javascript_api.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff  113091 Aug 23 12:14 2023-10-09-python_machine_learing_fitness.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   16271 Aug 23 12:14 2023-11-13-jwt-python-flask.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   15951 Aug 23 12:14 2023-11-13-vulnerabilities.ipynb
            -rw-r--r--  1 nikhilchakravarthula  staff   18328 Aug 23 12:14 2023-11-20-jwt-java-spring-challenge.md
            -rw-r--r--  1 nikhilchakravarthula  staff   10745 Aug 23 12:14 2024-01-04-cockpit-setup.ipynb
            drwxr-xr-x  3 nikhilchakravarthula  staff      96 Aug 23 12:14 files
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % source /tmp/variables.sh
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 _notebooks % cd $project
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % echo "show the contents of README.md"
            echo ""
            show the contents of README.md

            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % cat README.md
            ## Teacher Blog site
            This site is intended for the development of Teacher content.  This blogging site is built using GitHub Pages [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).
            - The purpose is to build lessons and distribute across different Computer Science sections (CSSE, CSP, CSA), a pathway that covers 3 years of High School Instruction.
            - The primary languages and frameworks that are taught are `JavaScript/HTML/CSS`, `Python/Flask`, `Java/Spring`.  Read below for more details.
            - In this course, Teacher content is not exclusively developed by Teachers.  In fact, many Students have been invited to develop and publish content into this repository.  Their names will appear as authors on the content which they aided in producing.
            - This site has incorporated ideas and has radically modified scripts from the now deprecated [fastpages](https://github.com/fastai/fastpages) repository.
            - This site includes assistance and guideance from ChatGPT, [chat.openai.com](https://chat.openai.com/) 

            ### Courses and Pathway
            The focus of the Del Norte Computer Science three-year pathway is `Full Stack Web Development`.  This focus provides a variety of technologies and exposures.  The intention of the pathway is breadth and exposure.
            - `JavaScript` documents are focused on frontend development and for entry class into the Del Norte Computer Science pathway.  JavaScript documents and materials are a prerequisites to Python and Java classes.
            - `Python` documents are focused on backend development and requirements for the AP Computer Science Principles exam.
            - `Java` documents are focused on backend development and requirements for the AP Computer Sciene A exam.
            - `Data Structures` materials embedded into JavaScript, Python, or Java documents are focused on college course articulation.

            ### Resources and Instruction
            The materials, such as this README, as well as `Tools`, `DevOps`, and `Collaboration` resources are integral part of this course and Computer Science in general.  Everything in our environment is part of our learning of Computer Science. 
            - `Visual Studio Code` is key the code-build-debug cycle editor used in this course, [VSCode download](https://code.visualstudio.com/).  This is an example of a resource, but inside of it it has features for collaboration.
            - `Tech Talks`, aka lectures, are intended to be interactive and utilize `Jupyter Notebooks` and Websites.  This is an example of blending instruction and tools together, which in turn provide additional resources for learning.  For instance, deep knowledge on  GitHub Pages and Notebooks are valuable in understanding principles behind Full Stack Development and Data Science. 

            ## GitHub Pages
            All `GitHub Pages` websites are managed on GitHub infrastructure. GitHub uses `Jekyll` to tranform your content into static websites and blogs. Each time we change files in GitHub it initiates a GitHub Action that rebuilds and publishes the site with Jekyll.  
            - GitHub Pages is powered by: [Jekyll](https://jekyllrb.com/).
            - Publised teacher website: [nighthawkcoders.github.io/teacher](https://nighthawkcoders.github.io/teacher/)

            ## Preparing a Preview Site 
            In all development, it is recommended to test your code before deployment.  The GitHub Pages development process is optimized by testing your development on your local machine, prior to files on GitHub

            Development Cycle. For GitHub pages, the tooling described below will create a development cycle  `make-code-save-preview`.  In the development cycle, it is a requirement to preview work locally, prior to doing a VSCode `commit` to git.

            Deployment Cycle.  In the deplopyment cycle, `sync-github-action-review`, it is a requirement to complete the development cycle prior to doing a VSCode `sync`.  The sync triggers github repository update.  The action starts the jekyll build to publish the website.  Any step can have errors and will require you to do a review.

            ### WSL and/or Ubuntu installation requirements
            - The result of these step is Ubuntu tools to run preview server.  These procedures were created using [jekyllrb.com](https://jekyllrb.com/docs/installation/ubuntu/)
            ```bash
            # 
            # WSL/Ubuntu setup
            #
            mkdir mkdir vscode
            git clone https://github.com/nighthawkcoders/teacher.git
            # run script, path vscode/teacher are baked in script
            ~/vscode/teacher/scripts/activate_ubuntu.sh
            #=== !!!Start a new Terminal!!! ===
            #=== Continue to next section ===
            ```

            ### MacOs installation requirements 
            - Ihe result of these step are MacOS tools to run preview server.  These procedures were created using [jekyllrb.com](https://jekyllrb.com/docs/installation/macos/). 

            ```bash
            # 
            # MacOS setup
            #
            mkdir mkdir vscode
            git clone https://github.com/nighthawkcoders/teacher.git
            # run script, path vscode/teacher are baked in script
            ~/vscode/teacher/scripts/activate_macos.sh
            #=== !!!Start a new Terminal!!! ===
            #=== Continue to next section ===
            ```


            ### Run Preview Server
            - The result of these step is server running on: http://0.0.0.0:4100/teacher/.  Regeneration messages will run in terminal on any save and update site upon refresh.  Terminal is active, press the Enter or Return key in the terminal at any time to see prompt to enter commands.

            - Complete installation
            ```bash
            cd ~/vscode/teacher
            bundle install
            make
            ```
            - Run Server.  This requires running terminal commands `make`, `make stop`, `make clean`, or `make convert` to manage the running server.  Logging of details will appear in terminal.   A `Makefile` has been created in project to support commands and start processes.

                - Start preview server in terminal
                ```bash
                cd ~/vscode/teacher  # my project location, adapt as necessary
                make
                ```

                - Terminal output of shows server address. Cmd or Ctl click http location to open preview server in browser. Example Server address message... 
                ```
                Server address: http://0.0.0.0:4100/teacher/
                ```

                - Save on ipynb or md activiates "regeneration". Refresh browser to see updates. Example terminal message...
                ```
                Regenerating: 1 file(s) changed at 2023-07-31 06:54:32
                    _notebooks/2024-01-04-cockpit-setup.ipynb
                ```

                - Terminal message are generated from background processes.  Click return or enter to obtain prompt and use terminal as needed for other tasks.  Alway return to root of project `cd ~/vscode/teacher` for all "make" actions. 
                    

                - Stop preview server, but leave constructed files in project for your review.
                ```bash
                make stop
                ```

                - Stop server and "clean" constructed files, best choice when renaming files to eliminate potential duplicates in constructed files.
                ```bash
                make clean
                ```

                - Test notebook conversions, best choice to see if IPYNB conversion is acting up.
                ```bash
                make convert
                ```
                %                                                                           (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % echo ""
            echo "end of README.md"

            end of README.md
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % echo "Show the shell environment variables, key on left of equal value on right"
            echo ""
            Show the shell environment variables, key on left of equal value on right

            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % env
            __CFBundleIdentifier=com.apple.Terminal
            TMPDIR=/var/folders/2n/s4c2yyjx7wdb5w0336x9ttv00000gn/T/
            XPC_FLAGS=0x0
            TERM=xterm-256color
            SSH_AUTH_SOCK=/private/tmp/com.apple.launchd.JhXCQqzmzc/Listeners
            XPC_SERVICE_NAME=0
            TERM_PROGRAM=Apple_Terminal
            TERM_PROGRAM_VERSION=447
            TERM_SESSION_ID=EF364C41-B9B6-4565-BC3D-D01F68736944
            SHELL=/bin/zsh
            HOME=/Users/nikhilchakravarthula
            LOGNAME=nikhilchakravarthula
            USER=nikhilchakravarthula
            PATH=/Users/nikhilchakravarthula/opt/anaconda3/bin:/Users/nikhilchakravarthula/opt/anaconda3/condabin:/opt/local/bin:/opt/local/sbin:/opt/homebrew/bin:/opt/homebrew/sbin:/Library/Frameworks/Python.framework/Versions/2.7/bin:/Library/Frameworks/Python.framework/Versions/3.10/bin:/usr/local/bin:/System/Cryptexes/App/usr/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Library/Apple/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin
            SHLVL=1
            PWD=/Users/nikhilchakravarthula/vscode/teacher
            OLDPWD=/Users/nikhilchakravarthula/vscode/teacher/_notebooks
            HOMEBREW_PREFIX=/opt/homebrew
            HOMEBREW_CELLAR=/opt/homebrew/Cellar
            HOMEBREW_REPOSITORY=/opt/homebrew
            MANPATH=/opt/local/share/man:/opt/homebrew/share/man::
            INFOPATH=/opt/homebrew/share/info:
            CONDA_EXE=/Users/nikhilchakravarthula/opt/anaconda3/bin/conda
            _CE_M=
            _CE_CONDA=
            CONDA_PYTHON_EXE=/Users/nikhilchakravarthula/opt/anaconda3/bin/python
            CONDA_SHLVL=1
            CONDA_PREFIX=/Users/nikhilchakravarthula/opt/anaconda3
            CONDA_DEFAULT_ENV=base
            CONDA_PROMPT_MODIFIER=(base) 
            project_dir=/Users/nikhilchakravarthula/vscode
            project=/Users/nikhilchakravarthula/vscode/teacher
            project_repo=https://github.com/nighthawkcoders/teacher.git
            posts=/Users/nikhilchakravarthula/vscode/teacher/_posts
            notebooks=/Users/nikhilchakravarthula/vscode/teacher/_notebooks
            LANG=en_US.UTF-8
            _=/usr/bin/env
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % source /tmp/variables.sh
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % cd $project
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % echo ""
            echo "show the secrets of .git"

            show the secrets of .git
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 teacher % cd .git
            ls -l
            total 56
            -rw-r--r--   1 nikhilchakravarthula  staff     21 Aug 23 12:14 HEAD
            -rw-r--r--   1 nikhilchakravarthula  staff    312 Aug 23 12:14 config
            -rw-r--r--   1 nikhilchakravarthula  staff     73 Aug 23 12:14 description
            drwxr-xr-x  15 nikhilchakravarthula  staff    480 Aug 23 12:14 hooks
            -rw-r--r--   1 nikhilchakravarthula  staff  11702 Aug 23 12:14 index
            drwxr-xr-x   3 nikhilchakravarthula  staff     96 Aug 23 12:14 info
            drwxr-xr-x   4 nikhilchakravarthula  staff    128 Aug 23 12:14 logs
            drwxr-xr-x   4 nikhilchakravarthula  staff    128 Aug 23 12:14 objects
            -rw-r--r--   1 nikhilchakravarthula  staff    112 Aug 23 12:14 packed-refs
            drwxr-xr-x   5 nikhilchakravarthula  staff    160 Aug 23 12:14 refs
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 .git % echo ""
            echo "look at config file"

            look at config file
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 .git % cat config
            [core]
                repositoryformatversion = 0
                filemode = true
                bare = false
                logallrefupdates = true
                ignorecase = true
                precomposeunicode = true
            [remote "origin"]
                url = https://github.com/nighthawkcoders/teacher.git
                fetch = +refs/heads/*:refs/remotes/origin/*
            [branch "main"]
                remote = origin
                merge = refs/heads/main
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 .git % cd /tmp
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % file="sample.md"
            if [ -f "$file" ]; then
                rm $file
            fi

            tee -a $file >/dev/null <<EOF
            heredoc> EOF
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % echo "- This bulleted element and lines below are generated using echo with standard output (>>) redirection operator." >> $file
            echo "- The list definition, as is, is using space to seperate lines.  Thus the use of commas and hyphens in output." >> $file
            actions=("ls,list-directory" "cd,change-directory" "pwd,present-working-directory" "if-then-fi,test-condition" "env,bash-environment-variables" "cat,view-file-contents" "tee,write-to-output" "echo,display-content-of-string" "echo_text_>\$file,write-content-to-file" "echo_text_>>\$file,append-content-to-file")
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % for action in ${actions[@]}; do  # for loop is very similar to other language, though [@], semi-colon, do are new
            action=${action//-/ }  # convert dash to space
            action=${action//,/: } # convert comma to colon
            action=${action//_text_/ \"sample text\" } # convert _text_ to sample text, note escape character \ to avoid "" having meaning
            echo "    - ${action//-/ }" >> $file  # echo is redirected to file with >>
            done
            zsh: parse error near `\n'
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % echo "- This bulleted element and lines below are generated using echo with standard output (>>) redirection operator." >> $file
            echo "- The list definition, as is, is using space to seperate lines.  Thus the use of commas and hyphens in output." >> $file
            actions=("ls,list-directory" "cd,change-directory" "pwd,present-working-directory" "if-then-fi,test-condition" "env,bash-environment-variables" "cat,view-file-contents" "tee,write-to-output" "echo,display-content-of-string" "echo_text_>\$file,write-content-to-file" "echo_text_>>\$file,append-content-to-file")
            for action in ${actions[@]}; do  # for loop is very similar to other language, though [@], semi-colon, do are new
            action=${action//-/ }  # convert dash to space
            action=${action//,/: } # convert comma to colon
            action=${action//_text_/ \"sample text\" } # convert _text_ to sample text, note escape character \ to avoid "" having meaning
            echo "    - ${action//-/ }" >> $file  # echo is redirected to file with >>
            done
            zsh: parse error near `\n'
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % for action in ${actions[@]}; doaction=${action//-/ }action=${action//,/: }action=${action//_text_/ \echo "    - ${action//-/ }"
            for braceparam> done
            for braceparam> 
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % for action in ${actions[@]}; do
            for> action=${action//-/ }
            for> action=${action//,/: }
            for> action=${action//_text_/ \
            for braceparam> echo "    - ${action//-/ }"
            for braceparam> echo "    - ${action//-/ }" >> $file
            for braceparam> ls
            for braceparam> çç
            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % actions=("ls,list-directory" "cd,change-directory" "pwd,present-working-directory" "if-then-fi,test-condition" "env,bash-environment-variables" "cat,view-file-contents" "tee,write-to-output" "echo,display-content-of-string" "echo_text_>\$file,write-content-to-file" "echo_text_>>\$file,append-content-to-file")

            (base) nikhilchakravarthula@Nikhils-MacBook-Air-2 /tmp % for action in ${actions[@]}; do
            for> action=${action//-/ }
            for> action=${action//,/: }
            for> action=${action//_text_/ \
            for braceparam> ls -l $file
            for braceparam> echo ""
            echo "File listing and status"
            ls -l $file # list file
            wc $file   # show words
            mdless $file  # this requires installation, but renders markown from terminal

            rm $file  # clean up termporary file
            for braceparam> ls -l $file
            for braceparam> wc $file
            for braceparam> mdless $file
            for braceparam> rm 
            for braceparam> 
        </p>
    </body>
</html>