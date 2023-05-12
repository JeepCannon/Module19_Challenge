# Module19_Challenge
Blockchain challenge assignment


Error Message I keep getting upon clicking send transaction in the streamlit app. [everything else works up until this final step] :
![image](https://github.com/JeepCannon/Module19_Challenge/assets/30644041/2041be65-a84f-41ae-a537-43ef908e657f)


 
Image at the moment before clicking send transaction:
![Screenshot 2023-05-12 011656](https://github.com/JeepCannon/Module19_Challenge/assets/30644041/7b72c7cd-740f-4cea-b9c1-0267f6efa6e8)
    
    
    
    
    
    
    
  Update: 1:39AM 
    I looked back through the crypto_wallet.py starter code and noticed that the "gasPrice" in my code was set to 0 and the "gas" was set to gasEstimate. Unsure if this was an error or it was something I was supposed to sniff out. I didnt see a mention of this in the instructions and it is like that in the starting file I downloaded. 
  ![image](https://github.com/JeepCannon/Module19_Challenge/assets/30644041/621c5152-6729-4e05-af73-af7637daf7e7)

 Either way I modified it to modify it to the gasEstimate as is reflected in the row above and BOOM. PROBLEM SOLVED!!! 
 ![image](https://github.com/JeepCannon/Module19_Challenge/assets/30644041/f7975334-befc-41f0-8252-c93546547ede)
   
    
  Transaction history in Gnache:
![image](https://github.com/JeepCannon/Module19_Challenge/assets/30644041/8a44244e-4423-47cd-8eba-6192fd224cbf)
 
![image](https://github.com/JeepCannon/Module19_Challenge/assets/30644041/3644b225-d787-46d0-b893-54b5efccc481)
