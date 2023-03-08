# Week 8 Lab Report 4
## Step 4
<img width="736" alt="Screenshot 2023-02-25 at 1 43 53 PM" src="https://user-images.githubusercontent.com/122561814/221384578-7f960084-ae56-4b7f-9df0-a81d27a91de9.png">

* Keys pressed: ssh cs15lwi23apw@ieng6.ucsd.edu `<enter>`
* Explanation: I use my ssh username to login to the remote server. Since I configured it to login without a password, I don't have to type it in.
## Step 5
<img width="603" alt="Screenshot 2023-02-25 at 2 43 24 PM" src="https://user-images.githubusercontent.com/122561814/221384581-d5eb671e-4477-4935-8a30-06c85b70f889.png">

* Keys pressed: git clone `<ctrl-v>` `<enter>`
* Explanation: I'm using the `git clone` command with the ssh link to clone the lab7 repo that I forked into my account on github.
## Step 6
  <img width="981" alt="Screenshot 2023-02-25 at 3 01 53 PM" src="https://user-images.githubusercontent.com/122561814/221384587-c74e3f78-d0fd-4e81-b164-8ff934077b57.png">

* Keys pressed: cd ./lab7 `<enter>` `<ctrl-v>` `<enter>` `<ctrl-v>` TesterListExamples `<enter>`
* Explanation: First, I cd into lab7 so that we can access the lib and starter folders. Then we use the compiling command for macOS that I just copy pasted. After pressing enter, the code compiles successfully. Then I run the junit tester file using the run command and adding `TestListExamples`. Once I press enter, the jUnit tests are run, and we can see that 1 test fails (testMerge2) due to a time out exception.
## Step 7
  <img width="581" alt="Screenshot 2023-02-25 at 3 21 31 PM" src="https://user-images.githubusercontent.com/122561814/221384591-2924d95d-a51b-459e-9bd1-edaaa63b8142.png">

* Keys pressed: sed -i '43 s/index1/index2/' ListExamples.java `<enter>`
* Explanation: Now that we know there is a bug, we must debug it. We can use the `sed` command to fix it. We tell `sed` to replace the string at line 43 in `ListExamples.java` to replace "index1" to "index2." `-i` tells it to edit file in place. Once we press enter, the changes have been made and hopefully our bug is fixed!
## Step 8
  <img width="977" alt="Screenshot 2023-02-25 at 3 21 59 PM" src="https://user-images.githubusercontent.com/122561814/221384598-ae865565-ac11-4e4c-941a-acea58792672.png">

* Keys pressed: `<up>` `<up>` `<up>` `<up>` `<up>` `<up>` `<enter>` `<up>` `<up>` `<up>` `<up>` `<up>` `<enter>`
* Explanation: To check if we have truly debugged our code, we must compile and run it again. So we go up till we find the compiling command we used in Step 6. Once it has successfully compiled, we do the same for the run command and press enter. From the screenshot, we can see the results are good and our bug is fixed!

## Step 9
<img width="722" alt="Screenshot 2023-02-25 at 3 38 27 PM" src="https://user-images.githubusercontent.com/122561814/221384574-17b454bd-cc1a-47ff-ad43-cb281696c82a.png">

* Keys pressed: git add List`<tab>` `<enter>` git commit -m 'Bugs Fixed' `<enter>` git push`<enter>`
* Explanation: now all we have to do is commit and push the changes we made onto github, so our repo is updated. For that we first add the file `ListExamples.java` that we just edited. Then we commit and add a brief message explaining what changes are being added. Finally, we push to the repo and our changes have been successfully updated!

