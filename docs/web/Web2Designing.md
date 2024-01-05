
<h1 style="text-align:center; font-size:2vw" >How to Build Website</h1>

(All the screenshot's are taken from installed software's from mac OS, so if you are using windows OS may be you will not able to find the exact button or option as showed in these screenshots. No worries, just look around your software's interface you will find it )

<h3>Steps of building -</h3>

STEP-1 : Installing all the necessary tools.<br>
STEP-2 : Open repository into <a href="https://github.com/">GitHub.</a><br>
STEP-3 : Publish the page from <a href="https://github.com/">GitHub.</a><br>
STEP-4 : Clone the repository into <a href="https://desktop.github.com/">GitHub Desktop.</a><br>
STEP-5 : Open the repository into <a href="https://code.visualstudio.com/">Visual Studio Code</a> and write the code.<br>
STEP-6 : Install Docsify from terminal.<br>
STEP-7 : Code writing.<br>
STEP-8 : Push all the changes into origin.<br>

### STEP-1 : Installing all the necessary tools<br>
  - <a href="https://github.com/">GitHub</a> as a host of the webpage.
  - <a href="https://desktop.github.com/">GitHub Desktop</a> to push the code from local to origin.
  - <a href="https://code.visualstudio.com/">Visual Studio Code</a> to write code and document.
  - <a href="https://nodejs.org/en">Nodejs</a> to build the environment.
  - <a href="https://www.nexmaker.com/doc/1projectmanage/markdown.html">Markdown</a> language to write the document.

### STEP-2 : Open repository into <a href="https://github.com/"> GitHub</a>
>First need to open an account on <a href="https://github.com/"> GitHub</a>.To create repository click New from home page.After that set the name,keep it public and add a readme file and then click create repository(follow the picture's where is surrounded by yellow circle for your better understand)


<img src="img/tm_logo/github_repositoryopen/githubnewbutton.png">
<br>

> Here, we use the repository name as "delete" to make this documentary.So don't be confuse.Repository name can be anything.
.
.
<img src="img/tm_logo/github_repositoryopen/createrepository.png">

### STEP-3 : Publish the page from <a href="https://github.com/"> GitHub</a>
>To publish the page,go to repository setting and select page from code and automation, then select main from the branch and select root from the folder.Late when docs will be installed folded,need to select doc/ from the folder and then click save.(follow pictures)
After this a link will be created which is our webpage link. For now the link page will be blank because we havn't written and pushed our code.

<img src="img/tm_logo/github_repositoryopen/sett_page.png"><br>


<img src="img/tm_logo/github_repositoryopen/page_save.png">

### STEP-4 : Clone the repository into <a href="https://desktop.github.com/"> GitHub Desktop</a>

>To clone the repoc open <a href="https://desktop.github.com/"> GitHub Desktop</a>. Find the option "Clone a repository" and search the repository created on <a href="https://github.com/"> GitHub</a> web and click Clone, Now the repository has been cloned.(follow pictures)
<br>
<img src="img/tm_logo/github_repositoryopen/clone_1.png">

<img src="img/tm_logo/github_repositoryopen/clone_2.png">

### STEP-5 : Open the repository into <a href="https://code.visualstudio.com/"> Visual Studio Code</a> and write the code

>To open the repository into VScode from github desktop click "Open in visual studio code". 
<img src="img/tm_logo/github_repositoryopen/open in_vs.png">

>Now the repositroy has opened in VScode.<br>
<br>
<img src="img/tm_logo/github_repositoryopen/vs_1.png">

### STEP-6 : Open terminal and Install docsify

>Now we need to open the temrinal because we are going to install docsify inside terminal with command.

- ### Open Terminal

>To open terminal look at navigation and click terminal and select new terminal then the terminal will open for the selected vs code folder. Here the terminal open for our folder called "DELETE" (see the picture below)

<img src="img/tm_logo/github_repositoryopen/terminal_open.png">

- ### Install docsify
To install docsify give the following command in terminal
> npm i docsify-cli -g
<img src="img/tm_logo/github_repositoryopen/terminalopen_vs.png">

after giving this command docsify should be install in your system, if not please click <a href="https://www.npmjs.com/package/docsify-build-cli?activeTab=readme"> docsify problem</a>.<br>

Now to create the doc folder give the following command in terminal
> docsify init ./docs
<img src="img/tm_logo/github_repositoryopen/doc_open.png">

- ### Add navigation bar and side bar 

>To add the navigation bar and side bar need to give the "loadsidebar" and "loadnavbar" true into script named "window.$docsify" inside main html file and then create _navbar.md and _sidebar.md file under docs and edit it as your need. (see code below)

~~~
      window.$docsify = {
      
      name: 'Content',
      loadSidebar: true,  //prepare for sidebar
      loadNavbar: true,   //prepare for navbar
      }
~~~  

_navbar.md 

~~~
- [Home]()
- [About US](AboutUs/TeamIntro.md)
~~~

<br>

_sidebar.md 
~~~
    <!-- docs/_sidebar.md -->
    - **1. Project Management**
      - [1. Website](web/Web2Designing.md)
      - [2. CAD design](cad/cad.md)
      - [3. 3D Printing](3dprinting/3dprinting.md)
      - [4. Laser Cutting](lasercutting/lasercut.md)
      - [5. Arduino](arduino/arduino.md)
      - [6. Interface application programming](processing/processing.md)

    - Final Project
      - [Final project](FinalProject/FinalProject.md) 
      
    - [About US](AboutUs/TeamIntro.md)
~~~

<br>


### STEP-7 Code writing 

In this section we explained how the write the document file and add upload picture and explain the html file.
- ### Document writing
>To write the document file just need to open .md file inside docs and edit it, for our team repository the document file for our this page (web2Designing.md) looks like as the code below - (This code is taken from our main team repository "2023ZJUDEM-7DE")

~~~
<h1 style="text-align:center; font-size:2vw" >How to Build Website</h1>

(All the screenshot's are taken from installed software's from mac OS, so if you are using windows OS may be you will not able to find the exact button or option as showed in these screenshots. No worries, just look around your software's interface you will find it )

<h3>Steps of building -</h3>

STEP-1 : Installing all the necessary tools.<br>
STEP-2 : Open repository into <a href="https://github.com/">GitHub.</a><br>
STEP-3 : Publish the page from <a href="https://github.com/">GitHub.</a><br>
STEP-4 : Clone the repository into <a href="https://desktop.github.com/">GitHub Desktop.</a><br>
STEP-5 : Open the repository into <a href="https://code.visualstudio.com/">Visual Studio Code</a> and write the code.<br>
STEP-6 : Install Docsify from terminal.<br>
STEP-7 : Code writing.<br>
STEP-8 : Push all the changes into origin.<br>

### STEP-1 : Installing all the necessary tools<br>
  - <a href="https://github.com/">GitHub</a> as a host of the webpage.
  - <a href="https://desktop.github.com/">GitHub Desktop</a> to push the code from local to origin.
  - <a href="https://code.visualstudio.com/">Visual Studio Code</a> to write code and document.
  - <a href="https://nodejs.org/en">Nodejs</a> to build the environment.
  - <a href="https://www.nexmaker.com/doc/1projectmanage/markdown.html">Markdown</a> language to write the document.

### STEP-2 : Open repository into <a href="https://github.com/"> GitHub</a>
>First need to open an account on <a href="https://github.com/"> GitHub</a>.To create repository click New from home page.After that set the name,keep it public and add a readme file and then click create repository(follow the picture's where is surrounded by yellow circle for your better understand)


<img src="img/tm_logo/github_repositoryopen/githubnewbutton.png">
<br>

> Here, we use the repository name as "delete" to make this documentary.So don't be confuse.Repository name can be anything.
.
.
<img src="img/tm_logo/github_repositoryopen/createrepository.png">

### STEP-3 : Publish the page from <a href="https://github.com/"> GitHub</a>
>To publish the page,go to repository setting and select page from code and automation, then select main from the branch and select root from the folder.Late when docs will be installed folded,need to select doc/ from the folder and then click save.(follow pictures)
After this a link will be created which is our webpage link. For now the link page will be blank because we havn't written and pushed our code.

<img src="img/tm_logo/github_repositoryopen/sett_page.png"><br>


<img src="img/tm_logo/github_repositoryopen/page_save.png">

### STEP-4 : Clone the repository into <a href="https://desktop.github.com/"> GitHub Desktop</a>

>To clone the repoc open <a href="https://desktop.github.com/"> GitHub Desktop</a>. Find the option "Clone a repository" and search the repository created on <a href="https://github.com/"> GitHub</a> web and click Clone, Now the repository has been cloned.(follow pictures)
<br>
<img src="img/tm_logo/github_repositoryopen/clone_1.png">

<img src="img/tm_logo/github_repositoryopen/clone_2.png">

### STEP-5 : Open the repository into <a href="https://code.visualstudio.com/"> Visual Studio Code</a> and write the code

>To open the repository into VScode from github desktop click "Open in visual studio code". 
<img src="img/tm_logo/github_repositoryopen/open in_vs.png">

>Now the repositroy has opened in VScode.<br>
<br>
<img src="img/tm_logo/github_repositoryopen/vs_1.png">

### STEP-6 : Open terminal and Install docsify

>Now we need to open the temrinal because we are going to install docsify inside terminal with command.

- ### Open Terminal

>To open terminal look at navigation and click terminal and select new terminal then the terminal will open for the selected vs code folder. Here the terminal open for our folder called "DELETE" (see the picture below)

<img src="img/tm_logo/github_repositoryopen/terminal_open.png">

- ### Install docsify
To install docsify give the following command in terminal
> npm i docsify-cli -g
<img src="img/tm_logo/github_repositoryopen/terminalopen_vs.png">

after giving this command docsify should be install in your system, if not please click <a href="https://www.npmjs.com/package/docsify-build-cli?activeTab=readme"> docsify problem</a>.<br>

Now to create the doc folder give the following command in terminal
> docsify init ./docs
<img src="img/tm_logo/github_repositoryopen/doc_open.png">

- ### Add navigation bar and side bar 

>To add the navigation bar and side bar need to give the "loadsidebar" and "loadnavbar" true into script named "window.$docsify" inside main html file and then create _navbar.md and _sidebar.md file under docs and edit it as your need. (see code below)

<pre>
  <code>
      window.$docsify = {
      
      name: 'Content',
      loadSidebar: true,  //prepare for sidebar
      loadNavbar: true,   //prepare for navbar
      }
  </code>
</pre>    

_navbar.md 
<pre>
<code>
- [Home]()
- [About US](AboutUs/TeamIntro.md)
</code>
</pre>
<br>

_sidebar.md 
<pre>
<code>
- **1. Project Management**
   - [1. Website](web/Web2Designing.md)
   - [2. Autodesk](cad/cad.md)

- Final Project
  - [Final project](FinalProject/FinalProject.md) 
  
- [About US](AboutUs/TeamIntro.md)
</code>
</pre>
<br>


### STEP-7 Code writing 

In this section we explained how the write the document file and add upload picture and explain the html file.
- ### Document writing
>To write the document file just need to open .md file inside docs and edit it, for our team repository the document file for our this page (web2Designing.md) looks like as the code below - (This code is taken from our main team repository "2023ZJUDEM-7DE")

(This Code)

- ### Add image
> To add image we stored all the images in a folder inside doc file and linked it with picture's path where needed. we use the normal html command to add image. 
<img src="img/tm_logo/github_repositoryopen/addimg.png">

- ### HTML file setting

HTML file details. (html file can be edit as your need) 
 > - In this html file there are some linked css file to design webpage
 > - Some content inside body section
 > - Load homepage, navigation and side bar.
 > - There are some links and script to design our document file and add code in document.
 <br>
 <br>
 <img src="img/tm_logo/github_repositoryopen/html.png">



### STEP-8 : Push all the changes into origin.

>To push the code in origin need to save the code and open GitHub Desktop and give a commit change comment and click "commit to main" and then click push origin.(follow the pictures)
<img src="img/tm_logo/github_repositoryopen/push_1.png">

<img src="img/tm_logo/github_repositoryopen/push_2.png">

> Here we use the repository name as "delete" so we didn't edited code in this repository. We have edited our code in our team repository.After push to origin all our code has updated in our github repository.Here is the picture.
.
<img src="img/tm_logo/github_repositoryopen/after_push.png">

### Final publish

Follow the step 3. As the docs folder created, now to publish the page open the repository and as follow

> setting > page > under page select the main branch and slect docs from the folder and save it and then the web page link will be available..

Picture -
<img src="img/tm_logo/github_repositoryopen/final_publish.png">

~~~

- ### Add image
> To add image we stored all the images in a folder inside doc file and linked it with picture's path where needed. we use the normal html command to add image. 
~~~
  <img src="image path">
~~~

- ### HTML file setting

HTML file details. (html file can be edit as your need) 
 > - In this html file there are some linked css file to design webpage
 > - Some content inside body section
 > - Load homepage, navigation and side bar.
 > - There are some links and script to design our document file and add code in document.
 <br>
 <br>

 ~~~
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Delete page</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="description" content="Description">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0">
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@4/lib/themes/vue.css">
</head>
<body>
  <div id="app">
    <h1>Welcome to My Website</h1>
    <p>This is a simple example of adding content to your HTML page.</p>
  </div>
  <script>
    window.$docsify = {
      name: '',
      repo: '',
      homepage: 'home.md',
      loadNavbar: true, // Enable the navbar
      loadSidebar: true, // Enable the sidebar
    }
  </script>
  <!-- Docsify v4 -->
  <script src="//cdn.jsdelivr.net/npm/docsify@4"></script>
</body>
</html>
 ~~~



### STEP-8 : Push all the changes into origin.

>To push the code in origin need to save the code and open GitHub Desktop and give a commit change comment and click "commit to main" and then click push origin.(follow the pictures)
<img src="img/tm_logo/github_repositoryopen/push_1.png">

<img src="img/tm_logo/github_repositoryopen/push_2.png">

> Here we use the repository name as "delete" so we didn't edited code in this repository. We have edited our code in our team repository.After push to origin all our code has updated in our github repository.Here is the picture.
.
<img src="img/tm_logo/github_repositoryopen/after_push.png">

### Final publish

Follow the step 3. As the docs folder created, now to publish the page open the repository and as follow

> setting > page > under page select the main branch and slect docs from the folder and save it and then the web page link will be available..

Picture -
<img src="img/tm_logo/github_repositoryopen/final_publish.png">

<hr>
<hr>

<h1 style="text-align:center; font-size:2vw" >How to collaborate with team</h1>
 (Here we describe the team collaboration way after build our website, so the picture used here are taken from our team repository. Do not be confused about repository name, when you are working with your team always remember you have use your team repository, just follow the steps)
 <br>
 <br>
Team collaboration is very very important for this course because course work is huge and you will be tired.If the team can collaborate with each other this course will be fun and easy and you can enjoy your holiday.

### Team Collaborations
<br>
As the students are from different backgrounds, so collaborating with a diverse team of individuals from different backgrounds on GitHub can be a rewarding experience. It allows for the pooling of various skills and perspectives to create better and foster a more inclusive and productive environment. Here's a step-by-step guide on how to collaborate using GitHub when team members come from different backgrounds:
<br>
<br>

STEP 1 : Open the repository.
<br>
<br>
<img src="img/collab/collab_01.png">
<br>
<br>
STEP 2 : Go to setting > Collaborators and teams > and click Add people from the manage access section
<br>
<br>
<img src="img/collab/collab_1.png">
<img src="img/collab/collab_03.png">
<br>
<br>
STEP 3 : Search for member by their name or email address
<br>
<br>
<img src="img/collab/collab_04.png">
<br>
<br>
STEP 4 : Select the member and choose the  role and Add
<br>
<br>
<img src="img/collab/collab_05.png">
<br>
<br>
Now the member name is in the Collaborators and teams list.
<br>
<br>
<img src="img/collab/collab_06.png">

Roles could be change by the team requirements :
Here the newly added member set a maintain role and another member as a write role.
<br>
<br>
<img src="img/collab/collab_07.jpg">
<br>
<br>
Like this way there 5 kinds of roles in github to maintain project :

1.Read - Can read and clone this repository. Can also open and comment on issues and pull requests.<br><br>
2.Triage - Can read and clone this repository. Can also manage issues and pull requests.<br><br>
3.Write - Can read, clone, and push to this repository. Can also manage issues and pull requests.<br><br>
4.Maintain - Can read, clone, and push to this repository. They can also manage issues, pull requests, and some repository settings.<br><br>
5.Admin - Can read, clone, and push to this repository. Can also manage issues, pull requests, and repository settings, including adding collaborators.<br><br>



