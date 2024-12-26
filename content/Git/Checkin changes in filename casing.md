

When changing the casing of a file, git does (under certain circumstances) not recognize the changes. To get the changes checked in, there is a
simple workaround.  
Assuming the file `Myfile.txt` was changed to `myfile.txt`, you can  

1. Rename the file to something entirely new (`mv myfile.txt myfile_tmp.txt`)  
2. Check that new file in (`git add myfile_tmp.txt`)  
3. Name the file back to the originally intended name (`mv myfile_tmp.txt myfile.txt`)  
4. Check the file in again (`git add myfile.txt`)  

Git should now recognize the changed casing in the filename.