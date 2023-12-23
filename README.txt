################  Typical pipeline of llm, Q&A ###################


1.    Extraction of snippets  >> embedding model >> vector >>

 2.   Q >> embedding >> snippet >> A from LLM  

The embedding model for the llm could be replaced by knowledge graph

################## opensource repo. ##############################

The knowledge graph represent the different level of semantic concept in a 
information retreived system.

################################### Git ##############################


git status

git init
git add.
git commit -m "This is to push the project to Github"
git remote add origin https://github.com/VCBELAPA/OCR_Image_Extraction.git
git push -u -f origin master




################## Installing using PIP ##############################
Installing pip using conda 

conda install -c anaconda pip


Installing pip using trusted hosted
pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org install openpyxl


Replace pandas


pip uninstall --trusted-host pypi.org --trusted-host files.pythonhosted.org docker
pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org docker

pip install pytorch-transformers

python -m pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org --upgrade pip

llama-index needs python>=3.9



##############     llama-index       #############################


the model that are used instead of openai are llama 2


################# Knowledge Based Graph ##########################

Current used Knowledge Based Graph with LLM

1. NebulaGraph

2. llama index

3. Neo4j

############################## env ###################################


working enviorment 

llm2  # for 
llmgraph # for llmgraph git repo.
deepke-llm # for Deepkm
llm_cpp # for llama index cpp, I am using it in knowledge graphs


##################### llama index demo on Google Colab ############
!Python --version
Python 3.10.12

!pip install llmx==0.0.2a0

!pip install llama-index

Then rest of demo program

llama-index.ipynb


Add metadata to the document (Customizing Documents section)






References:
https://towardsdatascience.com/knowledge-graph-embeddings-101-2cc1ca5db44f

#########################################################################

(base) C:\Users\su1127>ssh-keygen -t rsa -b 2048
Generating public/private rsa key pair.
Enter file in which to save the key (C:\Users\su1127/.ssh/id_rsa):
Created directory 'C:\Users\su1127/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in C:\Users\su1127/.ssh/id_rsa.
Your public key has been saved in C:\Users\su1127/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:hTV1DvFKAwHj1m11Hd7Kbq89TyYWz4rA5t0Xf7uENU8 intl\su1127@CZBRN0363
The key's randomart image is:
+---[RSA 2048]----+
|        o.=o+.o.+|
|       . = + *..o|
|        + o = o..|
|       . . o + . |
|        S   . +oE|
|         .   .o*o|
|          +  .=.O|
|         o o =.O+|
|          . o +=X|
+----[SHA256]-----+

(base) C:\Users\su1127>

########################################################################
Drawing the knowledge graph with VM GPU

## How to connect to VM:working ssh

ssh lab1@130.3.77.227 -p 8022 -i C:\Users\su1127\.ssh/id_rsa

ssh lab1@130.3.77.227 -p 8022 -i C:\Users\su1127\.ssh/id_rsa
source lab1/bin/activate
########################################################################


scp C:\Users\su1127\Downloads\llm_cpp\llm_cpp_v2.py lab1:/home/lab1/su11  # This is working one: copy from local to remote
scp C:\Users\su1127\Downloads\llm_cpp\data\llama_kg.py lab1:/home/lab1/su11/  # This is working one: copy from local to remote


scp lab1:/home/lab1/su11/llm_cpp.py C:\Users\su1127\Downloads\ 		# This is working one: copy from remote to local
scp lab1:/home/lab1/su11/KG.png C:\Users\su1127\Downloads\llm_cpp\buffer


#################################  env ################################

python3 -m venv ./ocr 


source ocr/bin/activate

deactivate
######################################################################

model_url = "https://huggingface.co/TheBloke/Llama-2-13B-chat-GGUF/resolve/main/llama-2-13b-chat.Q4_0.gguf"
#model_url = "https://huggingface.co/TheBloke/Llama-2-70B-chat-GGUF/resolve/main/llama-2-70b-chat.Q4_0.gguf"

######################################################################
watch -n 10 nvidia-smi

#####################################################################
Here's how each triplet was derived:

1. L2 VLAN switching is the subject, and Forwarding Domain and VPWS FD are the predicate and object, respectively, because the text mentions "L2 VLAN switching" and then describes the use of a Forwarding Domain and VPWS FD.
2. Flow Points is the subject, and MAC learning is the predicate, because the text mentions "Flow Points" and then states that they allow for MAC learning.


####################################################################

export LLAMA_CPP_LIB=/home/lab1/su11/llama.cpp/libllama.so


####################################################################

References:

## LLM for documents

https://medium.com/@onkarmishra/using-langchain-for-question-answering-on-own-data-3af0a82789ed

https://github.com/kennethleungty/Llama-2-Open-Source-LLM-CPU-Inference

## Lips sync 

https://github.com/carykh/lazykh

https://github.com/Rudrabha/Wav2Lip

####################################################################

This is Production - https://askambrin.att.com/static/Ask_Ambrin


This is test - https://askambrin.att.com/static/Test_Ask_Ambrin

This is dev - https://askambrin-dev.att.com/static/Ask_Ambrin

####################### USERSTORY 158  #############################



As AskAmbrin user I want the prompt template to be optimized for 
multiple context feeding as well as answer correctness, so that 
given answer by the LLM could be relied on.

Details:

1. Different ways to combine multiple retrieved context shall be tried and the best shall be demonstrated using data
2. Most optimized prompt instructions to prevent incorrect answers shall be provided 








http://127.0.0.1:8000/image-search?query=What are requirements for P2 EMUX Data Plane Forwarding?



#################################################################
Connect to remote VM
> In VScode

lab1@POC-HPC1:~$ source lab1/bin/activate

(lab1) lab1@POC-HPC1:~/ainlm2/AI_Backend/Ask_Ambrin$ flask --app backend run --port 4444 --debug


> In local terminal 

(base) C:\Users\su1127>ssh -L 8888:localhost:4444 lab1

> In Postman

Post localhost:8888/login

###################################################################

> Connect with your own account
ssh poc1user


source /home/su1127/python_env/bin/activate

backend (you need to call login first)
/login
POST
{"attuid" : "<your att uid>"}
 
/prompt
POST
{
    "prompt" : "Can you describe the nodes you mentioned?",
     "model" : "gpt4",
      "vector_db": "P1P2",
      "conversation_session": true
}
 
retriever tester (u need to call embedings route before retrieving anything)
/embedings
GET
http://localhost:6083/embeddings?tex type=paragraph
 
/retrieve
GET
http://localhost:6083/retrieve?text type=paragraph&retrieve count=3&prompt=What is the LLGR Restarter mode?

##################################################################


The number of parameters : 

1. Retrieved context Top-3 or Top-5
2. LLM (llama-2 or GPT-4)

Response:

which is closest to the correct answer





##################################################################
Sanjit_Sept_22
https://att.sharepoint.com/:x:/r/sites/AIFlows/_layouts/15/doc2.aspx?sourcedoc=%7B793F1F13-3A51-4054-8AEE-B191B1F2EC42%7D&file=Sanjit_Sept_22.xlsx&action=default&mobileredirect=true&isSPOFile=1&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMzA5MjkxMTIwOCIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D

##################################################################









