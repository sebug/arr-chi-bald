# ARR Chi Bald
Another three server setup, this time with IIS Application Request Routing.

## Install
Create a resource group ArChiBaldRG

Open a cloud shell in Azure.

    git clone https://github.com/sebug/arr-chi-bald/
    cd arr-chi-bald
    az deployment group create -f ./main.bicep -g ArChiBaldRG
