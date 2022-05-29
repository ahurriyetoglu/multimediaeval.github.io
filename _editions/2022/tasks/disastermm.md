---
# static info
layout: task
year: 2022
hide: true  <!-- # change this to false once you finish editing-->

# required info
title: DisasterMM: Multimedia Analysis of Disaster-Related Social Media Data
subtitle: <!-- # leave this blanck-->
blurb: Social media data have been widely used in disaster management and proven valuable to all phases of a disaster: from early warning to nowcasting and from response to recovery. Nevertheless, the large streams of user-generated content can be very noisy and usually lack geoinformation, which is an essential attribute. DisasterMM aims to tackle these challenges with two subtasks: RCTP asks participants to build a classifier that will predict whether a tweet is relevant or not to a disaster, and in particular floods, while LETT calls for a text analysis technique that detects which words inside a Twitter message refer to a location. The dataset for RCTP will be circa 8,000 tweets and for LETT circa 6,000 tweets. Both datasets will be in Italian and manually annotated by native speakers. The evaluation metric for the two tasks will be the F1-score.
---

<!-- # please respect the structure below-->
*See the [MediaEval 2022 webpage](https://multimediaeval.github.io/editions/2022/) for information on how to register and participate.*

#### Task Description
The DisasterMM task concerns the multimedia analysis of social media data, specifically posts from the popular platform of Twitter, that relate to natural or manmade disasters; this year, in particular, the disaster of floods. The participants of this task are provided with a set of Tweet IDs in order to download textual as well as visual information and other metadata of tweets that have been selected with keyword-based search that involved words/phrases about flood. DisasterMM includes two subtasks. In “Relevance Classification of Twitter Posts” (RCTP) the participants are asked to build a binary classification system that will be able to distinguish whether a tweet is relevant or not to flooding incidents. On the other hand, in “Location Extraction from Twitter Texts” (LETT) the participants are requested to develop a named-entity recognition model in order to identify which words (or sequence of words) inside a tweet’s text refer to locations. For both subtasks, the dataset is in Italian language, so as to encourage researchers to move away from a focus on English.

#### Motivation and background
Flooding is considered the deadliest type of severe weather and it can have devastating effects on the society. Besides loss of lives and property damage, floods can also lead to secondary consequences, such as long-term displacement of residents and spread of waterborne diseases. In the last years, social media data and crowdsourcing in general have been explored by first responders and civil protection authorities as an alternative source of information, complementary to traditional means such as telephone, in order to raise the situational awareness and support their operations. In parallel, the scientific society has been proposing AI and machine learning solutions that improve the quality of the incoming social data.

Nevertheless, exploiting user-generated content from social media platforms comes with two significant limitations. First, the large and continuous streams of published posts can be very noisy, with messages that do not refer to actual cases of floods, but contain flood-related words in a different context (e.g. in a metaphorical way). Second, the majority of posts are not geotagged (i.e. associated with a geographic position) or their geoinformation is questionable.

The automatic prediction of a post’s relevance could reduce the social media noise and thus assist the interested parties in receiving only useful information, without spending time on filtering out unrelated messages. In addition, recognizing the locations that are mentioned inside the post’s text could enhance the post with geographic information, which would allow the automatic positioning of a potential incident. By receiving solely high-quality and geotagged social data, disaster management practitioners will be able to manage their resources more efficiently, which could even lead to saving more human lives.

Furthermore, taking into consideration that most research works that involve text analysis support the English language, we would like to motivate researchers to move away from this focus and investigate another language. Thus, the respective dataset will be in Italian. 

#### Target group
Researchers in the areas of social media, multimedia and multilingual analysis, multimedia classification, named-entity recognition and information retrieval are strongly encouraged to participate in the DisasterMM challenge. Industries and SMEs that develop similar AI technologies for semantic data fusion and retrieval of multi- or cross-lingual content are also warmly invited to participate. Moreover, the task could be of interest to researchers and practitioners in the domains of disaster management, emergency response, situational awareness, water management, and any other flood-related domains.

#### Data
The dataset for the RCTP subtask is a set of circa 8,000 social media posts collected from Twitter between May 25, 2020 and June 12, 2020, by searching for Italian keywords about floods (e.g. “alluvione”, “allagamento”, “esondazione” – all translated as flood). The ground truth of the dataset refers to the relevance of a tweet, i.e. 1 = relevant / 0 = not relevant.

The dataset for the LETT subtask consists of circa 6,000 social media posts collected from Twitter between March 25, 2017 and August 1, 2018, again by searching for Italian, flood-related keywords. The ground truth of this dataset involves the following labels for each word of a tweet text: “B-LOC” for the first word of a sequence that refers to a location or a single-word location, “I-LOC” for the subsequent word of a sequence that refers to a location, and “O” for any non-location word. For instance, the ground truth for the sentence “Allagamento in via Prati della Farnesina” is “O O B-LOC I-LOC I-LOC I-LOC”.

Both datasets have been manually annotated by native speakers that are employed by the Eastern Alps River Basin District, which is responsible for the hydrogeological defense and flood risk management in the Eastern Alps partition of North-East Italy.

It should be also noted that only the IDs of the tweets will be distributed to the participants, in order to be fully compliant with the Twitter Developer Agreement & Policy. However, a tool to download them will be provided, while for the LETT subtask the clean, processed sentences will be also shared, for a fairer evaluation.


#### Ground truth

#### Evaluation methodology
In RCTP, the evaluation metric for the binary classification of tweets as relevant (1) or not relevant (0) will be F1-score.

In LETT, F1-score will be used too, not in sentence level, but in word level. To further explain, if a given label for a word matches the label of the annotator for this particular word, then it is considered as true (true positive if “B-LOC” or “I-LOC”, true negative if “O”).

#### Quest for insight
* Does the involvement of visual features improve or deteriorate the classification prediction?
* What metadata can be useful in relevance classification?
* What types of posts are misclassified as relevant to flooding incidents?
* Is it easier to detect single-word or multi-word locations?
* What types of words are misrecognized as locations?
* What additional challenges are met when analyzing Italian text, compared to English?

#### References and recommended reading
[1] Andreadis, S., Gialampoukidis, I., Bozas, A., Moumtzidou, A., Fiorin, R., Lombardo, F., Karakostas, A., Norbiato, D., Vrochidis, S., Ferri,M., and Kompatsiaris, I., 2021, December. [WaterMM: Water Quality in Social Multimedia Task at MediaEval 2021](https://2021.multimediaeval.com/paper4.pdf). In Proceedings of the MediaEval 2021 Workshop, Online.

[2] Andreadis, S., Antzoulatos, G., Mavropoulos, T., Giannakeris, P., Tzionis, G., Pantelidis, N., Ioannidis, K., Karakostas, A., Gialampoukidis, I., Vrochidis, S., Kompatsiaris, I., 2021, May. [A social media analytics platform visualising the spread of COVID-19 in Italy via exploitation of automatically geotagged tweets](https://doi.org/10.1016/j.osnem.2021.100134). In Online Social Networks and Media Journal, Elsevier, Volume 23, pp. 100-134.

[3] Andreadis, S., Gialampoukidis, I., Karakostas, A., Vrochidis, S., Kompatsiaris, I., Fiorin, R., Norbiato, D. and Ferri, M., 2020, December. [The flood-related multimedia task at mediaeval 2020](http://ceur-ws.org/Vol-2882/paper5.pdf). In Proceedings of the MediaEval 2020 Workshop, Online (pp. 14-15).

[4] Moumtzidou, A., Andreadis, S., Gialampoukidis, I., Karakostas, A., Vrochidis, S. and Kompatsiaris, I., 2018, April. [Flood relevance estimation from visual and textual content in social media streams](https://dl.acm.org/doi/abs/10.1145/3184558.3191620). In Companion Proceedings of the The Web Conference 2018 (pp. 1621-1627).

#### Task organizers
* Lead task organizer: Stelios Andreadis, Information Technologies Institute - Centre of Research and Technology Hellas (ITI - CERTH), Greece, andreadisst@iti.gr
* Aristeidis Bozas, Information Technologies Institute - Centre of Research and Technology Hellas (ITI - CERTH), Greece
* Ilias Gialampoukidis, Information Technologies Institute - Centre of Research and Technology Hellas (ITI - CERTH), Greece
* Thanassis Mavropoulos, Information Technologies Institute - Centre of Research and Technology Hellas (ITI - CERTH), Greece
* Anastasia Moumtzidou, Information Technologies Institute - Centre of Research and Technology Hellas (ITI - CERTH), Greece
* Stefanos Vrochidis, Information Technologies Institute - Centre of Research and Technology Hellas (ITI - CERTH), Greece
* Ioannis Kompatsiaris, Information Technologies Institute - Centre of Research and Technology Hellas (ITI - CERTH), Greece
* Roberto Fiorin, Eastern Alps River Basin District, Italy
* Francesca Lombardo, Eastern Alps River Basin District, Italy
* Daniele Norbiato, Eastern Alps River Basin District, Italy
* Michele Ferri, Eastern Alps River Basin District, Italy

#### Task Schedule
* XX XXX: Data release <!-- # Replace XX with your date. We suggest setting the date in June-July-->
* XX November: Runs due <!-- # Replace XX with your date. We suggest setting enough time in order to have enough time to assess and return the results by the Results returned deadline-->
* XX November: Results returned  <!-- Replace XX with your date. Latest possible should be 10 November-->
* 21 November: Working notes paper  <!-- Fixed. Please do not change.-->
* Beginning December: MediaEval 2022 Workshop <!-- Fixed. Please do not change. Exact date to be decided-->
