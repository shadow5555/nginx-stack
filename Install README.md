this readme is assuming that you have docker and docker compose already installed

connect to your machine that docker and docker compose is installed on
make the foillowing directories
mkdir docker
cd into docker folder
mkdir proxymanager
mkdir proxymangerdb
mkdir duckdns (assuming you are using duckdns) If you are using a paid domain you will need to create a wildcard dns entry using your public ip address. You will want to lookup instructions for your domain server you are using

next 
cd back to main directory

next

cd into docker again
sudo nano (insert favorite editor here) docker-compose.yaml

insert the code from my yaml file then cntrl x and answer yes to saving file

please note you will need to edit some variables to suit your needs/region/etc

next 

sudo nano .env file ( this is another file needed that answers your variables from yaml file) for instance your db passowrd/region/etc

Please see my example file .env and edit to suit your needs

after both files have been created you should see docker-compose.yaml and .ennv file in your docker folder
run the ls command to verify this

once you have created and verified your settings meet you needs lets get the containers built

to build everything

run sudo docker-compose up
sudo docker-compose up -d will make sure everything runs correctly on next reboot
