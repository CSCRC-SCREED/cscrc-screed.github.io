# SCReeD Platform Overview 

<p align="justify">
SCReeD is a platform purposefully designed for sharing cybersecurity research data, including, but not limited to cybersecurity datasets generated by CSCRC research projects. For sharing cyber-datasets, general-purpose dataset sharing platforms are not ideal, and often not suitable, due to many reasons, such as the data sensitivity, volume, complexity, and wide range of file formats and serialisations typical to cybersecurity research datasets; also they can be authentic, synthetic, or hybrid, with different potential applications. In addition, a variety of audiences should be considered when sharing cybersecurity datasets, and all these require different levels of access, whether for CSCRC partners, Australian researchers, Australian industry practitioners, 5 Eyes researchers, the EU, or the world, which makes access control crucial in this application—compared to having only the option to share datasets with the general public, which is what many general-purpose/domain-independent dataset sharing platforms focus on.
</p>

<p align="justify">
The data captured in cybersecurity research datasets can be beneficial not only to the academic community, but also the industry in terms of adding new functionalities to, and test existing capabilities of, software tools; evaluating analytic performance of tools; assessing IT infrastructures’ vulnerability; identifying new types of cyberthreats, etc.
</p>

<p align="justify">
SCReeD defines standards for sharing cybersecurity datasets, provides guidelines for users so that the metadata to capture for cybersecurity datasets is streamlined, including technical and legal considerations, without the need for the uploader to be an expert in data sharing.
</p>

# SCReeD Dataset Uploading Guidelines  
<p align="justify">
The guidelines are provided for SCReeD users regarding dataset uploading, ensuring a systematic approach and inclusion of all relevant metadata. 
</p>

## Before Uploading
Before uploading, users need to do following steps.

* Be a member of [CSCRC-SCREED](https://github.com/CSCRC-SCREED) organization on GitHub. (Please contact masooma.iftikhar@data61.csiro.au for membership.)
* Prepare the dataset(s) according to the [SCReeD Dataset Preparation Guidelines](https://github.com/CSCRC-SCREED/cscrc-screed.github.io/blob/main/assets/docs/SCReeD%20Dataset%20Preparation%20Guidelines.docx) (Click View Raw to download).
* Download and fill all relevant metadata in the [SCReeD Dataset Declaration Form](https://github.com/CSCRC-SCREED/cscrc-screed.github.io/blob/main/assets/docs/SCReeD%20Dataset%20Declaration%20Form.docx) (Click View Raw to download).

## The Uploading Process
Once you are done During the uploading process, users need to attach a form with all the required metadata (see separate file)

To upload data, users need to do following steps:
* Go to [CSCRC-SCREED](https://github.com/CSCRC-SCREED) and login.
* Click repositories on the top to create a GitHub repository to host a dataset.Click on the **+** on the top right as shown below.

  ![How to create a GitHub repository to host a dataset](https://dataherb.github.io/assets/videos/dataherb-demo-ufo-create-new-repo.gif)
  
* Create a folder to hold your data file, in this example, we will create a folder called **dataset**. Click on the **Create new file** button, and type in **dataset/.githold**. This will create a folder called **dataset** and place a file called** .githold** inside it.

  [![How to upload data file](/assets/videos/video-preview.png)](https://dataherb.github.io/assets/videos/dataherb-demo-ufo-upload-datafile-1.mp4)

* Upload your data file into this folder by clicking on button **Upload files**.
*	Create a **.dataherb** folder in the root of your repository. Now the folder structure should be
  
   ![.dataherb folder structure](/assets/imgs/dataherb.png)
 	
*	Create a file **.gitattributes** in the **.dataherb** folder with the following content:\
  *.docx    binary\
  *.pdf     binary

 	
*	Upload the prepared **SCReeD Dataset Declaration Form** in the **.dataherb** folder by clicking on the **Add file** button, and select upload files. Then ** drag and drop** the prepared SCReeD Dataset Declaration Form to upload in the **.dataherb** folder.
*	Create a file metadata.yml in the .dataherb with the following content:
  
name: [Name of your dataset]
description: [Describe your dataset here]
contributors:
- name: [Name of the the first contributor]
data:
- name: [name of your data file, optional]
  description: [description of your data file, optional]
  path: [path_to_your_data_file.csv]
  format: csv
  size: [size of your data file]
  fields:
  - name: [name of the first colomn]
    description: [description of the first column]
  - name: [name of the second colomn]
    description: [description of the second column]
- name: [name of your second data file, optional]
  description: [description of your second data file, optional]
  path: [path_to_your_data_file.csv]
  format: csv
  size: [size of your data file]
  fields:
  - name: [name of the first colomn]
    description: [description of the first column]
  - name: [name of the second colomn]
    description: [description of the second column]
license:
- name: [Name of the license of the dataset]
  link: [Link to the license page]
references:
- name: [Name of the first reference]
  link: [https://link_to_your_first_reference]


* Now the uploaded process is complete, and you can view your dataset repositories as shown in the below example.

  ![Example Repo](/assets/imgs/example.png)










