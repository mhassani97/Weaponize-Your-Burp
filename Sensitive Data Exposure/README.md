## Sensitive Data Exposure Automation in Burp Suite 
#### <em>Extentions: Logger++</em>

    
## Logger++ Filter For Sensitive Data Exposure

    Response.Body == /(?i)([a-z0-9]+){0,}((_|-){0,}(\\s){0,})(APIkey|secret|accesstoken|apiToken|localhost)(\\s){0,}(=|:|is|>){1,}/ AND Response.Headers CONTAINS "application/javascript"
    
    
    
    Request.QueryParams CONTAINS "file" OR Request.QueryParams CONTAINS "page" OR Request.QueryParams CONTAINS "site" OR Request.QueryParams CONTAINS "document" OR Request.QueryParams CONTAINS "folder" OR Request.QueryParams CONTAINS "download" OR Request.QueryParams CONTAINS "view" OR Request.QueryParams CONTAINS "path"
    

<h4><em>Happy Hunting ;) </em><h4>
