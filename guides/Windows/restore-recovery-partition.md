## 1. Use diskpart to create the partition

```cmd
diskpart
list volume ===> identify the volume # for C drive
select volume # ===> where # found from above
shrink desired=529 ===> the Recovery partition for Win10 ver. 1909
create par pri
format fs=NTFS quick label=Recovery
# For GPT
set id=DE94BBA4-06D1-4D40-A16A-BFD50179D6AC ===> Id for Recovery type
gpt attributes=0x8000000000000001

# For MBR
set id=27  ===> Id for Recovery type

exit
```

## 2. copy WinRE.wim and the uninitialized ReAgent.xml files from the installation Media to C:\Windows\System32\Recovery
Mount the Installation ISO. 
If already mounted, Under Sources folder, Use 7-zip to open either **install.ed** or **install.wim** then navigate to **Windows\system32\Recovery** then copy both files

> [!Note] 
> The install.esd or install.wim might contain multiple editions of Windows, just use any index.
> Also Recovery folder is hidden, you'd need to set the option to show hidden.

## 3. From Admin command
Run `reagentc /enable`. This will move WinRe.wim to the Recovery partition and set the GUID and location in ReAgent.xml 
