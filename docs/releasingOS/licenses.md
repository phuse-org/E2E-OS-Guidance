### Licenses: releasing a project 

Ultimately, the license used for a project would require in-house counsel guidance on what license is preferred. 

All code open-sourced should have a license. The license has a standard location of being a text file called ‘LICENSE’ in the root of the project folder, or a markdown file called ‘LICENSE.md’. Of particular note is that R packages often have the license specified in the R specific location of the DESCRIPTION file, or may have it in both the standard and R specific locations (in rare cases these can also contradict so it is important to read both). 

Generally, permissive licenses are more common in clinical reporting, with the majority of pharmaverse R packages using an MIT (https://choosealicense.com/licenses/mit/) or Apache 2.0 (https://choosealicense.com/licenses/apache-2.0/) license. These licences allow distribution, commercial use and modification. One primary difference between MIT and Apache 2.0 is that the former has patent protection language and rules around trademark usage, and may be preferred in larger projects due to its focus on more explicitly spelling out the terms. 