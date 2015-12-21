RISCOSS Community Platform is an application aimed at demonstrating the [RISCOSS](http://www.riscoss.eu) approach in the context of community projects such as the [OW2 Community](http://www.ow2.org). A live demo of the platform is available at the following URL: [RISCOSS Community Platform for the OW2 Community](https://projects.ow2.org/bin/view/riscoss/).

## Requirements

The following components are needed to deploy the RISCOSS Community Platform:
- A running XWiki instance (version 6.2 or above)
- A NodeJS environment

## Installation

The platform is packaged as an XWiki application under the XAR format (XWiki Application archive) and as a data collector runner. The installation consists first in deploying the application XAR into an XWiki instance, then in deploying the data collectors runner in a NodeJS environment.

### XWiki application generation installation

- Clone this repository
- Install Maven v3
- Run the command ```mvn clean install''' to generate a XAR package
- The generated XAR package should be available at the following path: ```xwiki-documents/target/riscoss-community-xwiki-documents.xar'''
- Upload the generated XAR to your XWiki server and deploy it
- Browse the 'riscoss' path of the wiki: http://localhost/xwiki/bin/view/riscoss/
- You should see the application home page illustrated above.
- From there, a sample project project can be accessed, as well as the default data collectors and risk models.

### Data collectors runner installation

The data collectors are executed by a dedicated script in a NodeJS environment.

The installation steps are the following:
- Checkout the code from the RISCOSS GitHub repository into a NodeJS environment.
- Edit the YAML configuration file 'config.yaml' and declare there all the service endpoints and the project references.
- Schedule a cron task executing the script daily.
- Gather the output files produced by the script and attach each of them to their respective project's page on the platform.

## License

This application is free software; you can redistribute it and/or modify it under the terms of the [GNU Lesser General Public License version 2.1](https://www.gnu.org/licenses/lgpl-2.1.txt) as published by the Free Software Foundation.

This software is distributed in the hope that it will be useful, but without any warranty; without even the implied warranty of merchantability or fitness for a particular purpose. See the GNU
Lesser General Public License for more details.
