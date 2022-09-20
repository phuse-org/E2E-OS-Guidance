### Preparing for release

#### When is a good time to open source?  

As a general rule arising IP[^3], that is IP generated as part of the project, is simpler to handle than background IP that already exists. So, there is often a strong benefit to define what you want to do, decide if it would be open sourced, and if so, then start it in an open-source setting. This also helps to encourage defining a clear scope from day one, and encourage others to engage early rather than initiate additional projects that later may not be compatible without significant refactoring. 

[^3]: https://www.lawinsider.com/dictionary/arising-intellectual-property

#### Does it matter where you put a package on github.com?  

What are the differences between GitHub organizations that host packages like phuse-org, rinpharma, ropensci, openpharma, personal organisations, company owned organisations and organisations created to host a single project? 

Ultimately, the license chosen has an impact on how a package can be used, rather than the location the code is shared from. The location though can influence how a project is perceived. If it is hosted on a GitHub organisation with the name of a pharma company, relative to a pan-company organisation, it may imply that the project is ‘Company A’s’ project rather than something they wish to co-create. As a general rule, the recommendation would be to place it in a company's organisation if you wish to remain control of the roadmap, but look to pan-company organisations if you wish to co-create and co-own the packages trajectory. Some examples are; 

* Personal Github orgs 
  * `diffdf` (gowerc/diffdf) and survival (therneau/survival) are examples of two repositories used in pharma hosted in Github orgs belonging to a specific individual 
* Project/Initiative Github orgs 
  * `openpharma`: While openpharma has a dashboard and metadata pipeline that is agnostic to where a package comes from, it also will house packages that do not want to be associated with a specific company or organisation 
  * `pharmaverse`: A sub-set of the pharmaverse clinical reporting repositories are also hosted on the pharmaverse Github org 
  * `pharmaR`: Houses repositories from the R Validation Hub working group 
* Company Github orgs 
  * Many companies maintain Github orgs either at the company or department in a company level, like `GSK-Biostatistics`, `Roche`, `Genentech`, `Novartis` 
* Organisation Github orgs 
  * `phuse-org`: PHUSE projects and working groups from PHUSE 
  * `ropensci`, `ropenscilabs`, `ropensci-docs`, etc: rOpenSci maintains several GitHub orgs, with rOpenSci housing mature R packages contributed by their staff, or peer-reviewed.  

#### What is important to look for when releasing a package that started life internally? 

If a package started its development on an internal git server, or a private repository on github.com, there could be some risk of exposing data either in issues, or historical commits. These could range from screen shots of patient data, tables or other business confidential information in issues, to passwords or files in the git commit history that were deleted but not purged. The recommendation is to always flatten the commit history, and wipe issues by starting a new git repository when open sourcing unless you are certain no information can be leaked.   

#### Could others claim we stole their IP? 

When discussing the open sourcing of a codebase, it is important to flag to internal counsel existing external projects, and the overlap of scope with the project you intend to release. 

It is possible that decisions made before open sourcing could become a risk after open sourcing. As an example of a plausible scenario; a team need to implement a new function. This function exists in another GPL-3 copy left licenced project. To add that project would introduce multiple dependencies that aren’t used by that particular function so a member of the team decides to copy the function into the package. One year later, the package is open sourced with the licence infringing code. Such an occurrence could be lessened by a Contributor License Agreement  (CLA; see https://github.com/contributor-assistant/github-action for an example of CLA automation). A CLA helps ensure that anyone contributing to a project acknowledges specific terms expected of contributions, like the contributions are novel code and the author will abide by the projects license terms. In the absence of a CLA it is important to ensure that all code within the package is original, and there is no culture of cannibalising external code and infringing on people’s copyright within the development team even for internal projects. 