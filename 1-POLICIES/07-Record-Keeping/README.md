# I commit to document expectations for record-keeping

This page collects real-world examples of lab record-keeping policies from around the world. We encourage all labs implementing the SAFE Labs Handbook to share their own record-keeping expectations here. To contribute, simply create a pull request adding your commitment under the appropriate country section. If you feel comfortable, you can include a link to your lab's website alongside your example, but this is entirely optional. Your examples will help other labs develop their own effective record-keeping policies!

## Details
Accurate, consistent, and accessible records are essential for reproducibility, accountability, and continuity. Written expectations reduce ambiguity about what to record, where to store it, and how to review it.

## Suggestions
- List required record types (e.g. lab notebooks, raw data, scripts, protocols, inventories, meeting notes)
- Define storage locations and responsibilities (shared drives/notebooks; individual vs group)
- Set documentation standards (dates, authors, versions, protocol deviations, metadata, naming)
- Outline backup/version-control expectations and review points (milestones, exits)
- Clarify access/sharing rules and data retention on departure

## Examples

### Australia
>_[BABLab_2026](https://github.com/BaBLab-UNSW/Lab_Manual/blob/main/06-data-analysis-and-code-practices.md)_:
>
>**What goes on GitHub, and what never does**
>
>Code goes on GitHub. **Raw or identifiable participant data never does — not even in a private repo.** GitHub is not an approved storage location for participant data under UNSW's data classification rules (see Data Access & Management); a repo being private doesn't change that. In practice:
>
>- Scripts should read data from its actual location on OneDrive/SharePoint (or wherever the project's approved storage lives), referenced by a relative path, not a hardcoded path to a specific person's laptop.
>- Add a `.gitignore` that explicitly excludes data folders, so a stray `git add .` can't accidentally commit a CSV full of participant responses. The lab manager can provide a standard `.gitignore` template — use it as your starting point for every new repo.
>- If a repo genuinely needs example data to run (e.g., so someone else can test the pipeline), use a small simulated or fully de-identified synthetic dataset built for that purpose, clearly labelled as such.
>- If you're ever unsure whether something is safe to commit, ask before pushing, not after.
>
>**Reproducibility mechanics**
>
>- Set a seed explicitly (`set.seed()`) anywhere randomness is involved (bootstrapping, permutation tests, train/test splits), and note why that seed and not another, if it matters.
>- Record the analysis environment: run `sessioninfo::session_info()` at the end of your analysis and save the output alongside your results, so package versions are documented. For larger or long-running projects, use [`renv`](https://rstudio.github.io/renv/) to lock package versions for the whole project.
>- Scripts should regenerate figures and tables from raw data through to the final output. If a figure in a paper was hand-edited after being exported from R, that's a red flag — the pipeline should produce the reportable output directly, or the manual edit should be documented and justified.

### Austria
>_[RendeiroLab_2026](https://doi.org/10.5281/zenodo.23398122)_:
>
>It is essential to maintain detailed, up-to-date records of daily activities. This includes:
>
>- Notes and sketches on ongoing projects.
>- Progress on analyses.
>- Logs of seminars attended, papers read, or other relevant activities.
>
>### Digital and Physical Notes
>
>- Use markdown-based notes in [Obsidian](https://github.com/rendeirolab/daily_notes) for digital documentation.
>- Optionally, concatenate markdown notes and print them on sticky paper for inclusion in physical lab notebooks.
>
>## Shared OneDrive Folder
>
>The official platform for file sharing is the CeMM-provided OneDrive, accessible here: [Shared Documents](https://cemmat.sharepoint.com/sites/rendeirolab/Shared%20Documents).
>
>### Best Practices
>
>- Update the folder regularly, especially when reaching milestones such as paper submissions, talk presentations, or poster creations.
>- Organize files in a compartmentalized manner by subject (e.g., figures, presentations, documents, notes).
>- Prefix all file names with the format `YYYY-MM-DD-` to ensure chronological order.

### Canada
>_[LRCNLab_2026](https://lrcn.uwo.ca/lab_manual/index.html)_:
>
>Every ongoing research project will have an associated OneDrive folder within a shared library for the lab. Please speak to me or the lab manager to be given access to the OneDrive shared library.
>
>Within this folder are subfolders for each aspect of the study from ethics to recruitment. If there are multiple studies attached to one ethics, there will be subfolders within the project folder indicating the project's title and the researchers name.If changes have been made to the study, these folders will need to be updated so that we have the most up-to-date information on how the study was conducted. This is to ensure that our studies are reproducible to the maximum extent we can manage.

>_[MindaLab_2026](https://osf.io/download/arywg/)_:
>
>Every ongoing research product should have an associated MS Word or Google Doc that is shared with lab members who are involved in that project. At the top of the document, is the internal title for the project, the names of the associated lab members, and links to important documents/folders (Manuscript drafts, data ﬁles, R-code). If you make a change in some code, collect data, edit a document, or do anything else related to a project, please record that information in the Google doc with the date and your initials.
>How much detail is required in this record? There’s no perfect answer to that question, but the document should be clear enough and detailed enough so that if we revisit the project several years later, we should be able to ﬁnd where the manuscript is, where any relevant code is, and where the data is stored.

>_[SFUGlaciologyGroup_2026](https://www.sfu.ca/~gflowers/SFU_GlaciologyGroup_Expectations.pdf)_:
>
>At the end of your program, you will be asked to organize, document and post all files relevant to your work on the NAS with a copy delivered to me. All data and research output will be considered our collective property, unless otherwise stated (see INTELLECTUAL PROPERTY). Field books and notes are considered property of the project, not personal.

>_[TemporalEcologyLab_2026](https://github.com/temporalecologylab/labgit/blob/master/datacodemgmt/wheredatacodelive/_READMEwheredatacodelive.md)_:
>
>WhereDataCodeLive is an important part of data management in the Temporal Ecology Lab; it's basically where we keep notes on the files that make up each project and keep track of when data will be made public following the rules in the lab data management plan (see tempeco_DMP.pdf).
>
>**How do I complete my wheredatacodelive?**
>
>Great question! Please copy the markdown (.md) in ZeTemplate/ZeTemplate.md (https://github.com/temporalecologylab/labgit/blob/master/datacodemgmt/wheredatacodelive/ZeTemplate/ZeTemplate.MD) and update it for EACH of your projects in the lab. More details are in tempeco_DMP.pdf.
>
>wheredatacodelive files should be stored in the labgit in the wheredatacodelive folder.
>
>**I have been asked to check someone else's file, how do I do that?**
>
>Notes on what to check for in a good wheredatacodelive project file are in wheredatacodelive_notes.txt

### France
>_[BoumendilLab_2026](https://igh.cnrs.fr/research-teams/team-charlene-boumendil/)_:
>
>All data and codes will be made available through public repositories, respecting the FAIR (findable, accessible, interoperable, reusable) data principles. A big part of ensuring that data are FAIR is by documenting all experiments, protocols, results etc… For this we use electronic labbooks and ensure their strict completion.

### Germany

>_[TSCNLab_2026](https://tscnlab.github.io/LabHandbook/background/MissionStatement_2024.09.02_v1.4.html)_:
>
>Our mission is to perform **robust and reproducible research**. We achieve this goal through various actions, including documentation of program code and analysis steps, preregistration of experiments, internal replication, and data and code reviews. We establish naming conventions for files and we write standard operating procedures (SOPs) for experiments, data collection and -management, data storage and for analysis. We respect subjects’ privacy, therefore we collect pseudonymized or anonymized data whenever possible.
>
>We want to constrain the [“researcher degrees of freedom”](https://doi.org/10.3389/fpsyg.2016.01832) in analyses by carefully specifying analytic strategies prior to data analysis. We avoid “research waste” and in the case of negative results, we will publish them. We prioritise quality over quantity in producing the data and in the publication of results. In case of mistakes in already published work, we acknowledge these mistakes and work to correct them.

### India

>_[TEE-Lab_2026](https://teelabiisc.wordpress.com/code-and-data-sharing-policy-tee-lab/)_:
>
>Specifics of code and data sharing: All students will create a Git-Hub login and are invited to the lab git-hub account (https://github.com/tee-lab). They create a private repository for the ongoing project within the lab git-hub account (with no licence, with all rights reserved); in some cases, an ongoing project may also be made Public with open access license.
>
>The project lead is encouraged to use features of git version control and directly update on git-hub. Alternatively, they can manually upload the latest codes at least once a month. This will also serve as a back up.

### Japan
>_[KiharaLab_2026](https://www.sci.kanagawa-u.ac.jp/chem/kihara/)_:
>
>【実験ノート／スペクトル】
>
>実験ノートは専用ノートを使用する。実験ノートの付け方は別紙。
>
>スペクトルには全て固有の番号を振る。コンピューターのファイル名はこの番号に対応するようにつける。実験ノートからもスペクトルからも互いが参照できるようにしておく。実験ノートとスペクトルは卒業時に全てまとめて研究室に残すので、普段から整理をしておくこと。
>
>_English translation:_
>
>[Lab notebooks / spectra]
>
>Use a dedicated notebook for your lab notes. How to keep the lab notebook is described on a separate sheet.
>
>Give every spectrum its own unique number, and name the computer files to match this number. Make sure the lab notebook and the spectra can each be traced from the other. Lab notebooks and spectra are all left with the lab when you graduate, so keep them organised day to day.

>_[ShojiLab_2026](https://scrapbox.io/shoji-lab-survey/莊司研究室データセット公開マニュアル)_:
>
>莊司研究室におけるデータセット公開は、研究室共同 GitHub アカウントを基盤として運用する。
>
>各学生は、研究室 GitHub 組織配下に個別のデータセットリポジトリを作成する。
>
>その際、当該学生の GitHub アカウントをCollaborator として招待し、本人がコミットを行う。
>
>これにより：
>
>　リポジトリ管理履歴にデータセット作成者が明示される
>
>　データ取得時期が最終コミット時刻として記録される
>
>
>
>また、複数学生のデータを単一リポジトリに集約する運用は行わない。
>
>理由としては：
>
>　更新履歴が混在する
>
>　データ取得時期の追跡が困難になる
>
>　個別引用が不明瞭になる
>
>したがって、「1データセット＝1リポジトリ」を基本原則とする。
>
>_English translation:_
>
>At the Shoji Lab, dataset publication is run on the lab's shared GitHub account.
>
>Each student creates their own dataset repository under the lab's GitHub organisation.
>
>The student's own GitHub account is invited as a Collaborator, and the student makes the commits themselves.
>
>This means that:
>
>- the dataset's creator is shown in the repository history
>- the time the data were collected is recorded as the time of the last commit
>
>We also do not combine several students' data in a single repository.
>
>The reasons are that:
>
>- the update histories get mixed together
>- it becomes hard to track when the data were collected
>- individual citation becomes unclear
>
>So "one dataset = one repository" is our basic principle.

### Spain
>_[BioKTGroup_2026](https://biokt.github.io/lab-handbook/02_project_organisation)_:
>
>Some things that make a notebook useful, wherever it lives:
>
>- Date every entry. Newest-first keeps the latest state at the top.
>- Record *decisions* and *why*: "Discarded rep3: box too small, protein
>  interacted with its periodic image at 40 ns." This is exactly the information
>  a referee asks for and a successor needs.
>- Record mistakes. A note like "the first 300K set used the wrong salt
>  concentration and was deleted" saves the next person from repeating the mistake.

### Switzerland

>_[Neurolinguistics-UZH_2026](https://gitlab.uzh.ch/alexis.hervais-adelman/dynoball.org/-/wikis/Lab_Manual/Lab_Manual_06)_:
>
>MS OneNote for Project Documentation
>
>Just like a traditional paper lab notebook, documentation here must be clear, complete, and auditable - this helps protect your work and ensures our research maintains the highest standards.
>
>All project-relevant decisions, design choices, and analysis choices must be documented clearly and comprehensibly, such that any collaborator can easily reconstruct the logic of an experiment and its analysis.
>
>We ask you to record what you did, how you did it, and the outcomes. This includes experiments, analyses, scripts, and major decisions.
>
>### Notebook structure
>
>Each project has a dedicated notebook with a standard structure. MS has made it impossible to save notebooks as a file so you must follow the following convoluted procedure to make your own: Open [this example notebook](https://1drv.ms/o/c/698e9eed515b4cdf/Et9MW1Htno4ggGmBAAAAAAABq7g0_OBummuRChpg61eIKg?e=kdgGBx) and go to edit \> in Desktop App. Once the notebook is open there, copy all the sections to your own new OneNote notebook by right-clicking and selecting "Copy Section to…". If you feel this does not meet your needs, agree on the improvements you plan to make with Alexis and customise as needed.

### United Kingdom
>_[DumbellLab_2026](https://dumbell-lab.com/blog/the-dumbell-lab-laboratory-handbook)_:
>
>All members will be issued with a lab book on joining the lab. This remains property of the lab and is a lasting record of your work. Lab members are expected to keep a detailed record of all their work in the lab including any data analysis. Records of where data is kept must be included in this lab book. Each page of the lab book must have the date, experiment title, lab book number, page continued from/to completed, and signed by the lab member. From time to time these lab books will be audited by the group leader who will then sign the latest completed page of the book to approve the record of the work. Results should all be recorded in the lab book in clear and readable text, or should be cross referenced to the location of the file on the sharepoint.

>_[EnvironmentalModellingResearchGroup_2026](https://envmodellinggroup.github.io/coc.html)_:
>
>All computers should be backed up. A set of two USB hard drives should be used as a daily automated back-up,
> rotated at regular intervals. Regular backup of important documents (e.g. model set-up files, manuscripts)
> to the lab group's google drive, the University's google drive or the University servers, preferably
> via a version control system, e.g. git.
>
>All data should be placed on an appropriate repository with a DOI and published alongside the manuscript wherever possible.
> Data includes. Suitable examples of repositories include FigShare and
> Pangaea. Staff and PhD students must also adhere to the
> University of
> York's Research Data Management Policy, which means as well as above, you must add the data to PURE, via the DOI above.
>
>All software and scripts should be developed using Git or other suitable code versioning system, ideally in
> an open online environment, such as GitHub. Group members are free to add repositories to this group's or
> start their own. Code should be released under a suitable, permissive licence, such as LGPL whenever possible.

>_[GrangeLab_2026](https://bookdown.org/JimGrange/lab_manual/science.html)_:
>
>If you are a BSc student, you can increase reproducibility by documenting all stages of your analysis in sufficient detail such that anyone could follow your steps exactly. If using JASP, make notes of what menu options you chose and in what order. Did you exclude any data? If so, document why. Did you transform any variables? if so, document why.
>
>If you are an MSc student, I would be expecting you to start to explore using statistical programming languages such as R for your analysis so that you have a script of your analysis code. If you are a PhD student, I absolutely expect you to be coding your own analysis. Of course, I am always on hand to help out if needed.

>_[SuperLab_2026](https://www.reshannereeder.com/lab-handbook)_:
>
>If you gave someone else your raw data, they should be able to reproduce your results exactly. This is critical, because if they can't reproduce your results, it suggests that one (or both) of you has made errors in the analysis, and the results can't be trusted. Reproducible research is an essential part of science, and an expectation for all projects in the lab. For results to be reproducible, the analysis pipeline must be organized and well documented.
>
>To meet these goals, you must document all aspects of your analysis pipeline. This means writing down how you did things every step of the way (and the order that you did things), from any pre-processing of the data, to running models, to statistical tests (including in analysis scripts, which should always be commented clearly so that every step is understandable by an outsider). If you are running your analyses in JASP, make sure to re-label standard headings of analyses (e.g., 'Repeated Measures ANOVA' could be relabeled to 'Vividness of immediate recall: repeated-measures ANOVA'), give outputs a sensible title, e.g., 'Immediate_recall_analyses', and save them all in the same 'results' folder.

### United States
>_[AeryJonesLab_2026](https://aeryjoneslab.github.io/philosophy)_:
>
**General principles:**

>- All data (raw and preprocessed), metadata, records (e.g. lab notebook), code, analysis, and writing must be backed up to cloud storage (e.g. OneDrive) or stored on a system with regular backups (the server). You can keep working copies of any data on the server in a second location as well. We must keep all these for several years after each paper is published, so it’s important that they are durably stored and easy to locate.
>- Log inventory and samples with their detailed locations. Label chemicals with when they arrived and when they were opened. Label physical samples with enough detail so they can be connected to the originating organism and data by someone else in lab (sample name, your initials, date, which hemisphere, which stains, etc).
>- Record early and often. Keep this level of detailed records and data management even for pilot data; you never know when you’ll need it. Your records and code don’t need to be clean or publication-ready to be stored; store them every day and organize them later. Use version control for all code.
>- Your lab notebook should record which protocols you used, how you deviated from them, any notable observations, lot numbers and concentrations of reagents used (if relevant), software versions used (if relevant), and locations of generated samples and data.
>- Use YYYY-MM-DD date format.
>- Help keep the lab wiki and protocols up to date. Add information you think may benefit others. Edit information and protocols as they change. If you do an experimental procedure not yet on the lab’s [protocols.io](http://protocols.io) workspace, add it there.
>- Data, code, and records you generate here belong to the lab. All data and repositories need to be accessible by everyone in lab. Keep your data on the server and your code in repositories within our lab’s Github team space. Lab notebooks need to be accessible to everyone in lab after you depart.

**All documentation, code, and data in our lab lives in the following locations:**

>- **Lab wiki:** this manual, other administrative protocols
>- **Protocols.io:** protocols. When you create  or majorly modify a protocol, print it and add it to the protocols binder (replace the old copy).
>- **Github:** data acquisition and analysis code, CAD files
>- **Server:** raw and preprocessed data, analysis. Data should be organized consistently across all your data and projects and explained in a README file in your server folder. Modified raw data must be stored as copies and the original left untouched. Data should be converted to non-proprietary formats (meaning the file can be opened without paying for a software license).
>- **ABED:** all metadata, inventory, physical locations of stocks and samples
>- **Dropbox/OneDrive:** I will share a Dropbox folder with everyone and ask you to add figures, presentations, or writing to it when we are working together on something. I find it’s often easier to work on early drafts of papers as a single Google doc, so all authors can work simultaneously, then migrate them to Word documents for formatting and submission.
>- **Fridge:** brains and slides

**Other recommended tools:**

>- **Notetaking software:** any will do. I use Notion, which is useful for long-term planning, connecting related notes, and integrating with other online tools.
>- **Reference manager:** any will do. I use Zotero, which is open source.

**Data Layers**

>- Directory structure: Data/[Project Name]/[Cohort or Subproject]/Raw Data, Preprocessed Data, Analysis
    - within Raw Data and Preprocessed Data: [Data Type]/[Animal Name]
>- Recording file naming scheme: [yyyymmdd]*[Animal Name]*[Track][Epoch]

>_[AlyLab_2026](https://github.com/alylab/labmanual/blob/master/aly-lab-manual.pdf)_:
>
>For results to be reproducible, the analysis pipeline must be organized and well documented. To meet these goals, you should take extensive notes on each step of your analysis pipeline. This means writing down how you did things every step of the way (and the order that you did things), from pre-processing, to running models, to statistical tests. You should take detailed notes on your experimental design as well. Your code should also be commented, and commented clearly. We all know what it’s like to sit down, quickly write a bunch of code to run an analysis without taking time to comment it, and then having no idea what we did a few months down the road. Comment your code so that every step is understandable by an outsider. Finally, it is highly encouraged that you use some form of version control (e.g., Git in combination with GitHub) to keep track of what code changes you made and when you made them, as well as sharing code with others. The lab’s GitHub is https://github.com/alylab.

>_[BacklundGroup_2026](https://backlundlab.scs.illinois.edu/files/2025/01/Backlund-Group-Expectations-vJan2025.pdf)_:
>
>Lab notes: Students are expected to maintain a daily record of their research. Some days it may make sense to handwrite notes in a physical notebook, while other days the most efficient record keeping method might be to take typed notes with interleaved screenshots. Students should maintain both a dedicated physical notebook for written record keeping and a dedicated Box folder to store digital notes (save, e.g., as Word documents). These notes must be sufficiently well-organized such that a future lab member can reasonably follow your prior work.

>_[BahlaiLab_2026](https://github.com/BahlaiLab/Policies/blob/master/Project_completion.md)_:
>
>Data used in support of the project must be:
>- [ ] Saved in an appropriate, non-proprietary format with accompanying metadata
>- [ ] In a public archive, or, if data is proprietary, a 'snapshot' version of the data used in the project must be saved in a private repository accessible to lab members
>- [ ] Linked and briefly described in the project README
>
>## Code
>Code used or developed in support of the project must be:
>- [ ] Well commented and complete
>- [ ] On Github, in the public project repository
>- [ ] Described in the README- what does each file do, what language was used, etc
>- [ ] Tested! can at least one other person (but more is better) make your analysis go on a different computer?

>_[BarberLab_2026](https://www.annikabarberlab.com/barber-lab-manual)_:
>
>You are expected to catch up on your lab notebook at least biweekly, and we may consult notebooks during individual or project group meetings. Your ELN is for documenting daily work. Each day you work in lab should have some note of what you did that day. You should plan fly crosses in your notebook, document genotyping gel results, blots, etc. If you prefer writing things out on paper, you may use your paper lab notebook and include a photo in your ELN with a short description for searchability–this is easily accomplished using the smartphone app. All raw data is stored on the Waksman Share Drive (see separate section) – only metadata, representative data and summary plots need to be in your ELN. The file path to raw data must be noted in your ELN for every experiment that generates data files, and metadata must also be stored with raw data (in addition to being in your ELN).

>_[BenjaminChungLab_2026](https://jadebc.github.io/lab-manual/checklists.html)_:
>
>- Does the script run without errors?
>- Is code self-contained within repo and/or associated Box folder?
>- Is all commented out code / remarks removed?
>- Does the header accurately describe the process completed in the script?
>- Are file paths relative (using here()) rather than absolute?
>- Are assertions present after merges, filters, and key variable creation steps?
>- Do unit tests pass (testthat::test_dir('9-tests'))?
>- Are random seeds set where relevant?
>- Is the script pushed to its github repository?
>- Does the code adhere to the coding style guide?
>- Are all warnings ignorable? Should any warnings be intentionally suppressed or addressed?

>_[BIRDLab_2026](https://uc-bird-lab.github.io/bird-lab-website/lab-guide/data-management/)_:
>
>The lab's shared Box folder is the system of record for all data, documents, photos, and videos. UC Davis provides it with unlimited storage, and it keeps a version history of recent changes. Work out of Box so your files are backed up at all times.
>
>Once a month, back up your Box data to an external lab hard drive. Keeping a second copy off the cloud is your responsibility as much as the PI's.

>_[ChiangLab_2026](https://chianglab.usc.edu/resources.html)_:
>
>Reproducibility: All developed methods, analytic pipelines and finalized results of your analysis should be well-documented. This is not just for scientific rigor, but also for training and as a service to your labmates. Other members of the lab will appreciate detailed records of what you have tried that failed (and what you have tried that succeeded), so that they can learn from your experience. You will also come to appreciate the fact that others will not need to constantly bug you with questions. We will try our best to post preprints of original research to preprint servers (like biorxiv), and post codes to online repositories (like GitHub), but even just a set of neatly kept READMEs on the lab server will go a long way to document your hard work.

>_[ContextualDynamicsLab_2026](https://github.com/ContextLab/lab-manual/blob/master/lab_manual.pdf)_:
>
>You should treat GitHub as a digital version of a “lab notebook”
> that contains a formal record of every contribution you make to your projects. We use GitHub logs to assign credit for ideas, code or writing contributions,
> determine authorship order, and more. It is therefore critical that you regularly check in (commit) your work via GitHub so that you receive appropriate credit for your
> ideas and maintain a continuous traceable log for your project.

>_[DeAngelisLab_2026](https://kristendeangelis.net/expectations/)_:
>
>Collaborative research. Our lab group is collaborative, and your PI is a coinvestigator on all projects. We share viewing access to all protocols, data, research and results internally through OSF, Overleaf, and/or Google docs. When you begin your work in the lab, we will have a shared online document where we can share research plans, data, shared papers, and writing. You should expect to have a dedicated folder for your project where you share results, plans and progress, including shared meeting notes document for both agenda items to discuss, and benchmarks for short- and long-term goals. People working on projects funded by public funds are obligated to share data and scripts at the time of publication, and this shared repository will also act as a place to draft these open source final documents.

>_[DolbowGroup_2026](https://dolbow.pratt.duke.edu/expectations-duke-computational-mechanics-laboratory-dolbow-research-group)_:
>
>All members are expected to keep their data files, input decks, etc. in a file system that is organized and stored on one of the workstations in the lab. Personal laptops should not be used to store data. Critical results should be saved. README files should be used in directories to explain what is there, when the work was done, and anything else that would be useful to future members to understand and reproduce the results. All members are entitled to take a copy of all of their data when they leave the lab.

>_[GureckisLab_2026](https://todd.gureckislab.org/2026/03/06/genaipolicy)_:
>
>**Code**
>
>- All analysis code must be published, not merely available upon request.
>- Repositories must include the verification and testing scripts from Section 3, so reviewers and readers can see what checks were performed.
>- Where AI tools generated substantial portions of code, note this in comments or the README.
>- Code must be documented well enough for another lab member to run it on the original data and reproduce reported results.
>- Except in exceptional cases, generative model output should not be a primary method of analysis — e.g., using an LLM to classify open-ended responses instead of writing a classifier.
>
>**Data**
>
>- Raw data (subject to IRB and participant privacy constraints) must be deposited in a public repository (OSF, GitHub, Zenodo, or equivalent) at the time of submission.
>- Preprocessing and exclusion scripts must be included. Avoid unpublished intermediate processing steps.

>_[HarmsLab_2026](https://github.com/harmslab/website/blob/master/source/records.md)_:
>
>If you didn’t document it, it didn’t happen.
>- In two years, you’ll wish you had written more down.
>
>#### Guidelines:
>
>- Legible, in pen. You can either use a normal lab notebook or build a loose-leaf notebook in a binder.
>- Enter information **directly** into the notebook [no paper towels :)].
>- Properly introduce **and** summarize each experiment.
>- Tape in any external results (graph printouts, etc.)
>- Note where any electronic files associated with experiment are stored.
>- Include complete details of all first-time procedures, and cross-reference to page with full details for repeated procedures.
>- Include calculations
>- Keep up with the table of contents.
>- Date and number each page.

>_[JonesLabUKY_2026](https://joneslab.ca.uky.edu/sites/joneslab.ca.uky.edu/files/joneslablivingdocument.pdf)_:
>
>We work with a variety of data types, including field observations, behavioral observations, molecular and genomic. It is imperative that you have multiple copies of your data in different locations. Imagine that the worst-case scenario is going to happen, because it very well might- your laptop will break, your external hard drive will fail, the building with your lab notebook will flood. You must back up your data to the cloud and ensure your data will not be lost due to an accident. This means taking pictures of handwritten data sheets, uploading these photos to the cloud and placing them in the lab shared drive. This means uploading raw sequencing data to NCBI (set the release date to the future so as not to release unpublished data) and having data on both an external hard drive and a UK/lab server. If you are collecting data in real time that at first exists in only one location, have a plan for how you will quickly back up those data on a regular (daily, if possible) basis. If you aren’t sure how to back up your data, ask!

>_[KalantryLab_2026](https://docs.google.com/document/d/1eyzD0XEeNR5zxahjrrJdHCjowNSiQVOb/edit)_:
>
>As a matter of lab policy, you are asked to use UM’s electronic lab notebook to record all your raw and processed data. You are also asked to share the electric notebook with Sundeep, who will refer to the lab notebook to examine raw and processed data. I cannot stress how important it is to develop good habits to record the details of your experiments. A thoroughly documented record of your experiments is a sign of - and contributes to - the clarity of your thoughts.

>_[LaskowskiLab_2026](https://laskowskilab.faculty.ucdavis.edu/lab-values-expectations/)_:
>
>- Keep a lab notebook. Every Amazon Warrior is required to have a hardcopy paper lab notebook. Anything that has to do with an experiment you run should be documented here.
>- Pages should be dated and written in ink. Write down details of the experimental planning, scheduling, behavioral assay protocols, a priori hypotheses, outline of the projected steps of the analysis. Trust me, you will forget details and you may need to reference them after months or (several) years.
>- The purpose of the lab notebook is to not only help you remember details of what you did and why months or potentially years later, but also as solid proof that we did the things the way we said we did.
>- Know that at any moment, Kate may ask to see your lab notebook and she will expect it to be up to date, complete and well organized.
>- Organize your lab notebook well – use tabs to start new sections. Write legibly. Keep a blank page at the beginning to fill in with Table of Contents.
>- Upload photos of your lab notebook pages to the lab Box every month!

>_[LePenLab_2026](https://hsph.harvard.edu/wp-content/uploads/2026/06/Le-Pen-Lab-Compact-2026-06-05.pdf)_:
>
>• Lab book entries should be titled using the lab member’s initials followed by a number, e.g., JLP637: Alpha vs Omicron growth curve in PLSCR1 KO Huh-7.5 cells.
>• All related files (e.g., datasets, graphs, images) should begin with the same index (e.g., JLP637_cell_count.xlsx) and be organized in a dedicated directory (e.g., '/Work/Experiments/JLP637').
>• Each lab member’s main Work directory should be automatically backed up to a cloud platform (e.g., Microsoft OneDrive, iCloud, or Dropbox). The department recommends using Microsoft OneDrive and provides all members with a free account.
>• The lab also maintains a Microsoft SharePoint account, which serves as a central cloudbased drive for general shared lab documents. It is accessible through OneDrive and used for materials such as shared scientific resources, meeting slides, onboarding documents, and more. Every new lab member will be shown how to connect to the lab SharePoint during onboarding.
>• Large files (e.g., sequencing or imaging data) should be stored in S-drive as cold storage at '/Volumes/shared/IID-Le Pen Lab/cold_storage' and properly indexed in the lab’s SharePoint at: ' /General/Data archive/Metadata table.xlsx'.

>_[MilliganMcClellanLab_2026](https://milligan-mcclellan-lab.mcb.uconn.edu/370-2/)_:
>
>Maintain a legible and thorough lab notebook. For each experiment, please write:
>- Objective
>- Background
>- Methods, including deviations from established methods
>- Results
>- Conclusion

>_[MsEELab_2026](https://mseelab.org/handbook.html)_:
>
>_Protocols:_ MsEE Lab encourages all members to write or annotate their own versions of protocols. Lab reference versions are stored publicly and updated on the [MsEE Lab Protocols repository on GitHub](https://github.com/mseeLab), which allows for version control and history.
>
>*Shared resources:* Presentations by all lab members, visuals, plasmid/strain databases, laboratory inventory, ordering history, and useful reference material are kept on the MsEE Lab Google Drive account.
>
>_Data:_ All lab data from published projects is available on GitHub repositories for the corresponding project or public online databases. Unpublished data for lab projects should be stored on the MsEE Lab Google Drive account as it is generated. Large data files may be stored on the lab server. 
>
>*Notebooks:* Lab members are required to keep any note-taking system that allows the downloaded storage of all the details required to replicate experiments or analysis, and understand when and how they were done. Computational projects should have changelog files that describe changes made to the code. Notebooks and changelog files can be public documents if the lab member so desires. Advances in different projects may be made public as research updates on the [MsEE Lab Substack](https://mseelab.substack.com/) if agreed to by the lab members working on the project.
>
>*Code:* Code used for simulations or data analysis should be shared publicly through the [MsEE Lab Github Organization](https://github.com/mseeLab). Code is shared under an [MIT License](https://choosealicense.com/licenses/mit/). All published projects should include a README file explaining the purpose and structure of the code, as well as information on the hardware used to run the code. A changelog file logging changes made to the code should be included as well (see above). We encourage [inline documentation of functions](https://github.com/resources/articles/tools-and-techniques-for-effective-code-documentation). Code not created by a member of MsEE Lab should be annotated with its source, whether it is existing code copied or modified from elsewhere or code generated by artificial intelligence. Computational tools designed for distribution and use by others should include full user interface documentation and usage examples. 
>
>*Publishing:* All projects are published as preprints as soon as they are completed for publication, and updated with new results whenever they are available. MsEE Lab prefers to publish in nonprofit research journals, but the choice of a target journal is an open matter of discussion for members of the project being published. [Elsevier is banned for being particularly egregious in its attacks on open science](https://en.wikipedia.org/wiki/Elsevier#Criticism_of_academic_practices) ([although making for a fascinating story along the way](https://www.theguardian.com/science/2017/jun/27/profitable-business-scientific-publishing-bad-for-science)). Yes, this includes all of Cell Press and The Lancet, sorry.

>_[NicholGroup_2026](https://sites.rochester.edu/nichol/wp-content/uploads/2024/05/lab_manual.pdf)_:
>
>The intended reader of your notes is not you at the present time. The intended audience is either me or you several years in the future once you have forgotten the details of your experiment. Write your notes with this in mind.

>_[OlanrewajuLab_2026](https://ayokunle.notion.site/Olanrewaju-Lab-Manual-cdf5d841306e44009fbdc752cf4724f6)_:
>
>All lab members are expected to maintain a lab notebook using Benchling. Each experiment should have its own unique entry in Benchling. Each experiment should be named in the following format “YYYY-MM-DD-Brief-Summary-of-Experiment-Purpose” and must have entries on two important tabs:
>Objectives: why was the experiment done?
>Methods: brief overview of key techniques and any deviations from previous experiments. You can link to previous experiments in Benchling using the “@” symbol and search for experiments by title.
>Include screenshots or images of key data here
>Also upload a copy of your raw & analyzed data for the experiment after completion so that it’s linked to the experiment.

>_[PeelleLab_2026](https://github.com/jpeelle/peellelab_manual/blob/master/peellelab_manual.pdf)_:
>
>Anyone conducting an independent research project should have a lab notebook for keeping track of discussions, experiments, and taking notes. You may also want to use an electronic notebook (e.g., Evernote) as your primary lab notebook, or to supplement a paper copy. The important thing is that you are keeping notes, and they are in one place.

>_[POISLab_2026](https://www.notion.so/22b9e68b69b6809b95a2c1e5d87f6c3e)_:
>
>Keep shared lab folders as organized as possible because different people will be accessing those files at different times (even after you leave the lab). For the same reason, include a README.txt in each project folder that includes information on the study, organization scheme of the folder, and links to any other information relevant to the project.
>
>Folder Structure
>    Use the following structure (a template folder titled newProject is in Box):
>    - /admin: for IRB-related documents, including approval letter, recruitment materials, and study protocol.
>    - /analysis: for analysis scripts.
>    - /data
>      - /output: for processed data files and statistical output, including visualizations.
>      - /raw: for raw (i.e., unprocessed) data. This is the dataset downloaded directly from the data collection platform and should never be modified directly. Create code for data cleaning for reproducibility.
>    - /materials
>      - /assessment: for self-report measures, diagnostic interviews, and other assessments.
>      - /stimuli: for anything related to conducting (or replicating) the study, including qualitative interview questions, treatment materials, and experimental manipulation.
>    - /refs: for any references or resources related to the project (e.g., articles from literature review).
>    - /writing
>      - /manuscript: for initial drafts of manuscript(s) related to the project.
>      - /submission: for journal submission.
>      - /conference: for conference abstracts, posters, and presentations.
>
>File Naming
>    Use CamelCase and underscores for file naming. Avoid spaces because not all systems read spaces well. In addition, generally, files should use the following format: StudyName_ParticipantID_FileType_Date. That way, we know what study the file is related to, what content it contains, and how recent it is. If you see a file that is named differently, please correct it to this format for consistency and legibility.

>_[RobertsLab_2026](https://robertslab.github.io/resources/Lab-Notebooks/)_:
>
>An online lab notebook is **required** for all lab members. Entries should be organized by date in reverse chronological order and **updated daily**. Document so that you or a stranger could reproduce the work years later.

>_[SantiagoTiradoLab_2026](https://fungilab.nd.edu/about-us/lab-culture/)_:
>
>There is no standard as whether it is a bound notebook, loose-sheet binders, or electronic files. You can use any, but please incorporate the following:
>- Table of contents – based on numbers or dates – specially important if using a bound book!
>- Group experiments on folders, and give each folder an identifier – useful if using a binder and/or electronic files.
>- Please upload protocols, presentations, or other important data to the Lab drive where it would be available to other members.
>- VERY IMPORTANT: prior to leaving for vacation or an extended period of time, write a summary for all the experiments you've done so far. Especially, highlight where you are and what you need to do next. This will be greatly useful for when you come back, believe me!

>_[SilvermanLab_2026](https://silverman.chemistry.illinois.edu/links/Silverman_lab_expectations.pdf)_:
>
>I expect each lab experiment to be assigned a specific lab notebook entry number (e.g., JQS3087 for notebook 3 of lab member with initials JQS, page 87) at the time that experiment is initiated, rather than using placeholder values (e.g., JQS30XX) with the intention to update the placeholders “later”, because that updating typically never actually happens. Lab experiments that are initiated close in time can be continued in the notebook on a nonconsecutive page simply by writing, e.g., “see page 89” at the bottom of page 87 when a different experiment is begun on page 88.

>_[SweedlerLab_2026](https://sweedler-lab.chemistry.illinois.edu/images/Sweedler_Group_Expectations.pdf)_:
>
>“Good Laboratory Practices” and I require notebooks to be used. For data, cross reference to the actual file locations. The notebooks are required to stay in the group (which is a requirement for most of our federal funding). Your data cannot live on the instrument it was collected on and so needs to be backed up to at least two locations. We have a current SOP on these details.

>_[VuraWeisLab_2026](https://xuv.scs.illinois.edu/Vura-Weis%20Group%20Policy_v7.pdf)_:
>
>Because lab notebooks are not only important for record keeping but also for patent applications (in the future), you are expected to follow following lab notebook organization guidelines in the lab:
>1. Laser notebook : For laser alignment and laser maintenance
>2. Data collection notebook (XUV and tUV/Vis separate notebooks): Data collected from the laser lab
>3. Synthesis notebook : You are expected to thoroughly note down your experiments in your lab notebook and leave it when graduating.

>_[WarnickGroup_2026](https://www.scp.byu.edu/mers/docs/Research_Assistant_Handbook.pdf)_:
>
>8. Label all data and plots clearly, including units for all axis labels, in every document you create. Include a title or caption that has the date, identifies what was being measured, and clearly describes where the data came from. Use a large font size so that text is legible when the plot is published in a thesis or paper.
>
>9. Keep your data files, codes, and other documents in a folder under your name, so other students know which files are yours, and to avoid lost files floating on computer drives.
>10. Label files that are part of batches beginning with the date in this format: YYYY-MMDD, followed by a consistent project abbreviation, a descriptive but concise name, and indicators that distinguish the particular details of the simulation or measurement.
>11. Save all of your project files in their proper places in our group folders or servers and keep the folders updated and organized. Design the folder structure(s) to reflect natural divisions in the data and to facilitate easy retrieval of files. Move out old file versions into a subdirectory so that the latest file versions can be easily located.
>12. Back up electronic data in three places, two of which should be in different physical locations.
