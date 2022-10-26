# Lab Report1

# 1: Installing VScode

![image](https://user-images.githubusercontent.com/114322721/193393272-2e5b97ef-d997-423b-b50f-9604b240ebee.png)


First I downlad the app https://code.visualstudio.com/.

# 2:Remotely connecting

![image](https://user-images.githubusercontent.com/114322721/193393265-e9f949ff-32dc-4027-b82a-ab0cf58b030e.png)

I opened "Terminal" and "New Terminal". I typed the command `ssh cs15lfa22lp@ieng6.ucsd.edu.`

# 3: Run Some Commands.

![image](https://user-images.githubusercontent.com/114322721/197934393-f96dab05-cafa-4df2-8d72-7d5c7d17a501.png)
)

I printed "Hello.txt" as shown in the screenshot. I got Hello World. 

# 4: Moving Files over SSH with scp

![image](https://user-images.githubusercontent.com/114322721/193393525-2308a8da-9d46-4b3e-9757-f4c9e28c8c98.png)

I created a file "WhereAmI.java" and I typed code `cs15lfa22lp@ieng6.ucsd.edu:~\` which send the "WhereAmI.java" to the remote server.

![image](https://user-images.githubusercontent.com/114322721/197942353-f780512c-d7e8-48e3-a33d-0cd87a1468d5.png)

I logged out of the remote server, and made a file WhereAmI.java. Running scp WhereAmI.java cs15lfa22lp@ieng6.ucsd.edu:~/.

# ssh key

![image](https://user-images.githubusercontent.com/114322721/197944278-dc4200ea-2c33-409c-9403-4ea499343b19.png)

To setup an SSH key, first use key-gen to generate an ssh key

# Optimizing Remote Running

![image](https://user-images.githubusercontent.com/114322721/197950499-05010708-10d8-46dc-8e63-e559fcc22d67.png)

We can see that ls listed the files we have on the server. We call the command on our local directory and, after the call, we are still in our local directory. We do not remain in the server.

![image](https://user-images.githubusercontent.com/114322721/197950234-f3436b8c-f33e-4d11-8b09-21c117cc22d1.png)

On the second command, ssh compiles and runs WhereAmI.java. From the results that are printed out, we can tell that the compile-and-run process was finished on the server, since the OS is linux but not Windows (my pc is Windows). Before and after the command, we all stay in our local directory, while the java program was run on the server.
