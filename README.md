# bloodhound-queries
Repository of cypher custom queries for Bloodhound, broken down along query family lines. The `customqueries.json` file is automatically recompiled every time the query category files are updated.

## Install
Replace the contents of the `customqueries.json` in the following locations with the contents of the repositories instance.

### Windows

```
c:\>(wget https://github.com/InfamousSYN/bloodhound-queries/raw/main/customqueries.json).content > C:\Users\%USERNAME%\AppData\Roaming\bloodhound\customqueries.json

```

### Linux

```
┌──(kali㉿kali)-[~]
└─$ wget -O - https://github.com/InfamousSYN/bloodhound-queries/raw/main/customqueries.json | jq '.' > ~/.config/bloodhound/customqueries.json

```

## Query List

Query count: 101


```
┌──(kali㉿kali)-[~]
└─$ jq '.queries[]| select(.category? and .name?)| "\(.category): \(.name)"' ~/.config/bloodhound/customqueries.json | sed 's/^.\(.*\).$/\1/'
Top 10: [WIP] Users with Most Local Admin Rights
Top 10: [WIP] Computers with Most Sessions [Required: sessions]
Top 10: [WIP] Users with Most Sessions [Required: sessions]
Top 10: List non-privileged user(s) with dangerous permissions to any node type
Top 10: Route non-privileged user(s) with dangerous permissions to any node type
Top 10: [WIP] Users with most cross-domain sessions [Required: sessions]
Domain / Macro: List high value target(s)
Domain / Macro: List domain(s)
Domain / Macro: List domain trust(s)
Domain / Macro: List enabled user(s)
Domain / Macro: List enabled user(s) with an email address
Domain / Macro: List non-managed service account(s)
Domain / Macro: List enabled principal(s) with \"Unconstrained Delegation\"
Domain / Macro: List domain controller(s)
Domain / Macro: List Certificate Authority server(s) [Required: Certipy]
Domain / Macro: List privileges for Certificate Authority server(s) [Required: Certipy]
Domain / Macro: List all Certificate Template(s) [Required: Certipy]
Domain / Macro: Find enabled Certificate Template(s) [Required: Certipy]
Domain / Macro: [WIP] List all Enrollment Right(s) for Certificate Template(s)
Domain / Macro: List computer(s) WITHOUT LAPS
Domain / Macro: List network share(s), ignoring SYSVOL
Domain / Macro: List all group(s)
Domain / Macro: List all GPO(s)
Domain / Macro: List all principal(s) with \"Local Admin\" permission
Domain / Macro: List all principal(s) with \"RDP\" permission
Domain / Macro: List all principal(s) with \"SQLAdmin\" permission
Domain / Macro: List all user session(s) [Required: sessions]
Domain / Macro: List all user(s) with description field
Domain / Macro: List all user(s) with \"userpassword\" attribute
Domain / Macro: List all enabled user(s) with \"password never expires\" attribute
Domain / Macro: List all enabled user(s) with \"password never expires\" attribute and not changed in last year
Domain / Macro: List all enabled user(s) with \"don't require passwords\" attribute
Domain / Macro: List all enabled user(s) but never logged in
Domain / Macro: List all enabled user(s) that logged in within the last 90 days
Domain / Macro: List all enabled user(s) that set password within the last 90 days
Owned: List all owned user(s)
Owned: List all owned & enabled user(s)
Owned: List all owned & enabled user(s) with an email address
Owned: List all owned & enabled user(s) with \"Local Admin\" permission, and any active sessions and their group membership(s)
Owned: List all owned & enabled user(s) with \"RDP\" permission, and any active sessions and their group membership(s)
Owned: List all owned & enabled user(s) with \"SQLAdmin\" permission
Owned: List all owned computer(s)
Owned: Route all owned & enabled group membership(s)
Owned: Route all owned & enabled non-privileged group(s) membership
Owned: Route all owned & enabled privileged group(s) membership
Owned: Route all owned & enabled user(s) with Dangerous Rights to any node type
Owned: Route all owned & enabled user(s) with Dangerous Rights to group(s)
Owned: Route all owned & enabled user(s) with Dangerous Rights to user(s)
Owned: Route from owned & enabled user(s) to all principals with \"Unconstrained Delegation\"
Owned: Route from owned & enabled principals to high value target(s)
Owned: Owned: [WIP] Find all owned user with privileged access to Azure Tenancy (Required: azurehound)
Owned: Owned: [WIP] Find all owned user where group membership grants privileged access to Azure Tenancy (Required: azurehound)
Owned: Owned: [WIP] Find all Owners of Azure Applications with Owners to Service Principals with Dangerous Rights (Required: azurehound)
Owned: Find all owned groups that grant access to network shares
Owned: Route all sessions to computers WITHOUT LAPS (Required: sessions)
Owned: Route all sessions to computers (Required: sessions)
Non-privileged: List enabled non-privileged user(s) with \"Local Admin\" permission
Non-privileged: List enabled non-privileged user(s) with \"Local Admin\" permission, and any active sessions and their group membership(s)
Non-privileged: List enabled non-privileged user(s) with \"RDP\" permission
Non-privileged: List enabled non-privileged user(s) with \"RDP\" permission, and any active sessions and their group membership(s)
Non-privileged: List enabled non-privileged user(s) with \"SQLAdmin\" permission
Non-privileged: List all \"Domain Users\" group membership(s)
Non-privileged: List all \"Authenticated Users\" group membership(s)
Privilege Escalation / Lateral Movement: Find all enabled AS-REP roastable user(s)
Privilege Escalation / Lateral Movement: Find all enabled kerberoastable user(s)
Privilege Escalation / Lateral Movement: Route non-privileged user(s) with dangerous rights to user(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged user(s) with dangerous rights to group(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged user(s) with dangerous rights to computer(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged user(s) with dangerous rights to GPO(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged user(s) with dangerous rights to privileged node(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged computer(s) with dangerous rights to user(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged computer(s) with dangerous rights to group(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged computer(s) with dangerous rights to computer(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged computer(s) with dangerous rights to GPO(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: Route non-privileged computer(s) with dangerous rights to privileged node(s) [HIGH RAM]
Privilege Escalation / Lateral Movement: List ESC1 vulnerable Certificate Template(s) [Required: Certipy]
Privilege Escalation / Lateral Movement: List ESC2 vulnerable Certificate Template(s) [Required: Certipy]
Privilege Escalation / Lateral Movement: List ESC3 vulnerable Certificate Template(s) [Required: Certipy]
Privilege Escalation / Lateral Movement: List ESC4 vulnerable Certificate Template(s) [Required: Certipy]
Privilege Escalation / Lateral Movement: List ESC6 vulnerable Certificate Template(s) [Required: Certipy]
Privilege Escalation / Lateral Movement: List ESC7 vulnerable Certificate Template(s) [Required: Certipy]
Privilege Escalation / Lateral Movement: List ESC8 vulnerable Certificate Template(s) [Required: Certipy]
Privilege Escalation / Lateral Movement: List all cross-domain user session(s) and user group membership(s)
Privileged: List privileged user(s) without \"Protected Users\" group membership
Privileged: List custom privileged group(s)
Privileged: List all enabled SVC account(s) with privileged group membership(s)
Privileged: Route all privileged user(s) with sessions to non-privileged computer(s) [Required: sessions]
Persistence: Find allshortestpaths with dangerous rights to AdminSDHolder object
Persistence: Find allshortestpaths with DCSync to domain object
AAD: List all Tenancy (Required: azurehound)
AAD: [WIP] List all AAD Group(s) that are synchronized with AD (Required: azurehound)
AAD: [WIP] List all principal(s) used for syncing AD and AAD
AAD: List all enabled Azure User(s) (Required: azurehound)
AAD: List all enabled Azure User(s) Azure Group membership(s) (Required: azurehound)
AAD: [WIP] List all AD principal(s) with edge(s) to Azure principal(s) (Required: azurehound)
AAD: [WIP] List all principal(s) with privileged access to Azure Tenancy (Required: azurehound)
AAD: [WIP] Route all principal(s) that have control permissions to Azure Application(s) running as Azure Service Principals (AzSP), and route from privileged ASP to Azure Tenancy (Required: azurehound)
AAD: [WIP] Route all user principal(s) that have control permissions to Azure Service Principals (AzSP), and route from AzSP to principal(s) (Required: azurehound)
AAD: [WIP] Route from Azure User principal(s) that have dangerous rights to Azure User and User principal(s) (Required: azurehound)
AAD: [WIP] Route from principal(s) to Azure VM (Required: azurehound)
AAD: [WIP] Route from principal(s) to principal(s) with Global Administrator permissions (Required: azurehound)
 
```

## Privileges

**AD**

```[r:Owns|AdminTo|SQLAdmin*1..]```

**AAD**

```[:AZGlobalAdmin|AZPrivilegedAdminRole*1..]```


## Dangerous Rights

**AD**

> ``` [r:Owns|GenericAll|GenericWrite|WriteOwner|WriteDacl|WriteSPN|AllExtendedRights|ExecuteDCOM|AllowedToDelegate|ForceChangePassword|AllowedToAct|AddAllowedToAct] ```

**AAD**

``` ```

## Access

**AD**

``` [r:AdminTo|SQLAdmin|HasSession|CanRDP] ```

**AAD**

``` ```
