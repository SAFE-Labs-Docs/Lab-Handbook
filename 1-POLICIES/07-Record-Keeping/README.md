# I commit to internally document the lab's expectations for record keeping

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
### United States
>_[AeryJonesLab_2026](https://aeryjones.github.io/philosophy)_:
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