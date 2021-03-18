# CERN ATLAS  
## Autoencoders for Data Compression  
Implementing Autoencoder network for compressing 4 variables data to 3 variables.  

![Autoencoder Architecture](https://raw.githubusercontent.com/kahanikaar/ATLAS/main/autoencoder_fig(1)(1).png)  
  
### Libraries & Frameworks used
* Numpy
* Pandas
* PyTorch
* FastAI
* Matplotlib

### Network Configuration  
#### Without Batch Normalization  
##### Encoder  
Input Linear Layer of (4,200) - Linear Layer of (200,200) - Linear layer of (200,20) - Linear Layer of (20,3)  
##### Decoder  
Linear Layer of (3,20) - Linear layer of (20,200) - Linear layer of (200,200) - Output Linear Layer of (200,4)  
  
#### With Batch Normalization
##### Encoder  
Input Linear Layer of (4,200) - BatchNorm layer of 200 - Linear Layer of (200,200) - BatchNorm Layer of 200 - Linear layer of (200,20) - BatchNorm Layer of 20 - Linear Layer of (20,3)  
##### Decoder  
Linear Layer of (3,20) - BatchNorm Layer of 20 - Linear layer of (20,200) - BatchNorm Layer of 200 - Linear layer of (200,200) - BatchNorm Layer of 200 - Output Linear Layer of (200,4)
