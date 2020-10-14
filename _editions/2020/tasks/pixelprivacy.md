---
# static info
layout: task
year: 2020
hide: false

# required info
title: "Pixel Privacy: Quality Camouflage for Social Images"
subtitle: 
blurb: In this task, participants develop adversarial approaches that camouflage the quality of images. A camouflaged image appears to be unchanged, or even enhanced, to the human eye. At the same time, the image will fool a Blind Image Quality Assessment algorithm into predicting that its quality is low. Quality camouflage will help to ensure that personal photos, e.g., vacation photos depicting people, are less easily findable via image search engines.
---

<!-- # please respect the structure below-->
*See the [MediaEval 2020 webpage](https://multimediaeval.github.io/editions/2020/) for information on how to register and participate.*

#### Task Description
High-quality images shared online can be misappropriated for promotional goals. In this task, participants work to defeat an automatic image quality classifier, which effectively hides images.
The camouflaged image appears to be appealing to the human eye, but the Blind Image Quality Assessment (BIQA) classifier finds it to be low quality, i.e., there is a dramatic descrease in the image's automatically predicted quality score.

Participants will receive a set of images (representative of images shared on social media) and are required to modify them. The modification should achieve two goals: (1) Protection: It must block the ability of a binary BIQA classifier from correctly predicting the quality of images and (2) Appeal: The changes made to the image must be as imperceptible to the human eye as possible, or the changes must contribute to enhancing the appeal of the image.
Note that the task is not focused on concealing sensitive information from humans, rather from automatic inference. 

This year the quality camouflage task is a "whitebox" attack. Participants' goal is to defeat a BIQA that predicts the perceptual quality of images. The BIQA is trained on KonIQ-10k, which contains 10,073 in-the-wild images annotated with subjective quality scores. 

Participants can choose to address the task in one of two different ways. In the first, the quality camouflage approach seeks to make invisible changes to the image. In the second, the approach makes visible changes to the image, but restricts itself to changes that enhance the image’s appeal, or at least do not bother someone looking at the image.

We encourage participants to release their code. 

#### Background and Motivation
Conventionally, adversarial images are studied in the context of scenarios in which they can cause harm by misleading computer vision system. *Pixel Privacy* introduces the notion that adversarial images can serve another goal as well: protect privacy-sensitive information in cases in which the computer vision system itself may be a source of harm. An important example is image search engines that can find images of people who are pictured in a specific location or setting. In the past installment of the task, we have investigated how adversarial images can effectively prevent the inference of semantic information concerning the scene of an image.

Semantic information, is not, however, the only characteristic that a search engine uses in order to return a results list to a user. Another characteristic is automatically-inferred image quality. In the 2020 Pixel Privacy task we turn our attention to *quality camouflage*, i.e., approaches which can cause a Blind Image Quality Assessment (BIQA) to misclassify an image as low quality, when it appears to be high quality to the human eye. Quality camouflage will help to ensure that personal photos reflecting sensitive scene information, e.g., vacation photos depicting people, are less easily findable via image search engines. 

<!--#### Motivation and Background-->
#### Target Group
We hope that this task attracts a wide range of participants who are concerned about privacy from computer scientists to artists and photographers. Within the field of computer science, people interested in machine learning, adversarial machine learning, computer graphics, privacy, and computer vision will find the task interesting.

#### Data
Development data will be the KonIQ-10k data set. Test data will be selected from the validation set of the Places365, and different from previous editions, we will use high-resolution images for ensuring relatively high quality. Participants are provided with a set of correctly classified images that are also predicted to have ‘good quality’ by the BIQA model. 

#### Evaluation Methodology
The protection score will be the accuracy of the BIQA prediction on modified images by participants. We specify the threshold that is to be used by BIQA. Note that we expect that accuracy to decrease after protection, but theoretically it is also possible that protection fails, and that it stays the same. 

We appreciate approaches that are robust against practical post-processing operations. So the submitted images will be evaluated on their slightly JPEG compressed (quality factor = 90%) version. We have confirmed such compression has little impact on the BIQA scores.

Appeal will be evaluated by a jury of computer vision experts. Submissions will be ranked as follows: All approaches that achieve a protection score of at least 50% (50% reduction in the accuracy of the prediction) will be ranked in terms of their appeal by the jury.

#### References and recommended reading
<!-- # Please use the ACM format for references https://www.acm.org/publications/authors/reference-formatting (but no DOI needed)-->
<!-- # The paper title should be a hyperlink leading to the paper online-->
Vlad Hosu, Hanhe Lin, Tamas Sziranyi and Dietmar Saupe. [KonIQ-10k: An Ecologically Valid Database for Deep Learning of Blind Image Quality Assessment](https://ieeexplore.ieee.org/document/8968750). In IEEE Transactions on Image Processing 29, (Jan. 2020), 4041-4056.

Samuel Dodge, and Lina Karam. [Understanding How Image Quality Affects Deep Neural Networks](https://ieeexplore.ieee.org/document/7498955). In Proceedings of 8th International Conference on Quality of Multimedia Experience (QoMEX '16). IEEE, 1-6.

Ian J. Goodfellow, Jonathon Shlens, and Christian Szegedy.[Explaining and Harnessing Adversarial Examples](https://arxiv.org/abs/1412.6572). International Conference on Learning Representations (ICLR '15).

Pixel Privacy Task. 2018. Working Notes Proceedings of the MediaEval 2018 Workshop. Retrieved from http://ceur-ws.org/Vol-2283/

Nilaksh Das, Madhuri Shanbhogue, Shang-Tse Chen, Fred Hohman, Siwei Li, Li Chen, Michael E. Kounavis, and Duen Horng Chau. 2018. [SHIELD: Fast, Practical Defense and Vaccination for Deep Learning using JPEG Compression](https://dl.acm.org/doi/10.1145/3219819.3219910). In Proceedings of the 24th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining (KDD ’18). Association for Computing Machinery, New York, NY, USA, 196–204.

Zhengyu Zhao, Zhuoran Liu, and Martha Larson. 2020. [Adversarial Color Enhancement: Generating Unrestricted Adversarial Images by Optimizing a Color Filter](https://arxiv.org/abs/2002.01008). In Proceedings of the 31th British Machine Vision Conference (BMVC '20).

<!-- # add a note to check out Pixel Privacy in past proceedings; also think about some other references-->

#### Task Organizers
<!-- # add the email address of the contact organizer-->
<p>Zhuoran Liu, Radboud University, Netherlands, z.liu (at) cs.ru.nl<br />
Zhengyu Zhao, Radboud University, Netherlands<br />
Martha Larson, Radboud University, Netherlands<br />
Laurent Amsaleg, CNRS-IRISA, France</p>



<!--#### Task Auxiliaries-->
<!-- # if there are people helping with the task, but are not bearing the main responsibility for the task, they are auxiliaries. Please delete this heading if you have no auxiliaries-->

#### Task Schedule
* 31 July: Data release <!-- # Replace XX with your date. Latest possible is 31 July-->
* 31 October: Runs due <!-- # Replace XX with your date. Latest possible is 31 October-->
* 15 November: Results returned  <!-- Fixed. Please do not change-->
* 30 November: Working notes paper  <!-- Fixed. Please do not change-->
* Early December: MediaEval 2020 Workshop <!-- Fixed. Please do not change-->

Workshop will be held online. Exact dates to be announced.