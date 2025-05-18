Creating the Jenkins Job
Opened Jenkins and clicked on “New Item”. Created a Freestyle project and named it Newitem. Under the Source Code Management section, selected Git. Entered my GitHub repository URL: https://github.com/Vaibhavi-sooda/Jenkins-Job-Creation_Implementing-Version-Control-in-Your-CI-CD-Pipeline Changed the branch specification from master to main, since my GitHub repo uses main as the default branch.

Adding Build Steps
In the Build section, I added a Windows batch command. I used the following command to simulate a simple build: echo "Building the project..." This command was added in the “Execute Windows batch command” section and used to verify that Jenkins executes the build step after cloning the repository.

Running the Build and Output
Clicked Build Now to trigger the build manually. Viewed the logs under Console Output, which showed the following:
![WhatsApp Image 2025-05-17 at 7 56 05 PM](https://github.com/user-attachments/assets/9e965f78-40ed-4511-96e2-0cc992fd35d4)
This confirmed that Jenkins successfully: Fetched the code from GitHub Checked out the correct commit Executed the batch command Finished the build successfully

Challenges Faced and Solution
I initially got an error: “Couldn't find any revision to build.” This happened because Jenkins was looking for the master branch, which didn’t exist in my GitHub repo. I resolved it by changing the branch specifier in Jenkins to main.
![WhatsApp Image 2025-05-17 at 7 56 06 PM](https://github.com/user-attachments/assets/a8d1b098-3f0a-4684-961c-e484d5959c46)
