# BT Panel Third-Party Cloud Platform

This is a BT Panel third-party cloud platform website program developed in PHP.

You can use this program to build your own BT Panel third-party cloud platform, enabling private deployment of the latest BT Panel version, without communicating with the official BT Panel interface, thus meeting privacy, security, and compliance requirements. It also removes the forced account binding of the panel and allows for DIY panel functionality.

The website backend management can synchronize the official BT Panel plugin list and incremental update plugin packages with one click, and also includes cloud usage records, IP blacklists and whitelists, operation logs, scheduled tasks, and other functions.

This project comes with the latest version installation packages and update packages for **BT Panel Linux**, **BT Panel Windows**, **aaPanel Panel**, and **BT Cloud Monitoring**, modified and adapted for this third-party cloud platform, and is fully open source with no encrypted files such as .so files.

If you like this project, please give it a Star!

## Declaration

1. This project is for personal use only and must not infringe upon the intellectual property rights and other legal rights of BT Panel and other third parties.

2. Setting up and using this project requires a certain level of programming and Linux system administration knowledge. It is not recommended for complete beginners. ## Environment Requirements

* `PHP` >= 7.4

* `MySQL` >= 5.6

* `fileinfo` extension

* `ZipArchive` extension

## Deployment Method

- [Download the latest Release package](https://github.com/flucont/btcloud/releases)

- If you downloaded the source code package, you need to execute `composer install --no-dev` to install dependencies. If you downloaded the Release package, this is not necessary.

- Set the website's running directory to `public`.

- Set the URL rewriting to `ThinkPHP`.

- Access the website; it will automatically redirect to the installation page. Follow the prompts to complete the installation.

## Usage Method

- In the `Batch Replace Tool`, execute the commands displayed on the page to batch replace `http://www.example.com` in BT installation packages, update packages, and script files with the current website's URL.

- Modify the BT Panel interface settings in `System Basic Settings`. You will need a BT Panel (or similar panel) that uses the latest official script to install and bind your account. This will be used to obtain the latest plugin list and plugin packages. Follow the on-screen instructions to install the required plugins.

- In the `Scheduled Task Settings`, execute the displayed command to retrieve the latest plugin list from the BT Panel official website and batch download plugin packages (incremental updates). Alternatively, you can go to the plugin list and download each plugin individually.

- Visit the website `/download` to view the one-click installation script using this third-party cloud service.

## Update Method

- [Download the latest Release package](https://github.com/flucont/btcloud/releases)

- Upload and overwrite all files except the data folder

- Use a batch replace tool in the backend -> Get the latest plugin list -> Modify the version number in the software version settings

## Other

- [Linux Panel Official Update Package Modification History](./wiki/update.md)

- [Windows Panel Official Update Package Modification History](./wiki/updatewin.md)

- [aaPanel Panel Official Update Package Modification History](./wiki/aapanel.md)

- [BT Cloud Monitor Installation Package Modification History](./wiki/btmonitor.md)

- Comparison between the official BT Panel version and this third-party cloud version:

| | Official Version | This Third-Party Cloud Version |

| ---------- | ------------------------------------------------------------ | -------------------------------------------------- |

| Version Update | Supported | Supported |

| Panel Ads | Has Ads | No ads |

| Fully open source | Not fully open source | Fully open source |

| Resource consumption | Various statistical reporting tasks result in slightly higher resource consumption | Many unnecessary scheduled tasks have been removed, resulting in lower resource consumption |

| Compatibility | Due to system architecture limitations of compiled .so files, compatibility is limited to the system architecture corresponding to the compiled .so file | As it is fully open source, there are no pre-compiled .so files, therefore there are no system architecture limitations |
