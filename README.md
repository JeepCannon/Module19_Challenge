# Module19_Challenge
Blockchain challenge assignment


Error Message I keep getting.

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
  
  
  
  
