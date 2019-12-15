# Google Colab

## Google Drive and Runnning `.py` scripts

Sample code for this can be found [here](SampleCode.ipynb).

## Long training sessions

There is no official doc, but [this](https://stackoverflow.com/questions/55050988/can-i-run-a-google-colab-free-edition-script-and-then-shutdown-my-computer) is a good source. Basically, even if the browser is opened and the computer is awake, the **maximum runtime** is **12 hours**. 

- The 'maximum lifetime' of a running notebook is 12 hours (browser open)
- An 'Idle' notebook (browser closed) instance cuts-off after 90 minutes
- You can have a maximum of 2 notebooks running concurrently
- If you close the notebook window and open it while the instance is still running, the cell outputs and variables will still persist. However if the notebook instance has been recycled, your cell outputs and variables will no longer be available.

Given this, the **best approach** seems to use **Keeping you Awake** and **leave** the **browser open**, **run** the **script** in a **mounted Google Drive** and **save** the **model each epoch**. Then, even if the sessions ends and the local data is lost, the model still should have been saved to Google Drive. 