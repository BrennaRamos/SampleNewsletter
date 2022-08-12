1. Make sure you have git and node.js installed in your system. Open Terminal in the directory of your choice 
(for this guide, I chose to create a new file in "C:\Users\{username}\OneDrive\Documents\New Project>")

You may check your git and node versions in Terminal with the following commands:

git --version

node --version

2. Run this statement to clone the repository with my code into your environment:

git clone https://github.com/BrennaRamos/SampleNewsletter.git

3. Run the following command to traverse into the root directory of the project:

cd SampleNewsletter

Note: cd applies to Windows terminal. Depending on your OS, the command may be different

4. Next, we need to establish an Angular CLI workspace in this same directory, so keep Terminal open. I will provide step-by-step instructions, but here is some supplementary documentation:
https://angular.io/guide/setup-local

5. Run these commands in Terminal:

npm install -g @angular/cli
npm install --legacy-peer-deps
npm audit fix --force

These set of commands will install the workspace in the root folder, make sure that the required dependencies are installed, and it will also force some fixes onto those installations. 

Important Note: Using the flags --legacy-peer-deps and --force is not recommended or the true solution to any of the dependency errors encountered during installation. These flags force peer dependencies to be ignored and bypass any conflicts. In a real environment, this type of solution should never be used, as it opens the system to vulnerabilities and incompatibilities capable of breaking the project. This is a temporary solution to have my old project run on other systems as a sample of the project.

6. Now we can begin hosting the server. Run the following command:

ng serve

You can access the website via http://localhost:4200/ (or whatever alternative Terminal may have provided).
 

7. The site is up! However, we are still not connected to a datasource. We will put up an artificial database for this sample project using JSON. This creates a pseudo REST API instance. Leaving the first Terminal as-is, open a second Terminal and travel to the root directory, TreehouseNewsletter. Then, run the following command:

npm run json:server

If all went well, the server is up and you should get a little smiley saying "Hi! Loading db.json done."
 
8. Refresh your connection to localhost on the browser and the tables should be populated! You can also make changes to the database with the functions available on the site. The functinos available include:

Viewing the dashboard of subscribers.
Adding new subscribers to the database.
Deleting existing subscribers from the database.
