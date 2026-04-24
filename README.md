Transformer based architecture of LLMs revolutionized how machines understand,generate and predict human-like text.However, despite their impressive performance, there remains a Fundamental Question: 

Do these LLMs unintentionally interpret a sentence similar to how humans interpret it?
Do LLMs develop an innate understanding of the grammar relationships between words automatically like humans do.

Motivation:

Through this project we aim to perform the first comprehensive evaluation of the specific grammar that emerges within LLMs. This study seeks to quantify exactly what kind of dependency grammar they have actually developed.
One of the main motivation is to establish a framework to differentiate between different types of linguistic learning:
Inductive Learning: Identifying which grammatical rules and linguistic constraints can be learned simply by processing massive amounts of data.
Innate Constraints: Determining which linguistic structures cannot be picked up through inductive learning alone.
Also there is a potential to gain some new insights into how humans comprehend sentences. By comparing the mathematical distributions of dependency structures in LLMs against structures from human-verified datasets (UD corpus),we can see how closely the understanding of these models mirrors human linguistic patterns.
Hypothesis:
The primary hypothesis is that the model develops the understanding of the grammar dependency as a by product of their training, the process of optimizing for this task forces the model to discover the underlying syntactic rules of a language 
Prediction: The LLMs would have a very high accuracy when compared to UD corpus.
Specific attention heads are not general-purpose but are instead highly specialized to identify and govern specific dependency relations These heads function similarly to cue-based retrieval in human cognitive memory models, allowing the model to pull relevant grammatical information from earlier in a sentence to process the current word correctly 
Prediction: The specific attention heads within the model will be found to focus almost exclusively on specific dependency relations, such as subject-verb or head-modifier links and as these specialized heads do the heavy lifting the project predicts that their performance is critical to the model's overall grammatical accuracy. 
