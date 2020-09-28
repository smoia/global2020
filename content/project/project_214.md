{
  "Title": "Integration of EEG inside Connectome-Mapper 3",
  "issue_number": 214,
  "link_to_issue": "https://github.com/ohbm/hackathon2020/issues/214",
  "labels": [
    {
      "name": "BIDS",
      "description": "some knowledge of BIDS required",
      "color": "562caa"
    },
    {
      "name": "EEG",
      "description": "Electroencephalography knowledge or experience required",
      "color": "006b75"
    },
    {
      "name": "EMEA hub",
      "description": "",
      "color": "b8aeef"
    },
    {
      "name": "Email ok",
      "description": "",
      "color": "bfdadc"
    },
    {
      "name": "Hackathon project",
      "description": "use this tag for submitted projects",
      "color": "fcffbc"
    },
    {
      "name": "nipype",
      "description": "some knowledge of nipype required",
      "color": "f433db"
    }
  ],
  "content": "## Project info\r\n<!-- *Please fill this in first and then submit the issue* -->\r\n\r\n**Title**: Integration of EEG inside Connectome-Mapper 3\r\n<!--Name of your awesome project. Please also update the title of the issue to be the title of your project-->\r\n\r\n\r\n**Project lead**: Sebastien Tourbier (sebastientourbier)\r\n<!--Your name and GitHub login, possibly more than 1 lead-->\r\n\r\n\r\n**[Timezone](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#timezone)**: UTC/GMT +2 hours (CEST)\r\n<!--UTC offset of your timezone (cf. https://www.timeanddate.com/time/map/ for example).-->\r\n\r\n\r\n**Hub**: Europe, Middle East and Africa\r\n<!--Asia and Pacific / Europe, Middle East and Africa / The Americas based on location of project lead. Possibly more than 1 hub.-->\r\n\r\n**Description**:\r\n<!--Describe the main idea and context of your project in a few sentences.-->\r\nFlexible pipelines for both diffusion MRI and functional MRI have been implemented in different software such as the Connectome Mapper 3, an open-source pipeline software, released as a BIDS App, for mapping hierarchical multi-scale connectomes from multi-modal datasets, but solutions for EEG and MEG are still lacking. This project intents to extends Connectome Mapper 3 to EEG. \r\n\r\n**Link to project**: https://github.com/connectomicslab/connectomemapper3/tree/ohbm-brainhack-2020\r\n\r\n**Mattermost handle**: sebastientourbier\r\n\r\n**Goals for the OHBM Brainhack**\r\n\r\n1. Creation of a sample BIDS dataset with EEG derivatives (computed inverse solutions):\r\n  - [x] Decide a sample dataset (open-source) to use (ultimately with T1w, DWI, rfMRI, EEG modality)\r\n  - [x] Organize the sample dataset according to BIDS MRI/EEG standard\r\n  - [x] EEG analysis (computes the inverse solution) by an open-source EEG analysis software such as MNE, EGGLab,... depending of the expertise in the team\r\n  - [ ] Organization of EEG analysis outputs into the derivatives of the dataset according to new derivatives specs introduced in BIDS 1.4.0 (https://bids-specification.readthedocs.io/en/stable/05-derivatives/01-introduction.html)\r\n\r\n2. Implementation of Nipype interfaces that:\r\n  - [ ] loads the inverse solutions and their respective x,y,z locations\r\n  - [ ] computes ROI source dipoles using the SVD technique\r\n  - [ ] computes single source dipoles per ROI based on SVD decomposition [Rubega et al. 2018] using pycartool (https://github.com/Functional-Brain-Mapping-Laboratory/PyCartool)\r\n  - [ ] computes diverse common functional connectivity metrics (Imaginary coherence, ...) using MNE - See how it integrates #203 \r\n\r\n3. Implementation of EEG pipeline in the Connectome Mapper 3\r\n  - [ ] Implementation of the EEG processing pipeline (`cmp/pipelines/functional/eeg.py`)\r\n  - [ ] Extension with graphical components (`cmp/bidsappmanager/pipelines/functional/eeg.py`)\r\n\r\n**Good first issues**: \r\n*  Get familiar to the Brain Imaging Data Structures: https://bids-specification.readthedocs.io/en/stable/\r\n* Get familiar to the BIDS App framework: https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005209\r\n* Get familiar with Nipype: https://miykael.github.io/nipype_tutorial/ \r\n\r\n**Skills**:\r\n* Brain Imaging Data Structure\r\n* EEG analysis\r\n* Nipype dataflow library\r\n\r\n\r\n**Chat channel**: https://mattermost.brainhack.org/brainhack/channels/hbm-eeginsidecmp3\r\n<!-- If you are creating a channel on the [brainhack mattermost](https://mattermost.brainhack.org/) try to create a\r\n**public** channel with one of the following template names:\r\n\r\n- hbmhack-NAME_OF_YOUR_PROJECT\r\n- hbm-NAME_OF_YOUR_PROJECT\r\n\r\nThese would be the corresponding URLs that you can paste here.\r\n\r\nhttps://mattermost.brainhack.org/brainhack/channels/hbmhack-NAME_OF_YOUR_PROJECT\r\nhttps://mattermost.brainhack.org/brainhack/channels/hbm-NAME_OF_YOUR_PROJECT\r\n-->\r\n\r\n<!--\r\n**Video channel**: https://meet.jit.si/EEGinsideCMP3\r\n\r\nWe are trying to be super careful about \"zoom bombing\" possibility.\r\nSo we want to avoid having links to video chats in \"public space\".\r\nWe suggest that you create a Jitsi or Zoom room and mention it in your text channel as \"pinned\" message or in the channel header.\r\n\r\n-->\r\n\r\n**Image for the OHBM brainhack website**\r\n\r\n![Connectome Mapper 3](https://raw.githubusercontent.com/connectomicslab/cmp3-ohbm2020/master/images/container_cmp3.png)\r\n\r\n## Project submission\r\n\r\n## Submission checklist\r\n*Once the issue is submitted, please check items in this list as you add under 'Additional project info'*\r\n\r\nPlease include the following above (all required):\r\n-   [x] Link to your project: could be a code repository, a shared document, etc. See [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#link-to-project)\r\n-   [x] Include your [Mattermost handle](https://mattermost.brainhack.org/) (i.e. your username). If you do not have an account, please [sign up here](https://mattermost.brainhack.org/signup_email).\r\n-   [x] Goals for the OHBM Brainhack: describe what you want to achieve during this brainhack. See [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#goals).\r\n-   [x] Flesh out at least 2 \"good first issues\": those are tasks that do not require any prior knowledge about your project, could be defined as issues in a GitHub repository, or in a shared document, cf [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#onboarding-2-good-first-issues).\r\n-   [x] Skills: list skills that would be particularly suitable for your project. We ask you to include at least one non-coding skill, cf. [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#onboarding-skills).\r\n-   [x] Chat channel: A link to a chat channel that will be used during the OHBM Brainhack. This can be an existing channel or a new one. We recommend using the [Brainhack space on mattermost](https://mattermost.brainhack.org/), cf. [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#chat).\r\n-   [x] Video channel: Please create a video channel that will be used during the OHBM Brainhack and share it in your chat channel above. This can be an existing channel or a new one. For instance a [jitsi meet](https://meet.jit.si/) room, cf. [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#video-calls).\r\n-   [x] Provide an image of your project for the OHBM brainhack website\r\n\r\nYou can also include information about (all optional):\r\n-   [ ] Number of participants, cf. [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#participant-capacity)\r\n-   [ ] Twitter-size summary of your project pitch, cf. [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#twitter-size-summary-of-your-project-pitch)\r\n-   [ ] Set up a kanban board on your repository to better divide the work and keep track of things, cf [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#set-up-a-kanban-board)\r\n-   [x] Project snippet for the OHBM Brainhack website, cf. [here](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#project-snippet-for-the-ohbm-brainhack-website)\r\n\r\nWe would like to think about how you will credit and onboard new members to your project. We recommend reading references from [this section](https://github.com/ohbm/hackathon2020/blob/master/.github/ISSUE_TEMPLATE/handbooks/projects.md#credit-and-onboarding). If you'd like to share your thoughts with future project participants, you can include information about (recommended):\r\n-   [ ] Specify how will you acknowledge contributions (e.g. listing members on a contributing page).\r\n-   [ ] Provide links to onboarding documents if you have some.\r\n"
}