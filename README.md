# Hashing-Lab
An entry level lab for those interested in learning more about hashing on both Windows and Linux systems. 

# As a disclaimer, it is highly recomended that this and any other labs, be conducted on a Virtual Machine with a known good backup!

# Windows-Linux-Hashing-Activity

## Objective

The Hashing Home Lab is designed to get individuals interested in the world of hashing and gain a foundation to which build upon for more advanced activitys. Hashing is when a mathematical algorithm is applied to digital data. It sereves as both a way of hiding and validating data. It can often be seen when storing passwords or when preserving data for forensic purposes. In this lab we will only be looking at two of the most basic forms of hash, MD5 and Sha-1. Thos following along will find and create hashes for data within their virtual system.

### Skills Learned

- Basic understanding of Hashing concepts and practical application.
- Proficiency in analyzing and interpreting Hashing types.
- Ability to utilize the GUI of the HashCalc Tool.
- Enhanced knowledge of both Windows and Linux terminals.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- HashCalc for creating and viewing multiple Hashes of data.
- Command Line tools(such as sigcheck) for creating Hashes of desired data samples.


  ### Skills: Window System
  
1. Right Click on the start button and select Run
   
   ![1 Run](https://github.com/Lantern76/Hashing-Lab/assets/119342094/19702845-d91e-4b18-b9bc-837829a5c269)

3. In the Run Box, type cmd and then click ok.
   
   ![2 cmd](https://github.com/Lantern76/Hashing-Lab/assets/119342094/39ac788d-06f4-4d57-9a0b-b4a3c0bc9a4e)

5. Type the following command to redirect the output to a file named hostname.txt  "hostname > hostname.txt"
   
   ![1 Hostname txt](https://github.com/Lantern76/Hashing-Lab/assets/119342094/44594aba-7eae-44e4-9643-0636df027ae8)

7. Type the following to display the computer name of your system (It should match your first name)
   
   ![1 Hostname](https://github.com/Lantern76/Hashing-Lab/assets/119342094/d3b804d2-cc08-4aba-a468-7ccf5d22a475)

9. Type the following to lanch the sysinternals tools sigcheck "sigcheck". Click I agree.
    
    ![2 sigcheck](https://github.com/Lantern76/Hashing-Lab/assets/119342094/3c3129bc-81f8-4fdf-9fac-455be63c3812)

11. Type the following to get the some of the more common hash values, "sigcheck -h hostname.txt". Click I agree.
    
    ![3  sigcheck hostname](https://github.com/Lantern76/Hashing-Lab/assets/119342094/fcca0f63-7ced-4e7d-b309-354ab8ea482b)

13. Type the following to rename hostname.txt to yourname.txt, "ren hostname.txt yourname.txt". Use your first name.
    
    ![2 Rename file ](https://github.com/Lantern76/Hashing-Lab/assets/119342094/2b748685-b1bf-4806-88e8-cf95c22e8197)

15. Type the following to get the some of the more common hash values, "sigcheck -h yourname.txt". Click I agree.
     - Notice that even though the name of the file changed the hash did not. The hashing process looks at the data
       within the file, not the name of the file or even the metadata of the file. Metadata is information like date created.
       
      ![3 Sigcheck ryan txt](https://github.com/Lantern76/Hashing-Lab/assets/119342094/1b237e13-71dc-4d87-9aaf-f7d5db78ef21)

16. Click on Windows Explorer in the taskbar. Double click on This PC, Local Disk C:, Users, Administrator. Find
   the yourname textfile. Right click on the file and go to properties. Then click on the Hashes tab. Compare
   the MD5 and SHA-1 hashes from sigcheck to the MD5 and SHA1 hashes of Hashtab. They are the same.

![4 Comparison](https://github.com/Lantern76/Hashing-Lab/assets/119342094/7e2eb3cb-d832-43fa-9ccd-cc816a903511)

18. In the Start Search box, type HashCalc.
    
    ![HachCalc](https://github.com/Lantern76/Hashing-Lab/assets/119342094/82bfb982-6976-458e-9395-c7e427d48af6)

20. After Hashcalc opens, click the button and browse to C:, Users, Administrator, yourname.txt. Select
every available hash and then click the calculate button. The hashes should match from the other tools.
    - Also, notice how some tools provide the hexadecimal characters (base 16) in lowercase which other tools provide them
      in uppercase. This can be useful if you are in a Capture the Flag competition asking for a case specific answer.

![5 Hashcalc](https://github.com/Lantern76/Hashing-Lab/assets/119342094/4bf43e1e-703b-488c-bf99-d6a949a27db4)



### Tools Used

- Mate Terminal for utilizing the tools and interacting with the Linux system. 
    - The command line. or terminal, will play a vital role in the cybersecurity career field and I recomend those unfamiliar with it use their Linux VM to play around with and get used to some of the more common commands such as ls and cp.
- Command Line tools including ls, md5sum, cp, sha1sum, sha256sum, sha512sum.

### Skills: Linux System


### Warning this side of the Project will be done as a root user 

1. Open terminal. Can be done by Ctrl + Alt + T, or by simply using the GUI. It is usually found under the applications tab but varies depending on Linux Distro version.
   
![HachCalc](https://github.com/Lantern76/Hashing-Lab/assets/119342094/a77546ee-33a2-4e79-8d1a-8a7e835edcd8)

2. Type the following command to switch into the directory on Kail Linux that has Windows executables, "cd /usr/share/windows-binaries"
  
![6 Root user](https://github.com/Lantern76/Hashing-Lab/assets/119342094/bdde1ded-4860-4ee4-9938-4144b1c21132)

3. Type the following command to view the files and folders in the directory, "ls -la"

![7 ls all](https://github.com/Lantern76/Hashing-Lab/assets/119342094/5c3cfe0c-508c-4a69-b50c-aabad435aafc)

4. Type the following command to get the MD5 hash of nc.exe, "md5sum nc.exe"

![8 md5sum](https://github.com/Lantern76/Hashing-Lab/assets/119342094/d2e7a201-51dd-46cf-a10d-b8b3fa7b7b9a)

5. Type the following command to copy nc.exe to yourname.exe (replace yourname with your first name.), "cp nc.exe yourname.exe"

6. Type the following command to navigate to the webserver directory, "ls -la". Find the newly named file under yourname.exe.

7. Type the following command to get the md5 hash of the yourname.exe file, which is actually nc.exe, "md5sum yourname.exe"

![6 md5sum ryan exe](https://github.com/Lantern76/Hashing-Lab/assets/119342094/814b3c7a-77ba-4bba-886b-5acfb17adca5)

8. Type the following command to get the sha1sum of the yourname.exe file, which is actually nc.exe, "sha1sum yourname.txt"

![7 Sha1sum ryan exe](https://github.com/Lantern76/Hashing-Lab/assets/119342094/2ef993d5-232f-4523-97e5-2ae44d989032)

9. Type the following command to get the sha256sum of the yourname.exe file, which is actually nc.exe, "sha256sum yourname.exe"

![8 Sha256 ryan exe](https://github.com/Lantern76/Hashing-Lab/assets/119342094/3b7ce4fd-8c8c-401b-982a-6c16fd71c872

10. Type the following command to get the sha512sum of the yourname.exe file, which is actually nc.exe, "sha512sum yourname.txt"

![10 Sha512 ryan exe](https://github.com/Lantern76/Hashing-Lab/assets/119342094/03375fff-47af-4156-9629-e59443e6a628)















   

