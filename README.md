# FalconEye Extension for Visual Studio Code

A [Visual Studio Code](https://code.visualstudio.com/) extension which helps [FalconEye](https://tataelxsi.com/Falconeye/index.html) automation script developers create, modify & debug test scripts in Python. This extension features an integrated DUT View, a real-time test execution log view, real-time videos of DUTs, and toolbar buttons for running scripts under the FalconEye framework. 

<img src=images/falconeye-overall-view.png >

## Important
This extension will only work if you have access to the FalconEye test automation system. For this extension's features to work, you must log-in using your FalconEye credentials from this extension. For more information on video test automation & QoE measurement using FalconEye, contact falcon@tataelxsi.com

## How to configure the extension for first use?

- Click on the settings icon on the bottom left hand side of the Visual Studio Code window.

     <img src=images/settings.png >
	 

	 
- Expand the 'Extensions' category and select FalconEye

     <img src=images/falcon_settings.png >
	 
- There are three values you need to configure there. 
	- FE_Ext_Logger_Server_Port:  this extension needs to talk to a specific port on the FalconEye execution servers to fetch the logs in real-time. This port needs to be specified in this field after consulting with your respective FalconEye support team. The default value is 9010.
	
	- FE_Ext_RTSP_Server: this extension accesses the video streams from a new service running on one of the execution servers. The IP address and the port of this service are to be given in this field. The default port is 7010. Please contact your respective FalconEye support team for the IP address. 
	
	- FEFramework_API_Gateway: The IP address and the port at which FalconEye Framework APIs are hosted.

## Log-in to FalconEye

-   **Step 1.** Click on the FalconEye icon on the sidebar of Visual Studio Code. This will show a FalconEye log-in page.
-   **Step 2.** Log-in using your FalconEye credentials.
-   **Step 3.** After logging in, you should see a DUT view on the UI pane to the left.

## Main UI Components of the Extension

### DUT View 

The DUT view will show all the DUTs that are locked under your user log-in. If you need a DUT to appear here, you should lock it in FalconEye client application. 

<img src=images/falconeye-dut-view.png>

Upon clicking on a DUT, you will see a Play icon on that item. Click on this icon to open up a video page that will show the real-time video from that DUT. You may rearrange the video page to suit your layout preferences within the Visual Studio Code’s window.

### FalconEyeLog View

To open FalconEye execution logs view, click on the “View” menu of Visual Studio Code and select “Output” (Or press Ctrl + Shift + U). This will open up the output pane at the bottom. On the dropdown at the top right of this pane, select FalconEye Log. The output pane is now ready to start showing a real-time log of the test execution.

<img src=images/falconeye-log-view.png>

### FalconEye Run/Debug Buttons

These buttons will appear along with the usual Run icon that appears on the top toolbar when you open up a Python file in Visual Studio Code editor. These are the buttons a user should use to start running or debugging a FalconEye test script. The regular Run button should not be used, as it will start the Python script without the necessary command-line arguments for the test script.

<img src=images/falconeye-debug-buttons.png>

## How to run or debug a FalconEye test script in Visual Studio Code

- **Pre-requisite**: You should open the Visual Studio Code in a folder that you use for FalconEye scripting. This can be done in three ways. 
	- If you have already opened up Visual Studio Code, click on File->Open Folder on the main menu, and select the folder.
	- Using a command prompt, navigate to the folder where you want to work, then type in "code ." (code followed by a space and then a dot) and hit enter.
	- Using windows explorers, go to the scripts folder and right click, and then select the "Open with Code" option.

Open a test script, select the device from the DUT view, and then click on the “Run with FalconEye” toolbar button. This will start the script after passing all the required command-line arguments automatically. This involves the DUT identifiers and other data needed for the FalconEye framework to run a test script properly.

Follow the same process to start debugging a script; however, you should click on the “Debug with FalconEye” instead of the “Run with FalconEye” button.

While a script is under the debugger, you will be able to use breakpoints and other standard debugger features such as step through, step inside, step outside, and so on. Read python extension’s readme section for getting yourself familiarized with how to use debugging features in Visual Studio Code.

## Code Snippet Feature

  - You can also add auto generated code to your newly created script by just typing Platform type(iOS/android/STB) in the text editor.
  - API snippets can be added by just typing API name in the text editor.For Example if you need to add QuickCapture API snippet,Just type (quickcapture).
    The UI wil provide you suggestions and you can add from there.
  

   Happy scripting!
