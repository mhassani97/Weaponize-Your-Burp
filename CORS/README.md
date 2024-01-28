## CORS Misconfiguration Automation in Burp Suite 
#### <em>Extentions: AutoRepeater and Logger++</em>


## AutoRepeater Replacement Configuration 
1) Add Origin Header:

    ```
    Type: Add Header
    Match: 
    Replace: Origin: https://mahdi.computer
    Which: Replace Frist
    Regex Match: Disabled
    ```
    
2) Replace Origin Header:

    ```
    Type: Request Header
    Match: Origin:
    Replace: Origin: https://mahdi.computer
    Witch: Replace Frist
    Regex Match: Disabled
    ```
    
## Logger++ Filter For AutoRepeater CORS Misconfiguration

    Response.Headers CONTAINS "Access-Control-Allow-Origin: https://mahdi.computer" AND Response.Headers CONTAINS "Access-Control-Allow-Credentials: true"
    

<h4><em>Happy Hunting ;) </em><h4>
