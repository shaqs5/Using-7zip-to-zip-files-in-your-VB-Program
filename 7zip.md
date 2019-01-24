# Using 7zip to zip files in your VB Program

Before you could start please download and install the 7-zip from [7-zip.org](http://www.7-zip.org/)
You can install in any path you like I installed it in “C:\Program Files\7-Zip”. 
7-zip in the command prompt is used as below 

```
C:\program files\7-Zip> 7z <command> [<switches>...] <archive_name> [<file_names>...]
```

## Example

```
C:\Program Files\7-Zip> 7z a C:\temp\test.zip C:\somefolder\test.txt
```
Where “a” is for Add file to archive and “C:\temp\test.zip” is the target path and filename for zip output. Last but not least is the source path and filename.

## How to use 7-zip

Below code shows how to use 7-zip in your VB.net desktop application.

```
Public Class frmZipFile
    Button that will call the ZipFile on Click
    Private Sub btnZipFile_Click(sender As Object, e As EventArgs) Handles btnZipFile.Click
        'Call ZipXML method here.
	ZipFile("C:\temp\tribcard.zip", "C:\temp\tribcard.txt")
    End Sub

    'Zip output files using windows command prompt processor "
    Private Sub ZipFile(ByVal ZipTarget As String, ByVal ZipSource As String)
        Process.Start("C:\Program Files\7-Zip\7z.exe", " a " & ZipTarget & " " & ZipSource & "")
    End Sub
End Class
```

## More details

For more details on usage, commands and switches please visit FAQ on [7zip.org](http://7zip.org)

## Author

* **Shaq**


