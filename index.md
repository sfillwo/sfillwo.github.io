# Profile
  <b>Ph.D., Computer Science (2024)</b>
  <br>
  <b>Emory University</b>
  <br><br>
  My research interests are in Conversational AI. 
  I have explored many facets of conversational systems, 
  including the development and deployment of a personal-experience-oriented dialogue system for large-scale usage 
  and improving the evaluation of dialogue models through fine-grained behavior analysis. 
  My most recent and ongoing works focus on improving social understanding and commonsense reasoning in dialogue models in the era of Large Language Models. 
  <br><br>
  <em>Awards:</em>
  <br>
  Amazon Alexa Prize 3 Winner
  <br>
  Emory George W. Woodruff Fellowship
  <br>
  Emory Schoettle Research Award
  <br>

# Portfolio

===
## Deployed Dialogue Systems
===


### Emora Chatbot: Winner of Amazon Alexa Prize 3

**Overview:** The goal of the Amazon Alexa Prize was to develop the most engaging and capable dialogue agent. We were one of 10 teams invited to participate based on our proposal, out of approximately 400 applicants. The competition lasted from August 2019 to July 2020, in which we developed and deployed our chatbot Emora to Amazon Alexa Devices that any user could connect to. In July 2020, we won this year's competition, advancing through two elimination rounds based on user ratings and then receiving the highest overall rating from the panel of final invited judges.

**Role:** I was the co-team-lead for Emory University's 14-person student team participating in the 3rd Amazon Alexa Prize. As co-team-lead, I held weekly meetings with Amazon to present our team's progress and coordinate team functions within the schedule of the competition. Towards Emora development, I planned and designed the Emora's overall vision and design in collaboration with the other team lead, as well as input from the rest of the developers on the team. I was also responsible for multiple dialogue topic handlers, creating conversational flows for topics including science fiction and teleportation, family/work/school-life, and pets.

An example conversation Emora can hold:
<img src="images/emora_convo_example.png"/>

The user ratings Emora received during the quarter and semifinal rounds of the competition:
<img src="images/dailyrating.png"/>

The system architecture of the Emora Chatbot:
<img src="images/architecture.png"/>

An illustration of the core dialogue logic representing the state-machine-based dialogue flow:
<img src="images/statemachine.png"/>

**More Information:**
* Read the Amazon Technical Proceedings paper [here](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexaprize/assets/challenge3/proceedings/Emory-Emora.pdf)

* &#9733; Code for running the winning Emora is available at the [Emora Github Repository](https://github.com/emora-chat/emora_ap3_parlai).

* Emora in the News in an [Amazon Article](https://www.amazon.science/latest-news/alexa-prize-interviews?fbclid=IwAR2Iu7HwssbVvqmy1AB2gSOtZfoOps5nbxcpQqlTLgrz1czMtWnEH5X1JVY) and an [Emory Article](https://news.emory.edu/stories/2020/08/er_alexa_prize/campus.html)!

* Learn more about Emora from our [Youtube Playlist](https://www.youtube.com/playlist?list=PLsMGYQfhCveJE1uSslBZjoiRAVHDJoiQa)!

---

### Article QABot using Generative AI

**Overview:** My internship at Got It AI focused on the development of an article-grounded conversational question-answering dialogue system that ingests online FAQ documents in order to offer customer support. 

**Role:** I led the development and execution of this project, under the supervision of my supervisor. I worked on the evaluation and integration of numerous approaches to dialogue-relevant tasks into the dialogue system, including information-retrieval, hallucination-detection, and response generation, focusing on prompt-based large language model approaches. By the end of my internship, I had implemented and deployed an initial fully-functional version of the Article QABot internally to the company.

An example prompt Article QABot uses to generate a response for user input "can I apply the morning glow serum at night?"
<div style="border: 2px solid black; display: inline-block; padding: 10px;">
  <img src="images/articlebot_response_example.png"/>
</div>

The overall Article QABot architecture:
<img src="images/articlebot_architecture.png"/>

The results of my prompt development on measured response correctness for Article QABot:
<img src="images/articlebot_response_prompt_improvement.png"/>

---

### Emory Virtual Assistant

**Overview:** The Emory Virtual Assistant is developed to provide both a companion role, talking to students about their daily lives, as well as an administrative role, handling inter-user messages and professor-student meeting scheduling.

**Role:** I was a Senior Research Mentor to a group of undergraduate students who were developed a virtual assistant for Emory students and professors.  I attended weekly meetings in which the development team gave status updates and provided guidance towards the design and implementation of the virtual assistant. In addition, I implemented a MongoDB wrapper for the developers to use that simplified the access patterns to the MongoDB infrastructure.

This is an example of a conversation with the companion role of the virtual assistant:
<img src="images/companion_bot_example.png"/>

This is an example of a conversation with the administrative role of the virtual assistant:
<img src="images/assistant_bot_example.png"/>




===
## Dialogue Commonsense
===

### Improving Commonsense Modeling for Dialogue: ConvoSense

**Overview:** ConvoSense addresses the limitations of existing dialogue datasets in commonsense reasoning by introducing a new synthetic dataset using ChatGPT. ConvoSense boasts greater contextual novelty, a higher volume of inferences per example, and substantially enriched detail than previous datasets. The final collected dataset includes over 500,000 inferences across 12,000 dialogues with 10 popular inference types. I then use this dataset to train more efficient T5 models that are proven to produce more plausible and novel inferences compared to those trained on previous datasets.

**Role:** I was first author on the ConvoSense paper. I tested several strategies for commonsense generation using ChatGPT, leading to the construction of 15 prompts corresponding to 15 commonsense types. I implemented and conducted the collection of the full ConvoSense dataset as well as the subsequent T5 model development. 

Example commonsense inference outputs of the ConvoSense-trained model:
<img src="images/convosense_model_example_edit.png"/>

Illustration of the ConvoSense ChatGPT framework including an example of the prompt: 
<img src="images/convosense_design.png"/>

Empirical results from human evaluation demonstrating the superiority of the ConvoSense-trained model against a model trained on the existing human datasets:
<img src="images/convosense_model_results.png"/>

**More Information:**

* Read the TACL 2024 paper [here](https://aclanthology.org/2023.acl-long.839/)!

* &#9733; Code for the ConvoSense project is available at the [Github repository]()

* &#9733; **Trained Model:** Our best-performing ConvoSense-trained model is released through HuggingFace [here](https://huggingface.co/sefinch/ConvoSenseGenerator)!

---

### Explicit Reasoning over Commonsense for Dialogue Response Generation

**Overview:** This project explored the impact of explicit reasoning against implicit reasoning over commonsense for dialogue response generation by leveraging Large Language Models to implement these strategies. The findings demonstrate that explicit reasoning leads to better dialogue interactions, improving naturalness, engagement, specificity, and overall response quality. Further experiments underscore the advantage of explicit reasoning by contrasting it with both the state-of-the-art in commonsense-grounded and commonsense-less dialogue models.

**Role:** I was first author on this project. I tested many implementations of these strategies to identify the best-performing prompts for both explicit and implicit reasoning over commonsense for response generation. I then developed the final dialogue approaches using the identified optimal prompts, and designed and conducted the human evaluation of these approaches.

Diagram portraying motivation of explicit reasoning over commonsense inferences to guide follow-up response generation:
<img src="images/dialogue-commonsense-example_cropped.png"/>

Illustrative responses generated through explicit reasoning (CS-E) and implicit reasoning (CS-I) as well as baseline models (Doctor, ChatGPT):
<img src="images/rgcs_example.png"/>

Human evaluation results showing superiority of explicit reasoning (ConvoSense-E) against alternative approaches:
<img src="images/rgcs_results.png"/>


===
## Dialogue Evaluation
===

### Novel Fine-grained Dialogue System Evaluation: Annotation of Behaviors in Chat Evaluation (ABC-Eval)

**Overview:** This project presents a novel evaluation framework for chat-oriented dialogue systems that measures the rate of 16 different dialogue behaviors that can be expressed by chatbots. ABC-Eval is shown to be a more reliable, discriminative, and informative evaluation of chatbots compared to the standard evaluations using Likert ratings or Pairwise Comparisons.

**Role:** I was co-first-author on the ABC-Eval paper. My unique contributions to this project were the development of the web-based annotation platform for ABC-Eval that was built on top of the ParlAI Javascript framework with major modifications to support the annotation requirements of the 16 ABC-Eval tasks. In addition, my co-author and I collaborated to identify, design, and pilot the 16 different dialogue behaviors covered by ABC-Eval.

The online interface for annotating the usage of Correct Facts and Incorrect Facts:
<img src="images/interface_knowledge.png"/>

The online interface for annotating consistency mistakes, including Self Contradictions, Partner Contradictions, and Redundant responses:
<img src="images/interface_consistency.png"/>

The online interface for annotating Empathetic responses and responses that convey a Lack of Empathy:
<img src="images/interface_empathy (1).png"/>

**More Information:**

* Read the ACL 2023 paper [here](https://aclanthology.org/2023.acl-long.839/)!

* &#9733; Code for running the ABC-Eval platform is available at the [Github repository](https://github.com/emorynlp/ChatEvaluationPlatform)


---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
