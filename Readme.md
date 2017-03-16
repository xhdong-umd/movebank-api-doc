# Intro on the fork
The fork is aimed to provide an update to the movebank api document. 

The first commit just convert original document from rtf to markdown with only format changes, which inlcude:
- convert links to markdown links
- quote code properly
- convert csv format data into markdown table, so it will be much easier to read. The code I used is in `csv-to-markdown-table.Rmd`. 
  Note I put the markdown table in fenced code mode instead of rendering it, because I feel this format is actually more readable with proper alignment. It will be more difficult to copy data in this format, but I expect all these data can be get from api call easily so this should not be a problem.

With documentation in markdown format, it will be much eaiser to manage with version control, accept pull requests from user etc.

## files
```
├── Readme.md
├── document
│   ├── all_attributes.md                             *all attributes annoated*
│   └── movebank_api.md                               *the api document in markdown*
│   └── rtf_format_version_2015.11
│       └── movebank_api.rtf                          *the original api document*
├── postman
│   ├── movebank_no_auth.postman_collection.json      *postman collection of some api calls*
│   ├── postman1.png
│   └── postman2.png

└── utils
    └── csv_to_markdown_table.Rmd                     *R code to convert csv into markdown table*
```

## Tips on working with API
- You can open a specific study page directly with url pattern like

    `https://www.movebank.org/movebank/#page=studies,path=study121041109`

    I found this is very helpful in development and testing.

- I added some notes to the `all attributes` response, which have many important API calls not covered by the original api document.

- I strong recommend to use [postman](https://www.getpostman.com/) for web API development.
    + You can save your user name and password in environment, then use them in any API call easily.
    For example, click the gear icon in right top corner, manage environments, globals, add `user` and `pass`, then add authorization in API call: Basic Auth, user name: {{user}}, password: {{pass}}.
  ![postman 1](postman/postman1.png?raw=true)
    + You can save your API call into a collection, edit API call parameters easily, check API call response header, results with different viewing modes.
  ![postman 2](postman/postman2.png?raw=true)
    + When using postman with a long list of attributes, the spaces after comma may cause problem. So instead of `id, local_identifier, taxon_id`, use `id,local_identifier,taxon_id`.

- I have uploaded my postman collection of some API calls in `postman` folder. However due to [a design flaw of postman](https://github.com/postmanlabs/postman-app-support/issues/1463), the basic auth header will be saved in exported postman collection which will expose user name and password. So I have to set all API calls as `no auth`, replace the header value in exported json. After importing this collection to postman, you need to set your own environment, then add the basic auth for API calls by yourself.
