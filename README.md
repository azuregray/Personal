# **P E R S O N A L &emsp; R E P O S I T O R Y**

> Author: **Darshan S**

> My Identity >>  [Github](https://github.com/azuregray/) | [LinkedIn](https://linkedin.com/in/arcticblue/) | [Instagram](https://instagram.com/thedarshgowda/) | [YouTube](https://www.youtube.com/@pantoneblue/) | [Telegram](https://t.me/adobegreen/) | [Mail](mailto:d7gowda@gmail.com)


### *Repository For My Own Personal Uses*.
#### *This repository is for my personal use so please Do Not Contact Me for anything here.*

> I have chosen to use **POWERSHELL** as the command interpreter as it is the new default in windows machines now and ofcourse there are windows machines everywhere.

---
## **U S A G E**

### Single File needs a *Single Command*:
```
(iwr -uri *UrlDirectToFile* ).content | clip
```
---
### Multiple Files simplified by a *Function*:
> _NOTE: You can write the whole function in a single line too.._

- **Function Definition as a BLOCK:**
```
function gcl{
param(
[parameter(mandatory=$true, position=0)]
[string] $uri)
(iwr -uri $uri).content | clip
}
```
- **Function definition as INLINE:**
```
function gcl{ param([parameter(mandatory=$true, position=0)] [string] $uri) (iwr -uri $uri).content | clip }
```

- **Usage of Inline Function:**
```
gcl UrlDirectToFile
```

- **Undefine the function:**
```
remove-item function:\gcl
```
---
### Repeated Fetching easier with _ForEach_ loop:

##### FOREACH LOOP SYNTAX

> rangeSTART.....rangeEND | foreach { command_with_($)sign_at_loopingPosition }

##### Examples: 
- For fetching _program1.html_ >> _program12.html_:
```
1..12 | foreach {iwr -uri https​://raw.githubusercontent.com/azuregray/Personal/main/program$($_).html -outfile program$($_).html}
```
- For fetching _q51.txt_ >> _q55.txt_:
```
1..5 | foreach {iwr -uri https​://raw.githubusercontent.com/azuregray/Personal/main/q5$($_).txt -outfile q5$($_).txt}
```
---
 _**UriDirectToFile**_ for this repo is as follows:

> https​://raw.githubusercontent.com/azuregray/Personal/main/<span><</span>FileName<span>></span>

---

