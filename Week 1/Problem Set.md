Question 1
![image](https://github.com/user-attachments/assets/a2adb434-620c-4ac8-a1cc-449b51bd9f65)

Question 2

![image](https://github.com/user-attachments/assets/fb2e8e8b-c71b-4c96-b769-c430e6199aa2)

Question 3
![image](https://github.com/user-attachments/assets/d47c470f-97eb-4c36-b967-2c83a34f85b5)
Question 4

![image](https://github.com/user-attachments/assets/7d893168-6eda-484e-b1c7-16b9ec15ccba)

Question 5

![image](https://github.com/user-attachments/assets/6e067774-0d2e-4b61-9bbd-16a361d23aa3)

Question 6

![image](https://github.com/user-attachments/assets/2a9d980e-5d89-44ad-a175-0d8a1b77064c)

Question 7

![image](https://github.com/user-attachments/assets/e5d5ced0-29f1-4804-b9c5-62dfbd6dae9e)

Question 8

The movie industry wants to protect digital content distributed on DVD’s. We develop a variant of a method used to protect Blu-ray disks called AACS.

Suppose there are at most a total of n DVD players in the world (e.g. n=2^32). We view these n players as the leaves of a binary tree of height log2n. Each node in this binary tree contains an AES key ki. These keys are kept secret from consumers and are fixed for all time. At manufacturing time each DVD player is assigned a serial number i∈[0,n−1]. Consider the set of nodes Si along the path from the root to leaf number i in the binary tree. The manufacturer of the DVD player embeds in player number i the keys associated with the nodes in the set Si. A DVD movie m is encrypted as

E(kroot,k)||E(k,m)

where k is a random AES key called a content-key and kroot is the key associated with the root of the tree. Since all DVD players have the key kroot all players can decrypt the movie m. We refer to E(kroot,k) as the header and E(k,m) as the body. In what follows the DVD header may contain multiple ciphertexts where each ciphertext is the encryption of the content-key k under some key ki in the binary tree.

Suppose the keys embedded in DVD player number r are exposed by hackers and published on the Internet. In this problem we show that when the movie industry distributes a new DVD movie, they can encrypt the contents of the DVD using a slightly larger header (containing about log2n keys) so that all DVD players, except for player number r, can decrypt the movie. In effect, the movie industry disables player number r without affecting other players.

As shown below, consider a tree with n=16 leaves. Suppose the leaf node labeled 25 corresponds to an exposed DVD player key. Check the set of keys below under which to encrypt the key k so that every player other than player 25 can decrypt the DVD. Only four keys are needed.

![image](https://github.com/user-attachments/assets/473e18e7-0f7c-41d6-90f1-422633d5aa7a)

Answer: 26, 6, 1, 11

Explain: Dựa vào cây nhị phân, khi khóa 25 bị lộ sẽ dẫn đến lộ khóa 12, 5, 2 và root. Khi phát hành DVD mới bằng cách tăng kích thước, thay đổi phần header của những khóa bị ảnh hưởng. Ở đây khóa bị ảnh hưởng là 1, 11, 26, 6. Chỉnh sửa 4 khóa này sẽ ngắt và làm cho những đầu đĩa DVD khác trừ đầu đĩa 25 có thể giải mã, vô hiệu hóa DVD 25.

Question 9

![image](https://github.com/user-attachments/assets/f778b982-f74f-4a24-b0be-c3b42df5d726)

Question 10: Continuing with question 8, suppose the leaf nodes labeled 16, 18, and 25 correspond to exposed DVD player keys. Check the smallest set of keys under which to encrypt the key k so that every player other than players 16,18,25 can decrypt the DVD.  Only six keys are needed.

Answer: 11, 6, 26, 15, 17, 4

Explain: Tương tự như trên thui.







