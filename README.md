# ami

#demo


# Steps to run packer build in your system

        1. install packer using following steps on fedora
           - sudo dnf install -y dnf-plugins-core
           - sudo dnf config-manager --add-repo https://rpm.releases.hashicorp.com/fedora/hashicorp.repo
           - sudo dnf -y install packer

        2. verify installation
           - packer

# How does the AMI is created using packer template
    
    Once you create a packer template file like ami.json in the current repository .

    "ami.json" takes aws_acces_key_id and aws_secret_key , aws region, aws account id from the github secrets as environment variables

    Run the following commands to validate and build the image
        - packer validate ami.json
        - packer buil ami.json
    
    If the above steps results in success then an aws machine image will be created in aws account for which you have provided the access to this packer script

    The packer Image built with the above script "ami.json" will have nodejs already installed

    


