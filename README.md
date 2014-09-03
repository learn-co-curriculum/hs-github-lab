---
  tags: git, kids, github 
  languages: git
  level: 1
  type: lab
---

## Github Workshop

The goal of the workshop is to introduce you to Github and add the code that we created in the last lab to Github. We use [Github](https://github.com/) to store all of our code and share it with others. Github is a web-based software for hosting your code, as well as version control, through git.

### Let's set up an account.

Go to Github, and fill out the form to create a username and click signup. You will need to then check your email to verify your new account by clicking a link in an email.

Next we'll need to set up your SSH key. 

### Setting Up Github SSH Keys

An SSH key is how github can identify you without you having to enter your username and password every single time you want to push code up to the server. Github has a great online documention [here](https://help.github.com/articles/generating-ssh-keys).

The first thing you'll need to do is open terminal and make sure you're at your root directory. It will look like `~`. If you're not there, `cd ~` will move you to the root directory.

Then we want to look and see if we have a .ssh directory. `ls -la` will show you all the hidden files. If you don't even have a `.ssh` directory, you can make it `mkdir .ssh`

Now we need to generate the SSH key, `ssh-keygen -t rsa -C "your_email@example.com"`. You'll need to enter the same email address that you used to set up your github account between the quotation marks.

You'll get prompted to type the password to your computer twice (the letters won't actually show up when you type. Don't worry, it's just for security purposes).

Once the SSH key generation is done, you'll enter `ssh-add ~/.ssh/id_rsa`

Then `pbcopy < ~/.ssh/id_rsa.pub` which just adds your SSH key to your clipboard.

Then you'll need to go to your github account online, and in the top right corner select Account Settings (the symbol with the wrench). In the left toolbar, you'll select SSH Keys. Then you'll select `Add SSH Key`.

You'll enter a name of `Github SSH` and then paste your SSH key into the `key` field. Then you'll click the green `Add Key` button.

After that, you'll want to go back to terminal and verify that you successfull added the SSH key, `ssh -T git@github.com`. You should get back `Hi username! You've successfully authenticated, but GitHub does not provide shell access.`

### Setting up your project on Github

Because this is a new project, we'll need to set up our remote repository, aka the version located on github.com. We need to go to https://github.com, and click the `+` located in the top right corner and select "new repository". We'll be directed to a page that let's us fill out information about our new repository. It's a good idea to keep your repository name consistent with the directory on your computer. In this case you should name it "my_code". 

The description is optional, but you can go ahead and fill out with something like "This is my code". You can now either chose to make your repositories public or private. I typically make all of my repositories public, so everyone can see it. Open source contributions are incredibly valuable in the tech community. It allows other developers to learn from your work. It also creates a nice history of your work, so potentially down the line when you're looking for internships or jobs, employers can get a good look at all the code you've written. You also have to pay for private repositories, so we'll go ahead and keep it public. And now we'll click `Create Repository`.

8. At the top, next to "Set up in Desktop", you'll see a line that starts with git@github.com... That's the remote location for our project. Let's copy that. We need to set our local version of our project to point to that. In your terminal in the directory for our project, enter:

`git remote add origin git@github.com:vicfriedman/my_code.git`

`remote` tells our computer "we're adding the remote location"

`origin` is the orginal remote repository, and we're telling it to be `git@github.com:vicfriedman/my_code.git`

9. At this point, our files are still only located on our computer. Let's go ahead and put them up on the remote version. 

`git push -u origin master`

This is the only time we'll enter this exact command, becuase it's the first time we're pushing our code to the server for this particular project. `push` is saying, go on code, get on up there. The `-u` means "upstream", which is just saying to go up to the github repository. 

Refresh the page on your github repository and check out the files you just added. Great job!

### Working on other people's code

So now that we've learned how to start and work on our own projects, let's learn how to work on someone else's. Let's go to https://github.com/flatiron-school-curriculum/hs-git-website-lab. 

There are two options for working on a project with someone else: forking and cloning. Cloning means your going to make an exact replica of the project on your computer, and it's going to point to that specific remote location. If you committed a change on master, it would show on master in their repository. Forking creates an exact replica of the project in your github account.

Let's fork this lab https://github.com/flatiron-school-curriculum/hs-git-website-lab by clicking the `Fork` button in the top right corner. When we do that, we notice the location of the new forked repository is vicfriedman/hs-git-website-lab. So now that it exists on my github account, we have to clone the project to get it on my computer.

`git clone git@github.com:vicfriedman/hs-git-website-lab.git`

Now that we have it up locally, we can cd into the project `cd hs-git-website-lab` and begin working on the lab!

<!-- After they complete the lab... -->

### Wrapping up

Now that you completed your lab, make sure it's all pushed up to your version of the repository on github. After that, we're going to create a pull request. A pull request is the best practice for submitting contribution of work to an open source project. To create a pull request, go to your version of the repository on your github account. We'll click the green button in the top left corner. On the next page, we'll want to enter a comment for the pull request, "completed lab" and click submit. This is how I'll be able to review your work and give you feedback on your code. 
