# ARR Chi Bald
Another three server setup, this time with IIS Application Request Routing.

## Install
Create a resource group ArChiBaldRG

Open a cloud shell in Azure.

    git clone https://github.com/sebug/arr-chi-bald/
    cd arr-chi-bald
    az deployment group create -f ./main.bicep -g ArChiBaldRG

While you're doing the manual setup steps you'll have to start up a Bastion instance as well.

First if you arrive on the machine, use Edge to connect to http://22.22.2.10 and http://22.22.2.11 to ensure the sites are up.

Here are the manual steps for installation: https://learn.microsoft.com/en-us/iis/extensions/installing-application-request-routing-arr/install-application-request-routing - be sure to use the exe to install so that you get all prerequisites.

And for configuration: https://learn.microsoft.com/en-us/iis/extensions/configuring-application-request-routing-arr/define-and-configure-an-application-request-routing-server-farm

When creating the farm, add the machines 22.22.2.10 and 22.22.2.11
