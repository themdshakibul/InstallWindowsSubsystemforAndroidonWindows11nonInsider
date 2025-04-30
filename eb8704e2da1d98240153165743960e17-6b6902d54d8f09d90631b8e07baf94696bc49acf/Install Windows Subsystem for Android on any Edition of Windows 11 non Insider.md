# Install Windows Subsystem for Android on Windows 11 non Insider

WSA or Windows Subsystem for Android is a Tool that allows Windows to run Android Apps directly without using any emulator. The problem is Windows Subsystem for Android is currently only available through preview via the Beta Channel of the Windows Insider Program. But if you follow this guide, you don't have to be in Windows Insider Program to try it out. The only thing you need is Windows 11 installed and some patience.

## Prerequisites:
* A Device with any version and Edition of Windows 11 installed.
* Internet Connection.
* [Hyper-V enabled](#Enable-Hyper-V).

## Enable Hyper-V:
* If Hyper-V is already enabled, [click here](#Follow-these-steps) to skip this part.
* If your Windows Edition is `Home`, [click here](https://gist.github.com/HimDek/6edde284203a620745fad3f762be603b) to know how to enable Hyper-V in Windows Home Edition.
* If your Windows Edition is `Pro`, `Enterprise` or `Education` follow the bellow steps to enable Hyper-V:
  * Search for `Turn Windows features on or off` in the Start Menu search bar and open it.
    ![10](https://user-images.githubusercontent.com/61367380/141923398-ee251035-8e1d-42e6-9551-5c797e2b8f73.png)
  * In the Window, lookout for `Hyper-V`, `Virtual Machine Platform` and `Windows Hypervisor Platform`. Then check the check boxes before them and click `OK`. This will also take some time and then a Restart is necessary. After this step, Hyper-V will be enabled.

## Follow these steps:
* Go to [https://store.rg-adguard.net/](https://store.rg-adguard.net/). You will see the page shown in the below screenshot.
  ![1](https://user-images.githubusercontent.com/61367380/141881825-20ca849d-ddb8-443d-b883-1af5fb21db9e.png)
* Select `ProductID` from the first drop down list.
* Enter `9p3395vx91nr` in the box next to it.
* Select `Slow` from the drop down box next to it.
  ![2](https://user-images.githubusercontent.com/61367380/141882202-2c5401cb-cdaf-4a10-a93d-67d231aafbe7.png)
* Then click the checkmark icon.
* A list of files will appear below as results.
* You have to find `MicrosoftCorporationII.WindowsSubsystemForAndroid_<version>.msixbundle` from that list. In the list the `<version>` will be replaced by the current version number. As of writing this the file size is around `1.2GB`.
* Right Click this file and click `Save link as...` from the context menu as shown in the screenshot below.
  ![3](https://user-images.githubusercontent.com/61367380/141882808-d3348fad-220d-4a21-b0fb-468ce144fb9b.png)
* Now save the file and remember its location. The file will be downloaded to that location.
* If you see a warning that the file can't be downloaded securely as shown in the screen shot below, click the upward arrow icon and click keep. Then the download will start.
  ![4](https://user-images.githubusercontent.com/61367380/141883353-19f2a557-9cbb-4a7f-8c3c-1e46f122592a.png)
* After the download is finished, browse to its location, Right click it and click `Copy as path` as shown in the screenshot below.
  ![5](https://user-images.githubusercontent.com/61367380/141884516-dda65b19-2abd-42e2-b2b5-a8afa24d3609.png)
* In the start menu, search `powershell`, right click `Windows PowerShell` and click `Run as Administrator` as shown in the screenshot below.
  ![6](https://user-images.githubusercontent.com/61367380/141885081-e84efb8a-32ef-4c95-9eda-91303d6c9cb7.png)
* In the powershell window, type `Add-AppxPackage ` and then paste the path that you copied by pressing `Ctrl + V`. The powershell window should look simillar to the screenshot below. Then press Enter. The installation will start.
  ![7](https://user-images.githubusercontent.com/61367380/141886091-d119b086-fa94-4dda-80dd-2c5a24242dc8.png)
* After the installation is done, you can close the PowerShell window and the `Windows Subsystem for Android Setting` will appear on the Start Menu.
  ![8](https://user-images.githubusercontent.com/61367380/141886990-9c745a77-ee8c-45ed-9d5a-c16cc0505b71.png)
* On running `Windows Subsystem for Android Setting`, the window shown in the screenshot below will appear. There, click on the icon in the extreme left side of the Files box. This will start Windows Subsystem for Android and open the `File Manager` App in Android.
  ![9](https://user-images.githubusercontent.com/61367380/141887519-c2f80fc2-75fe-449b-a899-b842c545788a.png)

## You might also like:
#### [Install Android apps or apk files in Windows using Windows Subsystem for Android (No Emulator)](https://gist.github.com/HimDek/e09340eae2861e1ad8b7f6bdba5ee9ff)