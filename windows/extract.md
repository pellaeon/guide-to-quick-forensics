# Extract Data for Further Analysis

[pcqf](https://github.com/botherder/pcqf) is a tool that allows to dump startup information and actual processes, along with memory for further analysis. It is really helpful for instance if you do not have time to check for everything on the computer and want to double check if there is anything suspicious later on.

You should run this program from a USB key with enough storage space, double click on the binary file and follow the instructions.

![pcqf](../.gitbook/assets/pcqf1.PNG)

Unless you have a good reason to do so, it is recommended not to take a memory snapshot as it is contains a lot of private information (it may contains passwords for instance).

Once finished, it will create a folder named by the acquisition ID (a sequence of hexadecimal number) , which contains :

* A `profile.json` file containing basic information on the computer system.
* A `process_list.json` file containing a list of running processes.
* An `autoruns.json` file containing a list of all items with persistence on the system.
* An `autoruns_bins/` folder containing copies of the files and executables marked for persistence in the previous JSON file.
* An `process_bins/` folder containing copies of running processes.
* If requested, a `memory/` folder will contain a physical memory dump as well as some metadata.
