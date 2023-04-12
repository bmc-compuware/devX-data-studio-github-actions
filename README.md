# Overview
The BMC AMI DevX Data Studio extension can be used to execute either Unit or Functional test scenarios automatically. 

# BMC AMI DevX Data Studio

This allows your GitHub Actions workflow to execute an automated test using Total Test. This action uses Total Test scenarios stored in your local Eclipse workspace. <br>
          
# Table of Contents

  * DevX_Data-Studio-CLI-Local
    * [Table of Contents](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#Table%20of%20Contents)
    * [Prerequisite](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#Prerequisite)
    * [Usage](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#Usage)
    * [Inputs](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#Inputs)
    * [Outputs](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#Outputs)
    * [Troubleshooting](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#Troubleshooting)
    * [License summary](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#license-summary)
    * [Product Assistance](https://github.com/marketplace/actions/bmc-ami-devx-data-studio/#product-assistance)

# Prerequisite

 * You can host your own runners and customize the environment used to run jobs in your GitHub Actions workflows, Click [here](https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners).
 * User need to setup BMC AMI DevX workbench CLI into local system.
 * User has to setup the MF password in github repository with the following steps
   * "Github Repository" -> Settings-> Secrets-> Actions-> New repository secret

# Usage

* Triggers the workflow to execute the provided test scenario on any pipeline where the BMC AMI DevX Data Studio Auto Run is added. 
* Steps to use the extension
  * Install the BMC AMI DevX workbench CLI into local system, Click [here](https://download.api.compuware.com/web/private/66jvM2Rf5dcHtVjXdYhudGtRn9CtHzYq/test-management/results.html).
  * CLI Execution path - Go to the local drive of a system and check the .bat file location i.e "C:\\BMC AMI DevX\\topazworkbenchcli.20.12.03.134\\".
  * HCI Connection - Provide the HCI connection i.e CW01.bmc.com
  * Port - Provide the HCI connection port number i.e 16196
  * Test Location Path - Test location path is your local path where you test cases being executed i.e    "C:\\Users\\your_username\\BMC\\Workbench\\workspace\\CLI_CWKTCOBX\\Tests\\Scenarios"
  * CLI path - Provide the CLI path where a workspace available i.e. "C:\\Users\\your_username\\git\\TED\\work\\workspace\\Security_Vulnerability\\TopazCliWkspc"
  * HCI user id - Provide you user id which can connect to MF
  * Password - Configure you MF password in "Github Repository" -> Settings-> Secrets-> Actions-> New repository secret
     
 
# Inputs


| Input name | Required | Description |
| --- | --- | --- |
| CLI Execution path | Required  | CLI execution path is the location where it is installed locally, provide path till .bat folder  |
| Repository | Required  | File-AID Ex Repository where specification are stored |
| Specification Llist | Required  | File-AID EX Specification Name & Type seperated by space |
| Execution Context | Required  | Context property file where all communication, exection host etc. details mentioned |
| HCI UserID  | Required  | Provide your Mainframe User ID |
| Target Host  | Required  | VM name where self-hosted runners is deplyed |
| Password  | Required  | "Github Repository" -> Settings-> Secrets-> Actions-> New repository secret |


# Outputs

Output will saved in Output folder created under Test Location Path in your local system.

# Troubleshooting

To enable debug logging in your GitHub actions workflow, see the guide [here](https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/enabling-debug-logging).

# License summary

This code is made available under the BMC license, Click [here](https://github.com/bmc-compuware/devX-data-studio-github-actions/blob/main/LICENSE.txt).

# Product Assistance

BMC provides assistance for customers with its documentation, the BMC Support Center web site, and telephone customer support.

### BMC Support Center

You can access online information for BMC products via our Support Center site at [https://support.bmc.com](https://support.bmc.com/). Support Center provides access to critical information about your BMC products. You can review frequently asked questions, read or download documentation, access product fixes, or e-mail your questions or comments. The first time you access Support Center, you must register and obtain a password. Registration is free.

### Contacting Customer Support

At BMC, we strive to make our products and documentation the best in the industry. Feedback from our customers helps us maintain our quality standards. If you need support services, please obtain the following information before calling BMC\'s 24-hour telephone support:

- The Github pipeline job output that contains any error messages or pertinent information.

- The name, release number, and build number of your product. This information is displayed in the installed extensions page. Apply filter: BMC in order to display all of the installed BMC extension.

- Environment information, such as the operating system and release on which the Workbench CLI is installed.

You can contact BMC in one of the following ways:


#### Web

You can report issues via BMC Support Center: [https://support.bmc.com](https://support.bmc.com/).

Note: Please report all high-priority issues by phone.

### Corporate Web Site

To access BMC site on the Web, go to [https://www.bmc.com/](https://www.bmc.com/). The BMC site provides a variety of product and support information.
