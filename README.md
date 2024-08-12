# finetune_llm
fine tuning llm from huggingface

# Setup
- install WSL2 on windows (this is for my home desktop)
- install image from https://rapids.ai/
- alias the following ```docker run --user rapids -it --rm --gpus all --name Geoffrey_Container -p 8888:8888 -v C:\Users\gsiis\Documents\mount_src:/home/rapids/mounted rapidsai```
- change user to root for changes needing su
- run previous alias to go inside docker
- give account ```rapids``` the ability to use sudo via logging in as root and ```passwd rapids``` (may need to add rapids to sudo group, this will make it easy to install things which requires sudo)

## on windows
- use powershell window run ```wsl```
- go to directory above mounted directory e.g. ```cd /mnt/c/Users/gsiis/Documents/mount_src``` (NOTE: /mnt/c takes place of C:\)
- may need to give permission to write to mount folder e.g. ```chmod 777 -R finetune_lm```
- if it still doesn't work, do the same command from a docker bash command with sudo

## on docker
- create jupyter config by running ```jupyter notebook --generate-config```
- uncomment line and rename hostname to ```c.NotebookApp.custom_display_url = 'http://localhost:8888'```
- start jupyter notebook with this alias ```jupyter notebook --ip 0.0.0.0```
- copy the line ```http://localhost:8888/?token=<replace this with actual token>```

## on windows
- assuming you're at the mounted directory run ```code .``` (NOTE: there is a dot at the end)
- on top right click "Select Kernel"
- click "Existing Jupyter Server"
- paste in the copied line wtih token
- give it a name (can be blank) then select "Python 3 (ipykernel)" (NOTE: may require installing ipykernel )
 
#### Source https://blog.ovhcloud.com/fine-tuning-llama-2-models-using-a-single-gpu-qlora-and-ai-notebooks/
