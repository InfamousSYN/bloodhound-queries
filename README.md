# bloodhound-queries
Repository of cypher custom queries for Bloodhound, broken down along query family lines. The `customqueries.json` file is automatically recompiled every time the query family files are updated.

## Install
Replace the contents of the `customqueries.json` in the following locations with the contents of the repositories instance.

**Windows**

```C:\Users\%USERNAME%\AppData\Roaming\bloodhound\customqueries.json```

**Linux**

```~/.config/bloodhound/customqueries.json```

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
