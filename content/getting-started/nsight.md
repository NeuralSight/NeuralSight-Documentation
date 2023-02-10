---
title: Get-to-Understand-NeuralSight-AI
weight: 8
---


## What is in this Documentation?
This repository contains a non technical overview of the project NeuralSight. It explain in brief about the solution, the objective and requirements of the project. It also gives an oveview of how to aqquire data necessary to successfully run the project, how to de-identify the data to protect patient information and the process of data annotation.

You will get to understand Quality control methods and approaches to data modelling to successfully build deep learning algorithms and performance evaluation that gives you a better view on how to ensure you develop a reliable and accurate Ai algorithm.

Lastly, we will take you through the project roadmap and future technology innovations to be implemented by Neural Labs Africa. 

## Table of Contents
* Introduction
* The Solution
* Objective 
* Project Requirements
* Data Acquisition
* Data De-identification
* Data Annotation
* Quality Control
* Data Modeling 
* Performance evaluation 
* Software Road Map 
* Future Technology Innovations 
* Obstacles of AI in Medical Imaging

## Important Resources:
1. [NeuralSight Project Documentation](https://neuralsight.github.io/NeuralSight_Docs/)
2. [NeuralSight AI Repository](https://github.com/NeuralSight/NeuralSight_AI/)
3. [NeuralSight Frontend Repository](https://github.com/NeuralSight/NeuralSight_frontend)
4. [Company Charter](https://github.com/NeuralSight/NeuralSight_Docs)
5. [Have a new Feature or an Issue you want fixed?](https://github.com/NeuralSight/NeuralSight_AI/tree/main/.github/ISSUE_TEMPLATE)


### 1. Introduction
Radiologists are faced with a high volume of medical images and a shortage of radiologists. Across the world, there's also an exponential increase in the number of patients who need radiology services. Our solution is deep learning and computer vision based technology that screens medical images in real time, helping Radiologists save time, reduce radiation exposure for patients, and improve patient experience.

We are proposing web Software as a service (SAAS) and mobile application( to be developed in the future) that will be  accessible to medical practitioners such as radiologists, radiographers, hospitals and diagnostic centres. This involves developing an application based on the DICOM standard which allows the upload of medical images such as digital radiography, ultrasonography,  secondary pictures and scanned images, digital angiography etc.,in various formats (JPEG,PNG ) be it monochromatic, coloured,  static images, uncompressed and compressed images. 

### 2. The Solution
Our AI algorithm NeuralSight™ is capable of identifying 15 respiratory and heart diseases which include: Pneumonia, COVID-19, Aortic enlargement, Atelectasis, Calcification, Cardiomegaly,Consolidation, Interstitial Lung Disease (ILD), Infiltration, Lung Opacity, Nodule/Mass, Pleural effusion, Pleural thickening, Pneumothorax, Pulmonary fibrosis  in Real Time. The ability to quantify the percentage of the lung affected due to lesions enables objective monitoring of disease progression.

We have evaluated and identified the problems faced by medical practitioners in Africa. Doctors and clinicians need the following for a successful deployment of AI solution in the clinical environment:
Models trained on datasets that represent the population;
Seamless integration into clinical workflows;
A technology platform to connect research and hospitals.
Automatically highlighting areas of pathology and calculating parameters to determine a diagnosis. In a perfect case scenario, algorithms will be able to create a pre-filled medical opinion using a variety of similar cases. In this case, the doctor will either approve or disapprove of the medical statement and thus save time.


### 3. Objective
NeuralSight is able to localize, qualify the lesions and score in under a minute, enabling clinicians to classify patients into priority categories: high, medium, low and none. The ability to quantify the percentage of the lung affected due to lesions enables objective monitoring of disease progression.
Ai-powered program management for tracking end-to-end disease management.


### 4. Project Requirements
The success of the project development is dependent on key factors that will influence the accuracy, efficiency and reliability of the platform. That said, some of these factors do not have a replacement hence due diligence on the cost, ease of access and value addition have to be placed in consideration by both the management and tech team at Neural Labs Africa.

These requirements include;
* Consultant Radiologist
* Complete Developer team(Frontend Dev/ Full-Stack Dev, Data Scientist, Machine Learning Engineer(MLOps) and UI/UX Designers)
* Advisory Board, both medical and business
* Research & Development team


### 5. Data Acquisition
Medical image data are acquired for different purposes, such as diagnosis, therapy planning, intraoperative navigation, post-operative monitoring, and biomedical research. Major requirements that guide the selection of imaging modalities in practice include:
the relevant anatomy must be depicted completely,
the resolution of the data should be sufficient to answer specific diagnostic and therapeutic questions,
the image quality with respect to contrast, signal-to-noise ratio (SNR) and artifacts must be sufficient to interpret the data with respect to diagnostic and therapeutic questions,
exposure and burden to the patient and to the medical doctor should be minimized, and
costs should be limited.


### 6. Data De-identification
According to the U.S. Health Insurance Portability and Accountability Act, or HIPAA, and the European General Data Protection Regulation, both retrospectively and prospectively gathered data require proper de-identification. Sensitive information includes but is not limited to name, medical record number, and date of birth. Identifiable information is commonly available in DICOM metadata(header) and multiple tools are available to automatically remove this information. When radiology data is shared in open-source research efforts, the DICOM metadata is often removed completely or converted to another format such as Neuroimaging Informatics Technology Initiative, or NIFTI, which retains only voxel size and patient position. Totally removing the DICOM metadata for open-source research efforts prevents privacy issues but reduces the value of data, because metadata is important for AI algorithm development.

### 7. Data Annotation
Medical image annotation is the process of labeling medical imaging data such as X-Ray, CT, MRI scans, Mammography, or Ultrasound. It is used to train AI algorithms for medical image analysis and diagnostics, helping doctors save time, make better-informed decisions, and improve patient outcomes. 

Image labels are annotations performed by medical experts such as radiologists. These annotations can be considered ground truth if imaging is the reference standard (eg, pneumothorax). Choosing the appropriate label for a given imaging AI application requires a balance between finding the best discriminating categories (ie, normal vs emergent) and clinically relevant granularity (ie, subtype of liver lesion) depending on the desired task. With the exception of AI methods that enhance image quality, medical images in isolation are generally not suitable for developing diagnostic AI models unless associated with a diagnosis through the free-text radiology report (which require additional labeling strategies discussed below), expert consensus, segmentation, or an applied ground truth label such as electronic phenotyping.

### 8. Quality Control
Medical Quality Control (QC) refers to the specific test required to ensure effective and safe equipment performance. QC tests check the performance of the equipment under routine clinical conditions, following established protocols for facilities, equipment and procedures. Quality Assurance involves planned and systematic actions that will produce consistently high quality images with minimum exposure of the patients and workers. Quality Assurance actions include both "Quality Control Techniques" and "Quality administration procedures".

* "Quality Assurance Program" means an organized entity designed to provide quality assurance for a Radiology facility.
* "Quality Control Techniques" are those techniques used in the monitoring, testing, and maintenance of the components of radiology equipment.
* "Quality Control Procedures" are the procedures that provide the organizational framework for the "Quality Assurance Program". They are the actions that guarantee that the monitoring techniques are uniformly performed and evaluated and that necessary 

Quality Assurance Program in radiology facility is determined by an analysis of the facility's objectives and resources and should include the following major constituents:
* Responsibilities
* Purchase specifications
* Standards for Image Quality
* Monitoring and Maintenance programs
* Installation/Operational/ Performance qualifications of equipment
* Records
* Quality Assurance Manual
* Training

### 9. Data Modeling 
NeuralSight is implemented using federated learning architecture.

<img align="centre" src="https://github.com/NeuralSight/Get-to-Understand-NeuralSight-AI/blob/main/images/data-modeling.png" width="960" height="712" /><img align="centre" src="https://github.com/NeuralSight/Get-to-Understand-NeuralSight-AI/blob/main/images/data-modeling2.png" width="960" height="256" />

### 10. Performance evaluation 
The proper functional performance of the AI solution in pathology is also assessed in regulatory procedures. In the EU, the performance evaluation required has three aspects: 
Scientific validity: Shows valid association between the software output and the targeted clinical condition. 
Analytical performance: Shows that the software produces accurate and reliable output.
Clinical performance: Shows that the output meets the intended purpose in a clinical context and for the target population.

#### Detection of different findings on chest x rays
Annotation of the findings.(Drawing bounding boxes).
Classify patients into priority categories: high, medium, low and none.
Flag abnormal scans


### 11. Software Road Map 
### Research Prototype
* Defined task and found applicable algorithmic approach.
* Tested feasibility of algorithm on first data.
* Evaluated performance of algorithm on limited dataset.

#### Clinical Prototype
* Evaluated algorithm on real-world data from routine pathology.
* Integrated solution prototype usable by developers.
* Prototype evaluated in routine pathology.

#### Product
* Documented test results and performance assessment for regulatory approval.
* Solution in production use in routine pathology.
<img align="centre" src="https://github.com/NeuralSight/Get-to-Understand-NeuralSight-AI/blob/main/images/roadmap.png" width="712" height="512" />

#### Integration
AI solutions in pathology are usually standalone tools, each having its  own interface for data input, output and execution. To ensure flawless usability in diagnostic routine, these tools must be integrated into the laboratory IT infrastructure and made interoperable with software developed by other manufaturers.

<img align="centre" src="https://github.com/NeuralSight/Get-to-Understand-NeuralSight-AI/blob/main/images/infrustructure.png" width="712" height="512" />

To use AI solutions in pathology you would require three pieces of software. 
* Image Archive
* Lab Information System
* Pathology Workstation


#### Integration of artificial intelligence
Integration of AI solutions into the laboratory IT infrastructure can be done as either standalone tools or workstation extensions. One huge advantage of standalone tools is their flexibility. This means they can be tailored to the specific needs of the analysis methods in terms of user interaction, parameterization and visualization. Workstation extensions, on the other hand, have the major advantage of workflow efficiency. They can be used without having to leave familiar workstation environments and without having to learn new tools. They also have a low development cost and are very interoperable software from other manufacturers. 


#### Cooperation is crucial
It is important for Neural Labs Africa to involve pathologists from an early stage of development. To obtain sufficient amounts of training and test data, partnerships must be established with pathologists and incentives be provided for them to provide image data and required annotations. Partnerships with multiple laboratories is essential in order to obtain a sample of interlaboratory variability.


#### Other challenges
There are further challenges in producing AI solutions that are beyond the scope of this report. This concerns the many algorithmic challenges associated with AI development, which have already been addressed in numerous publications. Other concerns include issues of usability and user experience.


### 12. Future Technology Innovations 
Neural Labs Africa has a bright vision to empower doctors and partners in the medical field with the aim of enabling access to diagnostic healthcare for all in Africa. We are looking into researching in different sectors using AI for Clinical Decision Support System (СDSS). Some of these areas include:
* AI-based software that enables doctors to calculate parameters for surgeries automatically, which allows them to avoid miscalculations and transfer the patient to the surgery department faster.
* AI-based analytics for screenings, precision medicine, and risk assessment to help doctors look at the genetics, environment, and lifestyle of a person in order to select a treatment that could work best for them.
* Monitoring nurses’ and doctors’ actions can help maintain patient bypass schedules. AI-driven video analytics can detect whether or not the patient was given the right medicine at the right time.

#### Who is to Benefit?
Healthcare is one of the few areas where even the slightest mistake can be critical. Both healthy people and hospital patients can receive an accurate doctor’s diagnosis, prescriptions, and recommendations.

Doctors are, first of all, people, and people can be distracted or tired. While everything depends on their decision, we need to develop more automated diagnostics solutions to help them identify conditions quicker, promoting early intervention.

Researchers have to go through vast amounts of data daily when discovering new drugs, conducting genetic research, or clinical trials. With AI-driven technology in medical imaging, they can process even larger data sets, approve new-to-market medications faster, and drive advances in modern healthcare.

Healthcare institutions can take advantage of computer vision technologies to manage operational processes. A few application examples would be monitoring staff activities or online check-in terminals.

Governments can predict the spread of viruses and diseases by analyzing large amounts of data.

### 13. Obstacles of AI in Medical Imaging
* #### Decentralized storage
Medical institutions usually store patient data on their local systems. The problem is that there is no centralized storage for the entire medical history of all patients. By analyzing big data individually and in combination, we can improve and control the quality of diagnostics and predict the course of diseases.

* #### General Data Protection Regulations Compliance
General Data Protection Regulations do not clearly explain the relationship between the developer and the medical personnel. The lack of transparent legal mechanisms delays the broader adoption of AI in medical imaging. Another technical issue is the time-consuming legalization of computer vision and AI-based solutions. The product must be registered and undergo various tests before being used in medical practice.

* #### Difficulties in Organizing Expert Consensus
It takes more than one doctor to train neural networks while developing a CDSS (Clinical Decision Support System) solution. Five or more specialists must verify the results before making a solid conclusion to avoid misinterpretations and mistakes that can be critical.
* #### Conservatism
The medical community’s reluctance to embrace a new product is normal. The only thing that can help overcome the issue is the increasing implementation of successful use cases confirming the effectiveness of innovative solutions.

> **Frankly, AI isn’t going to replace clinicians, it isn’t going to remove enormous amounts of workload and it certainly isn’t going to autonomously make treatment decisions. Those aren’t the problems that need to be solved right now and AI in healthcare is not going to be given the opportunity to run before it can walk (nor should it).**
