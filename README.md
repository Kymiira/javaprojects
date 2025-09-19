# NeoForge 1.21.1 Development with Visual Studio Code

This guide provides a step-by-step process for setting up a modding environment for Minecraft 1.21.1 using NeoForge and Visual Studio Code (VS Code).

### Prerequisites

* **Java Development Kit (JDK) 21:** Ensure you have JDK 21 installed and configured on your system.
    * Confirm your installation by running `java -version` in your terminal. The output should show a version number starting with `21`.
* **Visual Studio Code:** Download and install VS Code from the official website if you haven't already.

### Step 1: Install Required VS Code Extensions

VS Code is highly customizable through extensions. You'll need these to handle the Java and Gradle aspects of the project.

1.  Open VS Code.
2.  Go to the Extensions view by clicking the Extensions icon on the Activity Bar on the side of the window, or by pressing `Ctrl+Shift+X`.
3.  Search for and install the following extensions:
    * **Extension Pack for Java:** This is a bundle of popular extensions that includes language support, debugging, and project management.
    * **Gradle for Java:** This extension provides a Gradle Explorer view to easily manage and run Gradle tasks.

### Step 2: Download the NeoForge MDK

The Mod Development Kit (MDK) is a pre-configured project template for modding.

1.  Go to the official NeoForge downloads page: [https://www.neoforged.net/download/](https://www.neoforged.net/download/)
2.  Find the download for **Minecraft 1.21.1** and download the **MDK** file.

### Step 3: Unzip and Open the MDK in VS Code

1.  Create a new folder on your computer for your mod project. For example, `MyFirst1.21.1Mod`.
2.  Extract the contents of the downloaded MDK `.zip` file into this new folder.
3.  In VS Code, go to **File -> Open Folder...** and select the folder you just created.

### Step 4: Run Gradle Tasks

VS Code will recognize the Gradle project and the extensions will start working. You can see the progress of the Gradle sync in the bottom status bar.

1.  Open the Gradle view by clicking the **Gradle** icon in the Activity Bar.
2.  You should see your project listed. Expand it, then navigate to `Tasks -> forgegradle`.
3.  Double-click on the `genVsCodeRuns` task. This task is specifically for VS Code and will generate the necessary run and debug configurations.
4.  Once that task is complete, you will see new entries in the "Run and Debug" view (`Ctrl+Shift+D`). Select **runClient** from the dropdown menu.
5.  Click the green "Play" button (Run) to launch the game.

The first time you run `runClient`, Gradle will download all the necessary dependencies and the Minecraft client, which will take some time. Subsequent runs will be much faster.

### Step 5: Start Coding!

Congratulations, your environment is now set up!

* **Code Location:** Your mod code will be in the `src/main/java/` directory.
* **Mod ID:** Make sure to change the `MOD_ID` in your main mod class file to a unique identifier.
* **Editing & Debugging:** Use the built-in VS Code debugger to set breakpoints and step through your code.

You are now ready to begin writing your mod. Happy coding!

This guide is specifically tailored for VS Code, addressing the necessary extensions and the correct Gradle task (`genVsCodeRuns`) for that environment.

Let me know if you need help with the next steps, like creating your first mod class or adding a new item. I'm here to help!
