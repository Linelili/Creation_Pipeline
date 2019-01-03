The following jupyter notebooks can be used to create a valid SMBL model 
version 3 based on Excel sheets of the respective metabolites and reactions. 

Notebook 01_Model_Creation: 
- uses the metabolite and reaction Excel files as input
- creates a new model with cobraPy
- adds the definition of the medium 
- uses libSBML for 
	- adding the charge to the species
	- adding annotations to the species
	- adding groups to the SMBL file
	- adding the E.C. numbers to the reactions
	- adding authors/references/notes to the reactions


Notebook 02a_Selenium_Webrequest_for_reactions
- uses the selenium webdriver to request the respective kegg and bigg IDs 
from the modelseed database
- extracts the aliases and exports them to a txt file
- CAUTION: takes a lot of time, the requests might be interrupted due to the high
amount of requests to the modelseed database webpage
- Possibility to combine the dictionaries, if the webrequest was interrupted


Notebook 02b_Adding_reaction_annotations
- The dictionaries from 02a can be used to add annotations to the reactions

Notebook 03a_BiGG_Identifiers_for_Model_polisher
- The model polisher uses BiGG identifiers 
- The reaction identifieres are changed to BiGG IDs
- The metabolite identifiers are changed to BiGG IDs

Notebook 03b_Back_conversion_of_Ids
- The IDs are converted back to modelseed IDs
- The objective function is defined again 
- The problem of having 4 compartments is resolved

Notebook 04_Occurs_in_Pathway
- The KEGG pathways associated with the reactions are requested via Bio.KEGG
- ... and added as annotations 