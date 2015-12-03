# pub-list-from-ncbi
Fetch a publication list from the NCBI to populate a publications page on a website using javascript/jQuery. 

See the example in index.html, or at http://rna.berkeley.edu/publications.html.  Steps to use this: 

1) Come up with a pubmed search that finds the pubs you'd like to list

2) Replace the search in the URL below with yours and go to the URL in a browser to generate an NCBI WebEnv key for your pubmed search (note that you have to replace spaces with + in the pubmed search) 

`http://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=doudna+ja+[au]`

Take note of this field: 

```
<WebEnv>
NCID_1_402133617_130.14.18.34_9001_1449164560_72275993_0MetA0_S_MegaStore_F_1
</WebEnv>
```

This is the key that corresponds to your search in pubmed. Your WebEnv should be different than the one above. 

3) After you replace this code, look for the NCBI URL near the top `(url: "http://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&query_key=1&WebEnv=NCID_1_402133617_130.14.18.34_9001_1449164560_72275993_0MetA0_S_MegaStore_F_1",)`

Replace the WebEnv key in this URL with the one you generated for your search. 

4) Incorporate into your webpage by modifying the `pubGadget` target, or by creating a div on your webpage with the id `pubGadget`, which will then be populated by this script.  You'll also need to modify styles and etc as needed. 
