```
                          ____  __        ________ _______ ________ ________
                          __  |/ /        ___  __ \__  __ \___  __ \___  __/
                          __    / __________  /_/ /_  / / /__  /_/ /__  /   
                          _    |  _/_____/_  ____/ / /_/ / _  _, _/ _  /    
                          /_/|_|          /_/      \____/  /_/ |_|  /_/     

```                                                  

The tool was designed to ease on security operators by createing an automatic report to submit to their clients.
Your PoCs are uploaded to **Azure's Storage** as in a file-system type of order.
Then, **Ghostwriter's project** will generate a report, with all selected findings, including private URL tokens for each PoC.

# Installation
```
$ git clone https://github.com/practiccollie/x-port
$ cd x-port/
$ pip3 install -r requirements.txt
```
# Usage 
```
$ python3 x-port.py <path/to/findings-directory>
```
# Prerequisites
- Install ghostWriter with [Ghostwriter's github](https://github.com/GhostManager/Ghostwriter).
- Create an [Azure Data-Lake Storage Gen2](https://learn.microsoft.com/en-us/azure/storage/blobs/create-data-lake-storage-account) account.

# Customization
### Environmental Variables
The script looks for the "GW_USER" & "GW_PASS" as environment variables.  
You should add the following lines to your shell configuration file.
```
export GW_USER = "Your-Username>
export GW_PASS = "Your-Password>
```

### utils.py
Make sure to modify the following sections:
* **Prompts** 
https://github.com/practiccollie/x-port/blob/030c75c5217050e75b867f2d6475202ce1b92906/utils.py#L36-L67

* **GraphQL**
https://github.com/practiccollie/x-port/blob/030c75c5217050e75b867f2d6475202ce1b92906/utils.py#L87-L114

* **GhostWriter**
https://github.com/practiccollie/x-port/blob/030c75c5217050e75b867f2d6475202ce1b92906/utils.py#L119-L125

* **Azure**
https://github.com/practiccollie/x-port/blob/030c75c5217050e75b867f2d6475202ce1b92906/utils.py#L127-L135

# Authors
* [@practiccollie](https://github.com/practiccollie)
* [@ta1c0](https://github.com/ta1c0)
