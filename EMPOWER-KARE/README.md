# EMPOWER-KARE#

---

This repo contains the code of the paper "**EMPOWER-KARE: Deep Prompt Tuning for Knowledge-aware Response Generation in Clinical Counseling and Legal Support Conversations for Crime Victims**",

---

## Requirments ##

This code is tested on Python 3.8, Pytorch 1.7.1, and transformers 4.18.0

`pip install -r requirements.txt`

---

## Data ##

The dataset is available in the dataset folder as 'KARE-Sample.json'. The dataset contains the following information:

* dialogue_id: denotes an unique conversation number.

* utterance_no: denotes the utterance number in an ongoing conversation.	

* author_role: can take either of the two roles: agent/victim.
	** agent - the conversational agent acting as counselor to help the victim.
	** victim - user who is victim of some crime.	

* utterance: the text stated by agent/victim.

* knowledge: Knowledge associated with the dialogue.	


---

## Training ##

The EMPOWER model is trained in two levels. It is dual-tier deep prompt tuning approach. In the first level, it encapsulates the relevant knowledge into continuous knowledge-attributed deep prompts and in second level, it utilizes the encoded knowledge for knowledge-aware response generation.



**Stage 1: "KDPT: Knowledge-attributed Deep Prompt Tuning"**
For the first level training, run kdpt.sh script file.


**Stage 2: "RDPT: Response-attributed Deep Prompt Tuning"**
For RDPT tarining, run rdpt.sh script file.

---

## Inference ##
Once the training is finished, run the gen.sh script file to conduct the inference stage.




