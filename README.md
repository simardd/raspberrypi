**********************
Windows PowerShell transcript start
Start time: 20180510184837
Username: CCDEVENVRDP3\Joanne
RunAs User: CCDEVENVRDP3\Joanne
Configuration Name: 
Today is Wednesday
Meeting time!
Machine: CCDEVENVRDP3 (Microsoft Windows NT 10.0.16299.0)
Host Application: C:\WINDOWS\system32\WindowsPowerShell\v1.0\PowerShell_ISE.exe
Process ID: 6132
PSVersion: 5.1.16299.431
Cell Phone:
Powershell: 6.0
Powershell Rocks!!!
PSCompatibleVersions: 1.0, 2.0, 3.0, 4.0, 5.0, 5.1.16299.431
BuildVersion: 10.0.16299.431
CLRVersion: 4.0.30319.42000
WSManStackVersion: 3.0
PSRemotingProtocolVersion: 2.3
Jean-Mark is doing a Preentation in 5 minutes!!!
SerializationVersion: 1.1.0.1
**********************
Transcript started, output file is C:\Users\Joanne\Documents\PowerShell_transcript.CCDEVENVRDP3.J6icPSeX.20180510184837.txt
PS C:\Users\Joanne> $yesterday = get-date (get-date).addDays(-1) -UFormat "%Y%m%d"
PS C:\Users\Joanne> $yesterday
20180509
PS C:\Users\Joanne> $today = get-date -UFormat "%Y%m%d"
PS C:\Users\Joanne> $tomorrow = get-date (get-date).addDays(+1) -UFormat "%Y%m%d"
PS C:\Users\Joanne> $yesterday1 = get-date (get-date).addDays(-1) -UFormat "%d-%m-%Y"
PS C:\Users\Joanne> $yesterday1
09-05-2018
PS C:\Users\Joanne> $today2 = get-date -UFormat "%d-%m-%Y"
PS C:\Users\Joanne> $tomorrow2 = get-date (get-date).addDays(+1) -UFormat "%d-%m-%Y"
PS C:\Users\Joanne> $yesterday2 = get-date (get-date).addDays(-1) -UFormat "%m/%d/%Y"
PS C:\Users\Joanne> $yesterday2
05/09/2018
PS C:\Users\Joanne> $today3 = get-date -UFormat "%m/%d/%Y"
PS C:\Users\Joanne> $tomorrow3 = get-date (get-date).addDays(+1) -UFormat "%m/%d/%Y"
PS C:\Users\Joanne> $animals = "dog", "cat", "mouse"
PS C:\Users\Joanne> $animals -contains "Mouse"
True
PS C:\Users\Joanne> $animals -ccontains "Mouse"
False
PS C:\Users\Joanne> $addAnimals = "dog", "cat", "mouse", "turtle"
PS C:\Users\Joanne> Compare-Object $animals $addAnimals

InputObject SideIndicator
----------- -------------
turtle      =>


PS C:\Users\Joanne> (Compare-Object $animals $addAnimals).InputObject
turtle
PS C:\Users\Joanne> $append = (Compare-Object $animals $addAnimals).InputObject 
PS C:\Users\Joanne> $append | out-file -Append C:\temp1\powershell\ex4.txt
PS C:\Users\Joanne> $addAnimals+= "mouse"
PS C:\Users\Joanne> $addAnimals
dog
cat
mouse
turtle
mouse
PS C:\Users\Joanne> $addAnimals | select -uniq
dog
cat
mouse
turtle
PS C:\Users\Joanne> $sort = $addAnimals | select -uniq | Sort-Object -Descending
PS C:\Users\Joanne> $sort
turtle
mouse
dog
cat
PS C:\Users\Joanne> $sort | out-file -Append C:\temp1\powershell\ex4.txt
PS C:\Users\Joanne> Get-ChildItem C:\Windows\System32\ -file | Select -first 1


    Directory: C:\Windows\System32


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        9/29/2017   1:41 PM            308 @AudioToastIcon.png


PS C:\Users\Joanne> $lines = (Get-ChildItem C:\Windows\System32 -file | Select -first 1 | Measure-Object -Line).Lines
PS C:\Users\Joanne> $lines
1
PS C:\Users\Joanne> New-Alias Joanne
PS C:\Users\Joanne> Joanne
PS C:\Users\Joanne> Stop-Transcript
**********************
Windows PowerShell transcript end
**********************
