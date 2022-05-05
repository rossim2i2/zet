# Use PSScriptAnalyzer as a `Shellcheck` for PowerShell Scripts

I've recently been writing PowerShell scripts at work to take care of
some various tasks, which we'd otherwise need to outsource. While I'm
careful to inspect and understand what each line of code is doing, I was
hoping to find something like Shellcheck, which could offer suggestions
based on best practices.

I asked our new Head of Security if he knew of anything like this and he
instantly pointed me to PSScriptAnalyzer, which he said is the go-to in
the field. Although it seems to be more geared towards syntax checking,
compatibility checking, and style-checking.

To install the tool, as administrator, run the following command:

```PowerShell
Install-Module -Name PSScriptAnalyzer -Force
```

To run the check on a script, simple run:

```PowerShell
Invoke-ScriptAnalyzer -Path PathToScript.ps1
```

The output will list all issues found and their Severity.

```Powershell
PS> Invoke-ScriptAnalyzer -ScriptDefinition '"b" = "b"; function eliminate-file () { }'

RuleName            Severity   ScriptName Line Message
--------            --------   ---------- ---- -------
InvalidLeftHandSide ParseError            1    The assignment expression is not
                                               valid. The input to an
                                               assignment operator must be an
                                               object that is able to accept
                                               assignments, such as a variable
                                               or a property.
PSUseApprovedVerbs  Warning               1    The cmdlet 'eliminate-file' uses an
                                               unapproved verb.
```

    #security #scripting #PowerShell
