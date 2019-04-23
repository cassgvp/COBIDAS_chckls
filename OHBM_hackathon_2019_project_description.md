# Improving the COBIDAS cheklist for better neuroimaging methods and results reporting

Remi Gau ([ORCID](https://orcid.org/0000-0002-1535-9767
))

## Project Description
In 2012, in his review of the methods and results reporting of more than 200 fMRI paper, [Joshua Carp wrote](https://www.ncbi.nlm.nih.gov/pubmed/22796459): "_Although many journals urge authors to describe their methods to a level of detail such that independent investigators can fully reproduce their efforts, the results described here suggest that few studies meet this criterion._"

A few years ago, in order to improve the situation with  respect to [reproducibility](https://github.com/ohbm/hackathon2019/blob/master/Tutorial_Resources.md#reproducible-neuroimaging-tools) in f/MRI research, the Committee on Best Practices in Data Analysis and Sharing ([COBIDAS](https://www.humanbrainmapping.org/i4a/pages/index.cfm?pageid=3728)) of OHBM released a [report](https://www.biorxiv.org/content/10.1101/054262v2) to promote best practices for methods and results reporting. This was recently followed by a [similar initiative for EEG and MEG](https://osf.io/a8dhx/).

So far these guidelines do not seem to have been widely adopted and anecdotal evidence ([see that twitter poll and thread](https://treeverse.app/view/Xf3jfvIZ)) suggests that even among people who know about the report few of them use it to write or review papers. One likely reason for this might be the unwieldy nature of the report. Anyone who has used this checklist tends to agree that it is a great resource but that it is a bit cumbersome to interpret and apply.

So the short term goal of this project is to facilitate the use of this checklist. But, if done right, this could also in the long term enhance the adoption of emerging neuroimaging standards ([the Brain imaging data structure](https://github.com/ohbm/hackathon2019/blob/master/Tutorial_Resources.md#the-brain-imaging-data-structure-bids), fMRIprep, NIDM...), facilitate data sharing and pre-registration, help with peer-review...

### Short term goals

**The short term goal of this project is to make the Appendix D checklist easier to use**.

One way to achieve this may be to turn the checklist into a website that users can click through and provide the information requested by COBIDAS. Ideally this would generate a small text file (for example a json file) that summarizes what option was chosen for each item of the checklist. This machine readable file could then be used to automatically generate part of the methods section of an article.

A side branch of this project includes developing toolboxes  for the main neuroimaging software (SPM, FSL...) that given a processing batch file as input (e.g matlabbatch.mat for SPM or design.fsf for FSL) creates an output json file readable by the COBIDAS checklist website.

Other potential goals (interaction with BIDS and NIDM, further integration with main neuroimaging softwares) and potential applications (improving data-sharing and peer-review) of this project are described in this [repository](https://github.com/Remi-Gau/COBIDAS_chckls).

#### Requirements

The implementation of this project should remain flexible enough to:
- accommodate the inclusion of new items in the checklist as new neuroimaging methods mature (e.g new multivariate analysis, high-resolution MRI...),
- easily fork the project and convert it to create a checklist-website for a different field. In practice, this will most likely involve mean a deployment through a container technology like [docker](https://github.com/ohbm/hackathon2019/blob/master/Tutorial_Resources.md#containers).


## Skills required to participate

- To be enthusiastic about reproducibility
- Familiarity with the COBIDAS report for f/MRI, MEEG (not necessary)
- To know about web design (not necessary)
- Familiarity with one or more of the main neuroimaging software for [fMRI](https://github.com/ohbm/hackathon2019/blob/master/Tutorial_Resources.md#neuroimaging) (SPM, FSL...) or for [M/EEG](https://github.com/ohbm/hackathon2019/blob/master/Tutorial_Resources.md#main-eeg-and-meg-softwares) (Fieldtrip, EEGlab...) (not necessary)


## Milestones

- Discuss conceptual and structural details of the COBIDAS-json file.

- Create a template of the COBIDAS-json file

- Create a proof of concept website that
  - generates a checklist to by users from an empty template COBIDAS-json file,
  - a method section when given a populated COBIDAS-json file.

- Create a proof of concept toolbox for SPM or FSL that generates filled in COBIDAS-json file.


## Preparation material

Jeanette Mumford has a [30 min video](https://www.youtube.com/watch?v=bsM4KowO5Vc&t=175s) on her youtube channel explaining the background behind the COBIDAS report and giving a run through of the checklist.

The COBIDAS report:
- [for MRI and fMRI](https://www.biorxiv.org/content/10.1101/054262v2)
- [for EEG and MEG](https://osf.io/a8dhx/)

A [spreadsheet version](https://osf.io/qkb9t/) of the COBIDAS checklist (thanks to [Cass](https://github.com/cassgvp)!!!)

[The secret lives of experiments: methods reporting in the fMRI literature](https://www.ncbi.nlm.nih.gov/pubmed/22796459)

[A manifesto for reproducible science](https://www.nature.com/articles/s41562-016-0021)

## GitHub repo

[The github repository of this project can be found here](https://github.com/Remi-Gau/COBIDAS_chckls)


## Communication

Come and join us on the `cobidas_checklist` channel at [![slack_brainhack_3](https://user-images.githubusercontent.com/6297454/47951457-5b37b780-df61-11e8-9d77-7b5a4c7af875.png)](https://brainhack-slack-invite.herokuapp.com/).