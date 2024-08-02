# Solution approach
We defined a detector based on DNNs able to reveal the presence of malicious payloads, even when the attacker tries to implement basic evasion techniques such as obfuscation through compression or the use of alternative encoding schemes. 
Our approach focuses on processing and analysing the k LSBs of each pixel of the image under investigation. In essence, the k bits are used to yield a vectorial representation of the image to be offered to the DNN for the learning phase. The hidden layers combine this raw information and extract high-level discriminative features.

The DNN consists of a stack of different sub-nets. Each SubNet is composed of three main parts: a fully-connected dense layer equipped with a Rectified Linear Unit (ReLU), a batch-normalization layer and a dropout layer. The output layer of the DNN is instantiated on the basis of the specific task, detection or classification. 

## Dataset
Data used in our experimentation are reported in our work [Detection of Steganographic Threats Targeting Digital Images in Heterogeneous Ecosystems Through Machine Learning
]([https://github.com/Ocram95/Stego-Favicons-Dataset](https://isyou.info/jowua/papers/jowua-v13n3-4.pdf)).

## Authors
The code is developed and maintained by Massimo Guarascio, Nunziato Cassavia and Marco Zuppelli (massimo.guarascio@icar.cnr.it , nunziato.cassavia@icar.cnr.it, marco.zuppelli@ge.imati.cnr.it)

### Input details
We assume that the main directory includes a number of subfolders, one for each class (in our setting, legitimate favicons and the ones embedded with malicious payloads). Each subfolder contains the corresponding type of images.
