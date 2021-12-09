[comment]: # "Auto-generated SOAR connector documentation"
# Cyware

Publisher: Cyware Labs  
Connector Version: 1\.0\.3  
Product Vendor: Cyware Labs  
Product Name: Cyware Situational Awareness Platform  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.0\.251  

Implements event reporting on the Cyware platform

# cyware
Cyware Community App by Cyware


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Cyware Situational Awareness Platform asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**token** |  required  | password | Authentication Token
**secret** |  required  | password | Authentication Secret Key
**server** |  required  | string | Server IP/Hostname

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity  
[create ticket](#action-create-ticket) - Report cyber event  

## action: 'test connectivity'
Validate the asset configuration for connectivity

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'create ticket'
Report cyber event

Type: **generic**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**title** |  required  | Event title | string | 
**description** |  required  | Event description | string | 
**vault\_id** |  required  | Vault IDs of file to attach | string |  `vault id`  `pe file`  `pdf`  `flash`  `apk`  `jar`  `doc`  `xls`  `ppt`  `sha1` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.parameter\.vault\_id | string |  `vault id`  `pe file`  `pdf`  `flash`  `apk`  `jar`  `doc`  `xls`  `ppt`  `sha1` 
action\_result\.parameter\.description | string | 
action\_result\.parameter\.title | string | 
action\_result\.summary\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 
action\_result\.data\.\*\.status | numeric | 
action\_result\.data\.\*\.data\.soc\_media\.\*\.media\_file | string |  `url` 
action\_result\.data\.\*\.data\.title | string | 
action\_result\.data\.\*\.data\.description | string | 
action\_result\.data\.\*\.data\.incident\_id | string | 