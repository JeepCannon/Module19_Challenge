# Module19_Challenge
Blockchain challenge assignment


Error Message I keep getting upon clicking send transaction in the streamlit app. [everything else works up until this final step] :

ValueError: {'message': "VM Exception while processing transaction: Transaction's maxFeePerGas (0) is less than the block's baseFeePerGas (875000000) (vm hf=merge -> block -> tx)", 'stack': "RuntimeError: VM Exception while processing transaction: Transaction's maxFeePerGas (0) is less than the block's baseFeePerGas (875000000) (vm hf=merge -> block -> tx)\n at Miner.<anonymous> (C:\\Program Files\\WindowsApps\\GanacheUI_2.7.1.0_x64__rb4352f0jd4m2\\app\\resources\\static\\node\\node_modules\\ganache\\dist\\node\\1.js:2:38132)\n at async Miner.<anonymous> (C:\\Program Files\\WindowsApps\\GanacheUI_2.7.1.0_x64__rb4352f0jd4m2\\app\\resources\\static\\node\\node_modules\\ganache\\dist\\node\\1.js:2:36466)\n at async Miner.<anonymous> (C:\\Program Files\\WindowsApps\\GanacheUI_2.7.1.0_x64__rb4352f0jd4m2\\app\\resources\\static\\node\\node_modules\\ganache\\dist\\node\\1.js:2:35116)\n at async Miner.mine (C:\\Program Files\\WindowsApps\\GanacheUI_2.7.1.0_x64__rb4352f0jd4m2\\app\\resources\\static\\node\\node_modules\\ganache\\dist\\node\\1.js:2:39680)\n at async Blockchain.mine (C:\\Program Files\\WindowsApps\\GanacheUI_2.7.1.0_x64__rb4352f0jd4m2\\app\\resources\\static\\node\\node_modules\\ganache\\dist\\node\\1.js:2:60063)\n at async Promise.all (index 0)\n at async TransactionPool.emit (C:\\Program Files\\WindowsApps\\GanacheUI_2.7.1.0_x64__rb4352f0jd4m2\\app\\resources\\static\\node\\node_modules\\ganache\\node_modules\\emittery\\index.js:303:3)", 'code': -32000, 'name': 'RuntimeError', 'data': {'hash': '0x6b24a16e018c2709f273ea793956c1baca8f8c8b9f914b5a9729f3383b28ae86', 'programCounter': 0, 'result': '0x6b24a16e018c2709f273ea793956c1baca8f8c8b9f914b5a9729f3383b28ae86', 'reason': None, 'message': "Transaction's maxFeePerGas (0) is less than the block's baseFeePerGas (875000000) (vm hf=merge -> block -> tx)"}}
Traceback:
File "C:\Users\danie\anaconda3\envs\dev\lib\site-packages\streamlit\runtime\scriptrunner\script_runner.py", line 565, in _run_script
    exec(code, module.__dict__)
File "C:\Users\danie\Desktop\FinTech_Documents\99. Challenge_Assignments\Module19_Challenge_EthTransactions\Starter_Code\Starter_Code\krypto_jobs.py", line 298, in <module>
    transaction_hash = send_transaction(w3, account, candidate_address, wage)
File "C:\Users\danie\desktop\FinTech_Documents\99. Challenge_Assignments\Module19_Challenge_EthTransactions\Starter_Code\Starter_Code\crypto_wallet.py", line 80, in send_transaction
    return w3.eth.sendRawTransaction(signed_tx.rawTransaction)
File "C:\Users\danie\anaconda3\envs\dev\lib\site-packages\web3\module.py", line 58, in caller
    result = w3.manager.request_blocking(method_str, params, error_formatters)
File "C:\Users\danie\anaconda3\envs\dev\lib\site-packages\web3\manager.py", line 158, in request_blocking
    raise ValueError(response["error"])
 
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
