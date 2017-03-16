# Intro
The fork is aimed to provide a update to the movebank api document. The first commit just convert original document from rtf to markdown with only format changes, which inlcude:
- convert links to markdown links
- quote code properly
- convert csv format data into markdown table, so it will be much easier to read. The code I used is in `csv-to-markdown-table.Rmd`. 
  Note I put the markdown table in fenced code mode instead of rendering it, because I feel this format is actually more readable with proper alignment. It will be more difficult to copy data in this format, but I expect all these data can be get from api call easily so this should not be a problem.

With documentation in markdown format, it will be much eaiser to manage with version control, accept pull requests from user etc.

I'll start to add some notes to the document in next commit.
