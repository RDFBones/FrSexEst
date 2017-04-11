# Extension “Freiburg Sex Estimation” for RDFBones-O
## Anthropological background
This is an extension for the sex estimation of adults utilising cranial and mandibular traits. It is based on the data entry form for the sex estimation of adults used by Biological Anthropology Freiburg. The morphological methods applied in FrSexEst are based on the scoring system developed by Acsádi & Nemeskéri 1970 and adjusted by Ferembach et al. 1979. The evaluated traits and their respective weights (in brackets) in the calculation of the degree of sexualization are as follows:


### Cranium:

•	Glabella (3)

•	Mastoid process (3)

•	Nuchal planum (3)

•	Zygomatic process (3)

•	Superciliary arch (2)

•	Frontal and parietal eminences (2)

•	Zygomatics (2)

•	Supramastoid crest (2)

•	External occipital protuberance (2)

•	Orbital aperture (1)


### Mandible:

•	Mandible as a whole (3)

•	Mental protuberance (2)

•	Gonial angle (2)

•	Mylohyoid line (1)


These ten cranial and four mandibular traits and their respective weights are in general according to Ferembach et al. 1979 except for the frontal inclination of the skull and the supraorbital margin which are not part of FrSexEst.
The traits of FrSexEst were used in the sex estimation of skulls from the Alexander-Ecker-Collection in Freiburg (for further information on the Alexander-Ecker-Collection cf. Kästner et al. 2011). Thus, the collected data from the Alexander-Ecker-Collection can be digitized and made accessible for future research within the flexible RDFBones ontology by means of this extension. 
FrSexEst can be applied to estimate the sex of any adult human skull, of course. By adding the frontal inclination and the supraorbital margin, another extension can easily be created which is then fully congruent with Ferembach et al. 1979.


## References:
Acsádi, György, and Janos Nemeskéri. "History of human life span and mortality." Budapest: Acad. Kaido (1970).

Ferembach, Denise, Ilse Schwidetzky, and Milan Stloukal. "Empfehlungen für die Alters- und Geschlechtsdiagnose am Skelett.(Recommandations pour le diagnostic de l'âge et du sexe sur les squelettes)." Homo Göttingen 30.2 (1979): 1-32.

Kästner, M., Ortolf, S., Rüdell, A., Möller, D., & Wittwer-Backofen, U. (2011). The Alexander Ecker Collection in Freiburg. Documenta Archaeobiologiae, 8, 275-284.


## Wiki index
The Wiki for FrSexEst is a thorough online documentation of the FrSexEst ontology (https://github.com/RDFBones/FrSexEst/wiki). This Wiki should satisfy two objectives at once. On the one hand, the Wiki contains further information about the extension itself (mostly network graphs) and some general tips for writing extensions to make FrSexEst understandable and a valuable resource for programmers interested in writing their own extensions.  On the other hand, it explicates the workflow of a FrSexEst investigation for anthropologists interested in carrying out sex estimations accordingly and archiving research data. The Wiki provides further information on the following topics:


•	General structure of FrSexEst

•	Investigation planning

•	Study design execution

•	Drawing a conclusion

•	General tips for extension writing

## For future development
* Implement a R-package which automatically calculates the degree of sexualization from the sex scores
* Find a common data property to add text/strings to instances of ConclusionTextualEntity instead of the FrSexEst specific 'has text'
* Formulate a concrete idea of how documentig works
* Add a secondary skeletal inventory which refers directly to anatomical traits, for example the Glabella instead of frontal bone as input of the specimen collection process
* Since investigations correspond to the sex estimation of a single human skull, we need a sophisticated way to relate several investigations to a higher level research project
* Use cardinality restrictions more rigorously. For example, each investigation has exactly 1 study design execution, which has max. 1 Assay.Glabella and max. 1 Calculate_WeightedSexScore.Glabella but exactly 1 Calculate_DegreeOfSexaulization and so on
