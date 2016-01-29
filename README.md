

## Github Workshop

The goal of this workshop is to add the code that we created in the last lab to [Github](https://github.com/). We use Github to store all of our code and share it with others. 

### Setting up your project on Github

* First let's set up a remote repository on Github. Go to https://github.com, and click the `+` located in the top right corner and select "new repository". 

* Fill out information about your new repository. It's a good idea to keep your repository name consistent with the directory on your computer. In this case you should name it "git_practice". 

* The description is optional, but you can fill out with something like "This is my first repository!!!".

* Chose to make your repositories public. This allows other developers to see your work and lets you create a nice history that you can potentially show off when you are applying for an internship or job. (You also have to pay for private repositories, so that's another reason to keep it public.) 

* Now click `Create Repository`.

* On the next screen you should follow the instructions under ***…or push an existing repository from the command line***. Copy and past this command into your terminal (make sure you are in the `git_practice` directory on your computer):

`git remote add origin git@github.com:<your github username>/git_practice.git`

  This command is connecting the local version of your project to the `remote` address of your repository on github so you can upload our code to github.

* Now you are ready to push up your code to Github with that second command: 

`git push -u origin master`

* This `push` command is telling the code, get on up there to github. The `-u` stands for "upstream", the `origin` indicates that this is the "original" repository created for this project, and `master` indicates that you are pushing this code to the master branch. If you get a message prompting you to type in yes/no, type in yes. 

* We only use this extended command the first time that we push up code to a repository. After this you can push code up to this same repository with just the `git push` command.

* Refresh the page on your github repository and check out the files you just added. Great job!

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/hs-github-lab' title='Github Workshop'>Github Workshop</a> on Learn.co and start learning to code for free.</p>
