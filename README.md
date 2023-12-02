# Know More Names Website
This repo contains code used to create the Know More Names Web Application. 

## Purpose
This web application aims to serve community members, activists, and lawmakers by inter-linking existing datasets and rich unstructured data sources to make the information more easily accessible and contextualized. 

## Datasets and data structure: 
This web application leverages the following datasets: Wikidata knowledge graph (see KSR’s WikiProject [here](https://www.wikidata.org/wiki/Wikidata:WikiProject_Systemic_Racism_Knowledge_Graph)) and additional data to be completed (*). More specifically: 
1. Black people killed during encounters with the police in California
2. Event of those encounters
3. California law enforcement agencies (LEAs)
4. Military equipment index and taxonomy including images*
5. Key legal terms in policies and extracted (words in context) from LEA policy documents*
6. Military equipment inventories* 

## How it works
### Updating data to reflect Wikidata/other data source's changes
A scheduled GitHub Actions workflow runs every month to dynamically update the information on this website if there have been any changes to the data sources. 

### Data flow
The data in the information cards for the Fatal Encounters and Law Enforcement Agency sections is pulled directly from Wikidata using their API. For now, the data for the other sections on the website have not yet been entered into Wikidata, so they are being pulled from Google Sheets using Python's Pandas library. 

## Steps to update webpage:
1. On the main branch, go to the source file of the page(s) you want to edit (i.e. if you want to edit the home page, you would go to the index.qmd file)
2. Click on the edit icon and make your edits 
3. Commit your edits (by clicking on "Commit changes...", adding a commit message describing the changes you made, and clicking on the "Commit Changes")
   - **_Note_**: please be sure to add a message with your commit so others (and your future self) can understand what changes were made and (optionally) why
4. Review updates on the [website](https://know-systemic-racism.github.io/). **_Note_**: webpage takes ~ 1 minute to update


## Error with your commit?
1. Click on the "Actions" tab
2. Click on your commit that failed
3. Click on the "build-deploy" button in the publish.yml section
   - Here, you will find your actual error along with a call stack!
