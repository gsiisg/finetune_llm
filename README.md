# finetune_llm
fine tuning llm from huggingface

# Setup
- WSL2 on windows (this is for my home desktop)
- install image from https://rapids.ai/
- alias the following ```docker run --user rapids -it --rm --gpus all --name Geoffrey_Container -p 8888:8888 -v C:\Users\gsiis\Documents\mount_src:/home/rapids/mounted rapidsai```
- give account ```rapids``` the ability to use sudo via logging in as root and ```passwd rapids``` (may need to add rapids to sudo group)
- can access jupyter notebook on host windows via ```jupyter notebook --ip 0.0.0.0```

# Source (https://blog.ovhcloud.com/fine-tuning-llama-2-models-using-a-single-gpu-qlora-and-ai-notebooks/)
