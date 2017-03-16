# Intro on the fork
The fork is aimed to provide a update to the movebank api document. 

The first commit just convert original document from rtf to markdown with only format changes, which inlcude:
- convert links to markdown links
- quote code properly
- convert csv format data into markdown table, so it will be much easier to read. The code I used is in `csv-to-markdown-table.Rmd`. 
  Note I put the markdown table in fenced code mode instead of rendering it, because I feel this format is actually more readable with proper alignment. It will be more difficult to copy data in this format, but I expect all these data can be get from api call easily so this should not be a problem.

With documentation in markdown format, it will be much eaiser to manage with version control, accept pull requests from user etc.

# Tips on working with API
- You can open a specific study page directly with url pattern like

    `https://www.movebank.org/movebank/#page=studies,path=study121041109`

    I found this is very helpful in development and testing.

- I strong recommend to use [postman](https://www.getpostman.com/) for web API development.
    + You can save your user name and password in environment, then use them in any API call easily
  ![postman 1](postman/postman1.png?raw=true)
    + You can save your API call into a collection, edit API call parameters easily, check API call response header, results with different viewing modes.
  ![postman 2](postman/postman2.png?raw=true)
