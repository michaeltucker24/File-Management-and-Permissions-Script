# File Management and Permissions Script

<p align="center">
  

  
</p>

This project demonstrates the use of Linux commands to create and manage files and directories with specific permissions. The script covers creating a directory structure, generating files, applying permissions, and verifying access, showcasing practical file management techniques in Linux.

---

## **Project Steps and Screenshots**

### Step 1: Create Directory Structure

<p align="center">
  
  ![Screenshot 2024-12-06 at 5 24 01 PM](https://github.com/user-attachments/assets/94a2d74c-0328-4851-bbd9-65f4240c6a6d)

</p>

- **Description**: Created a directory structure with 'public' and 'private' subdirectories to manage files with different access levels.
- **Commands**:
  ```bash
  mkdir FileManagementProject
  cd FileManagementProject
  mkdir public private
  ```

---

### Step 2: Create Files and Add Content

<p align="center">


 ![Screenshot 2024-12-06 at 5 25 49 PM](https://github.com/user-attachments/assets/18c83d0c-9598-443d-a98b-869e0659464a)


</p>

- **Description**: Created sample files in the `public` and `private` directories. Added content to one file in each directory to prepare for managing permissions.
- **Commands**:
  ```bash
  cd public
  touch file1.txt file2.txt file3.txt
  echo "This is a public file." > file1.txt
  cd ../private
  touch private1.txt private2.txt
  echo "This is a private file." > private1.txt
  ```

---

### Step 3: Apply Permissions

<p align="center">

  ![Screenshot 2024-12-06 at 5 30 14 PM](https://github.com/user-attachments/assets/e6ce9a84-c1a8-4e55-b120-f5be48b9a51e)

</p>

- **Description**: Set and verified file permissions to control access to files in the `public` and `private` directories. Permissions ensure that `public` files are more accessible while `private` files are restricted to authorized users.
- **Commands**:
  ```bash
  chmod 666 public/file1.txt
  chmod 754 public/file2.txt
  chmod 700 public/file3.txt
  chmod 600 private/private1.txt
  chmod 644 private/private2.txt
  ls -l
  ```

---

### Step 4: Verify Permissions and Test Access

<p align="center">

  ![Screenshot 2024-12-06 at 5 32 54 PM](https://github.com/user-attachments/assets/8efb14f6-1e8a-4a57-b77a-57a285e7cd9e)

  
![Screenshot 2024-12-06 at 5 32 59 PM](https://github.com/user-attachments/assets/1e4bd292-fbfa-471c-8855-c92e9264bdb2)

</p>


- **Description**: Verified file permissions by observing access behaviors and confirming permission levels using `ls -l`. While `sudo` was restricted in this environment, the file permissions effectively enforced access control.
- **Commands**:
  ```bash
  cd public
  cat file1.txt
  echo "Editing file2 content." >> file2.txt
  cd ../private
  ls -l private1.txt
  cat private1.txt
  echo "Adding text to private2.txt" >> private2.txt
  ```

---

## **Key Commands Used**
- **`mkdir`**: Create directories.
- **`touch`**: Create empty files.
- **`chmod`**: Change file permissions.
- **`echo`**: Add content to files.
- **`ls -l`**: Verify file permissions.
- **`cat`**: Display file contents.

---

## **What I Learned**
This project helped me understand how to manage files and directories in Linux. I practiced creating and organizing files, applying specific permissions, and verifying access levels to ensure proper security and accessibility.

---

Feel free to share your feedback or suggestions. Check out more of my projects on my [GitHub profile](https://github.com/Mamutt7).
