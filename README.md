---
  tags: git, kids, github 
  languages: git
  level: 1
  type: lab
---

## Github Workshop

The goal of the workshop is to add the code that we created in the last lab to Github. We use [Github](https://github.com/) to store all of our code and share it with others. You should have already set up a Github account at the beginning of class.

### Setting up your project on Github

* First set up your remote repository, aka the version located on github.com. Go to https://github.com, and click the `+` located in the top right corner and select "new repository". 

* Fill out information about your new repository. It's a good idea to keep your repository name consistent with the directory on your computer. In this case you should name it "my_code". 

* The description is optional, but you can fill out with something like "This is my ruby code repository".

* Chose to make your repositories public. This allows other developers to see your work and lets you create a nice history that you can potentially show off when you are applying for an internship or job. (You also have to pay for private repositories, so that's another reason to keep it public. 

* Now we'll click `Create Repository`.

* Now you should see something that starts with git@github.com... That's the remote location for our project. We need to set our local version of our project to point to that. Copy that address and in your terminal in the directory for your project, enter:

`git remote add origin git@github.com:<your github username>/my_code.git`

* `remote` tells our computer "we're adding the remote location"

* `origin` is the orginal remote repository, and we're telling it to be `git@github.com:vicfriedman/my_code.git`

* At this point, your files are still only located on your computer. Go ahead and put them up on the remote version. 

`git push -u origin master`

* This is the only time we'll enter this exact command, becuase it's the first time we're pushing our code to the server for this particular project. `push` is saying, go on code, get on up there. The `-u` means "upstream", which is just saying to go up to the github repository. If you get a message prompting you to type in yes/no, type in yes.

* Refresh the page on your github repository and check out the files you just added. Great job!

### Working on other people's code

So now that we've learned how to start and work on our own projects, let's learn how to work on someone else's.

Go to http://ironboard-experiment.herokuapp.com/admin/lessons/566 and follow the instructions.
