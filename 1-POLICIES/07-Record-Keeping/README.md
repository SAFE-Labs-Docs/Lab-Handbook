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

### France
>_[BoumendilLab_2026](https://igh.cnrs.fr/research-teams/team-charlene-boumendil/)_:
>
>All data and codes will be made available through public repositories, respecting the FAIR (findable, accessible, interoperable, reusable) data principles. A big part of ensuring that data are FAIR is by documenting all experiments, protocols, results etc… For this we use electronic labbooks and ensure their strict completion.

### United Kingdom
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

>_[ContextualDynamicsLab_2026](https://github.com/ContextLab/lab-manual/blob/master/lab_manual.pdf)_:
>
>You should treat GitHub as a digital version of a “lab notebook”
> that contains a formal record of every contribution you make to your projects. We use GitHub logs to assign credit for ideas, code or writing contributions,
> determine authorship order, and more. It is therefore critical that you regularly check in (commit) your work via GitHub so that you receive appropriate credit for your
> ideas and maintain a continuous traceable log for your project.

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

>_[SantiagoTiradoLab_2026](https://fungilab.nd.edu/about-us/lab-culture/)_:
>
>There is no standard as whether it is a bound notebook, loose-sheet binders, or electronic files. You can use any, but please incorporate the following:
>- Table of contents – based on numbers or dates – specially important if using a bound book!
>- Group experiments on folders, and give each folder an identifier – useful if using a binder and/or electronic files.
>- Please upload protocols, presentations, or other important data to the Lab drive where it would be available to other members.
>- VERY IMPORTANT: prior to leaving for vacation or an extended period of time, write a summary for all the experiments you've done so far. Especially, highlight where you are and what you need to do next. This will be greatly useful for when you come back, believe me!

>_[SweedlerLab_2026](https://sweedler-lab.chemistry.illinois.edu/images/Sweedler_Group_Expectations.pdf)_:
>
>“Good Laboratory Practices” and I require notebooks to be used. For data, cross reference to the actual file locations. The notebooks are required to stay in the group (which is a requirement for most of our federal funding). Your data cannot live on the instrument it was collected on and so needs to be backed up to at least two locations. We have a current SOP on these details.

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

### Canada
>_[MindaLab_2026](https://osf.io/download/arywg/)_:
>
>Every ongoing research product should have an associated MS Word or Google Doc that is shared with lab members who are involved in that project. At the top of the document, is the internal title for the project, the names of the associated lab members, and links to important documents/folders (Manuscript drafts, data ﬁles, R-code). If you make a change in some code, collect data, edit a document, or do anything else related to a project, please record that information in the Google doc with the date and your initials.
>How much detail is required in this record? There’s no perfect answer to that question, but the document should be clear enough and detailed enough so that if we revisit the project several years later, we should be able to ﬁnd where the manuscript is, where any relevant code is, and where the data is stored.
