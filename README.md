# InstantMD

![GitHub last commit](https://img.shields.io/github/last-commit/prakhar-ai/InstantMD)
![GitHub contributors](https://img.shields.io/github/contributors/prakhar-ai/InstantMD)

:trophy: Winner of the HealthCare Track at MINeD Hackathon

Instant MD is a Investigation, Medication and Chief Complaint recognition application using NLP

## Screenshots


![alt text](https://github.com/prakhar-ai/InstantMD/blob/main/appimage2.png?raw=true)

![alt text](https://github.com/prakhar-ai/InstantMD/blob/main/appimage.png?raw=true)

## Installation

##### Initialize a virtual environment

Windows:
```
$ python -m venv venv
$ venv\Scripts\activate.bat
```

Unix/MacOS:
```
$ python -m venv venv
$ source venv/bin/activate
```
##### Install the dependencies

```
$ pip install -r requirements.txt
```

##### Running the app

```
$ python app.py
```
## Hackathon Details

### College: Nirma University

### Team
#### DeepBlue
* Prakhar Jain
* Nikhil Rajput
* Parth Desai
* Parth Panchal
* Nora Surani

### Libraries Used

All libraries versions used are listed in [requirements.txt](https://github.com/prakhar-ai/InstantMD/blob/main/requirements.txt)

### Approach Used

Our NLP approach uses both text and sentence tokenization.

**No third party NLP libraries were used for the project and all pattern matching was done through Regex**

This helps us serve results instantly as opposed to using popular libraries like nltk or spacy, giving us the name **InstantMD**. We preserving sentence structure while also searching the tokenized words. We can then extract symptoms using a list of [symptom keywords](https://github.com/prakhar-ai/InstantMD/blob/main/symptom_list.txt) and the chief complaint by matching with the part of the anatomy that the patient is experiencing symptoms in. This is done through the [anatomy keywords](https://github.com/prakhar-ai/InstantMD/blob/main/anatomy_list.txt). Other factors are similarly extracted using keywords and rules designed by us and implemented through Regex. 

## Problem Statement
### Abstract
Being able to have machines understand unstructured textual content already plays a big part nowadays in our life. NLP can contribute largely to the advancement of medical science. NLP is used to extract information from free text narratives written by a variety of healthcare providers. Here we approach natural language processing algorithm where we

* Evaluate the free text and compare it with the dataset of NLP Dictionary.
* Annotated the important textual content from the text like Medication, Investigation (Pathology, Radiology), Chief Complaint.
* After Segregation the highlighted data should automatically enter the flow of EMR.

### Problem Definition
To develop a solution, the first step is to understand the problem. Develop an NLP module to identify the keywords related to a patient's investigation, medication and chief complaint from a free text in the text box. Highlight the extracted content and feed them as input in EMR’s Chief complaint, Investigation and Medication module.

