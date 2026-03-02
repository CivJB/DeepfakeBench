Steps Jack took to accomplish this project:

1. Task
    - I was assigned with researching open source tools to detect AI imaging, videos, and other media.
    - I was tasked this because AI is on the rise and nowadays you are seeing frequent videos and pictures created by AI to defame people within social media or just the general public
    - Specifically, Kathy Hochul (NYS Gov) would like a tool to give to the public to detect AI and distinguish real and fake messages being produced by public officials (politicians)
    - Therefore, a large amount of NYS funding was given to creating an AI detection tool called deep fake o meter aka deepfakebench
    - This tool is being worked on by several universities in the hope that it can become the face of AI detection.

2. Project Forking 
    - When I was tasked this assignment, the first step I took was forking the already established repo located @ https://github.com/SCLBD/DeepfakeBench
    - Forking a repo is pretty much duplicating the project and providing ownership to yourself so that you can provide modifications and build upon the work thats already been done.
    - Therefore, the forked repo now is located @ https://github.com/CivJB/DeepfakeBench
    - You can fork a repo by doing the following steps:
        1. Create a Github Account
        2. go to the location in which the repo you are looking to fork is. So in this case: https://github.com/SCLBD/DeepfakeBench
        3. And click the 'Fork' button that is located in the mid-rightish of the repo's page
        4. Now you have a copy for you to experiment with, without destroying someone else work.

3. Environment Setup
    - After, completing the forking of the repo you now look into the projects requirements for getting this project working.
    - This is usually (hopefully) found within the readme of the project. If there is no readme supplied you will unfortunately need to start doing manual testing in order to just continue working through errors until they have all subsided.
    - In this case, we have been supplied a readme. It is located @ https://github.com/CivJB/DeepfakeBench/blob/main/README.md
    - So I started following the instructions listed, please note go slow, these are instructions are to be followed precisely as written. You can find these instructions @ https://github.com/CivJB/DeepfakeBench?tab=readme-ov-file#-quick-start
    - These are the following steps I took to complete the environment setup according to the readme: (readme needed to be updated)
        - Download/Install VS Code or Visual Studio
        - Clone the forked repo into your file structure within VS code or Visual Studio
        - pick the file structure you'd like. AKA choose where the project will go within your local machine
            - Ex: C:\Users\FVMSU\Documents\jack-bush\Projects\DeepfakeBench>
        - Within the terminal of VS Code or Visual Studio create a python virtual env 
            - This is done so you don't break your local machine with the updating/modifying of device dependency. 
            - I specifically used anaconda for my python virtual env
            - I did this by navigating my web browser to https://www.anaconda.com/download
            - I created an anaconda account (should be free)
            - And downloaded anaconda to my local machine by going to https://www.anaconda.com/download/success and clicking he graphical bit installer for the appropriate operating system
            - Once finished installing I clicked next through the default setup
            - Added anaconda to to our local machines path (google or use chatgpt... this is already getting super long)
        - Once you have anaconda all setup, and you are in your IDE's terminal type 'conda create -n deepfakebench python=3.10' 
        - Once created you should get a confirmation within your terminal and provide you with instructions to activate your newly created anaconda python virtual environment
        - you should type 'conda activate deepfakebench' and it will look like this (deepfakebench) PS C:\Users\FVMSU\Documents\jack-bush\Projects\DeepfakeBench>
            - When you are done working: type conda deactivate
    - Once your Project is forked, Saved within your local device, opened in an IDE, and your virtual env is created. You are now ready to move into project configuartion


4. Project Configuration
    - Now this is the point in the project where you need to digest the application. This shouldnt be rushed. Knowing how your project works from a overview --> the depths of each python file, etc is extremely important
    - Especially, you should look for a requirement.txt file or a file that lists all the dependencies (libraries) needed to help this application run/work
    - You will need to install all of these dependencies and most of the time they will need to be updated
    - In this case specifically, there was plenty of dependencies that needed to be updated and the venv listed within the readme was outdated
    - Therefore, I had to restart the project a couple of times to just get the configuration of the project just right.
    - I installed the neccessary libraries by just doing a long pip command within my IDE terminal
        - EX: pip install dlib imutils opencv-python tqdm scikit-image pillow
    - Something that additionally, wasn't forseen was that the deepfakebench project another projects datasets. 
    - To obtain these datasets you have to request approval access and set up the FaceForensics project. 
    - I have done both of these steps. Jason Cooper (a FVMSU manager) requested access through email and was aproved shortly after sending the email.
    - The dataset github is located @ https://github.com/ondyari/FaceForensics
    - Follow the readme supplied with that project to download the datasets
    - Then you can migrate the dataset within the deepfakebench project according to the readme project structure.
    - The datasets are large datasets, so currently (march 2nd, 2026) I have the original sequences and the FaceForensics++ DeepFakeDetection manipulated sequence within the project
        - This was accomplished by splitting the datsets into folders containing approximately 250 items of media content. 

5. Preprocessing

5. Project Testing