### VARIABLES
#### Strings
````
[System.String]$a = ""
[System.String]$b = "Hello!"
[System.String]$c = "Hello" + "!"
# Return the length of the string
$c.Length
# String formating
[System.String]::Format("My name is {0}! Hi {1}!", "John", "Dude")
````
#### Numbers
````
[System.Int32]$number = 1
[System.Int32]$number = 5 * 5
[System.Double]$float = 1.3
````
#### Arrays
````
$arr = "a", "b"             # Array of strings
$arr = @()                  # Empty array
$arr[5]                     # Sixth array element
$arr[-3..-1]                # Last three array elements
$arr[1,4+6..9]              # Elements at index 1,4, 6-9
$arr[1] += 200              # Add to array item value
$arrZ = $arrA + $arrB       # Two array into a single array
# Return the length of the array
$arr.Length
````
#### Hashtable
````
[Hashtable]$hashtable = @{"Title": "My Title"}  # Create hashtable
$hashtable
$hashtable.Title     # Return the value of key Title
$hashtable.Keys      # Returns the available keys
$hastable.Values     # Returns the values
$hashtable.GetType() # Returns the type of the variable
````
#### PSCustomObject
````
$psobject = New-Object PSObject
Add-Member -InputObject $psobject -MemberType NoteProperty -Name "Title" -Value "My Title"
$psobject
$psobject.Title       # Return the value of NoteProperty Title
$psobject.GetType()   # Returns the type of the variable
````
### DATE/TIME
#### Date
````
[System.DateTime]$datetime = (Get-Date).Date
$datetime.Day
$datetime.DayOfWeek
$datetime.AddDays(5)
# Define format
$datetime.ToString('yyyyMMdd')
# Get predefined formats
$datetime.GetDateTimeFormats()
$datetime.GetDateTimeFormats().IndexOf('Sonntag, 17. Februar 2019 23:00:00')
$datetime.GetDateTimeFormats()[47]
````
### LOOPS
#### While
````
$i = 0
While ($i -le 10) {
    $i
    $i++
}
````
#### ForEach
````
$j = @("a", "b", "c")
ForEach ($i in $j) {
    $i
}
````
#### For
````
For ($i = 1; $i -le 10; $i++) {
    $i
}
````
### FUNCTIONS
#### Function
````
function MyFunction($a, $b) {
    # do something with a and b
    return $a + $b
}
````
#### Function
````
function MyFunction() {
    param(
        [System.String]$a,
        [System.String]$b
    )
    # do something with a and b
    return $a + $b
}
````
### CLASSES
#### Class
````
class MyClass
{
    [System.String]$name
    
    [System.String]SayHello() {
        return "Hello, " + $this.name
    }
}
$class = [MyClass]::new()
$class.name = "John"
$class.SayHello()
````
### WRITE TO FILE
#### Transcript
````
Start-Transcript -Path "C:\logs\mytranscript-1.log" -NoClobber
# Your script here
Write-Output "My log entry.."
Stop-Transcript
````
#### Out-File
````
Write-Output "My log entry.." | Out-file -Path "C:\logs\my-1.log" -append
````
#### Export-Csv
````
Get-Service | Export-CSV .\service.csv
````
### CONFIG FILES
Use .psd1 file to separate config
````
# myConfig.psd1
@{
    apiUrl = 'https://<domain>/api/v1/'
  
    NestedOptions = @{
        Option1 = 'Value1'
        Option2 = 'Value2'
    }
}

# myScript.ps1
$config = Import-PowerShellDataFile -Path myConfig.psd1

# Read values
$config.url
$config.NestedOptions.Option1
$config.NestedOptions.Option2
````
### SECURITY
Credential object using Secure String
> Note: The System.Security.SecureString is calculated using the account you are running the current instance! 
````
"<password>" | ConvertTo-SecureString -AsPlainText -Force | ConvertFrom-SecureString #| Out-File "C:\password.txt"
$pass = "<securestring>" | ConvertTo-SecureString
$user = "<domain>\<account>"
$cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList ($user, $pass)
````
