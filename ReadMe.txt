1. Right-Click on "Install_CPIME.INF" file and run "Install".
2. Intall "Chinese (Traditional, Hong Kong SAR)" language in Windows Setting
3. Open Windows PowerShell and copy & paste the commands below to PowerShell window

##################################
$langs = Get-WinUserLanguageList
$hanthk = ($langs | Where-Object LanguageTag -like 'zh-Hant-HK')
$hanthk.InputMethodTips.Clear()
$hanthk.InputMethodTips.Add('0C04:E03D0C04')
Set-WinUserLanguageList $langs
##################################

4. Press Enter key and "Y" to finish setup

For details with screenshot, please refer to CPIME websites: https://www.cpime.hk/p/how-to-install.html?lang=en
